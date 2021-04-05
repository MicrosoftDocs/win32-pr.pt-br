---
title: Método Modify da classe MicrosoftDNS_MXType
description: O método Modify atualiza um registro de recurso do servidor de mensagens (MR).
ms.assetid: 40267ac9-0392-4e08-a5d2-145ee9639c39
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_MXType classe
- MicrosoftDNS_MXType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a665d0673e048eff684b4c985b54a1c57e030a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919124"
---
# <a name="modify-method-of-the-microsoftdns_mxtype-class"></a><span data-ttu-id="9e7c2-106">Método Modify da classe MicrosoftDNS \_ MXType</span><span class="sxs-lookup"><span data-stu-id="9e7c2-106">Modify method of the MicrosoftDNS\_MXType class</span></span>

<span data-ttu-id="9e7c2-107">O método **Modify** atualiza um registro de recurso do servidor de mensagens (Mr).</span><span class="sxs-lookup"><span data-stu-id="9e7c2-107">The **Modify** method updates a Mail Exchanger (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e7c2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e7c2-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              MailExchange,
  [out, ref]     MicrosoftDNS_MXType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="9e7c2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e7c2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e7c2-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9e7c2-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9e7c2-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="9e7c2-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="9e7c2-112">*Preferência* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9e7c2-112">*Preference* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9e7c2-113">Preferência dada a esse RR entre outros no mesmo proprietário.</span><span class="sxs-lookup"><span data-stu-id="9e7c2-113">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="9e7c2-114">Os valores mais baixos são preferenciais.</span><span class="sxs-lookup"><span data-stu-id="9e7c2-114">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="9e7c2-115">*MailExchange* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9e7c2-115">*MailExchange* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9e7c2-116">FQDN que especifica um host que está disposto a atuar como uma troca de email para o nome do proprietário.</span><span class="sxs-lookup"><span data-stu-id="9e7c2-116">FQDN specifying a host willing to act as a mail exchange for the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="9e7c2-117">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="9e7c2-117">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="9e7c2-118">Referência ao objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="9e7c2-118">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e7c2-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e7c2-119">Return value</span></span>

<span data-ttu-id="9e7c2-120">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9e7c2-120">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e7c2-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e7c2-121">Remarks</span></span>

<span data-ttu-id="9e7c2-122">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="9e7c2-122">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e7c2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e7c2-123">Requirements</span></span>



| <span data-ttu-id="9e7c2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e7c2-124">Requirement</span></span> | <span data-ttu-id="9e7c2-125">Valor</span><span class="sxs-lookup"><span data-stu-id="9e7c2-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e7c2-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e7c2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9e7c2-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9e7c2-127">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9e7c2-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e7c2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9e7c2-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9e7c2-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9e7c2-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="9e7c2-130">Namespace</span></span><br/>                | <span data-ttu-id="9e7c2-131">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="9e7c2-131">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="9e7c2-132">MOF</span><span class="sxs-lookup"><span data-stu-id="9e7c2-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e7c2-133"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e7c2-133"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e7c2-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e7c2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e7c2-135">**MicrosoftDNS \_ MXType**</span><span class="sxs-lookup"><span data-stu-id="9e7c2-135">**MicrosoftDNS\_MXType**</span></span>](microsoftdns-mxtype.md)
</dt> <dt>

[<span data-ttu-id="9e7c2-136">**Método CreateInstanceFromPropertyData da \_ classe MXType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9e7c2-136">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="9e7c2-137">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="9e7c2-137">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





