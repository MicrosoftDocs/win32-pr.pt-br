---
description: Procura uma marca filho dentro do pai especificado e retorna o TAGID do primeiro filho.
ms.assetid: 67538c7e-6360-40fa-b50f-dcbc7a6a147d
title: Função SdbGetFirstChild
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFirstChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: abc06ae0e4b5d842a968d0f3fbeb7a15702660b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500738"
---
# <a name="sdbgetfirstchild-function"></a><span data-ttu-id="35f76-103">Função SdbGetFirstChild</span><span class="sxs-lookup"><span data-stu-id="35f76-103">SdbGetFirstChild function</span></span>

<span data-ttu-id="35f76-104">Procura uma marca filho dentro do pai especificado e retorna o **TagId** do primeiro filho.</span><span class="sxs-lookup"><span data-stu-id="35f76-104">Searches for a child TAG within the specified parent and returns the **TAGID** of the first child.</span></span>

## <a name="syntax"></a><span data-ttu-id="35f76-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35f76-105">Syntax</span></span>


```C++
TAGID WINAPI SdbGetFirstChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent
);
```



## <a name="parameters"></a><span data-ttu-id="35f76-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35f76-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35f76-107">*PDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="35f76-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35f76-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="35f76-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="35f76-109">*tiParent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="35f76-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35f76-110">O **TagId** do início da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="35f76-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="35f76-111">Esse parâmetro pode ser **TagId \_ raiz** ou **\_ \_ lista de tipos de marca**.</span><span class="sxs-lookup"><span data-stu-id="35f76-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35f76-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="35f76-112">Return value</span></span>

<span data-ttu-id="35f76-113">O **TagId** do primeiro filho ou **TagId \_ nulo** não é um filho encontrado.</span><span class="sxs-lookup"><span data-stu-id="35f76-113">The **TAGID** of the first child or **TAGID\_NULL** is no child is found.</span></span>

## <a name="requirements"></a><span data-ttu-id="35f76-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35f76-114">Requirements</span></span>



| <span data-ttu-id="35f76-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="35f76-115">Requirement</span></span> | <span data-ttu-id="35f76-116">Valor</span><span class="sxs-lookup"><span data-stu-id="35f76-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35f76-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35f76-117">Minimum supported client</span></span><br/> | <span data-ttu-id="35f76-118">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="35f76-118">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="35f76-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35f76-119">Minimum supported server</span></span><br/> | <span data-ttu-id="35f76-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="35f76-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="35f76-121">DLL</span><span class="sxs-lookup"><span data-stu-id="35f76-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35f76-122"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35f76-122"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35f76-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="35f76-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35f76-124">**SdbFindFirstTag**</span><span class="sxs-lookup"><span data-stu-id="35f76-124">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> <dt>

[<span data-ttu-id="35f76-125">**SdbFindNextTag**</span><span class="sxs-lookup"><span data-stu-id="35f76-125">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
</dt> <dt>

[<span data-ttu-id="35f76-126">**SdbGetNextChild**</span><span class="sxs-lookup"><span data-stu-id="35f76-126">**SdbGetNextChild**</span></span>](sdbgetnextchild.md)
</dt> </dl>

 

 




