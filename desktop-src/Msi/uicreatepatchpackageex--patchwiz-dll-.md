---
description: A função UiCreatePatchPackageEx usa um arquivo de criação de pacote (arquivo. PCP) e gera um pacote de patches Windows Installer (pacote. msp). Chamar Msimsp.exe é o método recomendado para usar Patchwiz.dll.
ms.assetid: 76d9a21d-73bc-41fc-8ed0-7d7d7deff815
title: UiCreatePatchPackageEx (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac61371d1e7bf1809880c8f10a403d1730adc8e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759202"
---
# <a name="uicreatepatchpackageex-patchwizdll"></a><span data-ttu-id="799e9-104">UiCreatePatchPackageEx (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="799e9-104">UiCreatePatchPackageEx (Patchwiz.dll)</span></span>

<span data-ttu-id="799e9-105">A função UiCreatePatchPackageEx usa um arquivo de criação de pacote (arquivo. PCP) e gera um pacote de patches Windows Installer (pacote. msp).</span><span class="sxs-lookup"><span data-stu-id="799e9-105">The UiCreatePatchPackageEx function takes a package creation file (.pcp file) and generates a Windows Installer patch package (.msp package).</span></span> <span data-ttu-id="799e9-106">Chamar [Msimsp.exe](msimsp-exe.md) é o método recomendado para usar [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="799e9-106">Calling [Msimsp.exe](msimsp-exe.md) is the recommended method for using [Patchwiz.dll](patchwiz-dll.md).</span></span>

<span data-ttu-id="799e9-107">A função UiCreatePatchPackageEx está disponível começando com Patchwiz.dll versão 4,0 e estende a funcionalidade da função [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="799e9-107">The UiCreatePatchPackageEx function is available beginning with Patchwiz.dll version 4.0 and extends the functionality of the [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) function.</span></span>

``` syntax
UINT UiCreatePatchPackageEx(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  BOOL fRemoveTempFolderContents,
  DWORD dwFlags,
  DWORD dwReserved    
);
```

## <a name="parameters"></a><span data-ttu-id="799e9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="799e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="799e9-109"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*</span><span class="sxs-lookup"><span data-stu-id="799e9-109"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*</span></span>
</dt> <dd>

<span data-ttu-id="799e9-110">Caminho completo do arquivo de propriedades de criação de patch (arquivo. PCP) para este patch.</span><span class="sxs-lookup"><span data-stu-id="799e9-110">Full path to the patch creation properties file (.pcp file) for this patch.</span></span>

</dd> <dt>

<span data-ttu-id="799e9-111"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*</span><span class="sxs-lookup"><span data-stu-id="799e9-111"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*</span></span>
</dt> <dd>

<span data-ttu-id="799e9-112">Caminho completo do pacote de patches Windows Installer (arquivo. msp) a ser criado.</span><span class="sxs-lookup"><span data-stu-id="799e9-112">Full path to the Windows Installer patch package (.msp file) that is to be created.</span></span> <span data-ttu-id="799e9-113">Esse parâmetro pode ser **nulo** ou uma cadeia de caracteres vazia, mas não pode ser omitido.</span><span class="sxs-lookup"><span data-stu-id="799e9-113">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="799e9-114">Se for **nulo** ou uma cadeia de caracteres vazia, a função usará o valor de PatchOutputPath na [tabela de Propriedades (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="799e9-114">If it is **NULL** or an empty string, the function uses the value of PatchOutputPath in the [Properties Table (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="799e9-115"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*</span><span class="sxs-lookup"><span data-stu-id="799e9-115"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*</span></span>
</dt> <dd>

<span data-ttu-id="799e9-116">Caminho completo de um arquivo de log de texto que será anexado.</span><span class="sxs-lookup"><span data-stu-id="799e9-116">Full path to a text log file that will be appended.</span></span> <span data-ttu-id="799e9-117">Esse parâmetro pode ser **nulo** ou uma cadeia de caracteres vazia, mas não pode ser omitido.</span><span class="sxs-lookup"><span data-stu-id="799e9-117">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="799e9-118"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*</span><span class="sxs-lookup"><span data-stu-id="799e9-118"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*</span></span>
</dt> <dd>

<span data-ttu-id="799e9-119">Identificador para uma janela que exibe o texto de status.</span><span class="sxs-lookup"><span data-stu-id="799e9-119">Handle to a window that displays the status text.</span></span> <span data-ttu-id="799e9-120">Esse parâmetro pode ser **nulo** ou uma cadeia de caracteres vazia, mas não pode ser omitido.</span><span class="sxs-lookup"><span data-stu-id="799e9-120">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="799e9-121"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*</span><span class="sxs-lookup"><span data-stu-id="799e9-121"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*</span></span>
</dt> <dd>

<span data-ttu-id="799e9-122">Local para arquivos temporários.</span><span class="sxs-lookup"><span data-stu-id="799e9-122">Location for temporary files.</span></span> <span data-ttu-id="799e9-123">Esse parâmetro pode ser **nulo** ou uma cadeia de caracteres vazia, mas não pode ser omitido.</span><span class="sxs-lookup"><span data-stu-id="799e9-123">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="799e9-124">O usuário deve ter privilégios suficientes para ler e gravar nessa pasta.</span><span class="sxs-lookup"><span data-stu-id="799e9-124">The user must have sufficient privileges to read and write to this folder.</span></span> <span data-ttu-id="799e9-125">O local padrão é% TMP% \\ ~ PCW \_ tmp. tmp \\ .</span><span class="sxs-lookup"><span data-stu-id="799e9-125">The default location is %TMP%\\~pcw\_tmp.tmp\\.</span></span>

</dd> <dt>

<span data-ttu-id="799e9-126"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*</span><span class="sxs-lookup"><span data-stu-id="799e9-126"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*</span></span>
</dt> <dd>

<span data-ttu-id="799e9-127">Se **for true**, remova a pasta temporária e todo o seu conteúdo, se presente.</span><span class="sxs-lookup"><span data-stu-id="799e9-127">If **TRUE**, remove the temporary folder and all of its contents if present.</span></span> <span data-ttu-id="799e9-128">Se **false** e a pasta estiver presente, a função falhará.</span><span class="sxs-lookup"><span data-stu-id="799e9-128">If **FALSE**, and folder is present, the function fails.</span></span>

</dd> <dt>

<span data-ttu-id="799e9-129"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="799e9-129"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="799e9-130">Esse parâmetro pode ser definido como um ou uma combinação dos valores a seguir para especificar opções de log ou de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="799e9-130">This parameter can be set to one or a combination of the following values to specify logging or user interface options.</span></span>



| <span data-ttu-id="799e9-131">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="799e9-131">Flag</span></span>            | <span data-ttu-id="799e9-132">Valor</span><span class="sxs-lookup"><span data-stu-id="799e9-132">Value</span></span>       | <span data-ttu-id="799e9-133">Significado</span><span class="sxs-lookup"><span data-stu-id="799e9-133">Meaning</span></span>                                  |
|-----------------|-------------|------------------------------------------|
| <span data-ttu-id="799e9-134">LOGNONE</span><span class="sxs-lookup"><span data-stu-id="799e9-134">LOGNONE</span></span>         | <span data-ttu-id="799e9-135">0x00000000</span><span class="sxs-lookup"><span data-stu-id="799e9-135">0x00000000</span></span>  | <span data-ttu-id="799e9-136">Não grave nenhuma mensagem no log.</span><span class="sxs-lookup"><span data-stu-id="799e9-136">Write no messages to the log.</span></span>            |
| <span data-ttu-id="799e9-137">LOGINFO</span><span class="sxs-lookup"><span data-stu-id="799e9-137">LOGINFO</span></span>         | <span data-ttu-id="799e9-138">0x00000001</span><span class="sxs-lookup"><span data-stu-id="799e9-138">0x00000001</span></span>  | <span data-ttu-id="799e9-139">Grave mensagens informativas no log.</span><span class="sxs-lookup"><span data-stu-id="799e9-139">Write informational messages to the log.</span></span> |
| <span data-ttu-id="799e9-140">LOGWARN</span><span class="sxs-lookup"><span data-stu-id="799e9-140">LOGWARN</span></span>         | <span data-ttu-id="799e9-141">0x00000002</span><span class="sxs-lookup"><span data-stu-id="799e9-141">0x00000002</span></span>  | <span data-ttu-id="799e9-142">Grave avisos no log.</span><span class="sxs-lookup"><span data-stu-id="799e9-142">Write warnings to the log.</span></span>               |
| <span data-ttu-id="799e9-143">LOGERR</span><span class="sxs-lookup"><span data-stu-id="799e9-143">LOGERR</span></span>          | <span data-ttu-id="799e9-144">0x00000004</span><span class="sxs-lookup"><span data-stu-id="799e9-144">0x00000004</span></span>  | <span data-ttu-id="799e9-145">Grave mensagens de erro no log.</span><span class="sxs-lookup"><span data-stu-id="799e9-145">Write error messages to the log.</span></span>         |
| <span data-ttu-id="799e9-146">LOGPERFMESSAGES</span><span class="sxs-lookup"><span data-stu-id="799e9-146">LOGPERFMESSAGES</span></span> | <span data-ttu-id="799e9-147">0x00000008</span><span class="sxs-lookup"><span data-stu-id="799e9-147">0x00000008</span></span>  | <span data-ttu-id="799e9-148">Grave mensagens de desempenho no log.</span><span class="sxs-lookup"><span data-stu-id="799e9-148">Write performance messages to the log.</span></span>   |
| <span data-ttu-id="799e9-149">UINONE</span><span class="sxs-lookup"><span data-stu-id="799e9-149">UINONE</span></span>          | <span data-ttu-id="799e9-150">0x00000000f</span><span class="sxs-lookup"><span data-stu-id="799e9-150">0x00000000f</span></span> | <span data-ttu-id="799e9-151">Não exibir a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="799e9-151">Do not display the user interface.</span></span>       |
| <span data-ttu-id="799e9-152">UIALL</span><span class="sxs-lookup"><span data-stu-id="799e9-152">UIALL</span></span>           | <span data-ttu-id="799e9-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="799e9-153">0x00000010</span></span>  | <span data-ttu-id="799e9-154">Exibir a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="799e9-154">Display the user interface.</span></span>              |



 

</dd> <dt>

<span data-ttu-id="799e9-155"><span id="dwReserved"></span><span id="dwreserved"></span><span id="DWRESERVED"></span>*dwReserved*</span><span class="sxs-lookup"><span data-stu-id="799e9-155"><span id="dwReserved"></span><span id="dwreserved"></span><span id="DWRESERVED"></span>*dwReserved*</span></span>
</dt> <dd>

<span data-ttu-id="799e9-156">Reservado.</span><span class="sxs-lookup"><span data-stu-id="799e9-156">Reserved.</span></span> <span data-ttu-id="799e9-157">Esse parâmetro deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="799e9-157">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="799e9-158">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="799e9-158">Return Values</span></span>

<span data-ttu-id="799e9-159">Consulte a tabela em [valores de retorno para UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span><span class="sxs-lookup"><span data-stu-id="799e9-159">See the table in [Return Values for UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="799e9-160">Comentários</span><span class="sxs-lookup"><span data-stu-id="799e9-160">Remarks</span></span>

<span data-ttu-id="799e9-161">Para obter um exemplo de como criar um arquivo. PCP e usar o [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) para gerar um pacote de patches Windows Installer, consulte a seção [um exemplo de aplicação de patch de atualização pequena](a-small-update-patching-example.md).</span><span class="sxs-lookup"><span data-stu-id="799e9-161">For an example of authoring a .pcp file and using [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) to generate a Windows Installer patch package, see the section [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="799e9-162">A criação de um patch requer uma imagem de instalação descompactada, como uma imagem administrativa ou uma imagem de instalação descompactada de um CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="799e9-162">Creating a patch requires an uncompressed setup image, such as an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="799e9-163">[UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) não gera patches binários para arquivos em gabinetes.</span><span class="sxs-lookup"><span data-stu-id="799e9-163">[UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) does not generate binary patches for files in cabinets.</span></span>

 

 



