---
description: A função GetFrameMacType retorna o tipo de MAC do quadro.
ms.assetid: 8d3da770-1392-4638-a267-32c2dae289b0
title: Função GetFrameMacType (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameMacType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b85accc64a6e29424e3f65d070bafcf29bb3ec0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920698"
---
# <a name="getframemactype-function"></a><span data-ttu-id="8d9f5-103">Função GetFrameMacType</span><span class="sxs-lookup"><span data-stu-id="8d9f5-103">GetFrameMacType function</span></span>

<span data-ttu-id="8d9f5-104">A função **GetFrameMacType** retorna o tipo de Mac do quadro.</span><span class="sxs-lookup"><span data-stu-id="8d9f5-104">The **GetFrameMacType** function returns the MAC type of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d9f5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d9f5-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameMacType(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="8d9f5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d9f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d9f5-107">*hFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8d9f5-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d9f5-108">Identificador para o quadro.</span><span class="sxs-lookup"><span data-stu-id="8d9f5-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d9f5-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8d9f5-109">Return value</span></span>

<span data-ttu-id="8d9f5-110">A função retorna o tipo de MAC do quadro, que pode ter um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8d9f5-110">The function returns the MAC type of the frame, which can have one of the following values.</span></span>

-   <span data-ttu-id="8d9f5-111">tipo de MAC \_ \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="8d9f5-111">MAC\_TYPE\_UNKNOWN</span></span>
-   <span data-ttu-id="8d9f5-112">tipo de MAC \_ \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="8d9f5-112">MAC\_TYPE\_ETHERNET</span></span>
-   <span data-ttu-id="8d9f5-113">tipo de MAC \_ \_ TOKENRING</span><span class="sxs-lookup"><span data-stu-id="8d9f5-113">MAC\_TYPE\_TOKENRING</span></span>
-   <span data-ttu-id="8d9f5-114">tipo de MAC \_ \_ FDDI</span><span class="sxs-lookup"><span data-stu-id="8d9f5-114">MAC\_TYPE\_FDDI</span></span>

## <a name="remarks"></a><span data-ttu-id="8d9f5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d9f5-115">Remarks</span></span>

<span data-ttu-id="8d9f5-116">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetFrameMacType** .</span><span class="sxs-lookup"><span data-stu-id="8d9f5-116">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameMacType** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d9f5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d9f5-117">Requirements</span></span>



| <span data-ttu-id="8d9f5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d9f5-118">Requirement</span></span> | <span data-ttu-id="8d9f5-119">Valor</span><span class="sxs-lookup"><span data-stu-id="8d9f5-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8d9f5-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d9f5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8d9f5-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8d9f5-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8d9f5-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d9f5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8d9f5-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8d9f5-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8d9f5-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8d9f5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d9f5-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d9f5-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="8d9f5-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8d9f5-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="8d9f5-127"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d9f5-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="8d9f5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8d9f5-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d9f5-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d9f5-129"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




