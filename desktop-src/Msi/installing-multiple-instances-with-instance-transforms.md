---
description: Este tópico fornece diretrizes para instalar ou reinstalar uma instalação de várias instâncias que usa transformações de instância.
ms.assetid: cf9076b1-5674-4ba8-9890-e981221d7b03
title: Instalando várias instâncias com transformações de instância
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bae8d73ad60567e1557257c1207558290ba29db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010651"
---
# <a name="installing-multiple-instances-with-instance-transforms"></a>Instalando várias instâncias com transformações de instância

Este tópico fornece diretrizes para instalar ou reinstalar uma instalação de várias instâncias que usa transformações de instância.

-   Ao instalar uma nova instância com uma transformação de instância, inclua a propriedade **MSINEWINSTANCE** e defina **MSINEWINSTANCE**= 1.
-   Ao instalar uma nova instância com uma transformação de instância, inclua a propriedade Transforms e defina a primeira transformação na lista de transformações para a transformação instância que altera o código do produto. Todas as transformações de personalização devem seguir a transformação de instância no início desta lista.
-   A maneira mais fácil de iniciar uma instalação de manutenção e reinstalar uma instância do é fazer referência ao código do produto da instância do. Se você iniciar a instalação de manutenção usando o caminho do pacote, também deverá especificar o código do produto da instância. Na linha de comando, use a opção/n {código do produto}. No código ou script, use a propriedade **MSIINSTANCEGUID** .

O exemplo a seguir mostra a instalação de uma nova instância de uma linha de comando na qual a transformação da instância é prefixada por dois-pontos, o que especifica que a transformação é inserida no pacote.

**msiexec/I mypackage.msi transformações =: instância. MST MSINEWINSTANCE = 1/QB**

O exemplo a seguir mostra a instalação de uma nova instância usando [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta).

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("TRANSFORMS=:instance.mst MSINEWINSTANCE=1"));
```

O exemplo a seguir mostra a instalação da nova instância do script.

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "TRANSFORMS=:instance.mst MSINEWINSTANCE=1"
```

O exemplo a seguir reinstala uma instância sem armazenar em cache novamente o pacote. A instância é referenciada por seu código de produto {00000001-0002-0000-0000-624474736554} .

**msiexec/I {00000001-0002-0000-0000-624474736554} reinstalar = todas as REinstalaçãomode = omus/QB**

O exemplo a seguir reinstala uma instância e armazena novamente em cache o pacote da linha de comando. A instância é referenciada pelo caminho do pacote. Você só precisa incluir a opção/n {código do produto} se o produto for instalado originalmente com uma transformação de instância.

**msiexec/I c: \\ newpath \\mypackage.msi/N {00000001-0002-0000-0000-624474736554} reinstalar = todos os REINSTALLMODE = vomus/qb**

O exemplo a seguir reinstala uma instância e armazena o pacote em cache usando **MsiInstallProduct**. A instância é referenciada pelo caminho do pacote. Use a propriedade **MSIINSTANCEGUID** para fornecer o código do produto da instância.

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"));
```

O exemplo a seguir reinstala uma instância e armazena o pacote em cache usando o script. Use a propriedade **MSIINSTANCEGUID** para fornecer o código do produto da instância.

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"
```

O exemplo a seguir mostra como anunciar uma instância usando a linha de comando.

**msiexec/JM mypackage.msi/t: instance. MST/c/QB**

O exemplo a seguir mostra como instalar o para anunciar uma instância usando o **MsiAdvertiseProductEx**.

``` syntax
UINT uiStat = MsiAdvertiseProductEx(_T("path to mypackage.msi"), NULL, _T(":instance.mst"), 0, 0, MSIADVERTISEOPTIONS_INSTANCE);
```

O exemplo a seguir mostra como aplicar um patch a uma instância de uma linha de comando. Você só precisa incluir a opção/n {código do produto} se o produto tiver sido originalmente instalado com uma transformação de instância.

**msiexec/p mypatch. msp/n {00000001-0002-0000-0000-624474736554} /QB**

O exemplo a seguir mostra como aplicar um patch a uma instalação de instância usando o [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha).

``` syntax
UINT uiStat = MsiApplyPatch(_T("path to mypatch.msp"), _T("{00000001-0002-0000-0000-624474736554}"), INSTALLTYPE_SINGLE_INSTANCE, _T("REINSTALL=ALL REINSTALLMODE=omus"));
```

Para obter mais informações, consulte [Instalando várias instâncias de produtos e patches](installing-multiple-instances-of-products-and-patches.md) e [criando várias instâncias com transformações de instância](authoring-multiple-instances-with-instance-transforms.md).

 

 



