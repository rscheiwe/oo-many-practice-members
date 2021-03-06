# oo-many-practice-members

(after @aalexander3/oo-many-many-practice)

# Here's our domain:
  * Member
  * Institution
  * Membership

# How is this modeled?
  * A membership belongs_to a member
  * A membership belongs_to a institution
  * A member has_many memberships
  * An institution has_many memberships
  * A member has_many many institutions through memberships
  * An institution has_many members through memberships

==============================================================

# OBJECTIVES
  * Draw this domain on a whiteboard or http://awwapp.com/
  * Build out the three classes and files from scratch (keep in mind the relationships)
  * Think about how the classes will interact -- how does a doctor know about their patients?
  * Use attr_reader, attr_writer, & attr_accessor
  * Create a run file with a single point of entry
  * Maintain single source of truth for all classes

==============================================================

# DELIVERABLES
  * INSTITUTION
    * #initialize an institution is initialized with a name and a kind (e.g., gym, salon, etc.)
    * an institution cannot change its name, but can change its kind
    * Institution.all returns all instances of the institution class
    * #memberships returns an array of all the membership instances that belong_to an institution
    * #members return an array of all the members that are associated with an institution
    * #member names return an array of just the names of said members (First and Last), not the full object
    ====== BONUS ======
    * Institution.find_by_kind takes in a kind (e.g., "gym") as an argument and finds an institution by a given kind
    * #upgrade_membership takes in a membership and a new tier ("free" => "premium") and changes the membership's tier

==============================================================
  * MEMBER
    * #initialize a member is initialized with a first_name and last_name
    * a member cannot change their name
    * Member.all returns all instances of the member class
    * #member_name converts a member's first and last name to member_name (e.g., "John Smith => "jsmith")
    * #memberships returns an array of all the memberships associated with an instance of member
    * #buy_membership creates a new membership instance taking in an institution and a tier (e.g., 
free", "premium")
    ====== BONUS ======
    * Member.find_by_name takes in member_name (e.g., "jsmith", not "John Smith") as an argument and finds a member's full name by a member_name
    * #find_institution finds an institution by kind (e.g., "gym", "salon") -- utilizing the Institution.find_by_kind class method

==============================================================
  * MEMBERSHIP
    * #initialize  a membership is initialized with a tier ("free", "premium", etc.), a member and an institution
    * an membership has corresponding methods for all three attributes
    * Membership.all returns all instances of the membership class

==============================================================
