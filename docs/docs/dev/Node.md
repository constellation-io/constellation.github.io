# Node class

Node is an abstract class that should be used as base class for defining specific node types.

Important! Do not override GetHashCode() and Equals() virtual methods. These will be implemented by the Constellation.io in the base class and implementation might change at any point in time to improve performance. For that reason, an override in a derived class can break current or future core implementation.

Never create a node with same NodeType and Key as an already tracked one. If a node instance already exists, it should be reused.

Current behavior is for GetHashCode() and Equals() to work on instance. That means that if you create two instances of a derived Node class, even with all the attributes the same, they will not be equal.