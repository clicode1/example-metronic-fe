<template>
  <!--begin::Section-->
  <div class="pt-10">
    <!--begin::Heading-->
    <h1 class="anchor fw-bolder mb-5" id="fullscreen">
      <router-link to="#fullscreen"></router-link>
      Fullscreen
    </h1>
    <!--end::Heading-->

    <!--begin::Block-->
    <div class="py-5">
      Add <code>.modal-fullscreen</code> class to enable a modal with fullscreen
      mode. Add <code>.bg-body</code> and <code>.shadow-none</code> classes to
      fix background color and unwanted shadow issue when modal has a long
      scrollable content.
    </div>
    <!--end::Block-->

    <!--begin::Block-->
    <div class="py-5">
      <div class="rounded border p-10">
        <button
          type="button"
          class="btn btn-primary"
          data-bs-toggle="modal"
          data-bs-target="#kt_modal_2"
        >
          Launch demo modal
        </button>

        <div class="modal bg-body fade" tabindex="-1" id="kt_modal_2">
          <div class="modal-dialog modal-fullscreen">
            <div class="modal-content shadow-none">
              <div class="modal-header">
                <h5 class="modal-title">Modal title</h5>

                <!--begin::Close-->
                <div
                  class="btn btn-icon btn-sm btn-active-light-primary ms-2"
                  data-bs-dismiss="modal"
                  aria-label="Close"
                >
                  <span class="svg-icon svg-icon-2x">
                    <inline-svg src="media/icons/duotune/arrows/arr061.svg" />
                  </span>
                </div>
                <!--end::Close-->
              </div>

              <div class="modal-body">
                <p>Modal body text goes here.</p>
              </div>

              <div class="modal-footer">
                <button
                  type="button"
                  class="btn btn-light"
                  data-bs-dismiss="modal"
                >
                  Close
                </button>
                <button type="button" class="btn btn-primary">
                  Save changes
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!--end::Block-->

    <!--begin::Code-->
    <div class="py-5">
      <CodeHighlighter :fieldHeight="400" lang="html"
        >{{`<button
          type="button"
          class="btn btn-primary"
          data-bs-toggle="modal"
          data-bs-target="#kt_modal_2"
        >
          Launch demo modal
        </button>

        <div class="modal modal-fullscreen fade" tabindex="-1" id="kt_modal_2">
          <div class="modal-dialog">
            <div class="modal-content">
              <div class="modal-header">
                <h5 class="modal-title">Modal title</h5>

                <!--begin::Close-->
                <div
                  class="btn btn-icon btn-sm btn-active-light-primary ms-2"
                  data-bs-dismiss="modal"
                  aria-label="Close"
                >
                  <span class="svg-icon svg-icon-2x"></span>
                </div>
                <!--end::Close-->
              </div>

              <div class="modal-body">
                <p>Modal body text goes here.</p>
              </div>

              <div class="modal-footer">
                <button
                  type="button"
                  class="btn btn-light"
                  data-bs-dismiss="modal"
                >
                  Close
                </button>
                <button type="button" class="btn btn-primary">
                  Save changes
                </button>
              </div>
            </div>
          </div>
        </div>
        `}}</CodeHighlighter
      >
    </div>
    <!--end::Code-->
  </div>
  <!--end::Section-->
</template>

<script lang="ts">
import { defineComponent } from "vue";
import CodeHighlighter from "@/components/highlighters/CodeHighlighter.vue";

export default defineComponent({
  name: "modal-fullscreen",
  components: {
    CodeHighlighter,
  },
});
</script>
