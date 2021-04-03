---
description: Um patch de Windows Installer (MSP) pode ser aplicado ao instalar um aplicativo pela primeira vez usando a propriedade PATCH.
ms.assetid: 2c4b9d5a-34fb-4a0b-b530-30bf238468fd
title: Aplicação de patch nas instalações iniciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa85e15da18f7342f38cf82228bc31b6e3085f09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922810"
---
# <a name="patching-initial-installations"></a>Aplicação de patch nas instalações iniciais

Um patch de Windows Installer (MSP) pode ser aplicado ao instalar um aplicativo pela primeira vez usando a propriedade [**patch**](patch.md) .

Para aplicar um patch na primeira vez em que o aplicativo é instalado, a propriedade [**patch**](patch.md) deve ser definida na linha de comando. Especifique o caminho completo para o patch na linha de comando como o par de valor de propriedade "PATCH = {*path to patch*}".

Observe que a especificação da propriedade [**patch**](patch.md) na linha de comando substitui as verificações de aplicabilidade de patch executadas ao usar [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) ou a [opção de linha de comando](command-line-options.md)/p.

Se um patch for aplicado usando [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) ou a [opção de linha de comando](command-line-options.md)/p, o instalador compara os aplicativos atualmente instalados no computador com a lista de códigos de produto qualificados para receber o patch na propriedade Resumo do [**modelo**](template-summary.md) .

Quando você define a propriedade [**patch**](patch.md) na linha de comando para instalar na primeira instalação, os aplicativos qualificados para receber o patch são determinados pelas condições de validação nas transformações inseridas no pacote de patch. O método recomendado para gerar um pacote de patch é usar uma ferramenta de criação de patch, como [Msimsp.exe](msimsp-exe.md) e [PATCHWIZ.DLL](patchwiz-dll.md). As condições de validação em transformações no patch são originadas na coluna ProductValidateFlags na tabela [TargetImages](targetimages-table-patchwiz-dll-.md) do arquivo de propriedades de criação de patch (. PCP).

O patch pode ser aplicado na primeira vez em que o aplicativo é instalado por uma linha de comando, outro aplicativo ou script.

O seguinte mostra a primeira aplicação de patches da linha de comando.

**msiexec/i** *package.msi* **patch =**_"c: \\ Directory \\ patch. msp"_

O seguinte mostra a primeira aplicação de patch de outro aplicativo.

``` syntax
UINT uiStat = MsiInstallProduct(_T("package.msi"), _T("PATCH=c:\directory\patch.msp"));
```

O seguinte mostra a primeira aplicação de patches do script.


```VB
Dim Installer as Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "package.msi", "PATCH=c:\directory\patch.msp"
```



* * Windows Installer 3,0 e posterior: * *

A partir do Windows Installer versão 3,0, vários patches podem ser aplicados ao instalar um aplicativo pela primeira vez. Defina a propriedade [**patch**](patch.md) para uma lista delimitada por ponto e vírgula dos caminhos completos dos patches. O seguinte mostra a primeira aplicação de patches de vários patches da linha de comando.

**msiexec/i** *package.msi* **patch =**_"c: \\ Directory \\ patch. msp; c: \\ Directory \\ patch2. msp; c: \\ Directory \\ patch3. msp"_

 

 



