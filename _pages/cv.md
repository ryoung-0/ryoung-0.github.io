<div class="pdf-wrap">
  <div class="pdf-toolbar">
    <a href="{{ '/assets/cv.pdf' | relative_url }}">Download CV (PDF)</a>
    <span>(updated 3/2025)</span>
  </div>

  <object
    data="{{ '/assets/cv.pdf' | relative_url }}"
    type="application/pdf"
    class="pdf-embed">
    <p>Your browser can’t display PDFs here.
      <a href="{{ '/assets/cv.pdf' | relative_url }}">Open the CV</a>.
    </p>
  </object>
</div>

<style>
/* Container centers and limits the overall width (makes it “smaller”) */
.pdf-wrap {
  max-width: 900px;   /* ↓ reduce this to make it smaller (e.g., 800px, 720px) */
  margin: 0 auto 2rem auto;
}

/* Simple header row */
.pdf-toolbar {
  display: flex;
  gap: .75rem;
  align-items: baseline;
  margin: .5rem 0 1rem;
  font-size: 0.95rem;
  opacity: .9;
}

/* The PDF viewport: fixed height => internal scroll */
.pdf-embed {
  width: 100%;
  height: 75vh;       /* ↓ adjust: 60–80vh is typical. Fixed px works too, e.g., 700px */
  border: 1px solid rgba(0,0,0,.1);
  box-shadow: 0 4px 20px rgba(0,0,0,.06);
  border-radius: 8px;
}

/* Mobile: keep it usable without taking the whole screen */
@media (max-width: 640px) {
  .pdf-wrap { max-width: 100%; }
  .pdf-embed { height: 65vh; }
}
</style>
