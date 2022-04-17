Shell Permission



0. #!/bin/bash

su betty



1. #!/bin/bash

whoami



2. #!/bin/bash

groups



3. #!/bin/bash

chown betty hello



4. #!/bin/bash

touch hello



5. #!/bin/bash

chmod u+x hello



6. #!/bin/bash

chmod ug+x,o+r hello



7. #!/bin/bash

chmod a+x hello



8. #!/bin/bash

chmod 007 hello



9. #!/bin/bash

chmod 753 hello



10. #!/bin/bash

chmod --reference=olleh hello



11. #!/bin/bash

chmod a+X *



12. #!/bin/bash

mkdir -m 751 my_dir



13. #!/bin/bash

chgrp school hello



14. #!/bin/bash

chown vincent:staff *



16. #!/bin/bash

chown --from=guillaume betty hello



17. #!/bin/bash

telnet towel.blinkenlights.n
