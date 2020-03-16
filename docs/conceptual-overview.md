# Overview
**PyIAM** aims to be a package, which provides a framework for managing access to Resources (Python objects) in a system. The aim is to very generic and closely follow the IAM approach of AWS, which is a well proven system and provides a very good sepratation of concern to each part of the system.

## Basic Teminology
1. `ResourceType`: An entity for which accesses are being managed
2. `Resource`: An actual instance of a resource type
3. `Action`: Some operation that can be performed on a Resource, for now, the action would be limited to
    1. Create
    2. Read
    3. Update
    4. Delete
4. `Permissions`: A combination of Resource and Action
5. `Policies`: A set of permissions
6. `Groups`: A set of policies
    1. A group can contain both Policies and Permissions, however, policies are more encouraged
7. `Actor`: An entity which is capable of performing an Action on a Resource, according to the permissions. It can be a user, a web service, a Python object, anything which satisfies the interface. Can be persisted in a storage, or in memory.
    1. A `Actor` would be added to a `Group` to gain `Permissions`

