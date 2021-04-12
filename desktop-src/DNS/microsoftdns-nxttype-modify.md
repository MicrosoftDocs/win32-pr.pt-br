---
title: Método Modify da classe MicrosoftDNS_NXTType
description: O método Modify atualiza um próximo registro de recurso (NXT).
ms.assetid: 5a21b843-0761-4022-b00a-9dbcd6814454
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_NXTType classe
- MicrosoftDNS_NXTType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bab7bf8480c7e18914cac4f7ae0deb8a608090f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454867"
---
# <a name="modify-method-of-the-microsoftdns_nxttype-class"></a><span data-ttu-id="6750b-106">Método Modify da classe MicrosoftDNS \_ NXTType</span><span class="sxs-lookup"><span data-stu-id="6750b-106">Modify method of the MicrosoftDNS\_NXTType class</span></span>

<span data-ttu-id="6750b-107">O método **Modify** atualiza um próximo registro de recurso (NXT).</span><span class="sxs-lookup"><span data-stu-id="6750b-107">The **Modify** method updates a Next (NXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="6750b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6750b-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               NextDomainName,
  [in]           string               Types,
  [out, ref]     MicrosoftDNS_NXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="6750b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6750b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6750b-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="6750b-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6750b-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="6750b-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="6750b-112">*NextDomainName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6750b-112">*NextDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6750b-113">Próximo nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="6750b-113">Next domain name.</span></span>

</dd> <dt>

<span data-ttu-id="6750b-114">*Tipos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6750b-114">*Types* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6750b-115">Lista separada por espaços dos mnemônicos do tipo RR para o nome do proprietário do registro de recurso NXT.</span><span class="sxs-lookup"><span data-stu-id="6750b-115">Space-separated list of the RR-type mnemonics for the owner name of the NXT Resource Record.</span></span>

</dd> <dt>

<span data-ttu-id="6750b-116">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="6750b-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="6750b-117">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="6750b-117">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6750b-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6750b-118">Return value</span></span>

<span data-ttu-id="6750b-119">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6750b-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6750b-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="6750b-120">Remarks</span></span>

<span data-ttu-id="6750b-121">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="6750b-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="6750b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6750b-122">Requirements</span></span>



| <span data-ttu-id="6750b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6750b-123">Requirement</span></span> | <span data-ttu-id="6750b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="6750b-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6750b-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6750b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6750b-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6750b-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6750b-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6750b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6750b-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6750b-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6750b-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="6750b-129">Namespace</span></span><br/>                | <span data-ttu-id="6750b-130">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="6750b-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="6750b-131">MOF</span><span class="sxs-lookup"><span data-stu-id="6750b-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6750b-132"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6750b-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6750b-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="6750b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6750b-134">**MicrosoftDNS \_ NXTType**</span><span class="sxs-lookup"><span data-stu-id="6750b-134">**MicrosoftDNS\_NXTType**</span></span>](microsoftdns-nxttype.md)
</dt> <dt>

[<span data-ttu-id="6750b-135">**Método CreateInstanceFromPropertyData da \_ classe NXTType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6750b-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="6750b-136">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="6750b-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





