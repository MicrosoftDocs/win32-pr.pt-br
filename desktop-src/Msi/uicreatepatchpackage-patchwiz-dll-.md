---
description: A função UiCreatePatchPackage usa um arquivo de criação de pacote (arquivo. PCP) e gera um pacote de patches Windows Installer (pacote. msp).
ms.assetid: 77fedb80-b664-417d-879b-846e74cc4c23
title: UiCreatePatchPackage (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bcda07d74ffc32c76809037d9ac90cf11ea25c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826780"
---
# <a name="uicreatepatchpackage-patchwizdll"></a><span data-ttu-id="085c7-103">UiCreatePatchPackage (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="085c7-103">UiCreatePatchPackage (Patchwiz.dll)</span></span>

<span data-ttu-id="085c7-104">A função UiCreatePatchPackage usa um arquivo de criação de pacote (arquivo. PCP) e gera um pacote de patches Windows Installer (pacote. msp).</span><span class="sxs-lookup"><span data-stu-id="085c7-104">The UiCreatePatchPackage function takes a package creation file (.pcp file) and generates a Windows Installer patch package (.msp package).</span></span> <span data-ttu-id="085c7-105">Chamar [Msimsp.exe](msimsp-exe.md) é o método recomendado para usar [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="085c7-105">Calling [Msimsp.exe](msimsp-exe.md) is the recommended method for using [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="085c7-106">A função [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) está disponível na versão 4,0 do Patchwiz.dll e estende a funcionalidade da função UiCreatePatchPackage.</span><span class="sxs-lookup"><span data-stu-id="085c7-106">The [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function is available in version 4.0 of Patchwiz.dll and extends the functionality of the UiCreatePatchPackage function.</span></span>

``` syntax
UINT UiCreatePatchPackage(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  Bool fRemoveTempFolderContents  
);
```

## <a name="parameters"></a><span data-ttu-id="085c7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="085c7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="085c7-108"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*</span><span class="sxs-lookup"><span data-stu-id="085c7-108"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*</span></span>
</dt> <dd>

<span data-ttu-id="085c7-109">Caminho completo do arquivo de propriedades de criação de patch (arquivo. PCP) para este patch.</span><span class="sxs-lookup"><span data-stu-id="085c7-109">Full path to the patch creation properties file (.pcp file) for this patch.</span></span>

</dd> <dt>

<span data-ttu-id="085c7-110"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*</span><span class="sxs-lookup"><span data-stu-id="085c7-110"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*</span></span>
</dt> <dd>

<span data-ttu-id="085c7-111">Caminho completo do pacote de patches Windows Installer (arquivo. msp) a ser criado.</span><span class="sxs-lookup"><span data-stu-id="085c7-111">Full path to the Windows Installer patch package (.msp file) that is to be created.</span></span> <span data-ttu-id="085c7-112">Esse parâmetro pode ser **nulo** ou uma cadeia de caracteres vazia, mas não pode ser omitido.</span><span class="sxs-lookup"><span data-stu-id="085c7-112">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="085c7-113">Se for **nulo** ou uma cadeia de caracteres vazia, a função usará o valor de PatchOutputPath na [tabela de Propriedades (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="085c7-113">If it is **NULL** or an empty string, the function uses the value of PatchOutputPath in the [Properties Table (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="085c7-114"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*</span><span class="sxs-lookup"><span data-stu-id="085c7-114"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*</span></span>
</dt> <dd>

<span data-ttu-id="085c7-115">Caminho completo de um arquivo de log de texto que será anexado.</span><span class="sxs-lookup"><span data-stu-id="085c7-115">Full path to a text log file that will be appended.</span></span> <span data-ttu-id="085c7-116">Esse parâmetro pode ser **nulo** ou uma cadeia de caracteres vazia, mas não pode ser omitido.</span><span class="sxs-lookup"><span data-stu-id="085c7-116">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="085c7-117"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*</span><span class="sxs-lookup"><span data-stu-id="085c7-117"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*</span></span>
</dt> <dd>

<span data-ttu-id="085c7-118">Identificador para uma janela que exibe o texto de status.</span><span class="sxs-lookup"><span data-stu-id="085c7-118">Handle to a window that displays the status text.</span></span> <span data-ttu-id="085c7-119">Esse parâmetro pode ser **nulo** ou uma cadeia de caracteres vazia, mas não pode ser omitido.</span><span class="sxs-lookup"><span data-stu-id="085c7-119">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="085c7-120"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*</span><span class="sxs-lookup"><span data-stu-id="085c7-120"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*</span></span>
</dt> <dd>

<span data-ttu-id="085c7-121">Local para arquivos temporários.</span><span class="sxs-lookup"><span data-stu-id="085c7-121">Location for temporary files.</span></span> <span data-ttu-id="085c7-122">Esse parâmetro pode ser **nulo** ou uma cadeia de caracteres vazia, mas não pode ser omitido.</span><span class="sxs-lookup"><span data-stu-id="085c7-122">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="085c7-123">O local padrão é% TMP% \\ ~ PCW \_ tmp. tmp \\ .</span><span class="sxs-lookup"><span data-stu-id="085c7-123">The default location is %TMP%\\~pcw\_tmp.tmp\\.</span></span>

</dd> <dt>

<span data-ttu-id="085c7-124"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*</span><span class="sxs-lookup"><span data-stu-id="085c7-124"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*</span></span>
</dt> <dd>

<span data-ttu-id="085c7-125">Se **for true**, remova a pasta temporária e todo o seu conteúdo, se presente.</span><span class="sxs-lookup"><span data-stu-id="085c7-125">If **TRUE**, remove the temporary folder and all of its contents if present.</span></span> <span data-ttu-id="085c7-126">Se **false** e a pasta estiver presente, a função falhará.</span><span class="sxs-lookup"><span data-stu-id="085c7-126">If **FALSE**, and folder is present, the function fails.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="085c7-127">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="085c7-127">Return Values</span></span>

<span data-ttu-id="085c7-128">Consulte a tabela em [valores de retorno para UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span><span class="sxs-lookup"><span data-stu-id="085c7-128">See the table in [Return Values for UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="085c7-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="085c7-129">Remarks</span></span>

<span data-ttu-id="085c7-130">Para obter um exemplo de como criar um arquivo. PCP e usar o UiCreatePatchPackage para gerar um pacote de patches Windows Installer, consulte a seção [um exemplo de aplicação de patch de atualização pequena](a-small-update-patching-example.md).</span><span class="sxs-lookup"><span data-stu-id="085c7-130">For an example of authoring a .pcp file and using UiCreatePatchPackage to generate a Windows Installer patch package, see the section [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="085c7-131">A criação de um patch requer uma imagem de instalação descompactada, como uma imagem administrativa ou uma imagem de instalação descompactada de um CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="085c7-131">Creating a patch requires an uncompressed setup image, such as an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="085c7-132">UiCreatePatchPackage não gera patches binários para arquivos em gabinetes.</span><span class="sxs-lookup"><span data-stu-id="085c7-132">UiCreatePatchPackage does not generate binary patches for files in cabinets.</span></span>

 

 



