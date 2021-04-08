---
description: Confirma índices recém-criados para o banco de dados especificado.
ms.assetid: 92f05e5f-599a-4870-8175-61b83c943514
title: Função SdbCommitIndexes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCommitIndexes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0709a913dc78cefdf405a0a3bd29030801941c37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088995"
---
# <a name="sdbcommitindexes-function"></a><span data-ttu-id="8b2a2-103">Função SdbCommitIndexes</span><span class="sxs-lookup"><span data-stu-id="8b2a2-103">SdbCommitIndexes function</span></span>

<span data-ttu-id="8b2a2-104">Confirma índices recém-criados para o banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="8b2a2-104">Commits newly created indexes to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b2a2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b2a2-105">Syntax</span></span>


```C++
BOOL WINAPI SdbCommitIndexes(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a><span data-ttu-id="8b2a2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b2a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b2a2-107">*PDB* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="8b2a2-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b2a2-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="8b2a2-108">A handle to the shim database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b2a2-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8b2a2-109">Return value</span></span>

<span data-ttu-id="8b2a2-110">A função retorna **true** em caso de êxito ou **false** em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="8b2a2-110">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b2a2-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b2a2-111">Requirements</span></span>



| <span data-ttu-id="8b2a2-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b2a2-112">Requirement</span></span> | <span data-ttu-id="8b2a2-113">Valor</span><span class="sxs-lookup"><span data-stu-id="8b2a2-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b2a2-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b2a2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="8b2a2-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8b2a2-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8b2a2-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b2a2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="8b2a2-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8b2a2-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8b2a2-118">DLL</span><span class="sxs-lookup"><span data-stu-id="8b2a2-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b2a2-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b2a2-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b2a2-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b2a2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b2a2-121">**SdbDeclareIndex**</span><span class="sxs-lookup"><span data-stu-id="8b2a2-121">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="8b2a2-122">**SdbStartIndexing**</span><span class="sxs-lookup"><span data-stu-id="8b2a2-122">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> <dt>

[<span data-ttu-id="8b2a2-123">**SdbStopIndexing**</span><span class="sxs-lookup"><span data-stu-id="8b2a2-123">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




