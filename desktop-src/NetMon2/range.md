---
description: A estrutura do intervalo define um intervalo de valores de propriedade válidos.
ms.assetid: 7bd14410-f5c1-487b-8776-405567991e5a
title: Estrutura do intervalo (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RANGE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: bf465636f315e60e43350bb370e2002b8a96e635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757017"
---
# <a name="range-structure"></a><span data-ttu-id="623d1-103">Estrutura do intervalo</span><span class="sxs-lookup"><span data-stu-id="623d1-103">RANGE structure</span></span>

<span data-ttu-id="623d1-104">A estrutura do **intervalo** define um intervalo de valores de propriedade válidos.</span><span class="sxs-lookup"><span data-stu-id="623d1-104">The **RANGE** structure defines a range of valid property values.</span></span>

## <a name="syntax"></a><span data-ttu-id="623d1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="623d1-105">Syntax</span></span>


```C++
typedef struct range {
  DWORD MinValue;
  DWORD MaxValue;
} RANGE, *LPRANGE;
```



## <a name="members"></a><span data-ttu-id="623d1-106">Membros</span><span class="sxs-lookup"><span data-stu-id="623d1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="623d1-107">**MinValue**</span><span class="sxs-lookup"><span data-stu-id="623d1-107">**MinValue**</span></span>
</dt> <dd>

<span data-ttu-id="623d1-108">Menor valor possível em um intervalo.</span><span class="sxs-lookup"><span data-stu-id="623d1-108">Lowest possible value in a range.</span></span>

</dd> <dt>

<span data-ttu-id="623d1-109">**MaxValue**</span><span class="sxs-lookup"><span data-stu-id="623d1-109">**MaxValue**</span></span>
</dt> <dd>

<span data-ttu-id="623d1-110">Maior valor possível em um intervalo.</span><span class="sxs-lookup"><span data-stu-id="623d1-110">Highest possible value in a range.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="623d1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="623d1-111">Remarks</span></span>

<span data-ttu-id="623d1-112">A estrutura do **intervalo** é usada para especificar um intervalo válido de números para uma propriedade de protocolo.</span><span class="sxs-lookup"><span data-stu-id="623d1-112">The **RANGE** structure is used to specify a valid range of numbers for a protocol property.</span></span> <span data-ttu-id="623d1-113">Se o membro **Dataqualificador** da estrutura **PropertyInfo** estiver definido como **prop \_ igual \_ Range**, o membro **lpRange** da estrutura [PropertyInfo](propertyinfo.md) deverá fornecer um ponteiro para uma estrutura de **intervalo** .</span><span class="sxs-lookup"><span data-stu-id="623d1-113">If the **DataQualifier** member of the **PROPERTYINFO** structure is set to **PROP\_QUAL\_RANGE**, the **lpRange** member of the [PROPERTYINFO](propertyinfo.md) structure must provide a pointer to a **RANGE** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="623d1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="623d1-114">Requirements</span></span>



| <span data-ttu-id="623d1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="623d1-115">Requirement</span></span> | <span data-ttu-id="623d1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="623d1-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="623d1-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="623d1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="623d1-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="623d1-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="623d1-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="623d1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="623d1-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="623d1-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="623d1-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="623d1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="623d1-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="623d1-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="623d1-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="623d1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="623d1-124">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="623d1-124">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> </dl>

 

 




