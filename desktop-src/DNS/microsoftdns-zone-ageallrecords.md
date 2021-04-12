---
title: Método AgeAllRecords da classe MicrosoftDNS_Zone
description: O método AgeAllRecords habilita a duração de alguns ou todos os registros não NS e não SOA em uma zona.
ms.assetid: 0e0df1ab-6c7c-4bc4-b292-8f89095970eb
keywords:
- DNS do método AgeAllRecords
- Método AgeAllRecords DNS, classe MicrosoftDNS_Zone
- MicrosoftDNS_Zone classe DNS, método AgeAllRecords
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.AgeAllRecords
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c70a1435f96091070b2aee4ed7f079e5a6529a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455733"
---
# <a name="ageallrecords-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="d355d-106">Método AgeAllRecords da classe de \_ zona MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="d355d-106">AgeAllRecords method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="d355d-107">O método **AgeAllRecords** habilita a duração de alguns ou todos os registros não ns e não soa em uma zona.</span><span class="sxs-lookup"><span data-stu-id="d355d-107">The **AgeAllRecords** method enables aging for some or all non-NS and non-SOA records in a zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="d355d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d355d-108">Syntax</span></span>


```mof
uint32 AgeAllRecords(
  [in, optional] string  NodeName,
  [in, optional] boolean ApplyToSubtree
);
```



## <a name="parameters"></a><span data-ttu-id="d355d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d355d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d355d-110">*NodeName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d355d-110">*NodeName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d355d-111">Nome do nó para idade.</span><span class="sxs-lookup"><span data-stu-id="d355d-111">Name of the node to age.</span></span>

</dd> <dt>

<span data-ttu-id="d355d-112">*ApplyToSubtree* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d355d-112">*ApplyToSubtree* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d355d-113">Especifica se o envelhecimento deve ser aplicado a todos os registros na subárvore.</span><span class="sxs-lookup"><span data-stu-id="d355d-113">Specifies whether aging should apply to all records in the subtree.</span></span> <span data-ttu-id="d355d-114">Defina como TRUE para aplicar a duração a todos os registros na subárvore, começando com NodeName.</span><span class="sxs-lookup"><span data-stu-id="d355d-114">Set to TRUE to apply aging to all records in the subtree, beginning with NodeName.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d355d-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d355d-115">Return value</span></span>

<span data-ttu-id="d355d-116">\_O êxito do erro indica que a expiração foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="d355d-116">ERROR\_SUCCESS indicates the aging was successfully completed.</span></span> <span data-ttu-id="d355d-117">Qualquer outro valor é um código de erro.</span><span class="sxs-lookup"><span data-stu-id="d355d-117">Any other value is an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d355d-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="d355d-118">Remarks</span></span>

<span data-ttu-id="d355d-119">Se *NodeName* não for especificado, todos os registros estarão sujeitos à expiração e à eliminação.</span><span class="sxs-lookup"><span data-stu-id="d355d-119">If *NodeName* is not specified, all records will be subject to aging and scavenging.</span></span>

<span data-ttu-id="d355d-120">Se *NodeName* for especificado e *ApplyToSubtree* não for especificado ou definido como zero, os registros no nó especificado estarão sujeitos à expiração e à eliminação.</span><span class="sxs-lookup"><span data-stu-id="d355d-120">If *NodeName* is specified and *ApplyToSubtree* is not specified or set to zero, records at the specified node will be subjected to aging and scavenging.</span></span>

<span data-ttu-id="d355d-121">Se *NodeName* for especificado e *ApplyToSubtree* for definido como 1, todos os registros da subárvore começando em *NodeName* estarão sujeitos à expiração e à eliminação.</span><span class="sxs-lookup"><span data-stu-id="d355d-121">If *NodeName* is specified and *ApplyToSubtree* is set to 1, all records of the subtree starting at *NodeName* will be subjected to aging and scavenging.</span></span> <span data-ttu-id="d355d-122">O carimbo de data/hora é definido como a hora atual para todos os RRs não NS e não SOA com os nomes de proprietário identificados pelos parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="d355d-122">The time stamp is set to the current time for all non-NS and non-SOA RRs with the owner name(s) identified by the input parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="d355d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d355d-123">Requirements</span></span>



| <span data-ttu-id="d355d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d355d-124">Requirement</span></span> | <span data-ttu-id="d355d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d355d-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d355d-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d355d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d355d-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d355d-127">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d355d-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d355d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d355d-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d355d-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d355d-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="d355d-130">Namespace</span></span><br/>                | <span data-ttu-id="d355d-131">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="d355d-131">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d355d-132">MOF</span><span class="sxs-lookup"><span data-stu-id="d355d-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d355d-133"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d355d-133"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d355d-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="d355d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d355d-135">**\_Zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="d355d-135">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="d355d-136">**Método ChangeZoneType da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="d355d-136">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="d355d-137">**Método createzone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="d355d-137">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="d355d-138">**Método ForceRefresh da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="d355d-138">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="d355d-139">**Método getdistinguiname da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="d355d-139">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="d355d-140">**Método PauseZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="d355d-140">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="d355d-141">**Método ReloadZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="d355d-141">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="d355d-142">**Método ResetSecondaries da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="d355d-142">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="d355d-143">**Método ResumeZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="d355d-143">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="d355d-144">**Método UpdateFromDS da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="d355d-144">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="d355d-145">**Método WriteBackZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="d355d-145">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





