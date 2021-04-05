---
description: Especifica se um trabalho de impressão XPS está na fase de processamento de spool ou de renderização.
ms.assetid: 14871d29-59e4-45a2-9697-12550c58396c
title: Enumeração EPrintXPSJobOperation (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EPrintXPSJobOperation
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 917993be2af6e7a78afaec1ad4749dadcaebecba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662119"
---
# <a name="eprintxpsjoboperation-enumeration"></a><span data-ttu-id="bc711-103">Enumeração EPrintXPSJobOperation</span><span class="sxs-lookup"><span data-stu-id="bc711-103">EPrintXPSJobOperation enumeration</span></span>

<span data-ttu-id="bc711-104">Especifica se um trabalho de impressão XPS está na fase de processamento de spool ou de renderização.</span><span class="sxs-lookup"><span data-stu-id="bc711-104">Specifies whether an XPS print job is in the spooling or the rendering phase.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc711-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc711-105">Syntax</span></span>


```C++
typedef enum tagEPrintXPSJobOperation { 
  kJobProduction,
  kJobConsumption
} EPrintXPSJobOperation;
```



## <a name="constants"></a><span data-ttu-id="bc711-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="bc711-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bc711-107"><span id="kJobProduction"></span><span id="kjobproduction"></span><span id="KJOBPRODUCTION"></span>**kJobProduction**</span><span class="sxs-lookup"><span data-stu-id="bc711-107"><span id="kJobProduction"></span><span id="kjobproduction"></span><span id="KJOBPRODUCTION"></span>**kJobProduction**</span></span>
</dt> <dd>

<span data-ttu-id="bc711-108">O trabalho XPS está em spool.</span><span class="sxs-lookup"><span data-stu-id="bc711-108">The XPS job is spooling.</span></span>

</dd> <dt>

<span data-ttu-id="bc711-109"><span id="kJobConsumption"></span><span id="kjobconsumption"></span><span id="KJOBCONSUMPTION"></span>**kJobConsumption**</span><span class="sxs-lookup"><span data-stu-id="bc711-109"><span id="kJobConsumption"></span><span id="kjobconsumption"></span><span id="KJOBCONSUMPTION"></span>**kJobConsumption**</span></span>
</dt> <dd>

<span data-ttu-id="bc711-110">O trabalho XPS está sendo renderizado.</span><span class="sxs-lookup"><span data-stu-id="bc711-110">The XPS job is rendering.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc711-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc711-111">Remarks</span></span>

<span data-ttu-id="bc711-112">Essa enumeração é usada principalmente como um parâmetro para a função [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) .</span><span class="sxs-lookup"><span data-stu-id="bc711-112">This enumeration is primarily used as a parameter for the [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc711-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc711-113">Requirements</span></span>



| <span data-ttu-id="bc711-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc711-114">Requirement</span></span> | <span data-ttu-id="bc711-115">Valor</span><span class="sxs-lookup"><span data-stu-id="bc711-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc711-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc711-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bc711-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bc711-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="bc711-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc711-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bc711-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bc711-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bc711-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bc711-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc711-121"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bc711-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



 

 




