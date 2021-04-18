---
description: O GetPrintExecutionData recupera o contexto de impressão atual.
ms.assetid: bb9506aa-a0da-46bc-a86a-84a79587cd50
title: Função GetPrintExecutionData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintExecutionData
api_type:
- DllExport
api_location:
- winspool.drv
ms.openlocfilehash: a1b2f2674c9ef186338c91ed2e4500d8408964d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764051"
---
# <a name="getprintexecutiondata-function"></a><span data-ttu-id="26d0c-103">Função GetPrintExecutionData</span><span class="sxs-lookup"><span data-stu-id="26d0c-103">GetPrintExecutionData function</span></span>

<span data-ttu-id="26d0c-104">O **GetPrintExecutionData** recupera o contexto de impressão atual.</span><span class="sxs-lookup"><span data-stu-id="26d0c-104">The **GetPrintExecutionData** retrieves the current print context.</span></span>

> [!Note]  
> <span data-ttu-id="26d0c-105">Essa função destina-se a uso por drivers de impressora que estão em execução no contexto do spooler de impressão.</span><span class="sxs-lookup"><span data-stu-id="26d0c-105">This function is intended for use by printer drivers that are running in the context of the print spooler.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="26d0c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26d0c-106">Syntax</span></span>


```C++
BOOL WINAPI GetPrintExecutionData(
  _Out_ PRINT_EXECUTION_DATA *pData
);
```



## <a name="parameters"></a><span data-ttu-id="26d0c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26d0c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26d0c-108">*pData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="26d0c-108">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26d0c-109">Um ponteiro para uma variável que recebe o endereço da estrutura [**de \_ \_ dados de execução de impressão**](print-execution-data.md) .</span><span class="sxs-lookup"><span data-stu-id="26d0c-109">A pointer to a variable that receives the address of the [**PRINT\_EXECUTION\_DATA**](print-execution-data.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26d0c-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="26d0c-110">Return value</span></span>

<span data-ttu-id="26d0c-111">Retornará **true** se a função tiver sucesso; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="26d0c-111">Returns **TRUE** if the function succeeds; otherwise **FALSE**.</span></span> <span data-ttu-id="26d0c-112">Se o valor de retorno for **false**, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter o status de erro.</span><span class="sxs-lookup"><span data-stu-id="26d0c-112">If the return value is **FALSE**, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="26d0c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="26d0c-113">Remarks</span></span>

<span data-ttu-id="26d0c-114">Os drivers de impressora devem chamar o [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) no módulo winspool. drv para obter o endereço da função **GetPrintExecutionData** porque o **GetPrintExecutionData** não tem suporte no Windows Vista ou em versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="26d0c-114">Printer drivers should call [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) on the winspool.drv module to get the address of the **GetPrintExecutionData** function because **GetPrintExecutionData** is not supported on Windows Vista or earlier versions of Windows.</span></span>

<span data-ttu-id="26d0c-115">**GetPrintExecutionData** só falhará se o valor de *pData* for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="26d0c-115">**GetPrintExecutionData** only fails if the value of *pData* is **NULL**.</span></span>

<span data-ttu-id="26d0c-116">O valor do membro **clientAppPID** dos [**dados de \_ execução \_ de impressão**](print-execution-data.md) só será significativo se o valor do **contexto** for o contexto de **execução de impressão \_ \_ \_ WOW64**.</span><span class="sxs-lookup"><span data-stu-id="26d0c-116">The value of the **clientAppPID** member of [**PRINT\_EXECUTION\_DATA**](print-execution-data.md) is only meaningful if the value of **context** is **PRINT\_EXECUTION\_CONTEXT\_WOW64**.</span></span> <span data-ttu-id="26d0c-117">Se o valor do **contexto** não for **o \_ contexto de execução de impressão \_ \_ WOW64**, o valor de **clientAppPID** será 0.</span><span class="sxs-lookup"><span data-stu-id="26d0c-117">If the value of **context** is not **PRINT\_EXECUTION\_CONTEXT\_WOW64**, the value of **clientAppPID** is 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="26d0c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26d0c-118">Requirements</span></span>



| <span data-ttu-id="26d0c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="26d0c-119">Requirement</span></span> | <span data-ttu-id="26d0c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="26d0c-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26d0c-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26d0c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="26d0c-122">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="26d0c-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="26d0c-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26d0c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="26d0c-124">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="26d0c-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="26d0c-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="26d0c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="26d0c-126"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="26d0c-126"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="26d0c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="26d0c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26d0c-128"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="26d0c-128"><dt>Winspool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="26d0c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="26d0c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26d0c-130">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="26d0c-130">**GetLastError**</span></span>](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="26d0c-131">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="26d0c-131">**GetProcAddress**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="26d0c-132">**\_contexto de execução de impressão \_**</span><span class="sxs-lookup"><span data-stu-id="26d0c-132">**PRINT\_EXECUTION\_CONTEXT**</span></span>](print-execution-context.md)
</dt> <dt>

[<span data-ttu-id="26d0c-133">**IMPRIMIR \_ dados de execução \_**</span><span class="sxs-lookup"><span data-stu-id="26d0c-133">**PRINT\_EXECUTION\_DATA**</span></span>](print-execution-data.md)
</dt> </dl>

 

