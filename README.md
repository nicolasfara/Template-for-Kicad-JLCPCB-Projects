# Template-for-Kicad-JLCPCB-Projects

Template repository based on the great work of https://github.com/labtroll/KiCad-DesignRules.  
Please feel free to open a PR for improving this template.

## Enforce DRC and ERC checks in CI

If you want to enforce DRC and ERC checks in CI, enable `run_erc` and `run_drc` to `true`.

```yaml
uses: actions-for-kicad/kicad-actions@d51e6623d9465cf5d95958b3a9f651aa9702a317 # v1-k9.0
with:
  schematic_file_name: "${{ steps.file-names.outputs.schematic_file }}"
  pcb_file_name: "${{ steps.file-names.outputs.pcb_file }}"
  run_erc: true
  schematic_output_pdf: true
  run_drc: true
  pcb_output_gerbers_and_drill: true
  pcb_output_image: true
```
