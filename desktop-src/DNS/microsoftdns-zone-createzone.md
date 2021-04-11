---
title: Método createzone da classe MicrosoftDNS_Zone
description: O método createzone cria uma zona DNS.
ms.assetid: 55756284-20ef-4d38-a8d9-357f53a6fa4d
keywords:
- Método createzone DNS
- Método createzone DNS, classe MicrosoftDNS_Zone
- Classe de MicrosoftDNS_Zone de DNS, método createzone
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.CreateZone
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7e3780db9036e0fd7c87d91c769c3c6f5c6aaf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009544"
---
# <a name="createzone-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="bf2e8-106">Método createzone da classe de \_ zona MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="bf2e8-106">CreateZone method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="bf2e8-107">O método **createzone** cria uma zona DNS.</span><span class="sxs-lookup"><span data-stu-id="bf2e8-107">The **CreateZone** method creates a DNS zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf2e8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf2e8-108">Syntax</span></span>


```mof
void CreateZone(
  [in]           string            ZoneName,
  [in]           uint32            ZoneType,
  [in]           boolean           DsIntegrated,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a><span data-ttu-id="bf2e8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf2e8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf2e8-110">*Nome_da_Zona* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bf2e8-110">*ZoneName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2e8-111">Cadeia de caracteres que representa o nome da zona.</span><span class="sxs-lookup"><span data-stu-id="bf2e8-111">String representing the name of the zone.</span></span>

</dd> <dt>

<span data-ttu-id="bf2e8-112">*Zonatype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bf2e8-112">*ZoneType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2e8-113">Tipo de zona.</span><span class="sxs-lookup"><span data-stu-id="bf2e8-113">Type of zone.</span></span> <span data-ttu-id="bf2e8-114">Os valores válidos são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="bf2e8-114">Valid values are the following:</span></span>



| <span data-ttu-id="bf2e8-115">Valor</span><span class="sxs-lookup"><span data-stu-id="bf2e8-115">Value</span></span>                                                                        | <span data-ttu-id="bf2e8-116">Significado</span><span class="sxs-lookup"><span data-stu-id="bf2e8-116">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bf2e8-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="bf2e8-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="bf2e8-118">Integrado ao AD.</span><span class="sxs-lookup"><span data-stu-id="bf2e8-118">AD integrated.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="bf2e8-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="bf2e8-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="bf2e8-120">Zona secundária.</span><span class="sxs-lookup"><span data-stu-id="bf2e8-120">Secondary zone.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="bf2e8-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="bf2e8-121"><dt>3</dt></span></span> </dl> | <span data-ttu-id="bf2e8-122">Zona de stub.</span><span class="sxs-lookup"><span data-stu-id="bf2e8-122">Stub zone.</span></span><br/> <span data-ttu-id="bf2e8-123">**Windows Server 2003:** Esse tipo de zona é introduzido no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bf2e8-123">**Windows Server 2003:** This zone type is introduced in Windows Server 2003.</span></span><br/>      |
| <dl> <span data-ttu-id="bf2e8-124"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="bf2e8-124"><dt>4</dt></span></span> </dl> | <span data-ttu-id="bf2e8-125">Encaminhador de zona.</span><span class="sxs-lookup"><span data-stu-id="bf2e8-125">Zone forwarder.</span></span><br/> <span data-ttu-id="bf2e8-126">**Windows Server 2003:** Esse tipo de zona é introduzido no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bf2e8-126">**Windows Server 2003:** This zone type is introduced in Windows Server 2003.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bf2e8-127">*DsIntegrated* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bf2e8-127">*DsIntegrated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2e8-128">Indica se os dados de zona são armazenados no Active Directory ou em arquivos.</span><span class="sxs-lookup"><span data-stu-id="bf2e8-128">Indicates whether zone data is stored in the Active Directory or in files.</span></span> <span data-ttu-id="bf2e8-129">Se for TRUE, os dados serão armazenados no Active Directory; Se for FALSE, os dados serão armazenados em arquivos.</span><span class="sxs-lookup"><span data-stu-id="bf2e8-129">If TRUE, the data is stored in the Active Directory; if FALSE, the data is stored in files.</span></span>

</dd> <dt>

<span data-ttu-id="bf2e8-130">*DataFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="bf2e8-130">*DataFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2e8-131">Nome do arquivo de dados associado à zona.</span><span class="sxs-lookup"><span data-stu-id="bf2e8-131">Name of the data file associated with the zone.</span></span>

</dd> <dt>

<span data-ttu-id="bf2e8-132">*IPADDR* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="bf2e8-132">*IpAddr* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2e8-133">Endereço IP do servidor DNS mestre para a zona.</span><span class="sxs-lookup"><span data-stu-id="bf2e8-133">IP address of the master DNS Server for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="bf2e8-134">*AdminEmailName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="bf2e8-134">*AdminEmailName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2e8-135">Endereço de email do administrador responsável pela zona.</span><span class="sxs-lookup"><span data-stu-id="bf2e8-135">Email address of the administrator responsible for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="bf2e8-136">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="bf2e8-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2e8-137">RR do tipo **MicrosoftDns \_ Zone**.</span><span class="sxs-lookup"><span data-stu-id="bf2e8-137">RR of type **MicrosoftDns\_Zone**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf2e8-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bf2e8-138">Return value</span></span>

<span data-ttu-id="bf2e8-139">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="bf2e8-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf2e8-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf2e8-140">Requirements</span></span>



| <span data-ttu-id="bf2e8-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf2e8-141">Requirement</span></span> | <span data-ttu-id="bf2e8-142">Valor</span><span class="sxs-lookup"><span data-stu-id="bf2e8-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf2e8-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf2e8-143">Minimum supported client</span></span><br/> | <span data-ttu-id="bf2e8-144">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bf2e8-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="bf2e8-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf2e8-145">Minimum supported server</span></span><br/> | <span data-ttu-id="bf2e8-146">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bf2e8-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bf2e8-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="bf2e8-147">Namespace</span></span><br/>                | <span data-ttu-id="bf2e8-148">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="bf2e8-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="bf2e8-149">MOF</span><span class="sxs-lookup"><span data-stu-id="bf2e8-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf2e8-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf2e8-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf2e8-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf2e8-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf2e8-152">**\_Zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="bf2e8-152">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="bf2e8-153">**Método AgeAllRecords da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="bf2e8-153">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="bf2e8-154">**Método ChangeZoneType da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="bf2e8-154">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="bf2e8-155">**Método ForceRefresh da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="bf2e8-155">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="bf2e8-156">**Método getdistinguiname da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="bf2e8-156">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="bf2e8-157">**Método PauseZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="bf2e8-157">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="bf2e8-158">**Método ReloadZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="bf2e8-158">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="bf2e8-159">**Método ResetSecondaries da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="bf2e8-159">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="bf2e8-160">**Método ResumeZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="bf2e8-160">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="bf2e8-161">**Método UpdateFromDS da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="bf2e8-161">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="bf2e8-162">**Método WriteBackZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="bf2e8-162">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





