---
title: Propriedade ITsSbTarget TargetLoad
description: Recupera a carga relativa em um destino.
ms.assetid: 56618dcf-1319-4310-80ba-7ed71b8b02e8
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade TargetLoad
- Propriedade TargetLoad Serviços de Área de Trabalho Remota, interface ITsSbTarget
- Serviços de Área de Trabalho Remota de interface ITsSbTarget, Propriedade TargetLoad
- Propriedade TargetLoad Serviços de Área de Trabalho Remota, interface ITsSbTargetEx
- Serviços de Área de Trabalho Remota de interface ITsSbTargetEx, Propriedade TargetLoad
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetLoad
- ITsSbTarget.get_TargetLoad
- ITsSbTargetEx.TargetLoad
- ITsSbTargetEx.get_TargetLoad
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddfc9be9805406ab76b166e2a34bc47a7f5e9ab5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638596"
---
# <a name="itssbtargettargetload-property"></a><span data-ttu-id="07a02-108">Propriedade ITsSbTarget:: TargetLoad</span><span class="sxs-lookup"><span data-stu-id="07a02-108">ITsSbTarget::TargetLoad property</span></span>

<span data-ttu-id="07a02-109">Recupera a carga relativa em um destino.</span><span class="sxs-lookup"><span data-stu-id="07a02-109">Retrieves the relative load on a target.</span></span> <span data-ttu-id="07a02-110">Esse valor é baseado no número de sessões existentes e pendentes.</span><span class="sxs-lookup"><span data-stu-id="07a02-110">This value is based on the number of existing and pending sessions.</span></span> <span data-ttu-id="07a02-111">Por padrão, uma sessão pendente tem o mesmo valor de uma sessão existente.</span><span class="sxs-lookup"><span data-stu-id="07a02-111">By default a pending session has the same value as an existing session.</span></span>

<span data-ttu-id="07a02-112">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="07a02-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="07a02-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07a02-113">Syntax</span></span>


```C++
HRESULT get_TargetLoad(
  [out, retval] DWORD *pTargetLoad
);
```



## <a name="property-value"></a><span data-ttu-id="07a02-114">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="07a02-114">Property value</span></span>

<span data-ttu-id="07a02-115">Um número que representa a carga relativa em um destino.</span><span class="sxs-lookup"><span data-stu-id="07a02-115">A number representing the relative load on a target.</span></span>

## <a name="remarks"></a><span data-ttu-id="07a02-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="07a02-116">Remarks</span></span>

<span data-ttu-id="07a02-117">O peso de uma sessão pendente em relação a uma sessão ativa pode ser alterado definindo o valor do parâmetro *\_ ConnectionEstablishmentPenalty de lb* para o agente de conexão.</span><span class="sxs-lookup"><span data-stu-id="07a02-117">The weight of a pending session relative to an active session can be changed by setting the value of the *LB\_ConnectionEstablishmentPenalty* parameter for the Connection Broker.</span></span> <span data-ttu-id="07a02-118">Esse parâmetro está localizado na chave do registro **HKLM \\ System \\ CurrentControlSet \\ Services \\ Tssdis \\ Parameters** .</span><span class="sxs-lookup"><span data-stu-id="07a02-118">This parameter is located under the **HKLM\\System\\CurrentControlSet\\Services\\Tssdis\\Parameters** registry key.</span></span> <span data-ttu-id="07a02-119">O valor padrão de 1 especifica que as sessões pendentes têm o mesmo peso que as sessões ativas.</span><span class="sxs-lookup"><span data-stu-id="07a02-119">The default value of 1 specifies that pending sessions have the same weight as active sessions.</span></span>

<span data-ttu-id="07a02-120">Essa propriedade está disponível no Windows Server 2012 R2 com [KB3091411](https://support.microsoft.com/kb/3091411) instalado na interface [**ITsSbTargetEx**](itssbtargetex.md) .</span><span class="sxs-lookup"><span data-stu-id="07a02-120">This property is available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed in the [**ITsSbTargetEx**](itssbtargetex.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="07a02-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07a02-121">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="07a02-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07a02-122">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="07a02-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="07a02-123">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07a02-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07a02-124">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="07a02-125">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="07a02-125">Windows Server 2016</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07a02-126">INSERI</span><span class="sxs-lookup"><span data-stu-id="07a02-126">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="07a02-127"><dt>Sbtsv. idl</dt> </span><span class="sxs-lookup"><span data-stu-id="07a02-127"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07a02-128">IID</span><span class="sxs-lookup"><span data-stu-id="07a02-128">IID</span></span><br/></td>
<td><span data-ttu-id="07a02-129">IID_ITsSbTarget é definido como:</span><span class="sxs-lookup"><span data-stu-id="07a02-129">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="07a02-130">16616ECC-272D-411D-B324-126893033856</span><span class="sxs-lookup"><span data-stu-id="07a02-130">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="07a02-131">e85e10ea-db0b-4752-b456-5fd5840901c0 no Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="07a02-131">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="07a02-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="07a02-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07a02-133">**ITsSbTargetEx**</span><span class="sxs-lookup"><span data-stu-id="07a02-133">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="07a02-134">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="07a02-134">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





