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
# <a name="patching-initial-installations"></a><span data-ttu-id="f43ff-103">Aplicação de patch nas instalações iniciais</span><span class="sxs-lookup"><span data-stu-id="f43ff-103">Patching Initial Installations</span></span>

<span data-ttu-id="f43ff-104">Um patch de Windows Installer (MSP) pode ser aplicado ao instalar um aplicativo pela primeira vez usando a propriedade [**patch**](patch.md) .</span><span class="sxs-lookup"><span data-stu-id="f43ff-104">A Windows Installer Patch (MSP) can be applied when installing an application for the first time by using the [**PATCH**](patch.md) property.</span></span>

<span data-ttu-id="f43ff-105">Para aplicar um patch na primeira vez em que o aplicativo é instalado, a propriedade [**patch**](patch.md) deve ser definida na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f43ff-105">To apply a patch the first time the application is installed, the [**PATCH**](patch.md) property must be set on the command line.</span></span> <span data-ttu-id="f43ff-106">Especifique o caminho completo para o patch na linha de comando como o par de valor de propriedade "PATCH = {*path to patch*}".</span><span class="sxs-lookup"><span data-stu-id="f43ff-106">Specify the full path to the patch on the command line as the "PATCH={*path to patch*}" property-value pair.</span></span>

<span data-ttu-id="f43ff-107">Observe que a especificação da propriedade [**patch**](patch.md) na linha de comando substitui as verificações de aplicabilidade de patch executadas ao usar [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) ou a [opção de linha de comando](command-line-options.md)/p.</span><span class="sxs-lookup"><span data-stu-id="f43ff-107">Note that specifying the [**PATCH**](patch.md) property on the command line overrides the patch applicability checks performed when using [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the /p [Command Line Option](command-line-options.md).</span></span>

<span data-ttu-id="f43ff-108">Se um patch for aplicado usando [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) ou a [opção de linha de comando](command-line-options.md)/p, o instalador compara os aplicativos atualmente instalados no computador com a lista de códigos de produto qualificados para receber o patch na propriedade Resumo do [**modelo**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="f43ff-108">If a patch is applied using [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the /p [Command Line Option](command-line-options.md), the installer compares the applications currently installed on the computer to the list of product codes eligible to receive the patch in the [**Template Summary**](template-summary.md) property.</span></span>

<span data-ttu-id="f43ff-109">Quando você define a propriedade [**patch**](patch.md) na linha de comando para instalar na primeira instalação, os aplicativos qualificados para receber o patch são determinados pelas condições de validação nas transformações inseridas no pacote de patch.</span><span class="sxs-lookup"><span data-stu-id="f43ff-109">When you set the [**PATCH**](patch.md) property on the command line to install on first installation, the applications eligible to receive the patch is determined by validation conditions on the transforms embedded in the patch package.</span></span> <span data-ttu-id="f43ff-110">O método recomendado para gerar um pacote de patch é usar uma ferramenta de criação de patch, como [Msimsp.exe](msimsp-exe.md) e [PATCHWIZ.DLL](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="f43ff-110">The recommended method for generating a patch package is to use a patch creation tool such as [Msimsp.exe](msimsp-exe.md) and [PATCHWIZ.DLL](patchwiz-dll.md).</span></span> <span data-ttu-id="f43ff-111">As condições de validação em transformações no patch são originadas na coluna ProductValidateFlags na tabela [TargetImages](targetimages-table-patchwiz-dll-.md) do arquivo de propriedades de criação de patch (. PCP).</span><span class="sxs-lookup"><span data-stu-id="f43ff-111">The validation conditions on transforms in the patch originate from the ProductValidateFlags column in the [TargetImages](targetimages-table-patchwiz-dll-.md) table of the Patch Creation Properties (.pcp) file.</span></span>

<span data-ttu-id="f43ff-112">O patch pode ser aplicado na primeira vez em que o aplicativo é instalado por uma linha de comando, outro aplicativo ou script.</span><span class="sxs-lookup"><span data-stu-id="f43ff-112">The patch can be applied the first time the application is installed by a command line, another application, or script.</span></span>

<span data-ttu-id="f43ff-113">O seguinte mostra a primeira aplicação de patches da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f43ff-113">The following shows first-time patching from the command line.</span></span>

<span data-ttu-id="f43ff-114">**msiexec/i** *package.msi* **patch =**_"c: \\ Directory \\ patch. msp"_</span><span class="sxs-lookup"><span data-stu-id="f43ff-114">**msiexec /I** *package.msi* **PATCH=**_"c:\\directory\\patch.msp"_</span></span>

<span data-ttu-id="f43ff-115">O seguinte mostra a primeira aplicação de patch de outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f43ff-115">The following shows first-time patching from another application.</span></span>

``` syntax
UINT uiStat = MsiInstallProduct(_T("package.msi"), _T("PATCH=c:\directory\patch.msp"));
```

<span data-ttu-id="f43ff-116">O seguinte mostra a primeira aplicação de patches do script.</span><span class="sxs-lookup"><span data-stu-id="f43ff-116">The following shows first-time patching from script.</span></span>


```VB
Dim Installer as Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "package.msi", "PATCH=c:\directory\patch.msp"
```



<span data-ttu-id="f43ff-117">\* \* Windows Installer 3,0 e posterior: \* \*</span><span class="sxs-lookup"><span data-stu-id="f43ff-117">\*\*Windows Installer 3.0 and later:  \*\*</span></span>

<span data-ttu-id="f43ff-118">A partir do Windows Installer versão 3,0, vários patches podem ser aplicados ao instalar um aplicativo pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="f43ff-118">Beginning with Windows Installer version 3.0, multiple patches can be applied when installing an application for the first time.</span></span> <span data-ttu-id="f43ff-119">Defina a propriedade [**patch**](patch.md) para uma lista delimitada por ponto e vírgula dos caminhos completos dos patches.</span><span class="sxs-lookup"><span data-stu-id="f43ff-119">Set the [**PATCH**](patch.md) property to a semicolon delimited list of the patches' full paths.</span></span> <span data-ttu-id="f43ff-120">O seguinte mostra a primeira aplicação de patches de vários patches da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f43ff-120">The following shows first-time patching of multiple patches from the command line.</span></span>

<span data-ttu-id="f43ff-121">**msiexec/i** *package.msi* **patch =**_"c: \\ Directory \\ patch. msp; c: \\ Directory \\ patch2. msp; c: \\ Directory \\ patch3. msp"_</span><span class="sxs-lookup"><span data-stu-id="f43ff-121">**msiexec /I** *package.msi* **PATCH=**_"c:\\directory\\patch.msp;c:\\directory\\patch2.msp;c:\\directory\\patch3.msp"_</span></span>

 

 



