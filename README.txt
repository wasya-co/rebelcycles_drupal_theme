
  find . -name .git -prune -o -type f -exec perl -pi -e 's/bootstrap_barrio_subtheme/rebelcycles_drupal_theme/g' {} +


find . -name .git -prune -o -depth -name '*bootstrap_barrio_subtheme*' -exec sh -c '
for f do
  mv "$f" "${f//bootstrap_barrio_subtheme/rebelcycles_drupal_theme}"
done
' sh {} +




