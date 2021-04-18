---
description: A função DeletePrinterDriverEx remove o nome de driver de impressora especificado da lista de nomes de drivers com suporte em um servidor e exclui os arquivos associados ao driver. Essa função também pode excluir versões específicas do driver.
ms.assetid: 1a3d7c7f-1d45-4877-a8f7-a77f40e3c319
title: Função DeletePrinterDriverEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverEx
- DeletePrinterDriverExA
- DeletePrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b88ef38236961286875a1885dad9dde936887d13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763001"
---
# <a name="deleteprinterdriverex-function"></a><span data-ttu-id="6fcba-104">Função DeletePrinterDriverEx</span><span class="sxs-lookup"><span data-stu-id="6fcba-104">DeletePrinterDriverEx function</span></span>

<span data-ttu-id="6fcba-105">A função **DeletePrinterDriverEx** remove o nome de driver de impressora especificado da lista de nomes de drivers com suporte em um servidor e exclui os arquivos associados ao driver.</span><span class="sxs-lookup"><span data-stu-id="6fcba-105">The **DeletePrinterDriverEx** function removes the specified printer-driver name from the list of names of supported drivers on a server and deletes the files associated with the driver.</span></span> <span data-ttu-id="6fcba-106">Essa função também pode excluir versões específicas do driver.</span><span class="sxs-lookup"><span data-stu-id="6fcba-106">This function can also delete specific versions of the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fcba-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6fcba-107">Syntax</span></span>


```C++
BOOL DeletePrinterDriverEx(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName,
  _In_ DWORD  dwDeleteFlag,
  _In_ DWORD  dwVersionFlag
);
```



## <a name="parameters"></a><span data-ttu-id="6fcba-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6fcba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fcba-109">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6fcba-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fcba-110">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor do qual o driver deve ser excluído.</span><span class="sxs-lookup"><span data-stu-id="6fcba-110">A pointer to a null-terminated string that specifies the name of the server from which the driver is to be deleted.</span></span> <span data-ttu-id="6fcba-111">Se esse parâmetro for **nulo**, a função excluirá o driver de impressora do computador local.</span><span class="sxs-lookup"><span data-stu-id="6fcba-111">If this parameter is **NULL**, the function deletes the printer-driver from the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="6fcba-112">*pEnvironment* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6fcba-112">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fcba-113">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente do qual o driver deve ser excluído (por exemplo, Windows NT x86, Windows IA64 ou Windows x64).</span><span class="sxs-lookup"><span data-stu-id="6fcba-113">A pointer to a null-terminated string that specifies the environment from which the driver is to be deleted (for example, Windows NT x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="6fcba-114">Se esse parâmetro for **nulo**, o nome do driver será excluído do ambiente atual do aplicativo de chamada e do computador cliente (não do aplicativo de destino e do servidor de impressão).</span><span class="sxs-lookup"><span data-stu-id="6fcba-114">If this parameter is **NULL**, the driver name is deleted from the current environment of the calling application and client computer (not of the destination application and print server).</span></span>

</dd> <dt>

<span data-ttu-id="6fcba-115">*pDriverName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6fcba-115">*pDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fcba-116">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do driver a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="6fcba-116">A pointer to a null-terminated string specifying the name of the driver to delete.</span></span>

</dd> <dt>

<span data-ttu-id="6fcba-117">*dwDeleteFlag* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6fcba-117">*dwDeleteFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fcba-118">As opções para excluir arquivos e versões do driver.</span><span class="sxs-lookup"><span data-stu-id="6fcba-118">The options for deleting files and versions of the driver.</span></span> <span data-ttu-id="6fcba-119">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6fcba-119">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="6fcba-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6fcba-120">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="6fcba-121">Significado</span><span class="sxs-lookup"><span data-stu-id="6fcba-121">Meaning</span></span>                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DPD_DELETE_SPECIFIC_VERSION"></span><span id="dpd_delete_specific_version"></span><dl> <span data-ttu-id="6fcba-122"><dt>**DPD \_ excluir \_ \_ versão específica**</dt></span><span class="sxs-lookup"><span data-stu-id="6fcba-122"><dt>**DPD\_DELETE\_SPECIFIC\_VERSION**</dt></span></span> </dl> | <span data-ttu-id="6fcba-123">Exclui a versão especificada em *dwVersionFlag*.</span><span class="sxs-lookup"><span data-stu-id="6fcba-123">Deletes the version specified in *dwVersionFlag*.</span></span> <span data-ttu-id="6fcba-124">Isso não garante que o driver será removido da lista de drivers com suporte para o servidor.</span><span class="sxs-lookup"><span data-stu-id="6fcba-124">This does not ensure that the driver will be removed from the list of supported drivers for the server.</span></span><br/>                  |
| <span id="DPD_DELETE_UNUSED_FILES"></span><span id="dpd_delete_unused_files"></span><dl> <span data-ttu-id="6fcba-125"><dt>**DPD \_ excluir \_ arquivos não utilizados \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6fcba-125"><dt>**DPD\_DELETE\_UNUSED\_FILES**</dt></span></span> </dl>             | <span data-ttu-id="6fcba-126">Remove todos os arquivos de driver não utilizados.</span><span class="sxs-lookup"><span data-stu-id="6fcba-126">Removes any unused driver files.</span></span><br/>                                                                                                                                           |
| <span id="DPD_DELETE_ALL_FILES"></span><span id="dpd_delete_all_files"></span><dl> <span data-ttu-id="6fcba-127"><dt>**DPD \_ excluir \_ todos os \_ arquivos**</dt></span><span class="sxs-lookup"><span data-stu-id="6fcba-127"><dt>**DPD\_DELETE\_ALL\_FILES**</dt></span></span> </dl>                      | <span data-ttu-id="6fcba-128">Excluirá o driver somente se todos os seus arquivos associados puderem ser removidos.</span><span class="sxs-lookup"><span data-stu-id="6fcba-128">Deletes the driver only if all its associated files can be removed.</span></span> <span data-ttu-id="6fcba-129">A operação de exclusão falhará se qualquer um dos arquivos do driver estiver sendo usado por algum outro driver instalado.</span><span class="sxs-lookup"><span data-stu-id="6fcba-129">The delete operation fails if any of the driver's files are being used by some other installed driver.</span></span><br/> |



 

<span data-ttu-id="6fcba-130">Se DPD \_ excluir \_ \_ versão específica não for especificado, a função excluirá todas as versões do driver se nenhuma delas estiver em uso.</span><span class="sxs-lookup"><span data-stu-id="6fcba-130">If DPD\_DELETE\_SPECIFIC\_VERSION is not specified, the function deletes all versions of the driver if none of them is in use.</span></span> <span data-ttu-id="6fcba-131">Se nem DPD \_ excluir \_ arquivos não utilizados \_ nem DPD \_ excluir \_ todos os \_ arquivos for especificado, a função não excluirá os arquivos de driver.</span><span class="sxs-lookup"><span data-stu-id="6fcba-131">If neither DPD\_DELETE\_UNUSED\_FILES nor DPD\_DELETE\_ALL\_FILES is specified, the function does not delete driver files.</span></span>

</dd> <dt>

<span data-ttu-id="6fcba-132">*dwVersionFlag* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6fcba-132">*dwVersionFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fcba-133">A versão do driver a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="6fcba-133">The version of the driver to be deleted.</span></span> <span data-ttu-id="6fcba-134">Esse parâmetro pode ser 0, 1, 2 ou 3.</span><span class="sxs-lookup"><span data-stu-id="6fcba-134">This parameter can be 0, 1, 2 or 3.</span></span> <span data-ttu-id="6fcba-135">Esse parâmetro será usado somente se *dwDeleteFlag* incluir o \_ sinalizador de versão específica de exclusão de DPD \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6fcba-135">This parameter is used only if *dwDeleteFlag* includes the DPD\_DELETE\_SPECIFIC\_VERSION flag.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fcba-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6fcba-136">Return value</span></span>

<span data-ttu-id="6fcba-137">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="6fcba-137">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="6fcba-138">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="6fcba-138">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fcba-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="6fcba-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6fcba-140">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="6fcba-140">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="6fcba-141">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6fcba-141">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="6fcba-142">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="6fcba-142">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="6fcba-143">Antes que a função exclua os arquivos de driver, ele chama a função **DrvDriverEvent** do driver, permitindo que o driver remova todos os arquivos privados que não são usados.</span><span class="sxs-lookup"><span data-stu-id="6fcba-143">Before the function deletes the driver files, it calls the driver's **DrvDriverEvent** function, allowing the driver to remove any private files that are not used.</span></span> <span data-ttu-id="6fcba-144">Para obter mais informações sobre o **DrvDriverEvent**, consulte o Microsoft Windows Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="6fcba-144">For more information about **DrvDriverEvent**, see the Microsoft Windows Driver Development Kit (DDK).</span></span>

<span data-ttu-id="6fcba-145">Se os arquivos de driver estiverem carregados no momento, a função os moverá para um diretório temporário e os marcará para exclusão na reinicialização.</span><span class="sxs-lookup"><span data-stu-id="6fcba-145">If the driver files are currently loaded, the function moves them to a temp directory and marks them for deletion on restart.</span></span>

<span data-ttu-id="6fcba-146">Antes de chamar **DeletePrinterDriverEx**, você deve excluir todos os objetos de impressora que usam o driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="6fcba-146">Before calling **DeletePrinterDriverEx**, you must delete all printer objects that use the printer driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fcba-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fcba-147">Requirements</span></span>



| <span data-ttu-id="6fcba-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fcba-148">Requirement</span></span> | <span data-ttu-id="6fcba-149">Valor</span><span class="sxs-lookup"><span data-stu-id="6fcba-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fcba-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fcba-150">Minimum supported client</span></span><br/> | <span data-ttu-id="6fcba-151">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6fcba-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6fcba-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fcba-152">Minimum supported server</span></span><br/> | <span data-ttu-id="6fcba-153">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6fcba-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6fcba-154">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6fcba-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fcba-155"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6fcba-155"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6fcba-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6fcba-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="6fcba-157"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6fcba-157"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="6fcba-158">DLL</span><span class="sxs-lookup"><span data-stu-id="6fcba-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fcba-159"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="6fcba-159"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="6fcba-160">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="6fcba-160">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6fcba-161">**DeletePrinterDriverExW** (Unicode) e **DeletePrinterDriverExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6fcba-161">**DeletePrinterDriverExW** (Unicode) and **DeletePrinterDriverExA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="6fcba-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="6fcba-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fcba-163">Impressão</span><span class="sxs-lookup"><span data-stu-id="6fcba-163">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6fcba-164">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="6fcba-164">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="6fcba-165">**AddPrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="6fcba-165">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> </dl>

 

 




