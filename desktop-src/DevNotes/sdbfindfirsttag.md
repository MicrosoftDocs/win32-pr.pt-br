---
description: Procura uma correspondência de marca dentro do pai especificado e retorna o TAGID da primeira correspondência.
ms.assetid: ecbe216c-1e46-4472-b1d1-e2ac7ace82ab
title: Função SdbFindFirstTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: dc8b752d536be83d90ded55474166d14521f0f7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920102"
---
# <a name="sdbfindfirsttag-function"></a><span data-ttu-id="493db-103">Função SdbFindFirstTag</span><span class="sxs-lookup"><span data-stu-id="493db-103">SdbFindFirstTag function</span></span>

<span data-ttu-id="493db-104">Procura uma correspondência de marca dentro do pai especificado e retorna o **TagId** da primeira correspondência.</span><span class="sxs-lookup"><span data-stu-id="493db-104">Searches for a TAG match within the specified parent and returns the **TAGID** of the first match.</span></span>

## <a name="syntax"></a><span data-ttu-id="493db-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="493db-105">Syntax</span></span>


```C++
TAGID WINAPI SdbFindFirstTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAG   tTag
);
```



## <a name="parameters"></a><span data-ttu-id="493db-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="493db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="493db-107">*PDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="493db-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="493db-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="493db-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="493db-109">*tiParent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="493db-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="493db-110">O **TagId** do início da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="493db-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="493db-111">Esse parâmetro pode ser **TagId \_ raiz** ou **\_ \_ lista de tipos de marca**.</span><span class="sxs-lookup"><span data-stu-id="493db-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="493db-112">*tTag* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="493db-112">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="493db-113">A marca a ser correspondida.</span><span class="sxs-lookup"><span data-stu-id="493db-113">The TAG to be matched.</span></span> <span data-ttu-id="493db-114">Consulte a [marca](tag.md) para obter uma lista de valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="493db-114">See [TAG](tag.md) for a list of possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="493db-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="493db-115">Return value</span></span>

<span data-ttu-id="493db-116">O **TagId** da primeira correspondência.</span><span class="sxs-lookup"><span data-stu-id="493db-116">The **TAGID** of the first match.</span></span>

## <a name="requirements"></a><span data-ttu-id="493db-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="493db-117">Requirements</span></span>



| <span data-ttu-id="493db-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="493db-118">Requirement</span></span> | <span data-ttu-id="493db-119">Valor</span><span class="sxs-lookup"><span data-stu-id="493db-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="493db-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="493db-120">Minimum supported client</span></span><br/> | <span data-ttu-id="493db-121">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="493db-121">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="493db-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="493db-122">Minimum supported server</span></span><br/> | <span data-ttu-id="493db-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="493db-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="493db-124">DLL</span><span class="sxs-lookup"><span data-stu-id="493db-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="493db-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="493db-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="493db-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="493db-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="493db-127">**SdbFindNextTag**</span><span class="sxs-lookup"><span data-stu-id="493db-127">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
</dt> <dt>

[<span data-ttu-id="493db-128">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="493db-128">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> </dl>

 

 




