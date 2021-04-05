---
title: Método Modify da classe MicrosoftDNS_WKSType
description: O método Modify atualiza um registro de recurso de serviços de Well-Known (WKS).
ms.assetid: 3a9100eb-dc90-45bb-9739-14026da100fd
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_WKSType classe
- MicrosoftDNS_WKSType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30f7cf58a231d93288a3cdc170fa857bb12687af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824552"
---
# <a name="modify-method-of-the-microsoftdns_wkstype-class"></a><span data-ttu-id="77495-106">Método Modify da classe MicrosoftDNS \_ WKSType</span><span class="sxs-lookup"><span data-stu-id="77495-106">Modify method of the MicrosoftDNS\_WKSType class</span></span>

<span data-ttu-id="77495-107">O método **Modify** atualiza um registro de recurso de serviços de Well-Known (WKS).</span><span class="sxs-lookup"><span data-stu-id="77495-107">The **Modify** method updates a Well-Known Services (WKS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="77495-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77495-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               InternetAddress,
  [in, optional] uint8                IPProtocol,
  [in, optional] uint8                Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="77495-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77495-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77495-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="77495-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="77495-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="77495-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="77495-112">*InternetAddress* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="77495-112">*InternetAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="77495-113">Endereço IP da Internet para o proprietário do registro.</span><span class="sxs-lookup"><span data-stu-id="77495-113">Internet IP address for the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="77495-114">*IPProtocol* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="77495-114">*IPProtocol* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="77495-115">Cadeia de caracteres que representa o protocolo IP para este registro.</span><span class="sxs-lookup"><span data-stu-id="77495-115">String representing the IP protocol for this record.</span></span> <span data-ttu-id="77495-116">Os valores válidos são UDP ou TCP.</span><span class="sxs-lookup"><span data-stu-id="77495-116">Valid values are UDP or TCP.</span></span>

</dd> <dt>

<span data-ttu-id="77495-117">*Serviços* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="77495-117">*Services* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="77495-118">Cadeia de caracteres que contém todos os serviços usados pelo registro WKS (serviço bem conhecido).</span><span class="sxs-lookup"><span data-stu-id="77495-118">String containing all services used by the Well Known Service (WKS) record.</span></span>

</dd> <dt>

<span data-ttu-id="77495-119">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="77495-119">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="77495-120">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="77495-120">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77495-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77495-121">Return value</span></span>

<span data-ttu-id="77495-122">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="77495-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="77495-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="77495-123">Remarks</span></span>

<span data-ttu-id="77495-124">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="77495-124">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="77495-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77495-125">Requirements</span></span>



| <span data-ttu-id="77495-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="77495-126">Requirement</span></span> | <span data-ttu-id="77495-127">Valor</span><span class="sxs-lookup"><span data-stu-id="77495-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="77495-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77495-128">Minimum supported client</span></span><br/> | <span data-ttu-id="77495-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="77495-129">None supported</span></span><br/>                                                              |
| <span data-ttu-id="77495-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77495-130">Minimum supported server</span></span><br/> | <span data-ttu-id="77495-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="77495-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="77495-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="77495-132">Namespace</span></span><br/>                | <span data-ttu-id="77495-133">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="77495-133">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="77495-134">MOF</span><span class="sxs-lookup"><span data-stu-id="77495-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77495-135"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="77495-135"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77495-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="77495-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77495-137">**MicrosoftDNS \_ WKSType**</span><span class="sxs-lookup"><span data-stu-id="77495-137">**MicrosoftDNS\_WKSType**</span></span>](microsoftdns-wkstype.md)
</dt> <dt>

[<span data-ttu-id="77495-138">**Método CreateInstanceFromPropertyData da \_ classe WKSType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="77495-138">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="77495-139">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="77495-139">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





