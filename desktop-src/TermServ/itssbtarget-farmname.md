---
title: Propriedade Farmname de ITsSbTarget
description: Recupera ou especifica o nome do farm ao qual esse destino está associado.
ms.assetid: 83e168ae-f985-40f9-912b-496c0695f82a
ms.tgt_platform: multiple
keywords:
- Propriedade farmname Serviços de Área de Trabalho Remota
- Propriedade farmname Serviços de Área de Trabalho Remota, interface ITsSbTarget
- Serviços de Área de Trabalho Remota de interface ITsSbTarget, Propriedade Farmname
- Propriedade farmname Serviços de Área de Trabalho Remota, interface ITsSbTargetEx
- Serviços de Área de Trabalho Remota de interface ITsSbTargetEx, Propriedade Farmname
topic_type:
- apiref
api_name:
- ITsSbTarget.FarmName
- ITsSbTarget.get_FarmName
- ITsSbTarget.put_FarmName
- ITsSbTargetEx.FarmName
- ITsSbTargetEx.get_FarmName
- ITsSbTargetEx.put_FarmName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94f86b2cf0ec257be9fe9b801e6fceae364a46e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638508"
---
# <a name="itssbtargetfarmname-property"></a><span data-ttu-id="5636d-108">Propriedade ITsSbTarget:: Farmname</span><span class="sxs-lookup"><span data-stu-id="5636d-108">ITsSbTarget::FarmName property</span></span>

<span data-ttu-id="5636d-109">Recupera ou especifica o nome do farm ao qual esse destino está associado.</span><span class="sxs-lookup"><span data-stu-id="5636d-109">Retrieves or specifies the name of the farm to which this target is joined.</span></span>

<span data-ttu-id="5636d-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5636d-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5636d-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5636d-111">Syntax</span></span>


```C++
HRESULT put_FarmName(
  [in]          BSTR Val
);

HRESULT get_FarmName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="5636d-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5636d-112">Property value</span></span>

<span data-ttu-id="5636d-113">Uma variável **BSTR** que contém o nome do farm.</span><span class="sxs-lookup"><span data-stu-id="5636d-113">A **BSTR** variable that contains the farm name.</span></span>

## <a name="requirements"></a><span data-ttu-id="5636d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5636d-114">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5636d-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5636d-115">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="5636d-116">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5636d-116">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5636d-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5636d-117">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="5636d-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5636d-118">Windows Server 2012</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5636d-119">INSERI</span><span class="sxs-lookup"><span data-stu-id="5636d-119">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="5636d-120"><dt>Sbtsv. idl</dt> </span><span class="sxs-lookup"><span data-stu-id="5636d-120"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5636d-121">IID</span><span class="sxs-lookup"><span data-stu-id="5636d-121">IID</span></span><br/></td>
<td><span data-ttu-id="5636d-122">IID_ITsSbTarget é definido como:</span><span class="sxs-lookup"><span data-stu-id="5636d-122">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="5636d-123">16616ECC-272D-411D-B324-126893033856</span><span class="sxs-lookup"><span data-stu-id="5636d-123">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="5636d-124">e85e10ea-db0b-4752-b456-5fd5840901c0 no Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5636d-124">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="5636d-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5636d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5636d-126">**ITsSbTargetEx**</span><span class="sxs-lookup"><span data-stu-id="5636d-126">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="5636d-127">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="5636d-127">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





