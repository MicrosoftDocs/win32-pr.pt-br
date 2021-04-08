---
description: O método recomendado para gerar um pacote de patch é usar uma ferramenta de criação de patch, como Msimsp.exe para chamar UiCreatePatchPackage em Patchwiz.dll. Msimsp.exe e PatchWiz.dll são fornecidos no SDK do Windows Installer.
ms.assetid: 7fa661aa-d52c-4b08-961f-90ec778f02ff
title: Gerando um pacote de patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef64ac66cd0201ae99080ec86e32230bc88407b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922030"
---
# <a name="generating-a-patch-package"></a>Gerando um pacote de patch

O método recomendado para gerar um pacote de patch é usar uma ferramenta de criação de patch, como [Msimsp.exe](msimsp-exe.md) para chamar [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) em [Patchwiz.dll](patchwiz-dll.md). Msimsp.exe e PatchWiz.dll são fornecidos no SDK do Windows Installer.

A linha de comando de exemplo a seguir usa Msimsp.exe e o arquivo. PCP criado na [criação de um arquivo de propriedades de criação de patch](creating-a-patch-creation-properties-file.md) para gerar o pacote de patch de exemplo MNP2000. msp.

**Msimsp.exe-s C: \\ Observação do \_ patch do instalador \\ \\ MNP2000. PCP-p C: \\ Observação patch do \_ instalador \\ \\ MNP2000. msp**

Uma ferramenta de criação de patches criada pode gerar o pacote de patch chamando [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) da seguinte maneira.

``` syntax
UiCreatePatchPackage ("C:\\Note_Installer\\Patch\\MNP2000.pcp", "C:\\Note_Installer\\Patch\\MNP2000.msp", NULL, NULL, "", TRUE)
```

[Continuar](applying-a-patch-package-to-a-local-installation.md)

 

 



