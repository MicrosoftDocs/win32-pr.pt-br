---
description: A função GetEnabledProtocols retorna uma tabela de todos os protocolos marcados como habilitados.
ms.assetid: 11feac64-c770-47b2-a740-fc372e97b8ed
title: Função GetEnabledProtocols (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetEnabledProtocols
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 284d6c87bf5a3b26d6c3f379a710966be21006d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747940"
---
# <a name="getenabledprotocols-function"></a><span data-ttu-id="77046-103">Função GetEnabledProtocols</span><span class="sxs-lookup"><span data-stu-id="77046-103">GetEnabledProtocols function</span></span>

<span data-ttu-id="77046-104">A função **GetEnabledProtocols** retorna uma tabela de todos os protocolos marcados como habilitados.</span><span class="sxs-lookup"><span data-stu-id="77046-104">The **GetEnabledProtocols** function returns a table of all protocols that are marked Enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="77046-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77046-105">Syntax</span></span>


```C++
LPPROTOCOLTABLE WINAPI GetEnabledProtocols(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="77046-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77046-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77046-107">*hCapture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="77046-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77046-108">Identificador para a captura.</span><span class="sxs-lookup"><span data-stu-id="77046-108">Handle to the capture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77046-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77046-109">Return value</span></span>

<span data-ttu-id="77046-110">Se a função for bem-sucedida, o valor de retorno será um ponteiro para uma estrutura de [protocoltable](protocoltable.md) que lista todos os protocolos habilitados na captura.</span><span class="sxs-lookup"><span data-stu-id="77046-110">If the function is successful, the return value is a pointer to a [PROTOCOLTABLE](protocoltable.md) structure that lists all the enabled protocols in the capture.</span></span>

<span data-ttu-id="77046-111">Se a função não for bem-sucedida, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="77046-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="77046-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="77046-112">Remarks</span></span>

<span data-ttu-id="77046-113">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetEnabledProtocols** .</span><span class="sxs-lookup"><span data-stu-id="77046-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetEnabledProtocols** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="77046-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77046-114">Requirements</span></span>



| <span data-ttu-id="77046-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="77046-115">Requirement</span></span> | <span data-ttu-id="77046-116">Valor</span><span class="sxs-lookup"><span data-stu-id="77046-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="77046-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77046-117">Minimum supported client</span></span><br/> | <span data-ttu-id="77046-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="77046-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="77046-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77046-119">Minimum supported server</span></span><br/> | <span data-ttu-id="77046-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="77046-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="77046-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="77046-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="77046-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="77046-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="77046-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="77046-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="77046-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77046-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="77046-125">DLL</span><span class="sxs-lookup"><span data-stu-id="77046-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77046-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77046-126"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77046-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="77046-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77046-128">PROTOCOLOtable</span><span class="sxs-lookup"><span data-stu-id="77046-128">PROTOCOLTABLE</span></span>](protocoltable.md)
</dt> </dl>

 

 




