---
description: O identificador do índice a ser acessado em um banco de dados.
ms.assetid: 559e73bf-91c2-4dbf-a667-e5c0431aaffa
title: INDEXid
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b6ef6b79dd19183f575930e9793a6ab2f1f5cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089423"
---
# <a name="indexid"></a><span data-ttu-id="3492e-103">INDEXid</span><span class="sxs-lookup"><span data-stu-id="3492e-103">INDEXID</span></span>

<span data-ttu-id="3492e-104">O identificador do índice a ser acessado em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3492e-104">The identifier of the index to be accessed in a database.</span></span>


```C++
typedef DWORD INDEXID;
```



## <a name="remarks"></a><span data-ttu-id="3492e-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="3492e-105">Remarks</span></span>

<span data-ttu-id="3492e-106">Um **IndexID** pode ser um valor inteiro que representa o índice ou o seguinte valor:</span><span class="sxs-lookup"><span data-stu-id="3492e-106">An **INDEXID** can be an integer value that represents the index, or the following value:</span></span>

<dl> <dt>

<span data-ttu-id="3492e-107"><span id="INDEXID_NULL___INDEXID_-1_"></span><span id="indexid_null___indexid_-1_"></span>INDEXid \_ nulo ((IndexID)-1)</span><span class="sxs-lookup"><span data-stu-id="3492e-107"><span id="INDEXID_NULL___INDEXID_-1_"></span><span id="indexid_null___indexid_-1_"></span>INDEXID\_NULL ((INDEXID)-1)</span></span>
</dt> <dd>

<span data-ttu-id="3492e-108">Um **IndexID** inválido.</span><span class="sxs-lookup"><span data-stu-id="3492e-108">An invalid **INDEXID**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3492e-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3492e-109">Requirements</span></span>



| <span data-ttu-id="3492e-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="3492e-110">Requirement</span></span> | <span data-ttu-id="3492e-111">Valor</span><span class="sxs-lookup"><span data-stu-id="3492e-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3492e-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3492e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="3492e-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3492e-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3492e-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3492e-114">Minimum supported server</span></span><br/> | <span data-ttu-id="3492e-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3492e-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3492e-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="3492e-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3492e-117">**SdbDeclareIndex**</span><span class="sxs-lookup"><span data-stu-id="3492e-117">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="3492e-118">**SdbStartIndexing**</span><span class="sxs-lookup"><span data-stu-id="3492e-118">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> <dt>

[<span data-ttu-id="3492e-119">**SdbStopIndexing**</span><span class="sxs-lookup"><span data-stu-id="3492e-119">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




