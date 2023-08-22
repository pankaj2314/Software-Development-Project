![image](https://github.com/pankaj2314/Software-Development-Project/assets/109330359/bfff4ab4-70de-42d9-aa4e-360cd52c5e95)# Software-Development-Project
def plan_software_development():
  """Plans a software development project by gathering requirements."""

  # Gather requirements from stakeholders.
  requirements = []
  for stakeholder in ["customer", "developer", "manager"]:
    requirements.extend(stakeholder_get_requirements())

  # Prioritize requirements.
  requirements.sort(key=lambda requirement: requirement["priority"])

  # Create a project plan.
  project_plan = {
      "requirements": requirements,
      "schedule": create_schedule(),
      "budget": create_budget(),
  }

  return project_plan

def stakeholder_get_requirements():
  """Gets requirements from a stakeholder."""

  print("What are your requirements for the software development project?")
  requirements = []
  while True:
    requirement = input("Requirement: ")
    if requirement == "":
      break
    requirement_type = input("Requirement type (functional or non-functional): ")
    priority = int(input("Requirement priority (1-10): "))
    requirements.append({
        "requirement": requirement,
        "type": requirement_type,
        "priority": priority,
    })

  return requirements

def create_schedule():
  """Creates a schedule for the software development project."""

  print("What is the estimated start date for the software development project?")
  start_date = input()
  print("What is the estimated end date for the software development project?")
  end_date = input()

  schedule = {
      "start_date": start_date,
      "end_date": end_date,
  }

  return schedule

def create_budget():
  """Creates a budget for the software development project."""

  print("What is the estimated budget for the software development project?")
  budget = int(input())

  return budget

if __name__ == "__main__":
  project_plan = plan_software_development()
  print(project_plan)
