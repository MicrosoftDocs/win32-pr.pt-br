---
description: Contém informações de contexto de pesquisa.
ms.assetid: 4b865563-98c2-459b-bb2b-75420d51d6a7
title: Estrutura de FIND_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIND_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7d6b6dea42c008178c22f6e342a64b2f8d193ec5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752926"
---
# <a name="find_info-structure"></a><span data-ttu-id="ea30b-103">LOCALIZAR \_ estrutura de informações</span><span class="sxs-lookup"><span data-stu-id="ea30b-103">FIND\_INFO structure</span></span>

<span data-ttu-id="ea30b-104">Contém informações de contexto de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ea30b-104">Contains search context information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea30b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea30b-105">Syntax</span></span>


```C++
typedef struct _FIND_INFO {
  TAGID     tiIndex;
  TAGID     tiCurrent;
  TAGID     tiEndIndex;
  TAG       tName;
  DWORD     dwIndexRec;
  DWORD     dwFlags;
  ULONGLONG ullKey;
  union {
    LPCTSTR szName;
    DWORD   dwName;
    GUID    *pguidName;
  };
} FIND_INFO, *PFIND_INFO;
```



## <a name="members"></a><span data-ttu-id="ea30b-106">Membros</span><span class="sxs-lookup"><span data-stu-id="ea30b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ea30b-107">**tiIndex**</span><span class="sxs-lookup"><span data-stu-id="ea30b-107">**tiIndex**</span></span>
</dt> <dd>

<span data-ttu-id="ea30b-108">O **TagId** para o índice a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="ea30b-108">The **TAGID** for the index to be searched.</span></span>

</dd> <dt>

<span data-ttu-id="ea30b-109">**tiCurrent**</span><span class="sxs-lookup"><span data-stu-id="ea30b-109">**tiCurrent**</span></span>
</dt> <dd>

<span data-ttu-id="ea30b-110">O **TagId** para o item atual que estava localizado.</span><span class="sxs-lookup"><span data-stu-id="ea30b-110">The **TAGID** for the current item that was located.</span></span>

</dd> <dt>

<span data-ttu-id="ea30b-111">**tiEndIndex**</span><span class="sxs-lookup"><span data-stu-id="ea30b-111">**tiEndIndex**</span></span>
</dt> <dd>

<span data-ttu-id="ea30b-112">O **TagId** para o último registro após FindFirst se o índice for exclusivo.</span><span class="sxs-lookup"><span data-stu-id="ea30b-112">The **TAGID** for the last record after FindFirst if the index is UNIQUE.</span></span>

</dd> <dt>

<span data-ttu-id="ea30b-113">**tName**</span><span class="sxs-lookup"><span data-stu-id="ea30b-113">**tName**</span></span>
</dt> <dd>

<span data-ttu-id="ea30b-114">O tipo do item a ser localizado.</span><span class="sxs-lookup"><span data-stu-id="ea30b-114">The type of the item to be located.</span></span> <span data-ttu-id="ea30b-115">Consulte [tipos de marca](tag-types.md).</span><span class="sxs-lookup"><span data-stu-id="ea30b-115">See [TAG Types](tag-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea30b-116">**dwIndexRec**</span><span class="sxs-lookup"><span data-stu-id="ea30b-116">**dwIndexRec**</span></span>
</dt> <dd>

<span data-ttu-id="ea30b-117">Um contador interno usado para controlar onde deve iniciar a próxima operação Localizar.</span><span class="sxs-lookup"><span data-stu-id="ea30b-117">An internal counter used to track where in the index the next find operation should start.</span></span>

</dd> <dt>

<span data-ttu-id="ea30b-118">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="ea30b-118">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="ea30b-119">Esse membro pode ser 0 ou **SHIMDB \_ \_ \_ chave exclusiva de índice** (0x00000001), que indica que se trata de um índice de chave exclusiva.</span><span class="sxs-lookup"><span data-stu-id="ea30b-119">This member can be 0 or **SHIMDB\_INDEX\_UNIQUE\_KEY** (0x00000001), which indicates that this is a unique-key index.</span></span>

</dd> <dt>

<span data-ttu-id="ea30b-120">**ullKey**</span><span class="sxs-lookup"><span data-stu-id="ea30b-120">**ullKey**</span></span>
</dt> <dd>

<span data-ttu-id="ea30b-121">A chave para a entrada atual.</span><span class="sxs-lookup"><span data-stu-id="ea30b-121">The key for the current entry.</span></span>

</dd> <dt>

<span data-ttu-id="ea30b-122">**szName**</span><span class="sxs-lookup"><span data-stu-id="ea30b-122">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="ea30b-123">A cadeia de caracteres atual (se o tipo de marca for **tipo de marca \_ \_ STRINGREF**).</span><span class="sxs-lookup"><span data-stu-id="ea30b-123">The current string (if the tag type is **TAG\_TYPE\_STRINGREF**).</span></span>

</dd> <dt>

<span data-ttu-id="ea30b-124">**dwName**</span><span class="sxs-lookup"><span data-stu-id="ea30b-124">**dwName**</span></span>
</dt> <dd>

<span data-ttu-id="ea30b-125">O valor **DWORD** atual (se o tipo de marca for **marca \_ tipo \_ DWORD**).</span><span class="sxs-lookup"><span data-stu-id="ea30b-125">The current **DWORD** value (if the tag type is **TAG\_TYPE\_DWORD**).</span></span>

</dd> <dt>

<span data-ttu-id="ea30b-126">**pguidName**</span><span class="sxs-lookup"><span data-stu-id="ea30b-126">**pguidName**</span></span>
</dt> <dd>

<span data-ttu-id="ea30b-127">O valor de GUID atual (se o tipo de marca for **marca \_ tipo \_ binário** e a marca for **\_ \_ ID do banco de dados de marca**).</span><span class="sxs-lookup"><span data-stu-id="ea30b-127">The current GUID value (if the tag type is **TAG\_TYPE\_BINARY** and the TAG is **TAG\_DATABASE\_ID**).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea30b-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea30b-128">Requirements</span></span>



| <span data-ttu-id="ea30b-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea30b-129">Requirement</span></span> | <span data-ttu-id="ea30b-130">Valor</span><span class="sxs-lookup"><span data-stu-id="ea30b-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ea30b-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea30b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ea30b-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea30b-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ea30b-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea30b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ea30b-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ea30b-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ea30b-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea30b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea30b-136">**SdbFindFirstDWORDIndexedTag**</span><span class="sxs-lookup"><span data-stu-id="ea30b-136">**SdbFindFirstDWORDIndexedTag**</span></span>](sdbfindfirstdwordindexedtag.md)
</dt> </dl>

 

 




