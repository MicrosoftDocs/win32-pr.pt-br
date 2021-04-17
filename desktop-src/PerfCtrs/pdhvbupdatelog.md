---
description: A função de função PdhVbUpdateLog atualiza a consulta atual e grava novos dados no arquivo de log. Essa função chama PdhUpdateLog.
ms.assetid: a7a3ad18-2d61-448e-9764-ba363398e804
title: Função PdhVbUpdateLog
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbUpdateLog
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: c02e533f57481004b0a7de9f779399b20bddc0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758288"
---
# <a name="pdhvbupdatelog-function"></a><span data-ttu-id="be7d5-104">Função PdhVbUpdateLog</span><span class="sxs-lookup"><span data-stu-id="be7d5-104">PdhVbUpdateLog function</span></span>

<span data-ttu-id="be7d5-105">A função de função **PdhVbUpdateLog** atualiza a consulta atual e grava novos dados no arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="be7d5-105">The **PdhVbUpdateLog** function function updates the current query and writes new data to the log file.</span></span> <span data-ttu-id="be7d5-106">Essa função chama [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga).</span><span class="sxs-lookup"><span data-stu-id="be7d5-106">This function calls [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be7d5-107">A função que este tópico descreve pode ser alterada ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="be7d5-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="be7d5-108">Em vez disso, a Microsoft recomenda que você use as funções descritas em [funções de contadores de desempenho](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="be7d5-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="be7d5-109">Função PdhVbUpdateLog ( \_ ByVal HLog as \_ hLog PDH, \_ ByVal szUserString as LPCTSTR \_ )</span><span class="sxs-lookup"><span data-stu-id="be7d5-109">Function PdhVbUpdateLog( \_ ByVal hLog As PDH\_HLOG, \_ ByVal szUserString As LPCTSTR \_ )</span></span>

## <a name="parameters"></a><span data-ttu-id="be7d5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be7d5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be7d5-111">*hLog* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="be7d5-111">*hLog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be7d5-112">Identificador para o arquivo de log a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="be7d5-112">Handle to the log file to be updated.</span></span> <span data-ttu-id="be7d5-113">Esse identificador é retornado pela função [**PdhVbOpenLog**](pdhvbopenlog.md) .</span><span class="sxs-lookup"><span data-stu-id="be7d5-113">This handle is returned by the [**PdhVbOpenLog**](pdhvbopenlog.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="be7d5-114">*szUserString* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="be7d5-114">*szUserString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be7d5-115">Ponteiro para uma cadeia de caracteres que especifica os dados a serem adicionados ao arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="be7d5-115">Pointer to a string that specifies the data to be added to the log file.</span></span> <span data-ttu-id="be7d5-116">Isso geralmente é usado para comentários no arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="be7d5-116">This is generally used for comments within the log file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be7d5-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="be7d5-117">Return value</span></span>

<span data-ttu-id="be7d5-118">Se a função for realizada com sucesso, ela retornará 0.</span><span class="sxs-lookup"><span data-stu-id="be7d5-118">If the function succeeds, it returns 0.</span></span>

<span data-ttu-id="be7d5-119">Se a função falhar, o valor de retorno será um [código de erro do sistema](/windows/desktop/Debug/system-error-codes) ou um código de [erro PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="be7d5-119">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="be7d5-120">Os valores a seguir são possíveis.</span><span class="sxs-lookup"><span data-stu-id="be7d5-120">The following are possible values.</span></span>



| <span data-ttu-id="be7d5-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="be7d5-121">Return code</span></span>                                                                                                | <span data-ttu-id="be7d5-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="be7d5-122">Description</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="be7d5-123"><dt>**\_buffer insuficiente de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="be7d5-123"><dt>**PDH\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>   | <span data-ttu-id="be7d5-124">Os dados solicitados são maiores que o buffer fornecido.</span><span class="sxs-lookup"><span data-stu-id="be7d5-124">The requested data is larger than the buffer supplied.</span></span> <span data-ttu-id="be7d5-125">Não é possível retornar os dados solicitados.</span><span class="sxs-lookup"><span data-stu-id="be7d5-125">Unable to return the requested data.</span></span><br/> |
| <dl> <span data-ttu-id="be7d5-126"><dt>**\_argumento inválido de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="be7d5-126"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>      | <span data-ttu-id="be7d5-127">Um ou mais dos buffers de cadeia de caracteres não tem o tamanho correto.</span><span class="sxs-lookup"><span data-stu-id="be7d5-127">One or more of the string buffers is not the correct size.</span></span><br/>                                  |
| <dl> <span data-ttu-id="be7d5-128"><dt>**\_identificador inválido de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="be7d5-128"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>        | <span data-ttu-id="be7d5-129">O identificador não é um objeto PDH válido.</span><span class="sxs-lookup"><span data-stu-id="be7d5-129">The handle is not a valid PDH object.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="be7d5-130"><dt>**\_ \_ \_ erro ao abrir arquivo de log PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="be7d5-130"><dt>**PDH\_LOG\_FILE\_OPEN\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="be7d5-131">Não é possível abrir o arquivo de log especificado.</span><span class="sxs-lookup"><span data-stu-id="be7d5-131">Unable to open the specified log file.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="be7d5-132"><dt>**\_arquivo PDH \_ não \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="be7d5-132"><dt>**PDH\_FILE\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="be7d5-133">Não é possível localizar o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="be7d5-133">Unable to find the specified file.</span></span><br/>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="be7d5-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="be7d5-134">Remarks</span></span>

<span data-ttu-id="be7d5-135">Deve haver uma consulta aberta no momento e os contadores desejados devem ser adicionados a ela antes que essa função seja chamada.</span><span class="sxs-lookup"><span data-stu-id="be7d5-135">There must be a currently opened query, and the desired counters must be added to it before this function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="be7d5-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be7d5-136">Requirements</span></span>



| <span data-ttu-id="be7d5-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="be7d5-137">Requirement</span></span> | <span data-ttu-id="be7d5-138">Valor</span><span class="sxs-lookup"><span data-stu-id="be7d5-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="be7d5-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be7d5-139">Minimum supported client</span></span><br/> | <span data-ttu-id="be7d5-140">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="be7d5-140">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="be7d5-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be7d5-141">Minimum supported server</span></span><br/> | <span data-ttu-id="be7d5-142">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="be7d5-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="be7d5-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="be7d5-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="be7d5-144"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be7d5-144"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="be7d5-145">DLL</span><span class="sxs-lookup"><span data-stu-id="be7d5-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be7d5-146"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be7d5-146"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be7d5-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="be7d5-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be7d5-148">**PdhUpdateLog**</span><span class="sxs-lookup"><span data-stu-id="be7d5-148">**PdhUpdateLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
</dt> <dt>

[<span data-ttu-id="be7d5-149">**PdhVbGetLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="be7d5-149">**PdhVbGetLogFileSize**</span></span>](pdhvbgetlogfilesize.md)
</dt> <dt>

[<span data-ttu-id="be7d5-150">**PdhVbOpenLog**</span><span class="sxs-lookup"><span data-stu-id="be7d5-150">**PdhVbOpenLog**</span></span>](pdhvbopenlog.md)
</dt> </dl>

 

