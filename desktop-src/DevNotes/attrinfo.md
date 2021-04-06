---
description: Contém os dados de atributo de um arquivo.
ms.assetid: f23f801c-826c-4269-bf96-0e01430484f4
title: Estrutura ATTRINFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 01c061330db3e97989e0700452fd4a205488a9fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826128"
---
# <a name="attrinfo-structure"></a><span data-ttu-id="65a67-103">Estrutura ATTRINFO</span><span class="sxs-lookup"><span data-stu-id="65a67-103">ATTRINFO structure</span></span>

<span data-ttu-id="65a67-104">Contém os dados de atributo de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="65a67-104">Contains the attribute data for a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="65a67-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65a67-105">Syntax</span></span>


```C++
typedef struct tagATTRINFO {
  TAG   tAttrID;
  DWORD dwFlags;
  union {
    ULONGLONG ullAttr;
    DWORD     dwAttr;
    TCHAR     *lpAttr;
  };
} ATTRINFO, *PATTRINFO;
```



## <a name="members"></a><span data-ttu-id="65a67-106">Membros</span><span class="sxs-lookup"><span data-stu-id="65a67-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="65a67-107">**tAttrID**</span><span class="sxs-lookup"><span data-stu-id="65a67-107">**tAttrID**</span></span>
</dt> <dd>

<span data-ttu-id="65a67-108">O tipo de atributo.</span><span class="sxs-lookup"><span data-stu-id="65a67-108">The attribute type.</span></span> <span data-ttu-id="65a67-109">Consulte [tipos de marca](tag-types.md).</span><span class="sxs-lookup"><span data-stu-id="65a67-109">See [TAG Types](tag-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="65a67-110">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="65a67-110">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="65a67-111">Os sinalizadores para este atributo.</span><span class="sxs-lookup"><span data-stu-id="65a67-111">The flags for this attribute.</span></span>



| <span data-ttu-id="65a67-112">Valor</span><span class="sxs-lookup"><span data-stu-id="65a67-112">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="65a67-113">Significado</span><span class="sxs-lookup"><span data-stu-id="65a67-113">Meaning</span></span>                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="ATTRIBUTE_AVAILABLE"></span><span id="attribute_available"></span><dl> <span data-ttu-id="65a67-114"><dt>**Atributo \_ DISPONÍVEL**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="65a67-114"><dt>**ATTRIBUTE\_AVAILABLE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="65a67-115">O atributo está disponível.</span><span class="sxs-lookup"><span data-stu-id="65a67-115">The attribute is available.</span></span><br/>                             |
| <span id="ATTRIBUTE_FAILED"></span><span id="attribute_failed"></span><dl> <span data-ttu-id="65a67-116"><dt>**Atributo \_ FALHA**</dt> de <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="65a67-116"><dt>**ATTRIBUTE\_FAILED**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="65a67-117">A chamada falhou porque o atributo não está disponível.</span><span class="sxs-lookup"><span data-stu-id="65a67-117">The call failed because the attribute is not available.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="65a67-118">**ullAttr**</span><span class="sxs-lookup"><span data-stu-id="65a67-118">**ullAttr**</span></span>
</dt> <dd>

<span data-ttu-id="65a67-119">Um valor **QWORD** (se o tipo de marca for **marca \_ tipo \_ QWORD**).</span><span class="sxs-lookup"><span data-stu-id="65a67-119">A **QWORD** value (if the tag type is **TAG\_TYPE\_QWORD**).</span></span>

</dd> <dt>

<span data-ttu-id="65a67-120">**dwAttr**</span><span class="sxs-lookup"><span data-stu-id="65a67-120">**dwAttr**</span></span>
</dt> <dd>

<span data-ttu-id="65a67-121">Um valor **DWORD** (se o tipo de marca for **marca \_ tipo \_ DWORD**).</span><span class="sxs-lookup"><span data-stu-id="65a67-121">A **DWORD** value (if the tag type is **TAG\_TYPE\_DWORD**).</span></span>

</dd> <dt>

<span data-ttu-id="65a67-122">**lpAttr**</span><span class="sxs-lookup"><span data-stu-id="65a67-122">**lpAttr**</span></span>
</dt> <dd>

<span data-ttu-id="65a67-123">Um ponteiro para uma cadeia de caracteres (se o tipo de marca for **tipo de marca \_ \_ STRINGREF**).</span><span class="sxs-lookup"><span data-stu-id="65a67-123">A pointer to a string (if the tag type is **TAG\_TYPE\_STRINGREF**).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="65a67-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65a67-124">Requirements</span></span>



| <span data-ttu-id="65a67-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="65a67-125">Requirement</span></span> | <span data-ttu-id="65a67-126">Valor</span><span class="sxs-lookup"><span data-stu-id="65a67-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="65a67-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65a67-127">Minimum supported client</span></span><br/> | <span data-ttu-id="65a67-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="65a67-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="65a67-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65a67-129">Minimum supported server</span></span><br/> | <span data-ttu-id="65a67-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="65a67-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="65a67-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="65a67-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65a67-132">**SdbFormatAttribute**</span><span class="sxs-lookup"><span data-stu-id="65a67-132">**SdbFormatAttribute**</span></span>](sdbformatattribute.md)
</dt> <dt>

[<span data-ttu-id="65a67-133">**SdbFreeFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="65a67-133">**SdbFreeFileAttributes**</span></span>](sdbfreefileattributes.md)
</dt> <dt>

[<span data-ttu-id="65a67-134">**SdbGetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="65a67-134">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
</dt> </dl>

 

 




