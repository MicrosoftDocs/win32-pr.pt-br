---
title: Método Modify da classe MicrosoftDNS_MINFOType
description: O método Modify atualiza um registro de recurso de informações de email (MINFO).
ms.assetid: fbec0cd3-f735-44c6-b010-80f35cc33d98
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_MINFOType classe
- MicrosoftDNS_MINFOType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b59d7d1231ed88e61a0ecf94cef50041ca772f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454868"
---
# <a name="modify-method-of-the-microsoftdns_minfotype-class"></a><span data-ttu-id="cc317-106">Método Modify da classe MicrosoftDNS \_ MINFOType</span><span class="sxs-lookup"><span data-stu-id="cc317-106">Modify method of the MicrosoftDNS\_MINFOType class</span></span>

<span data-ttu-id="cc317-107">O método **Modify** atualiza um registro de recurso de informações de email (MINFO).</span><span class="sxs-lookup"><span data-stu-id="cc317-107">The **Modify** method updates a Mail Information (MINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc317-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc317-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 ResponsibleMailbox,
  [in, optional] string                 ErrorMailbox,
  [out, ref]     MicrosoftDNS_MINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="cc317-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc317-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc317-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cc317-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cc317-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="cc317-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="cc317-112">*ResponsibleMailbox* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cc317-112">*ResponsibleMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cc317-113">FQDN que especifica uma caixa de correio responsável pela lista de endereçamento ou caixa de correio especificada no nome do proprietário do registro.</span><span class="sxs-lookup"><span data-stu-id="cc317-113">FQDN specifying a mailbox responsible for the mailing list or mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="cc317-114">*ErrorMailbox* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cc317-114">*ErrorMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cc317-115">FQDN que especifica uma caixa de correio para receber mensagens de erro relacionadas à lista de endereçamento ou à caixa de correio especificada pelo nome do proprietário do registro MINFO.</span><span class="sxs-lookup"><span data-stu-id="cc317-115">FQDN specifying a mailbox to receive error messages related to either the mailing list, or to the mailbox specified by the owner name of the MINFO record.</span></span>

</dd> <dt>

<span data-ttu-id="cc317-116">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="cc317-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="cc317-117">Referência ao objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="cc317-117">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc317-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cc317-118">Return value</span></span>

<span data-ttu-id="cc317-119">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="cc317-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc317-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc317-120">Remarks</span></span>

<span data-ttu-id="cc317-121">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="cc317-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc317-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc317-122">Requirements</span></span>



| <span data-ttu-id="cc317-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc317-123">Requirement</span></span> | <span data-ttu-id="cc317-124">Valor</span><span class="sxs-lookup"><span data-stu-id="cc317-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc317-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc317-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cc317-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="cc317-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="cc317-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc317-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cc317-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cc317-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cc317-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="cc317-129">Namespace</span></span><br/>                | <span data-ttu-id="cc317-130">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="cc317-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="cc317-131">MOF</span><span class="sxs-lookup"><span data-stu-id="cc317-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc317-132"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc317-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc317-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc317-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc317-134">**MicrosoftDNS \_ MINFOType**</span><span class="sxs-lookup"><span data-stu-id="cc317-134">**MicrosoftDNS\_MINFOType**</span></span>](microsoftdns-minfotype.md)
</dt> <dt>

[<span data-ttu-id="cc317-135">**Método CreateInstanceFromPropertyData da \_ classe MINFOType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="cc317-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="cc317-136">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="cc317-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





