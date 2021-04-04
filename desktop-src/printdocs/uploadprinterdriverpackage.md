---
description: Carrega um driver de impressora no repositório de drivers de servidores de impressão para que ele possa ser instalado chamando InstallPrinterDriverFromPackage.
ms.assetid: dd3b3a3b-8ded-44ae-85dd-e630bc62e898
title: Função UploadPrinterDriverPackage (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UploadPrinterDriverPackage
- UploadPrinterDriverPackageA
- UploadPrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f616c4f731d3a416806f499a513f48466263f441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171325"
---
# <a name="uploadprinterdriverpackage-function"></a><span data-ttu-id="d1145-103">Função UploadPrinterDriverPackage</span><span class="sxs-lookup"><span data-stu-id="d1145-103">UploadPrinterDriverPackage function</span></span>

<span data-ttu-id="d1145-104">Carrega um driver de impressora no repositório de drivers do servidor de impressão para que ele possa ser instalado chamando [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md).</span><span class="sxs-lookup"><span data-stu-id="d1145-104">Uploads a printer driver to the print server's driver store so that it can be installed by calling [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1145-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1145-105">Syntax</span></span>


```C++
HRESULT UploadPrinterDriverPackage(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszInfPath,
  _In_    LPCTSTR pszEnvironment,
  _In_    DWORD   dwFlags,
  _In_    HWND    hwnd,
  _Out_   LPTSTR  pszDestInfPath,
  _Inout_ PULONG  pcchDestInfPath
);
```



## <a name="parameters"></a><span data-ttu-id="d1145-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1145-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1145-107">*pszServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1145-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1145-108">Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica o nome do servidor de impressão.</span><span class="sxs-lookup"><span data-stu-id="d1145-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="d1145-109">Use **NULL** se o servidor for o computador local.</span><span class="sxs-lookup"><span data-stu-id="d1145-109">Use **NULL** if the server is the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="d1145-110">*pszInfPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1145-110">*pszInfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1145-111">Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica o caminho de origem para o arquivo. inf do driver.</span><span class="sxs-lookup"><span data-stu-id="d1145-111">A pointer to a constant ,null-terminated string that specifies the source path to the driver's .inf file.</span></span>

</dd> <dt>

<span data-ttu-id="d1145-112">*pszEnvironment* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1145-112">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1145-113">Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica a arquitetura do processador do servidor (por exemplo, Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="d1145-113">A pointer to a constant, null-terminated string that specifies the server's processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="d1145-114">Isso pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="d1145-114">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d1145-115">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1145-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1145-116">Isso pode ser qualquer um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="d1145-116">This can be any of the following values:</span></span>



| <span data-ttu-id="d1145-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d1145-117">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="d1145-118">Significado</span><span class="sxs-lookup"><span data-stu-id="d1145-118">Meaning</span></span>                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UPDP_SILENT_UPLOAD"></span><span id="updp_silent_upload"></span><dl> <span data-ttu-id="d1145-119"><dt>**UPDP_SILENT_UPLOAD**</dt></span><span class="sxs-lookup"><span data-stu-id="d1145-119"><dt>**UPDP_SILENT_UPLOAD**</dt></span></span> </dl>             | <span data-ttu-id="d1145-120">A interface do usuário não será mostrada durante o carregamento.</span><span class="sxs-lookup"><span data-stu-id="d1145-120">The UI will not be shown during the upload.</span></span><br/>                                                                                                             |
| <span id="UPDP_UPLOAD_ALWAYS"></span><span id="updp_upload_always"></span><dl> <span data-ttu-id="d1145-121"><dt>**UPDP_UPLOAD_ALWAYS**</dt></span><span class="sxs-lookup"><span data-stu-id="d1145-121"><dt>**UPDP_UPLOAD_ALWAYS**</dt></span></span> </dl>             | <span data-ttu-id="d1145-122">Os arquivos serão carregados mesmo se o pacote já estiver no repositório de drivers do servidor.</span><span class="sxs-lookup"><span data-stu-id="d1145-122">The files will be uploaded even if the package is already in the server's driver store.</span></span><br/>                                                                 |
| <span id="UPDP_CHECK_DRIVERSTORE"></span><span id="updp_check_driverstore"></span><dl> <span data-ttu-id="d1145-123"><dt>**UPDP_CHECK_DRIVERSTORE**</dt></span><span class="sxs-lookup"><span data-stu-id="d1145-123"><dt>**UPDP_CHECK_DRIVERSTORE**</dt></span></span> </dl> | <span data-ttu-id="d1145-124">O repositório de drivers do servidor será verificado antes do carregamento para ver se o pacote já está lá.</span><span class="sxs-lookup"><span data-stu-id="d1145-124">The server's driver store will be checked before upload to see if the package is already there.</span></span> <span data-ttu-id="d1145-125">Essa configuração será ignorada se UPDP_UPLOAD_ALWAYS estiver definida.</span><span class="sxs-lookup"><span data-stu-id="d1145-125">This setting is ignored if UPDP_UPLOAD_ALWAYS is set.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d1145-126">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1145-126">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1145-127">Um identificador para a interface do usuário de cópia.</span><span class="sxs-lookup"><span data-stu-id="d1145-127">A handle to the copying user interface.</span></span>

</dd> <dt>

<span data-ttu-id="d1145-128">*pszDestInfPath* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d1145-128">*pszDestInfPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1145-129">Um ponteiro para o caminho de destino, no repositório de drivers, ao qual o arquivo. inf do driver foi copiado.</span><span class="sxs-lookup"><span data-stu-id="d1145-129">A pointer to the destination path, in the driver store, to which the driver's .inf file was copied.</span></span>

</dd> <dt>

<span data-ttu-id="d1145-130">*pcchDestInfPath* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d1145-130">*pcchDestInfPath* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1145-131">Na entrada, especifica o tamanho, em caracteres, do buffer *pszDestInfPath* .</span><span class="sxs-lookup"><span data-stu-id="d1145-131">On input, specifies the size, in characters, of the *pszDestInfPath* buffer.</span></span> <span data-ttu-id="d1145-132">Na saída, recebe o tamanho, em caracteres, da cadeia de caracteres do caminho, incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="d1145-132">On output, receives the size, in characters, of the path string, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1145-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d1145-133">Return value</span></span>

<span data-ttu-id="d1145-134">Se a operação for concluída com sucesso, o valor de retorno será S_OK, caso contrário, o **HRESULT** conterá um código de erro.</span><span class="sxs-lookup"><span data-stu-id="d1145-134">If the operation succeeds, the return value is S_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="d1145-135">Para obter mais informações sobre códigos de erro COM, consulte [tratamento de erros](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="d1145-135">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d1145-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1145-136">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d1145-137">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="d1145-137">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="d1145-138">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d1145-138">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="d1145-139">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="d1145-139">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="d1145-140">O repositório de drivers normalmente é% windir% \\ inf ou% windir% \\ System32 \\ DriverStore \\ FileRepository.</span><span class="sxs-lookup"><span data-stu-id="d1145-140">The driver store is typically either %windir%\\inf or %windir%\\System32\\DriverStore\\FileRepository.</span></span>

<span data-ttu-id="d1145-141">Somente um pacote por vez pode ser carregado.</span><span class="sxs-lookup"><span data-stu-id="d1145-141">Only one package at a time can be uploaded.</span></span> <span data-ttu-id="d1145-142">Se um pacote for dependente de outros, eles deverão ser carregados separadamente.</span><span class="sxs-lookup"><span data-stu-id="d1145-142">If a package is dependent on others, they must be uploaded separately.</span></span>

<span data-ttu-id="d1145-143">Somente pacotes de driver assinados podem ser carregados.</span><span class="sxs-lookup"><span data-stu-id="d1145-143">Only signed driver packages can be uploaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1145-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1145-144">Requirements</span></span>



| <span data-ttu-id="d1145-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1145-145">Requirement</span></span> | <span data-ttu-id="d1145-146">Valor</span><span class="sxs-lookup"><span data-stu-id="d1145-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1145-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1145-147">Minimum supported client</span></span><br/> | <span data-ttu-id="d1145-148">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d1145-148">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="d1145-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1145-149">Minimum supported server</span></span><br/> | <span data-ttu-id="d1145-150">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d1145-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d1145-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1145-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1145-152"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1145-152"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d1145-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d1145-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="d1145-154"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1145-154"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d1145-155">DLL</span><span class="sxs-lookup"><span data-stu-id="d1145-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1145-156"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1145-156"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="d1145-157">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="d1145-157">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d1145-158">**UploadPrinterDriverPackageW** (Unicode) e **UploadPrinterDriverPackageA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d1145-158">**UploadPrinterDriverPackageW** (Unicode) and **UploadPrinterDriverPackageA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="d1145-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1145-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1145-160">Impressão</span><span class="sxs-lookup"><span data-stu-id="d1145-160">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d1145-161">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="d1145-161">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

