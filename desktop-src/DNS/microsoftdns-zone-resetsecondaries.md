---
title: Método ResetSecondaries da classe MicrosoftDNS_Zone
description: O método ResetSecondaries redefine os endereços IP para servidores DNS secundários na zona.
ms.assetid: b9a47714-f180-40cf-831a-f59e804a4ca2
keywords:
- DNS do método ResetSecondaries
- Método ResetSecondaries DNS, classe MicrosoftDNS_Zone
- MicrosoftDNS_Zone classe DNS, método ResetSecondaries
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ResetSecondaries
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a78d65b2153782c38d6d91d34f642860e896ed1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918768"
---
# <a name="resetsecondaries-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="c1763-106">Método ResetSecondaries da classe de \_ zona MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="c1763-106">ResetSecondaries method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="c1763-107">O método **ResetSecondaries** redefine os endereços IP para servidores DNS secundários na zona.</span><span class="sxs-lookup"><span data-stu-id="c1763-107">The **ResetSecondaries** method resets the IP addresses for secondary DNS Servers in the zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1763-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1763-108">Syntax</span></span>


```mof
void ResetSecondaries(
  [in]       string            SecondaryServers[],
  [in]       uint32            SecureSecondaries,
  [in]       string            NotifyServers[],
  [in]       uint32            Notify,
  [out, ref] MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a><span data-ttu-id="c1763-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1763-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1763-110">*SecondaryServers* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c1763-110">*SecondaryServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1763-111">Matriz de endereços IP para servidores DNS secundários.</span><span class="sxs-lookup"><span data-stu-id="c1763-111">Array of IP addresses for secondary DNS Servers.</span></span>

</dd> <dt>

<span data-ttu-id="c1763-112">*SecureSecondaries* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c1763-112">*SecureSecondaries* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1763-113">Especifica a segurança a ser aplicada e deve ser uma das seguintes:</span><span class="sxs-lookup"><span data-stu-id="c1763-113">Specifies the security to be applied and must be one of the following:</span></span>

-   <span data-ttu-id="c1763-114">SECSECURE de zona \_ \_ sem \_ segurança</span><span class="sxs-lookup"><span data-stu-id="c1763-114">ZONE\_SECSECURE\_NO\_SECURITY</span></span>
-   <span data-ttu-id="c1763-115">ZONA \_ SECSECURE \_ \_ somente NS</span><span class="sxs-lookup"><span data-stu-id="c1763-115">ZONE\_SECSECURE\_NS\_ONLY</span></span>
-   <span data-ttu-id="c1763-116">lista de SECSECURE de zona \_ \_ \_ somente</span><span class="sxs-lookup"><span data-stu-id="c1763-116">ZONE\_SECSECURE\_LIST\_ONLY</span></span>
-   <span data-ttu-id="c1763-117">SECSECURE de zona \_ \_ sem \_ XFR</span><span class="sxs-lookup"><span data-stu-id="c1763-117">ZONE\_SECSECURE\_NO\_XFR</span></span>

</dd> <dt>

<span data-ttu-id="c1763-118">*NotifyServers* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c1763-118">*NotifyServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1763-119">Endereço IP dos servidores DNS a ser notificado quando a zona for alterada.</span><span class="sxs-lookup"><span data-stu-id="c1763-119">IP address of DNS Servers to be notified when the zone changes.</span></span>

</dd> <dt>

<span data-ttu-id="c1763-120">*Notificar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c1763-120">*Notify* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1763-121">A configuração de notificação e deve ser uma das seguintes:</span><span class="sxs-lookup"><span data-stu-id="c1763-121">Notification setting and must be one of the following:</span></span>

-   <span data-ttu-id="c1763-122">notificação de zona \_ \_ desativada</span><span class="sxs-lookup"><span data-stu-id="c1763-122">ZONE\_NOTIFY\_OFF</span></span>
-   <span data-ttu-id="c1763-123">\_notificar \_ todos os \_ SECUNDÁRIOs da zona</span><span class="sxs-lookup"><span data-stu-id="c1763-123">ZONE\_NOTIFY\_ALL\_SECONDARIES</span></span>
-   <span data-ttu-id="c1763-124">lista de notificações de zona \_ \_ \_ somente</span><span class="sxs-lookup"><span data-stu-id="c1763-124">ZONE\_NOTIFY\_LIST\_ONLY</span></span>

</dd> <dt>

<span data-ttu-id="c1763-125">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="c1763-125">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c1763-126">RR do tipo [**MicrosoftDNS \_ Zone**](microsoftdns-zone.md).</span><span class="sxs-lookup"><span data-stu-id="c1763-126">RR of type [**MicrosoftDNS\_Zone**](microsoftdns-zone.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1763-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c1763-127">Return value</span></span>

<span data-ttu-id="c1763-128">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c1763-128">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1763-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1763-129">Requirements</span></span>



| <span data-ttu-id="c1763-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1763-130">Requirement</span></span> | <span data-ttu-id="c1763-131">Valor</span><span class="sxs-lookup"><span data-stu-id="c1763-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1763-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1763-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c1763-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c1763-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c1763-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1763-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c1763-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c1763-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c1763-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1763-136">Namespace</span></span><br/>                | <span data-ttu-id="c1763-137">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="c1763-137">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c1763-138">MOF</span><span class="sxs-lookup"><span data-stu-id="c1763-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1763-139"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1763-139"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1763-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1763-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1763-141">**\_Zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c1763-141">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="c1763-142">**Método AgeAllRecords da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c1763-142">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="c1763-143">**Método ChangeZoneType da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c1763-143">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="c1763-144">**Método createzone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c1763-144">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="c1763-145">**Método ForceRefresh da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c1763-145">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="c1763-146">**Método getdistinguiname da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c1763-146">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="c1763-147">**Método PauseZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c1763-147">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="c1763-148">**Método ReloadZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c1763-148">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="c1763-149">**Método ResumeZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c1763-149">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="c1763-150">**Método UpdateFromDS da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c1763-150">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="c1763-151">**Método WriteBackZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c1763-151">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





