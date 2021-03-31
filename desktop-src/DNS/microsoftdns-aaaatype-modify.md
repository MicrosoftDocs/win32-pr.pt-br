---
title: Método Modify da classe MicrosoftDNS_AAAAType
description: O método Modify atualiza um registro de recurso de endereço IPv6 (AAAA).
ms.assetid: d58f8a88-8473-4b26-89f0-237d2457f00b
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_AAAAType classe
- MicrosoftDNS_AAAAType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc216233fe3d41e4f1e31fe0d471e766c4dc8476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824420"
---
# <a name="modify-method-of-the-microsoftdns_aaaatype-class"></a><span data-ttu-id="d2918-106">Método Modify da classe MicrosoftDNS \_ aaaatype</span><span class="sxs-lookup"><span data-stu-id="d2918-106">Modify method of the MicrosoftDNS\_AAAAType class</span></span>

<span data-ttu-id="d2918-107">O método **Modify** atualiza um registro de recurso de endereço IPv6 (aaaa).</span><span class="sxs-lookup"><span data-stu-id="d2918-107">The **Modify** method updates an IPv6 address (AAAA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2918-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2918-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] string                IPv6Address,
  [out, ref]     MicrosoftDNS_AAAAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="d2918-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2918-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2918-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d2918-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2918-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="d2918-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="d2918-112">*IPv6Address* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d2918-112">*IPv6Address* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2918-113">Endereço IPv6 para o host.</span><span class="sxs-lookup"><span data-stu-id="d2918-113">IPv6 address for the host.</span></span>

</dd> <dt>

<span data-ttu-id="d2918-114">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="d2918-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d2918-115">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="d2918-115">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2918-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2918-116">Return value</span></span>

<span data-ttu-id="d2918-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d2918-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2918-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2918-118">Remarks</span></span>

<span data-ttu-id="d2918-119">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="d2918-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2918-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2918-120">Requirements</span></span>



| <span data-ttu-id="d2918-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2918-121">Requirement</span></span> | <span data-ttu-id="d2918-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d2918-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2918-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2918-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d2918-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d2918-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d2918-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2918-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d2918-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d2918-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d2918-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="d2918-127">Namespace</span></span><br/>                | <span data-ttu-id="d2918-128">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="d2918-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d2918-129">MOF</span><span class="sxs-lookup"><span data-stu-id="d2918-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2918-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2918-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2918-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d2918-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2918-132">**MicrosoftDNS \_ aaaatype**</span><span class="sxs-lookup"><span data-stu-id="d2918-132">**MicrosoftDNS\_AAAAType**</span></span>](microsoftdns-aaaatype.md)
</dt> <dt>

[<span data-ttu-id="d2918-133">**Método CreateInstanceFromPropertyData da \_ classe aaaatype MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="d2918-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="d2918-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="d2918-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





