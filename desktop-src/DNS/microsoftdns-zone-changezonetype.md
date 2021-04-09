---
title: Método ChangeZoneType da classe MicrosoftDNS_Zone
description: O método ChangeZoneType altera o tipo de uma zona.
ms.assetid: a0a9f495-fdbb-4258-a313-ee9551da762f
keywords:
- DNS do método ChangeZoneType
- Método ChangeZoneType DNS, classe MicrosoftDNS_Zone
- MicrosoftDNS_Zone classe DNS, método ChangeZoneType
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ChangeZoneType
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1611eda876532f32534e24257478b3a5986af3aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009246"
---
# <a name="changezonetype-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="514bd-106">Método ChangeZoneType da classe de \_ zona MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="514bd-106">ChangeZoneType method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="514bd-107">O método **ChangeZoneType** altera o tipo de uma zona.</span><span class="sxs-lookup"><span data-stu-id="514bd-107">The **ChangeZoneType** method changes the type of a zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="514bd-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="514bd-108">Syntax</span></span>


```mof
void ChangeZoneType(
  [in]           uint32            ZoneType,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a><span data-ttu-id="514bd-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="514bd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="514bd-110">*Zonatype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="514bd-110">*ZoneType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="514bd-111">Tipo de zona.</span><span class="sxs-lookup"><span data-stu-id="514bd-111">Type of zone.</span></span> <span data-ttu-id="514bd-112">Os valores válidos são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="514bd-112">Valid values are the following:</span></span>



| <span data-ttu-id="514bd-113">Valor</span><span class="sxs-lookup"><span data-stu-id="514bd-113">Value</span></span>                                                                        | <span data-ttu-id="514bd-114">Significado</span><span class="sxs-lookup"><span data-stu-id="514bd-114">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="514bd-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="514bd-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="514bd-116">Zona primária.</span><span class="sxs-lookup"><span data-stu-id="514bd-116">Primary zone.</span></span><br/>   |
| <dl> <span data-ttu-id="514bd-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="514bd-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="514bd-118">Zona secundária.</span><span class="sxs-lookup"><span data-stu-id="514bd-118">Secondary zone.</span></span><br/> |
| <dl> <span data-ttu-id="514bd-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="514bd-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="514bd-120">Zona de stub.</span><span class="sxs-lookup"><span data-stu-id="514bd-120">Stub zone.</span></span><br/>      |
| <dl> <span data-ttu-id="514bd-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="514bd-121"><dt>3</dt></span></span> </dl> | <span data-ttu-id="514bd-122">Encaminhador de zona.</span><span class="sxs-lookup"><span data-stu-id="514bd-122">Zone forwarder.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="514bd-123">*DataFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="514bd-123">*DataFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="514bd-124">Nome do arquivo de dados associado à zona.</span><span class="sxs-lookup"><span data-stu-id="514bd-124">Name of the data file associated with the zone.</span></span>

</dd> <dt>

<span data-ttu-id="514bd-125">*IPADDR* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="514bd-125">*IpAddr* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="514bd-126">Endereço IP do servidor DNS do mate para a zona.</span><span class="sxs-lookup"><span data-stu-id="514bd-126">IP address of the mater DNS Server for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="514bd-127">*AdminEmailName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="514bd-127">*AdminEmailName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="514bd-128">Endereço de email do administrador responsável pela zona.</span><span class="sxs-lookup"><span data-stu-id="514bd-128">Email address of the administrator responsible for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="514bd-129">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="514bd-129">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="514bd-130">RR do tipo **MicrosoftDns \_ Zone**.</span><span class="sxs-lookup"><span data-stu-id="514bd-130">RR of type **MicrosoftDns\_Zone**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="514bd-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="514bd-131">Return value</span></span>

<span data-ttu-id="514bd-132">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="514bd-132">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="514bd-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="514bd-133">Requirements</span></span>



| <span data-ttu-id="514bd-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="514bd-134">Requirement</span></span> | <span data-ttu-id="514bd-135">Valor</span><span class="sxs-lookup"><span data-stu-id="514bd-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="514bd-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="514bd-136">Minimum supported client</span></span><br/> | <span data-ttu-id="514bd-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="514bd-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="514bd-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="514bd-138">Minimum supported server</span></span><br/> | <span data-ttu-id="514bd-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="514bd-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="514bd-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="514bd-140">Namespace</span></span><br/>                | <span data-ttu-id="514bd-141">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="514bd-141">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="514bd-142">MOF</span><span class="sxs-lookup"><span data-stu-id="514bd-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="514bd-143"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="514bd-143"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="514bd-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="514bd-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="514bd-145">**\_Zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="514bd-145">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="514bd-146">**Método AgeAllRecords da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="514bd-146">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="514bd-147">**Método createzone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="514bd-147">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="514bd-148">**Método ForceRefresh da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="514bd-148">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="514bd-149">**Método getdistinguiname da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="514bd-149">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="514bd-150">**Método PauseZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="514bd-150">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="514bd-151">**Método ReloadZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="514bd-151">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="514bd-152">**Método ResetSecondaries da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="514bd-152">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="514bd-153">**Método ResumeZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="514bd-153">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="514bd-154">**Método UpdateFromDS da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="514bd-154">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="514bd-155">**Método WriteBackZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="514bd-155">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





