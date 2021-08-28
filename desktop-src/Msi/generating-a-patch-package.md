---
description: O método recomendado para gerar um pacote de patch é usar uma ferramenta de criação de patch, como Msimsp.exe para chamar UiCreatePatchPackage em Patchwiz.dll. Msimsp.exe e PatchWiz.dll são fornecidos no SDK do Windows Installer.
ms.assetid: 7fa661aa-d52c-4b08-961f-90ec778f02ff
title: Gerando um pacote de patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0577c678bbb378da425ff438a0e165dcba95d6e1fc1eecc1d9c311fe2c78bca2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581426"
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

 

 



