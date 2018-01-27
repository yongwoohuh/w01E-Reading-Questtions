# W01E Reading & Questions
* model object has no explicit connection to user interface
## Q1 Explain the different components of MVC - what are their responsibilities?
* model - responsible for data storage and data structures.
* view - how the information is displayed and the user UI
* controller - bridging the model and the view

## What are some benefits of having an NSObject protocol separate from the NSObject class?
when you don’t need all of the NSObject method but  still want the basic methods make your protocol conform to NSObject protocol. Mainly used when making custom protocols.

## Q3
Given the following person class, create a subclass LLShoutingPerson whose designated initializer is initWithLoudMessage:. Write the implementation for LLShoutingPerson's initializer.

@interface LLPerson : NSObject

-(instancetype)initWithMessage:(NSString*)msg;
+(instancetype)personWithMessage:(NSString*)msg;

-(void)sayIt;

@end

### answer

    `@interface LLShoutingPerson : LLPerson`
    `- (instancetype)initWithLoudMessage:(NSString *)msg;`
`@end`

`@implementation LLShoutingPerson`
```- (instancetype)initWithLoudMessage:(NSString *)msg
{
  self = [super initWithMessage:(NSString *)msg];
  if (self) {
    _msg = msg;
  }
  return self;
}
@end
