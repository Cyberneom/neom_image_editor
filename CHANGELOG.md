### 1.0.0 - Initial Release & Decoupling from neom_posts / neom_media_upload

This marks the **initial official release (v1.0.0)** of `neom_image_editor` as a standalone, independent module within the Open Neom ecosystem. Previously, image editing functionalities (specifically cropping) were often embedded directly within content creation workflows in modules like `neom_posts`, or implicitly handled by `neom_media_upload`. This decoupling is a crucial step in formalizing the image processing layer, enhancing modularity, and strengthening Open Neom's adherence to Clean Architecture principles.

**Key Highlights of this Release:**

* **Module Decoupling & Self-Containment:**
    * `neom_image_editor` now encapsulates all image editing logic, starting with cropping, completely separated from content creation or media selection modules.
    * This ensures that `neom_image_editor` is a highly focused and reusable component for any image manipulation requirement across the application.

* **Centralized Image Cropping Functionality:**
    * Provides a dedicated and robust image cropping feature, allowing precise adjustments to image dimensions and aspect ratios.
    * Utilizes `image_cropper` as its core external dependency, ensuring a high-quality, platform-optimized user experience for cropping.

* **Direct External Dependencies:**
    * Now directly manages its external image editing dependency (`image_cropper`), centralizing its usage within this module.

* **Enhanced Maintainability & Future Scalability:**
    * As a dedicated and self-contained module, `neom_image_editor` is now significantly easier to maintain, test, and extend for future image editing features (e.g., filters, adjustments, overlays).
    * Any module requiring image editing capabilities can simply depend on `neom_image_editor` and its `ImageEditorService`.
    * This aligns perfectly with the overall architectural vision of Open Neom, fostering a more collaborative and efficient development environment for visual content.

* **Leverages Core Open Neom Modules:**
    * Built upon `neom_core` for foundational services and `neom_commons` for reusable UI components and utilities, ensuring consistency and seamless integration within the ecosystem.