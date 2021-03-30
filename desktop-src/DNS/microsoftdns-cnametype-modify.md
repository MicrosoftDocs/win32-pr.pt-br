---
title: Método Modify da classe MicrosoftDNS_CNAMEType
description: O método Modify atualiza um registro de recurso de nome canônico (CNAME).
ms.assetid: 7e550026-d901-44a0-86ac-520682232ccb
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_CNAMEType classe
- MicrosoftDNS_CNAMEType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_CNAMEType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ddbe1e1592c4331be808340c216954cd8d7b14f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455161"
---
# <a name="modify-method-of-the-microsoftdns_cnametype-class"></a><span data-ttu-id="4f0d0-106">Método Modify da classe MicrosoftDNS \_ cnametype</span><span class="sxs-lookup"><span data-stu-id="4f0d0-106">Modify method of the MicrosoftDNS\_CNAMEType class</span></span>

<span data-ttu-id="4f0d0-107">O método **Modify** atualiza um registro de recurso de nome CANÔNICO (CNAME).</span><span class="sxs-lookup"><span data-stu-id="4f0d0-107">The **Modify** method updates a Canonical Name (CNAME) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f0d0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f0d0-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 PrimaryName,
  [out, ref]     MicrosoftDNS_CNAMEType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="4f0d0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f0d0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f0d0-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4f0d0-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f0d0-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="4f0d0-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="4f0d0-112">*Primárioname* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4f0d0-112">*PrimaryName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f0d0-113">Cadeia de caracteres que representa o nome primário do registro CNAME.</span><span class="sxs-lookup"><span data-stu-id="4f0d0-113">String representing the primary name for the CNAME record.</span></span>

</dd> <dt>

<span data-ttu-id="4f0d0-114">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="4f0d0-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="4f0d0-115">Referência ao objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="4f0d0-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f0d0-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4f0d0-116">Return value</span></span>

<span data-ttu-id="4f0d0-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4f0d0-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f0d0-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f0d0-118">Remarks</span></span>

<span data-ttu-id="4f0d0-119">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="4f0d0-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f0d0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f0d0-120">Requirements</span></span>



| <span data-ttu-id="4f0d0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f0d0-121">Requirement</span></span> | <span data-ttu-id="4f0d0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4f0d0-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f0d0-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f0d0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4f0d0-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4f0d0-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4f0d0-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f0d0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4f0d0-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4f0d0-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4f0d0-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="4f0d0-127">Namespace</span></span><br/>                | <span data-ttu-id="4f0d0-128">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="4f0d0-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="4f0d0-129">MOF</span><span class="sxs-lookup"><span data-stu-id="4f0d0-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f0d0-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f0d0-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f0d0-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4f0d0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f0d0-132">**\_Cnametype MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="4f0d0-132">**MicrosoftDNS\_CNAMEType**</span></span>](microsoftdns-cnametype.md)
</dt> <dt>

[<span data-ttu-id="4f0d0-133">**Método CreateInstanceFromPropertyData da \_ classe cnametype MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="4f0d0-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_CNAMEType Class**</span></span>](microsoftdns-cnametype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="4f0d0-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="4f0d0-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





