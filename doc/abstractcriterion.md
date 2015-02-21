<a name="nn.Criterion"/>
## Criterion ##

The Criterion is an abstract class which declares methods defined in all criterions.
Like most things in torch, this class is [serializable](https://github.com/torch/torch7/blob/master/doc/file.md#serialization-methods).

<a name="nn.Criterion.forward"/>
### [output] forward(input, target) ###

Given an `input` and a `target`, compute the loss function associated to the criterion and return the
result. In general `input` and `target` are [tensors](https://github.com/torch/torch7/blob/master/doc/tensor.md), but some specific criterions
might require some other type of object.

The `output` returned should be a scalar in general.

The state variable [self.output](#nn.Criterion.output) should be updated after a call to `forward()`.

<a name="nn.Criterion.backward"/>
### [gradInput] backward(input, target) ###

Given an `input` and a `target`, compute the gradients of the loss function associated to the criterion and
return the result.In general `input`, `target` and `gradInput` are [tensors](..:torch:tensor), but some specific criterions
might require some other type of object.

The state variable [self.gradInput](#nn.Criterion.gradInput) should be updated after a call to `backward()`.

<a name="nn.Criterion.output"/>
### State variable: output ###

State variable which contains the result of the last [forward(input, target)](#nn.Criterion.forward) call.

<a name="nn.Criterion.gradInput"/>
### State variable: gradInput ###

State variable which contains the result of the last [backward(input, target)](#nn.Criterion.backward) call.
