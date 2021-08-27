---
description: Este tópico fornece diretrizes para instalar ou reinstalar uma instalação de várias instâncias que usa as transformação de instância.
ms.assetid: cf9076b1-5674-4ba8-9890-e981221d7b03
title: Instalando várias instâncias com transformações de instância
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a25b2cba8fd91316d62692d278345e0f7d9751f018e1c33239412988bfe118a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074896"
---
# <a name="installing-multiple-instances-with-instance-transforms"></a>Instalando várias instâncias com transformações de instância

Este tópico fornece diretrizes para instalar ou reinstalar uma instalação de várias instâncias que usa as transformação de instância.

-   Ao instalar uma nova instância com uma transformação de instância, inclua a propriedade **MSINEWINSTANCE** e de conjunto **MSINEWINSTANCE**=1.
-   Ao instalar uma nova instância com uma transformação de instância, inclua a propriedade TRANSFORMS e de definir a primeira transformação na lista de transformações para a transformação da instância que altera o código do produto. Qualquer transformação de personalização deve seguir a transformação da instância no início desta lista.
-   A maneira mais fácil de iniciar uma instalação de manutenção e reinstalar uma instância é referenciar o código do produto da instância. Se você iniciar a instalação de manutenção usando o caminho do pacote, também deverá especificar o código do produto da instância. Na linha de comando, use a opção /n {Product Code}. No código ou script, use a **propriedade MSIINSTANCEGUID.**

O exemplo a seguir mostra a instalação de uma nova instância de uma linha de comando em que a transformação da instância é prefixada por dois-pontos, que especifica que a transformação é inserida no pacote.

**msiexec /I mypackage.msi TRANSFORMS=:instance.mst MSINEWINSTANCE=1 /qb**

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

O exemplo a seguir reinstala uma instância sem re-caching do pacote. A instância é referenciada pelo código do produto {00000001-0002-0000-0000-624474736554} .

**msiexec /I {00000001-0002-0000-0000-624474736554} REINSTALL=ALL REINSTALLMODE=omus /qb**

O exemplo a seguir reinstala uma instância e armazena novamente em cache o pacote da linha de comando. A instância é referenciada pelo caminho do pacote. Você só precisa incluir a opção /n {Product Code} se o produto for originalmente instalado com uma transformação de instância.

**msiexec /I c: \\ newpath \\mypackage.msi /n {00000001-0002-0000-0000-624474736554} REINSTALL=ALL REINSTALLMODE=vomus /qb**

O exemplo a seguir reinstala uma instância e armazena em cache o pacote **usando MsiInstallProduct**. A instância é referenciada pelo caminho do pacote. Use a **propriedade MSIINSTANCEGUID** para fornecer o código do produto da instância.

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"));
```

O exemplo a seguir reinstala uma instância e armazena em cache o pacote usando script. Use a **propriedade MSIINSTANCEGUID** para fornecer o código do produto da instância.

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"
```

O exemplo a seguir mostra como anunciar uma instância usando a linha de comando.

**msiexec /jm mypackage.msi /t :instance.mst /c /qb**

O exemplo a seguir mostra como instalar para anunciar uma instância usando **MsiAdvertiseProductEx**.

``` syntax
UINT uiStat = MsiAdvertiseProductEx(_T("path to mypackage.msi"), NULL, _T(":instance.mst"), 0, 0, MSIADVERTISEOPTIONS_INSTANCE);
```

O exemplo a seguir mostra como aplicar um patch a uma instância de uma linha de comando. Você só precisa incluir a opção /n {Product Code} se o produto tiver sido originalmente instalado com uma transformação de instância.

**msiexec /p mypatch.msp /n {00000001-0002-0000-0000-624474736554} /qb**

O exemplo a seguir mostra como aplicar um patch a uma instalação de instância usando [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha).

``` syntax
UINT uiStat = MsiApplyPatch(_T("path to mypatch.msp"), _T("{00000001-0002-0000-0000-624474736554}"), INSTALLTYPE_SINGLE_INSTANCE, _T("REINSTALL=ALL REINSTALLMODE=omus"));
```

Para obter mais informações, [consulte Instalando várias instâncias](installing-multiple-instances-of-products-and-patches.md) de produtos e patches e Como autor de várias [instâncias com transformações de instância](authoring-multiple-instances-with-instance-transforms.md).

 

 



