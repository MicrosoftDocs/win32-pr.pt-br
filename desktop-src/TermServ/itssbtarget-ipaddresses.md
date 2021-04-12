---
title: Propriedade IpAddresses de ITsSbTarget
description: Recupera ou especifica os endereços IP externos do destino.
ms.assetid: 938a753c-d541-4772-b41b-817324488685
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade TargetExternalIpAddresses
- Propriedade TargetExternalIpAddresses Serviços de Área de Trabalho Remota, interface ITsSbTarget
- Propriedade TargetExternalIpAddresses Serviços de Área de Trabalho Remota, interface ITsSbTarget
- Propriedade IpAddresses Serviços de Área de Trabalho Remota
- Propriedade IpAddresses Serviços de Área de Trabalho Remota, interface ITsSbTarget
- Serviços de Área de Trabalho Remota de interface ITsSbTarget, Propriedade IpAddresss
- Propriedade IpAddresses Serviços de Área de Trabalho Remota, interface ITsSbTargetEx
- Serviços de Área de Trabalho Remota de interface ITsSbTargetEx, Propriedade IpAddresss
topic_type:
- apiref
api_name:
- ITsSbTarget.IpAddresses
- ITsSbTarget.get_IpAddresses
- ITsSbTarget.put_IpAddresses
- ITsSbTargetEx.IpAddresses
- ITsSbTargetEx.get_IpAddresses
- ITsSbTargetEx.put_IpAddresses
- TargetExternalIpAddresses
- ITsSbTarget.TargetExternalIpAddresses
- ITsSbTarget get_TargetExternalIpAddresses
- ITsSbTarget put_TargetExternalIpAddresses
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8b3902840b24bc49ae3bda0510c8355afb67810
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364816"
---
# <a name="itssbtargetipaddresses-property"></a><span data-ttu-id="13bfb-111">Propriedade ITsSbTarget:: IpAddresss</span><span class="sxs-lookup"><span data-stu-id="13bfb-111">ITsSbTarget::IpAddresses property</span></span>

<span data-ttu-id="13bfb-112">Recupera ou especifica os endereços IP externos do destino.</span><span class="sxs-lookup"><span data-stu-id="13bfb-112">Retrieves or specifies the external IP addresses of the target.</span></span>

<span data-ttu-id="13bfb-113">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="13bfb-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="13bfb-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="13bfb-114">Syntax</span></span>


```C++
HRESULT put_IpAddresses(
  [in, size_is(numAddresses)]   TSSD_ConnectionPoint *sockaddr,
  [in]                          DWORD                numAddresses
);

HRESULT get_IpAddresses(
  [out, size_is(*numAddresses)] TSSD_ConnectionPoint *sockaddr,
  [in, out]                     DWORD                *numAddresses
);
```



## <a name="property-value"></a><span data-ttu-id="13bfb-115">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="13bfb-115">Property value</span></span>

<span data-ttu-id="13bfb-116">Um ponteiro para uma matriz de estruturas [**tssd \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) que recebem os endereços IP externos do destino.</span><span class="sxs-lookup"><span data-stu-id="13bfb-116">A pointer to an array of [**TSSD\_ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) structures that receive the external IP addresses of the target.</span></span>

<span data-ttu-id="13bfb-117">Um ponteiro para uma variável **DWORD** que contém o número de endereços IP externos no parâmetro *SOCKADDR* .</span><span class="sxs-lookup"><span data-stu-id="13bfb-117">A pointer to a **DWORD** variable that contains the number of external IP addresses in the *sockaddr* parameter.</span></span> <span data-ttu-id="13bfb-118">Se o número de endereços for desconhecido, passe *SOCKADDR* como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="13bfb-118">If the number of addresses is unknown, pass *sockaddr* as **NULL**.</span></span> <span data-ttu-id="13bfb-119">O método retornará o número de estruturas [**\_ ConnectionPoint tssd**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) necessárias para alocar na matriz apontada pelo parâmetro *SOCKADDR* .</span><span class="sxs-lookup"><span data-stu-id="13bfb-119">The method will return the number of [**TSSD\_ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) structures necessary to allocate in the array pointed to by the *sockaddr* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="13bfb-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="13bfb-120">Remarks</span></span>

<span data-ttu-id="13bfb-121">Essa propriedade era conhecida anteriormente como **TargetExternalIpAddresses** no Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="13bfb-121">This property was formerly known as **TargetExternalIpAddresses** in Windows Server 2008 R2.</span></span>

<span data-ttu-id="13bfb-122">Se o número de endereços IP externos for desconhecido, você poderá chamar esse método com *SOCKADDR* definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="13bfb-122">If the number of external IP addresses is unknown, you can call this method with *sockaddr* set to **NULL**.</span></span> <span data-ttu-id="13bfb-123">O método será retornado, no parâmetro *numAddresses* , o número de estruturas [**\_ ConnectionPoint tssd**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) necessárias para receber todos os endereços IP externos.</span><span class="sxs-lookup"><span data-stu-id="13bfb-123">The method will then return, in the *numAddresses* parameter, the number of [**TSSD\_ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) structures necessary to receive all the external IP addresses.</span></span> <span data-ttu-id="13bfb-124">Aloque a matriz para *SOCKADDR* com base nesse número e, em seguida, chame o método novamente, configurando *SOCKADDR* para a matriz alocada recentemente e *numAddresses* para o número retornado pela primeira chamada.</span><span class="sxs-lookup"><span data-stu-id="13bfb-124">Allocate the array for *sockaddr* based on this number, and then call the method again, setting *sockaddr* to the newly allocated array and *numAddresses* to the number returned by the first call.</span></span>

## <a name="requirements"></a><span data-ttu-id="13bfb-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13bfb-125">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="13bfb-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13bfb-126">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="13bfb-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="13bfb-127">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="13bfb-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13bfb-128">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="13bfb-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="13bfb-129">Windows Server 2012</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="13bfb-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="13bfb-130">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="13bfb-131"><dt>Sbtsv. idl</dt> </span><span class="sxs-lookup"><span data-stu-id="13bfb-131"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="13bfb-132">IID</span><span class="sxs-lookup"><span data-stu-id="13bfb-132">IID</span></span><br/></td>
<td><span data-ttu-id="13bfb-133">IID_ITsSbTarget é definido como:</span><span class="sxs-lookup"><span data-stu-id="13bfb-133">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="13bfb-134">16616ECC-272D-411D-B324-126893033856</span><span class="sxs-lookup"><span data-stu-id="13bfb-134">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="13bfb-135">e85e10ea-db0b-4752-b456-5fd5840901c0 no Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="13bfb-135">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="13bfb-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="13bfb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13bfb-137">**ITsSbTargetEx**</span><span class="sxs-lookup"><span data-stu-id="13bfb-137">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="13bfb-138">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="13bfb-138">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[<span data-ttu-id="13bfb-139">**\_CONNECTIONPOINT tssd**</span><span class="sxs-lookup"><span data-stu-id="13bfb-139">**TSSD\_ConnectionPoint**</span></span>](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint)
</dt> </dl>

 

 





