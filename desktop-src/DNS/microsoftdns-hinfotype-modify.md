---
title: Método Modify da classe MicrosoftDNS_HINFOType
description: O método Modify atualiza um registro de recurso de informações de host (HINFO).
ms.assetid: 8f8148f3-804f-4f99-8e79-606cd3cea660
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_HINFOType classe
- MicrosoftDNS_HINFOType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29a01eb94d82d080142d3496bab5f7f0b9acac8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644661"
---
# <a name="modify-method-of-the-microsoftdns_hinfotype-class"></a><span data-ttu-id="3a4fe-106">Método Modify da classe MicrosoftDNS \_ HINFOType</span><span class="sxs-lookup"><span data-stu-id="3a4fe-106">Modify method of the MicrosoftDNS\_HINFOType class</span></span>

<span data-ttu-id="3a4fe-107">O método **Modify** atualiza um registro de recurso de informações de host (HINFO).</span><span class="sxs-lookup"><span data-stu-id="3a4fe-107">The **Modify** method updates a Host Information (HINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a4fe-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a4fe-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 CPU,
  [in, optional] string                 OS,
  [out, ref]     MicrosoftDNS_HINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="3a4fe-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a4fe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a4fe-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3a4fe-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3a4fe-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="3a4fe-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="3a4fe-112">*CPU* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3a4fe-112">*CPU* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3a4fe-113">Tipo de CPU do proprietário do registro.</span><span class="sxs-lookup"><span data-stu-id="3a4fe-113">CPU type of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="3a4fe-114">*Sistema operacional* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3a4fe-114">*OS* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3a4fe-115">Sistema operacional do proprietário do registro.</span><span class="sxs-lookup"><span data-stu-id="3a4fe-115">Operating system of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="3a4fe-116">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="3a4fe-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="3a4fe-117">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="3a4fe-117">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a4fe-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3a4fe-118">Return value</span></span>

<span data-ttu-id="3a4fe-119">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3a4fe-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a4fe-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a4fe-120">Remarks</span></span>

<span data-ttu-id="3a4fe-121">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="3a4fe-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a4fe-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a4fe-122">Requirements</span></span>



| <span data-ttu-id="3a4fe-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a4fe-123">Requirement</span></span> | <span data-ttu-id="3a4fe-124">Valor</span><span class="sxs-lookup"><span data-stu-id="3a4fe-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a4fe-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a4fe-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3a4fe-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3a4fe-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3a4fe-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a4fe-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3a4fe-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3a4fe-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3a4fe-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a4fe-129">Namespace</span></span><br/>                | <span data-ttu-id="3a4fe-130">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="3a4fe-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="3a4fe-131">MOF</span><span class="sxs-lookup"><span data-stu-id="3a4fe-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a4fe-132"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a4fe-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a4fe-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3a4fe-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a4fe-134">**MicrosoftDNS \_ HINFOType**</span><span class="sxs-lookup"><span data-stu-id="3a4fe-134">**MicrosoftDNS\_HINFOType**</span></span>](microsoftdns-hinfotype.md)
</dt> <dt>

[<span data-ttu-id="3a4fe-135">**Método CreateInstanceFromPropertyData da \_ classe HINFOType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="3a4fe-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_HINFOType Class**</span></span>](microsoftdns-hinfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="3a4fe-136">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="3a4fe-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





