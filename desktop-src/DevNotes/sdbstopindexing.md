---
description: Desabilita a criação e modificação de índice para o banco de dados especificado.
ms.assetid: d079eae2-574e-4ac1-a0f9-11796e56a790
title: Função SdbStopIndexing
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbStopIndexing
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 3c9c6b34c265d611b57a3e73bb0c8fb1822fe752
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500869"
---
# <a name="sdbstopindexing-function"></a><span data-ttu-id="97cae-103">Função SdbStopIndexing</span><span class="sxs-lookup"><span data-stu-id="97cae-103">SdbStopIndexing function</span></span>

<span data-ttu-id="97cae-104">Desabilita a criação e modificação de índice para o banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="97cae-104">Disables index creation and modification for the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="97cae-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="97cae-105">Syntax</span></span>


```C++
BOOL WINAPI SdbStopIndexing(
  _In_ PDB     pdb,
  _In_ INDEXID iiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="97cae-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97cae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97cae-107">*PDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="97cae-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97cae-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="97cae-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="97cae-109">*iiWhich* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="97cae-109">*iiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97cae-110">O identificador do índice.</span><span class="sxs-lookup"><span data-stu-id="97cae-110">The index identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97cae-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="97cae-111">Return value</span></span>

<span data-ttu-id="97cae-112">A função retorna **true** em caso de êxito ou **false** em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="97cae-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="97cae-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97cae-113">Requirements</span></span>



| <span data-ttu-id="97cae-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="97cae-114">Requirement</span></span> | <span data-ttu-id="97cae-115">Valor</span><span class="sxs-lookup"><span data-stu-id="97cae-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97cae-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97cae-116">Minimum supported client</span></span><br/> | <span data-ttu-id="97cae-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="97cae-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="97cae-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97cae-118">Minimum supported server</span></span><br/> | <span data-ttu-id="97cae-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="97cae-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="97cae-120">DLL</span><span class="sxs-lookup"><span data-stu-id="97cae-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97cae-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97cae-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97cae-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="97cae-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97cae-123">**SdbCommitIndexes**</span><span class="sxs-lookup"><span data-stu-id="97cae-123">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
</dt> <dt>

[<span data-ttu-id="97cae-124">**SdbDeclareIndex**</span><span class="sxs-lookup"><span data-stu-id="97cae-124">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="97cae-125">**SdbStartIndexing**</span><span class="sxs-lookup"><span data-stu-id="97cae-125">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> </dl>

 

 




