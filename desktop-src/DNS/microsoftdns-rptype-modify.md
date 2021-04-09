---
title: Método Modify da classe MicrosoftDNS_RPType
description: O método Modify atualiza um registro de recurso de pessoa responsável (RP).
ms.assetid: a779b905-922c-42ff-b3d9-318b3a848230
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_RPType classe
- MicrosoftDNS_RPType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ec575424e6e26c79f8d6a27e62732cad6ddc57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824505"
---
# <a name="modify-method-of-the-microsoftdns_rptype-class"></a><span data-ttu-id="38d06-106">Método Modify da classe MicrosoftDNS \_ RPType</span><span class="sxs-lookup"><span data-stu-id="38d06-106">Modify method of the MicrosoftDNS\_RPType class</span></span>

<span data-ttu-id="38d06-107">O método **Modify** atualiza um registro de recurso de pessoa responsável (RP).</span><span class="sxs-lookup"><span data-stu-id="38d06-107">The **Modify** method updates a Responsible Person (RP) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="38d06-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38d06-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              RPMailbox,
  [in, optional] string              TXTDomainName,
  [out, ref]     MicrosoftDNS_RPType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="38d06-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38d06-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38d06-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="38d06-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="38d06-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="38d06-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="38d06-112">*RPMailbox* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="38d06-112">*RPMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="38d06-113">FQDN que especifica a caixa de correio da pessoa responsável.</span><span class="sxs-lookup"><span data-stu-id="38d06-113">FQDN specifying the mailbox for the responsible person.</span></span>

</dd> <dt>

<span data-ttu-id="38d06-114">*TXTDomainName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="38d06-114">*TXTDomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="38d06-115">FQDN para o qual os registros de recurso TXT existem.</span><span class="sxs-lookup"><span data-stu-id="38d06-115">FQDN for which TXT Resource Records exist.</span></span>

</dd> <dt>

<span data-ttu-id="38d06-116">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="38d06-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="38d06-117">Referência ao objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="38d06-117">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38d06-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="38d06-118">Return value</span></span>

<span data-ttu-id="38d06-119">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="38d06-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="38d06-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="38d06-120">Remarks</span></span>

<span data-ttu-id="38d06-121">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="38d06-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="38d06-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38d06-122">Requirements</span></span>



| <span data-ttu-id="38d06-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="38d06-123">Requirement</span></span> | <span data-ttu-id="38d06-124">Valor</span><span class="sxs-lookup"><span data-stu-id="38d06-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="38d06-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38d06-125">Minimum supported client</span></span><br/> | <span data-ttu-id="38d06-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="38d06-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="38d06-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38d06-127">Minimum supported server</span></span><br/> | <span data-ttu-id="38d06-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="38d06-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="38d06-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="38d06-129">Namespace</span></span><br/>                | <span data-ttu-id="38d06-130">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="38d06-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="38d06-131">MOF</span><span class="sxs-lookup"><span data-stu-id="38d06-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38d06-132"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38d06-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38d06-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="38d06-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38d06-134">**MicrosoftDNS \_ RPType**</span><span class="sxs-lookup"><span data-stu-id="38d06-134">**MicrosoftDNS\_RPType**</span></span>](microsoftdns-rptype.md)
</dt> <dt>

[<span data-ttu-id="38d06-135">**Método CreateInstanceFromPropertyData da \_ classe RPType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="38d06-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="38d06-136">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="38d06-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





