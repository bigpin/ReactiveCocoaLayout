# ReactiveCocoaLayout

ReactiveCocoaLayout is a framework for describing Cocoa and Cocoa Touch layouts
in a reactive way, based on
[ReactiveCocoa](https://github.com/github/ReactiveCocoa).

This framework is very much a work in progress at the moment, and should be
considered **alpha quality**. Breaking changes may happen often during this
time.

## Why Not Use Auto Layout?

RCL intends to offer the following advantages over Auto Layout:

 * **Explicit and linear layout.** Reactive layout proceeds in a linear fashion,
   making it easier to understand and debug the steps it takes along the way.
 * **Top-down layout.** A view's layout doesn't interact with its superview's
   layout unless the former's size or frame is explicitly incorporated in the
   latter's layout chain, creating a unidirectional relationship that leads to
   better encapsulation and less complexity. Bidirectional relationships are
   still possible, but must be made explicit.
 * **Conditional layouts at runtime.** RCL is built on the full power
   of [ReactiveCocoa](https://github.com/github/ReactiveCocoa), and signals can
   be composed to dynamically disable and re-enable entire layout chains (like
   when you want to hide and show views) without actually modifying them.
 * **Implicit animations.** To animate the setting of a view's frame, simply add
   an animation method into the signal chain. No need to explicitly animate
   constants anywhere.
   _([Planned](https://github.com/github/ReactiveCocoaLayout/issues/3), but not
   yet implemented.)_
 * **Extensibility.** RCL is made up of many independent bits of functionality
   unified into a framework. It's easy to extend it with your own functionality
   if you want it to behave differently.
 * **Not a black box.** Unlike AppKit and UIKit, RCL is an open source project,
   so you can crack open any particular bit and see why it behaves the way it
   does.

## Getting Started

To start building the framework, clone this repository and then run `git
submodule update --init --recursive`. This will automatically pull down any
dependencies.

## License

ReactiveCocoaLayout is released under the MIT license. See
[LICENSE.md](https://github.com/github/ReactiveCocoaLayout/blob/master/LICENSE.md).
