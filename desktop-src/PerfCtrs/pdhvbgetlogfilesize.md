---
description: A função PdhVbGetLogFileSize retorna o tamanho do arquivo de log especificado. Essa função chama PdhGetLogFileSize.
ms.assetid: 8f4fbb68-b0f5-4163-ae6e-5b7139a35adf
title: Função PdhVbGetLogFileSize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetLogFileSize
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 0b9f490477704086bd9aa8c53dd32456d486471e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756879"
---
# <a name="pdhvbgetlogfilesize-function"></a><span data-ttu-id="b5167-104">Função PdhVbGetLogFileSize</span><span class="sxs-lookup"><span data-stu-id="b5167-104">PdhVbGetLogFileSize function</span></span>

<span data-ttu-id="b5167-105">A função **PdhVbGetLogFileSize** retorna o tamanho do arquivo de log especificado.</span><span class="sxs-lookup"><span data-stu-id="b5167-105">The **PdhVbGetLogFileSize** function returns the size of the specified log file.</span></span> <span data-ttu-id="b5167-106">Essa função chama [**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize).</span><span class="sxs-lookup"><span data-stu-id="b5167-106">This function calls [**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b5167-107">A função que este tópico descreve pode ser alterada ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="b5167-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="b5167-108">Em vez disso, a Microsoft recomenda que você use as funções descritas em [funções de contadores de desempenho](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="b5167-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="b5167-109">Função PdhVbGetLogFileSize ( \_ ByVal HLog como PDH \_ hLog, \_ ByRef llSize como Long \_ ) como DWORD</span><span class="sxs-lookup"><span data-stu-id="b5167-109">Function PdhVbGetLogFileSize( \_ ByVal hLog As PDH\_HLOG, \_ ByRef llSize As LONG \_ ) As DWORD</span></span>

## <a name="parameters"></a><span data-ttu-id="b5167-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5167-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5167-111">*hLog* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b5167-111">*hLog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5167-112">Identificador para o arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="b5167-112">Handle to the log file.</span></span> <span data-ttu-id="b5167-113">Esse identificador é retornado pela função [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) .</span><span class="sxs-lookup"><span data-stu-id="b5167-113">This handle is returned by the [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) function.</span></span>

</dd> <dt>

<span data-ttu-id="b5167-114">*llSize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b5167-114">*llSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5167-115">Ponteiro para uma variável que recebe o tamanho do arquivo de log, em bytes.</span><span class="sxs-lookup"><span data-stu-id="b5167-115">Pointer to a variable that receives the size of the log file, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5167-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b5167-116">Return value</span></span>

<span data-ttu-id="b5167-117">Se a função for realizada com sucesso, ela retornará 0.</span><span class="sxs-lookup"><span data-stu-id="b5167-117">If the function succeeds, it returns 0.</span></span>

<span data-ttu-id="b5167-118">Se a função falhar, o valor de retorno será um [código de erro do sistema](/windows/desktop/Debug/system-error-codes) ou um código de [erro PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b5167-118">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="b5167-119">Os valores a seguir são possíveis.</span><span class="sxs-lookup"><span data-stu-id="b5167-119">The following are possible values.</span></span>



| <span data-ttu-id="b5167-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b5167-120">Return code</span></span>                                                                                                | <span data-ttu-id="b5167-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5167-121">Description</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b5167-122"><dt>**\_buffer insuficiente de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5167-122"><dt>**PDH\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>   | <span data-ttu-id="b5167-123">Os dados solicitados são maiores que o buffer fornecido.</span><span class="sxs-lookup"><span data-stu-id="b5167-123">The requested data is larger than the buffer supplied.</span></span> <span data-ttu-id="b5167-124">Não é possível retornar os dados solicitados.</span><span class="sxs-lookup"><span data-stu-id="b5167-124">Unable to return the requested data.</span></span><br/> |
| <dl> <span data-ttu-id="b5167-125"><dt>**\_argumento inválido de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5167-125"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>      | <span data-ttu-id="b5167-126">Um ou mais dos buffers de cadeia de caracteres não tem o tamanho correto.</span><span class="sxs-lookup"><span data-stu-id="b5167-126">One or more of the string buffers is not the correct size.</span></span><br/>                                  |
| <dl> <span data-ttu-id="b5167-127"><dt>**\_identificador inválido de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5167-127"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>        | <span data-ttu-id="b5167-128">O identificador não é um objeto PDH válido.</span><span class="sxs-lookup"><span data-stu-id="b5167-128">The handle is not a valid PDH object.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="b5167-129"><dt>**\_ \_ \_ erro ao abrir arquivo de log PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5167-129"><dt>**PDH\_LOG\_FILE\_OPEN\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="b5167-130">Não é possível abrir o arquivo de log especificado.</span><span class="sxs-lookup"><span data-stu-id="b5167-130">Unable to open the specified log file.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="b5167-131"><dt>**\_arquivo PDH \_ não \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="b5167-131"><dt>**PDH\_FILE\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="b5167-132">Não é possível localizar o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="b5167-132">Unable to find the specified file.</span></span><br/>                                                          |



 

## <a name="requirements"></a><span data-ttu-id="b5167-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5167-133">Requirements</span></span>



| <span data-ttu-id="b5167-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5167-134">Requirement</span></span> | <span data-ttu-id="b5167-135">Valor</span><span class="sxs-lookup"><span data-stu-id="b5167-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b5167-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5167-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b5167-137">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b5167-137">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b5167-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5167-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b5167-139">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b5167-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b5167-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b5167-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="b5167-141"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5167-141"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="b5167-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b5167-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5167-143"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5167-143"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5167-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5167-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5167-145">**PdhGetLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="b5167-145">**PdhGetLogFileSize**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
</dt> <dt>

[<span data-ttu-id="b5167-146">**PdhVbOpenLog**</span><span class="sxs-lookup"><span data-stu-id="b5167-146">**PdhVbOpenLog**</span></span>](pdhvbopenlog.md)
</dt> <dt>

[<span data-ttu-id="b5167-147">**PdhVbUpdateLog**</span><span class="sxs-lookup"><span data-stu-id="b5167-147">**PdhVbUpdateLog**</span></span>](pdhvbupdatelog.md)
</dt> </dl>

 

