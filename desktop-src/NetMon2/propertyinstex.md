---
description: A estrutura PROPERTYINSTEX define uma instância de forma livre e de propriedade estendida.
ms.assetid: a2316baf-07e2-4617-bb35-e20cfb11fbcb
title: Estrutura PROPERTYINSTEX (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINSTEX
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f7b196d30e96f9d047f7f923d969d65a918aa4f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787044"
---
# <a name="propertyinstex-structure"></a><span data-ttu-id="0e8c3-103">Estrutura PROPERTYINSTEX</span><span class="sxs-lookup"><span data-stu-id="0e8c3-103">PROPERTYINSTEX structure</span></span>

<span data-ttu-id="0e8c3-104">A estrutura **PROPERTYINSTEX** define uma instância de forma livre e de propriedade estendida.</span><span class="sxs-lookup"><span data-stu-id="0e8c3-104">The **PROPERTYINSTEX** structure defines a freeform, extended property instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e8c3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e8c3-105">Syntax</span></span>


```C++
typedef struct _PROPERTYINSTEX {
  WORD    Length;
  WORD    LengthEx;
  ULPVOID lpData;
  union {
    BYTE          Byte[];
    WORD          Word[];
    DWORD         Dword[];
    LARGE_INTEGER LargeInt[];
    SYSTEMTIME    SysTime[];
    TYPED_STRING  TypedString;
  };
} PROPERTYINSTEX;
```



## <a name="members"></a><span data-ttu-id="0e8c3-106">Membros</span><span class="sxs-lookup"><span data-stu-id="0e8c3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0e8c3-107">**Comprimento**</span><span class="sxs-lookup"><span data-stu-id="0e8c3-107">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="0e8c3-108">Comprimento dos dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="0e8c3-108">Length of the data in Bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0e8c3-109">**LengthEx**</span><span class="sxs-lookup"><span data-stu-id="0e8c3-109">**LengthEx**</span></span>
</dt> <dd>

<span data-ttu-id="0e8c3-110">Comprimento dos dados estendidos.</span><span class="sxs-lookup"><span data-stu-id="0e8c3-110">Length of the extended data.</span></span>

</dd> <dt>

<span data-ttu-id="0e8c3-111">**lpData**</span><span class="sxs-lookup"><span data-stu-id="0e8c3-111">**lpData**</span></span>
</dt> <dd>

<span data-ttu-id="0e8c3-112">Ponteiro para os dados estendidos.</span><span class="sxs-lookup"><span data-stu-id="0e8c3-112">Pointer to the extended data.</span></span>

</dd> <dt>

<span data-ttu-id="0e8c3-113">**Byte**</span><span class="sxs-lookup"><span data-stu-id="0e8c3-113">**Byte**</span></span>
</dt> <dd>

<span data-ttu-id="0e8c3-114">Ponteiro para os dados de **byte** .</span><span class="sxs-lookup"><span data-stu-id="0e8c3-114">Pointer to the **BYTE** data.</span></span>

</dd> <dt>

<span data-ttu-id="0e8c3-115">**Word**</span><span class="sxs-lookup"><span data-stu-id="0e8c3-115">**Word**</span></span>
</dt> <dd>

<span data-ttu-id="0e8c3-116">Ponteiro para os dados do **Word** .</span><span class="sxs-lookup"><span data-stu-id="0e8c3-116">Pointer to the **WORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="0e8c3-117">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="0e8c3-117">**Dword**</span></span>
</dt> <dd>

<span data-ttu-id="0e8c3-118">Ponteiro para os dados **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="0e8c3-118">Pointer to the **DWORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="0e8c3-119">**LargeInt**</span><span class="sxs-lookup"><span data-stu-id="0e8c3-119">**LargeInt**</span></span>
</dt> <dd>

<span data-ttu-id="0e8c3-120">Ponteiro para os dados de **LARGEINT** .</span><span class="sxs-lookup"><span data-stu-id="0e8c3-120">Pointer to the **LARGEINT** data.</span></span>

</dd> <dt>

<span data-ttu-id="0e8c3-121">**SysTime**</span><span class="sxs-lookup"><span data-stu-id="0e8c3-121">**SysTime**</span></span>
</dt> <dd>

<span data-ttu-id="0e8c3-122">Ponteiro para os dados de **SYSTEMTIME** .</span><span class="sxs-lookup"><span data-stu-id="0e8c3-122">Pointer to the **SYSTEMTIME** data.</span></span>

</dd> <dt>

<span data-ttu-id="0e8c3-123">**Tipo de**</span><span class="sxs-lookup"><span data-stu-id="0e8c3-123">**TypedString**</span></span>
</dt> <dd>

<span data-ttu-id="0e8c3-124">Uma cadeia de caracteres tipada que pode ter dados estendidos.</span><span class="sxs-lookup"><span data-stu-id="0e8c3-124">A typed string that may have extended data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0e8c3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e8c3-125">Requirements</span></span>



| <span data-ttu-id="0e8c3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e8c3-126">Requirement</span></span> | <span data-ttu-id="0e8c3-127">Valor</span><span class="sxs-lookup"><span data-stu-id="0e8c3-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0e8c3-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e8c3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0e8c3-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0e8c3-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0e8c3-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e8c3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0e8c3-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0e8c3-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0e8c3-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0e8c3-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e8c3-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e8c3-133"><dt>Netmon.h</dt></span></span> </dl> |



 

 




