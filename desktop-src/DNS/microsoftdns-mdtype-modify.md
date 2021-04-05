---
title: Método Modify da classe MicrosoftDNS_MDType
description: O método Modify atualiza um registro de recurso do agente de email para o domínio (MD).
ms.assetid: d14c8ada-d715-489f-9956-a940b94006e5
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_MDType classe
- MicrosoftDNS_MDType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MDType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78ed5e3a8d7f819447d256ba3bce31f4eaa6986a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085528"
---
# <a name="modify-method-of-the-microsoftdns_mdtype-class"></a><span data-ttu-id="54dc4-106">Método Modify da classe MicrosoftDNS \_ MDType</span><span class="sxs-lookup"><span data-stu-id="54dc4-106">Modify method of the MicrosoftDNS\_MDType class</span></span>

<span data-ttu-id="54dc4-107">O método **Modify** atualiza um registro de recurso do agente de email para o domínio (MD).</span><span class="sxs-lookup"><span data-stu-id="54dc4-107">The **Modify** method updates a Mail Agent for Domain (MD) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="54dc4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="54dc4-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MDHost,
  [out, ref]     MicrosoftDNS_MDType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="54dc4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54dc4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54dc4-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="54dc4-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="54dc4-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="54dc4-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="54dc4-112">*MDHost* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="54dc4-112">*MDHost* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="54dc4-113">Cadeia de caracteres que representa o host de entrega de email.</span><span class="sxs-lookup"><span data-stu-id="54dc4-113">String representing the mail delivery host.</span></span>

</dd> <dt>

<span data-ttu-id="54dc4-114">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="54dc4-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="54dc4-115">Referência ao objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="54dc4-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54dc4-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="54dc4-116">Return value</span></span>

<span data-ttu-id="54dc4-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="54dc4-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="54dc4-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="54dc4-118">Remarks</span></span>

<span data-ttu-id="54dc4-119">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="54dc4-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="54dc4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54dc4-120">Requirements</span></span>



| <span data-ttu-id="54dc4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="54dc4-121">Requirement</span></span> | <span data-ttu-id="54dc4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="54dc4-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54dc4-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54dc4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="54dc4-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="54dc4-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="54dc4-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54dc4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="54dc4-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="54dc4-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="54dc4-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="54dc4-127">Namespace</span></span><br/>                | <span data-ttu-id="54dc4-128">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="54dc4-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="54dc4-129">MOF</span><span class="sxs-lookup"><span data-stu-id="54dc4-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54dc4-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="54dc4-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54dc4-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="54dc4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54dc4-132">**MicrosoftDNS \_ MDType**</span><span class="sxs-lookup"><span data-stu-id="54dc4-132">**MicrosoftDNS\_MDType**</span></span>](microsoftdns-mdtype.md)
</dt> <dt>

[<span data-ttu-id="54dc4-133">**Método CreateInstanceFromPropertyData da \_ classe MDType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="54dc4-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MDType Class**</span></span>](microsoftdns-mdtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="54dc4-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="54dc4-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





