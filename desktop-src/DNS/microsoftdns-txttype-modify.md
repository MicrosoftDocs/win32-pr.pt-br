---
title: Método Modify da classe MicrosoftDNS_TXTType
description: O método Modify atualiza um registro de recurso de texto (TXT).
ms.assetid: af61057e-95be-4290-83da-a63f01ead476
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_TXTType classe
- MicrosoftDNS_TXTType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 285dfb6d5323ca3775f981aecbf5a0170392cd3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085250"
---
# <a name="modify-method-of-the-microsoftdns_txttype-class"></a><span data-ttu-id="a24fa-106">Método Modify da classe MicrosoftDNS \_ TXTType</span><span class="sxs-lookup"><span data-stu-id="a24fa-106">Modify method of the MicrosoftDNS\_TXTType class</span></span>

<span data-ttu-id="a24fa-107">O método **Modify** atualiza um registro de recurso de texto (txt).</span><span class="sxs-lookup"><span data-stu-id="a24fa-107">The **Modify** method updates a Text (TXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="a24fa-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a24fa-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               DescriptiveText,
  [out, ref]     MicrosoftDNS_TXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="a24fa-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a24fa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a24fa-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a24fa-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a24fa-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="a24fa-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="a24fa-112">*DescriptiveText* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a24fa-112">*DescriptiveText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a24fa-113">Texto descritivo, a semântica que depende do domínio do proprietário.</span><span class="sxs-lookup"><span data-stu-id="a24fa-113">Descriptive text, the semantics of which depend on the owner domain.</span></span>

</dd> <dt>

<span data-ttu-id="a24fa-114">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="a24fa-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="a24fa-115">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="a24fa-115">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a24fa-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a24fa-116">Return value</span></span>

<span data-ttu-id="a24fa-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a24fa-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a24fa-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="a24fa-118">Remarks</span></span>

<span data-ttu-id="a24fa-119">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="a24fa-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="a24fa-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a24fa-120">Requirements</span></span>



| <span data-ttu-id="a24fa-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a24fa-121">Requirement</span></span> | <span data-ttu-id="a24fa-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a24fa-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a24fa-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a24fa-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a24fa-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a24fa-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a24fa-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a24fa-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a24fa-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a24fa-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a24fa-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="a24fa-127">Namespace</span></span><br/>                | <span data-ttu-id="a24fa-128">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="a24fa-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="a24fa-129">MOF</span><span class="sxs-lookup"><span data-stu-id="a24fa-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a24fa-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a24fa-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a24fa-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="a24fa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a24fa-132">**MicrosoftDNS \_ TXTType**</span><span class="sxs-lookup"><span data-stu-id="a24fa-132">**MicrosoftDNS\_TXTType**</span></span>](microsoftdns-txttype.md)
</dt> <dt>

[<span data-ttu-id="a24fa-133">**Método CreateInstanceFromPropertyData da \_ classe TXTType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="a24fa-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="a24fa-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="a24fa-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





