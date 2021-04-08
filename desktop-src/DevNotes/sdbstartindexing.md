---
description: Habilita a criação e modificação de índice para o banco de dados especificado.
ms.assetid: f780034e-6963-423c-8ffa-9fbe98dca7e1
title: Função SdbStartIndexing
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbStartIndexing
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e3324b4cb0d42ca33ee7c3234a1acc099adcb743
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089068"
---
# <a name="sdbstartindexing-function"></a><span data-ttu-id="ccd24-103">Função SdbStartIndexing</span><span class="sxs-lookup"><span data-stu-id="ccd24-103">SdbStartIndexing function</span></span>

<span data-ttu-id="ccd24-104">Habilita a criação e modificação de índice para o banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="ccd24-104">Enables index creation and modification for the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccd24-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ccd24-105">Syntax</span></span>


```C++
BOOL WINAPI SdbStartIndexing(
  _In_ PDB     pdb,
  _In_ INDEXID iiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="ccd24-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ccd24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccd24-107">*PDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccd24-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd24-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="ccd24-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="ccd24-109">*iiWhich* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccd24-109">*iiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd24-110">O identificador do índice.</span><span class="sxs-lookup"><span data-stu-id="ccd24-110">The index identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccd24-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ccd24-111">Return value</span></span>

<span data-ttu-id="ccd24-112">A função retorna **true** em caso de êxito ou **false** em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="ccd24-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccd24-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccd24-113">Requirements</span></span>



| <span data-ttu-id="ccd24-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccd24-114">Requirement</span></span> | <span data-ttu-id="ccd24-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ccd24-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccd24-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccd24-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ccd24-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ccd24-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ccd24-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccd24-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ccd24-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ccd24-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ccd24-120">DLL</span><span class="sxs-lookup"><span data-stu-id="ccd24-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccd24-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccd24-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccd24-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccd24-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccd24-123">**SdbCommitIndexes**</span><span class="sxs-lookup"><span data-stu-id="ccd24-123">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
</dt> <dt>

[<span data-ttu-id="ccd24-124">**SdbDeclareIndex**</span><span class="sxs-lookup"><span data-stu-id="ccd24-124">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="ccd24-125">**SdbStopIndexing**</span><span class="sxs-lookup"><span data-stu-id="ccd24-125">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




