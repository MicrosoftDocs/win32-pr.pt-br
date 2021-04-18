---
description: O utilitário do verificador de arquivos do sistema, Sfc.exe, permite que os administradores verifiquem todos os recursos protegidos para verificar suas versões.
ms.assetid: 72f69ad2-15d9-4191-a8aa-4c23a2392006
title: " Verificador de Arquivos do Sistema"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da4e0d67f6de6aba62fe262969d7f30db0c45335
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757057"
---
# <a name="system-file-checker"></a><span data-ttu-id="cb8c1-103"> Verificador de Arquivos do Sistema</span><span class="sxs-lookup"><span data-stu-id="cb8c1-103">System File Checker</span></span>

<span data-ttu-id="cb8c1-104">O utilitário do verificador de arquivos do sistema, Sfc.exe, permite que os administradores verifiquem todos os recursos protegidos para verificar suas versões.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-104">The system file checker utility, Sfc.exe, allows administrators to scan all protected resources to verify their versions.</span></span>

<span data-ttu-id="cb8c1-105">Arquivos críticos para reiniciar o Windows que não correspondem à versão esperada do Windows podem ser substituídos pelas versões corretas.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-105">Files critical to restart Windows that do not match the expected Windows version may be replaced with the correct versions.</span></span> <span data-ttu-id="cb8c1-106">Se um arquivo for reparado, os dados de registro correspondentes também serão reparados.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-106">If a file is repaired, the corresponding registry data is also repaired.</span></span> <span data-ttu-id="cb8c1-107">Arquivos protegidos não críticos para reiniciar o Windows não são reparados.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-107">Protected files not critical to restart Windows are not repaired.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb8c1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb8c1-108">Syntax</span></span>

<span data-ttu-id="cb8c1-109">A seguir está a sintaxe de linha de comando para o Sfc.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-109">The following is the command-line syntax for Sfc.</span></span>

<span data-ttu-id="cb8c1-110">**Opções de SFC \[ = caminho completo do arquivo\]**</span><span class="sxs-lookup"><span data-stu-id="cb8c1-110">**SFC options \[=full file path\]**</span></span>

## <a name="options"></a><span data-ttu-id="cb8c1-111">Opções</span><span class="sxs-lookup"><span data-stu-id="cb8c1-111">Options</span></span>

<dl> <dt>

<span data-ttu-id="cb8c1-112"><span id="_CACHESIZE_x"></span><span id="_cachesize_x"></span><span id="_CACHESIZE_X"></span>/CACHESIZE =*x*</span><span class="sxs-lookup"><span data-stu-id="cb8c1-112"><span id="_CACHESIZE_x"></span><span id="_cachesize_x"></span><span id="_CACHESIZE_X"></span>/CACHESIZE=*x*</span></span>
</dt> <dd>

<span data-ttu-id="cb8c1-113">Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-113">This value is not supported.</span></span>

<span data-ttu-id="cb8c1-114">**Windows Server 2003 e Windows XP:** Define o tamanho do cache de arquivos.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-114">**Windows Server 2003 and Windows XP:** Sets the file cache size.</span></span> <span data-ttu-id="cb8c1-115">O tamanho padrão do cache é 0x32 (50 MB).</span><span class="sxs-lookup"><span data-stu-id="cb8c1-115">The default size of the cache is 0x32 (50 MB).</span></span>

</dd> <dt>

<span data-ttu-id="cb8c1-116"><span id="_CANCEL"></span><span id="_cancel"></span>/CANCEL</span><span class="sxs-lookup"><span data-stu-id="cb8c1-116"><span id="_CANCEL"></span><span id="_cancel"></span>/CANCEL</span></span>
</dt> <dd>

<span data-ttu-id="cb8c1-117">Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-117">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="cb8c1-118"><span id="_ENABLE"></span><span id="_enable"></span>/ENABLE</span><span class="sxs-lookup"><span data-stu-id="cb8c1-118"><span id="_ENABLE"></span><span id="_enable"></span>/ENABLE</span></span>
</dt> <dd>

<span data-ttu-id="cb8c1-119">Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-119">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="cb8c1-120"><span id="_FILESONLY"></span><span id="_filesonly"></span>/FILESONLY</span><span class="sxs-lookup"><span data-stu-id="cb8c1-120"><span id="_FILESONLY"></span><span id="_filesonly"></span>/FILESONLY</span></span>
</dt> <dd>

<span data-ttu-id="cb8c1-121">Verificar ou reparar somente arquivos.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-121">Verify or repair only files.</span></span> <span data-ttu-id="cb8c1-122">Não verifique ou repare as chaves do registro.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-122">Do not verify or repair registry keys.</span></span>

<span data-ttu-id="cb8c1-123">**Windows XP:** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-123">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="cb8c1-124"><span id="_OFFBOOTDIR"></span><span id="_offbootdir"></span>/OFFBOOTDIR</span><span class="sxs-lookup"><span data-stu-id="cb8c1-124"><span id="_OFFBOOTDIR"></span><span id="_offbootdir"></span>/OFFBOOTDIR</span></span>
</dt> <dd>

<span data-ttu-id="cb8c1-125">Use esta opção para reparos offline.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-125">Use this option for offline repairs.</span></span> <span data-ttu-id="cb8c1-126">Especifique o local do diretório de inicialização offline.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-126">Specify the location of the offline boot directory.</span></span>

<span data-ttu-id="cb8c1-127">**Windows XP:** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-127">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="cb8c1-128"><span id="_OFFWINDIR"></span><span id="_offwindir"></span>/OFFWINDIR</span><span class="sxs-lookup"><span data-stu-id="cb8c1-128"><span id="_OFFWINDIR"></span><span id="_offwindir"></span>/OFFWINDIR</span></span>
</dt> <dd>

<span data-ttu-id="cb8c1-129">Use esta opção para reparos offline.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-129">Use this option for offline repairs.</span></span> <span data-ttu-id="cb8c1-130">Especifique o local do diretório offline do Windows.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-130">Specify the location of the offline Windows directory.</span></span>

<span data-ttu-id="cb8c1-131">**Windows XP:** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-131">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="cb8c1-132"><span id="_PURGECACHE"></span><span id="_purgecache"></span>/PURGECACHE</span><span class="sxs-lookup"><span data-stu-id="cb8c1-132"><span id="_PURGECACHE"></span><span id="_purgecache"></span>/PURGECACHE</span></span>
</dt> <dd>

<span data-ttu-id="cb8c1-133">Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-133">This value is not supported.</span></span>

<span data-ttu-id="cb8c1-134">**Windows Server 2003 e Windows XP:** Esvazia o cache de arquivos e examina todos os arquivos protegidos do sistema.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-134">**Windows Server 2003 and Windows XP:** Empties the file cache and scans all protected system files.</span></span>

</dd> <dt>

<span data-ttu-id="cb8c1-135"><span id="_QUIET"></span><span id="_quiet"></span>/QUIET</span><span class="sxs-lookup"><span data-stu-id="cb8c1-135"><span id="_QUIET"></span><span id="_quiet"></span>/QUIET</span></span>
</dt> <dd>

<span data-ttu-id="cb8c1-136">Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-136">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="cb8c1-137"><span id="_REVERT"></span><span id="_revert"></span>/REVERT</span><span class="sxs-lookup"><span data-stu-id="cb8c1-137"><span id="_REVERT"></span><span id="_revert"></span>/REVERT</span></span>
</dt> <dd>

<span data-ttu-id="cb8c1-138">Retornar às configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-138">Return to default settings.</span></span>

<span data-ttu-id="cb8c1-139">**Windows Server 2008 e Windows Vista:** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-139">**Windows Server 2008 and Windows Vista:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="cb8c1-140"><span id="_SCANBOOT"></span><span id="_scanboot"></span>/SCANBOOT</span><span class="sxs-lookup"><span data-stu-id="cb8c1-140"><span id="_SCANBOOT"></span><span id="_scanboot"></span>/SCANBOOT</span></span>
</dt> <dd>

<span data-ttu-id="cb8c1-141">Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-141">This value is not supported.</span></span>

<span data-ttu-id="cb8c1-142">**Windows Server 2003 e Windows XP:** Examina todos os arquivos protegidos do sistema em cada inicialização.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-142">**Windows Server 2003 and Windows XP:** Scans all protected system files at every boot.</span></span>

</dd> <dt>

<span data-ttu-id="cb8c1-143"><span id="_SCANFILE"></span><span id="_scanfile"></span>/SCANFILE</span><span class="sxs-lookup"><span data-stu-id="cb8c1-143"><span id="_SCANFILE"></span><span id="_scanfile"></span>/SCANFILE</span></span>
</dt> <dd>

<span data-ttu-id="cb8c1-144">Verifica e repara o arquivo localizado no caminho completo especificado.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-144">Scans and repairs the file located at the specified full path.</span></span>

<span data-ttu-id="cb8c1-145">**Windows XP:** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-145">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="cb8c1-146"><span id="_SCANNOW"></span><span id="_scannow"></span>/SCANNOW</span><span class="sxs-lookup"><span data-stu-id="cb8c1-146"><span id="_SCANNOW"></span><span id="_scannow"></span>/SCANNOW</span></span>
</dt> <dd>

<span data-ttu-id="cb8c1-147">Examina todos os arquivos protegidos do sistema imediatamente.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-147">Scans all protected system files immediately.</span></span>

</dd> <dt>

<span data-ttu-id="cb8c1-148"><span id="_SCANONCE"></span><span id="_scanonce"></span>/SCANONCE</span><span class="sxs-lookup"><span data-stu-id="cb8c1-148"><span id="_SCANONCE"></span><span id="_scanonce"></span>/SCANONCE</span></span>
</dt> <dd>

<span data-ttu-id="cb8c1-149">Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-149">This value is not supported.</span></span>

<span data-ttu-id="cb8c1-150">**Windows Server 2003 e Windows XP:** Examina todos os arquivos protegidos do sistema na próxima inicialização.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-150">**Windows Server 2003 and Windows XP:** Scans all protected system files at the next boot.</span></span>

</dd> <dt>

<span data-ttu-id="cb8c1-151"><span id="_VERIFYFILE"></span><span id="_verifyfile"></span>/VERIFYFILE</span><span class="sxs-lookup"><span data-stu-id="cb8c1-151"><span id="_VERIFYFILE"></span><span id="_verifyfile"></span>/VERIFYFILE</span></span>
</dt> <dd>

<span data-ttu-id="cb8c1-152">Verifica o arquivo no caminho completo especificado.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-152">Verifies the file at the specified full path.</span></span> <span data-ttu-id="cb8c1-153">Essa opção não repara o arquivo.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-153">This option does not repair the file.</span></span>

<span data-ttu-id="cb8c1-154">**Windows XP:** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-154">**Windows XP:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="cb8c1-155"><span id="_VERIFYONLY"></span><span id="_verifyonly"></span>/VERIFYONLY</span><span class="sxs-lookup"><span data-stu-id="cb8c1-155"><span id="_VERIFYONLY"></span><span id="_verifyonly"></span>/VERIFYONLY</span></span>
</dt> <dd>

<span data-ttu-id="cb8c1-156">Examina todos os arquivos protegidos do sistema, mas não repara os arquivos.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-156">Scans all protected system files but does not repair files.</span></span>

<span data-ttu-id="cb8c1-157">**Windows XP:** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-157">**Windows XP:** Not supported.</span></span>

</dd> </dl>

<span data-ttu-id="cb8c1-158">O SFC define o seguinte valor de registro:</span><span class="sxs-lookup"><span data-stu-id="cb8c1-158">Sfc sets the following registry value:</span></span>

 <span data-ttu-id="cb8c1-159">= HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SFCScan</span><span class="sxs-lookup"><span data-stu-id="cb8c1-159">= HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon\\SFCScan</span></span>

<span data-ttu-id="cb8c1-160">Para obter mais informações, consulte [valores do registro de WFP](wfp-registry-values.md).</span><span class="sxs-lookup"><span data-stu-id="cb8c1-160">For more information, see [WFP Registry Values](wfp-registry-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cb8c1-161">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb8c1-161">Remarks</span></span>

<span data-ttu-id="cb8c1-162">Somente no Windows Vista, você pode definir a variável de ambiente do arquivo de **\_ \_ log do Windows TRACING** para o local de um diretório válido para receber um arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-162">On Windows Vista only, you can set the **WINDOWS\_TRACING\_LOGFILE** environment variable to the location of a valid directory to receive a log file.</span></span>

## <a name="examples"></a><span data-ttu-id="cb8c1-163">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cb8c1-163">Examples</span></span>

<span data-ttu-id="cb8c1-164">As linhas de comando de exemplo a seguir são exemplos de sintaxe de sfc.exe.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-164">The following sample command lines are examples of sfc.exe syntax.</span></span>

<span data-ttu-id="cb8c1-165">**SFC/SCANNOW**</span><span class="sxs-lookup"><span data-stu-id="cb8c1-165">**sfc /SCANNOW**</span></span>

<span data-ttu-id="cb8c1-166">**Sfc/VERIFYFILE = c: \\ Windows \\ System32 \\kernel32.dll**</span><span class="sxs-lookup"><span data-stu-id="cb8c1-166">**sfc /VERIFYFILE=c:\\windows\\system32\\kernel32.dll**</span></span>

<span data-ttu-id="cb8c1-167">**Sfc/SCANFILE = d: \\ Windows \\ System32 \\kernel32.dll/OFFBOOTDIR = d: \\ /OFFWINDIR = d: \\ Windows**</span><span class="sxs-lookup"><span data-stu-id="cb8c1-167">**sfc /SCANFILE=d:\\windows\\system32\\kernel32.dll /OFFBOOTDIR=d:\\ /OFFWINDIR=d:\\windows**</span></span>

<span data-ttu-id="cb8c1-168">**/FILESONLY/VERIFYONLY Sfc**</span><span class="sxs-lookup"><span data-stu-id="cb8c1-168">**sfc /VERIFYONLY /FILESONLY**</span></span>

 

 



