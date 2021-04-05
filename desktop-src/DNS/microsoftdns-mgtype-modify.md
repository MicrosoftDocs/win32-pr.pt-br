---
title: Método Modify da classe MicrosoftDNS_MGType
description: O método Modify atualiza um registro de recurso de grupo de emails (MG).
ms.assetid: c7d42964-19fb-410d-a434-85af20754e20
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_MGType classe
- MicrosoftDNS_MGType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 706502569687a3c035c943e0a9dcc04aa1732492
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085908"
---
# <a name="modify-method-of-the-microsoftdns_mgtype-class"></a><span data-ttu-id="5cbc6-106">Método Modify da classe MicrosoftDNS \_ MGType</span><span class="sxs-lookup"><span data-stu-id="5cbc6-106">Modify method of the MicrosoftDNS\_MGType class</span></span>

<span data-ttu-id="5cbc6-107">O método **Modify** atualiza um registro de recurso de grupo de emails (mg).</span><span class="sxs-lookup"><span data-stu-id="5cbc6-107">The **Modify** method updates a Mail Group (MG) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cbc6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5cbc6-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MGMailbox,
  [out, ref]     MicrosoftDNS_MGType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="5cbc6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5cbc6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cbc6-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5cbc6-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5cbc6-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="5cbc6-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="5cbc6-112">*MGMailbox* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5cbc6-112">*MGMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5cbc6-113">FQDN que especifica uma caixa de correio que é membro do grupo de emails especificado pelo nome do proprietário do registro.</span><span class="sxs-lookup"><span data-stu-id="5cbc6-113">FQDN specifying a mailbox that is a member of the mail group specified by the record's owner name.</span></span>

</dd> <dt>

<span data-ttu-id="5cbc6-114">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="5cbc6-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="5cbc6-115">Referência ao objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="5cbc6-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cbc6-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5cbc6-116">Return value</span></span>

<span data-ttu-id="5cbc6-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5cbc6-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cbc6-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="5cbc6-118">Remarks</span></span>

<span data-ttu-id="5cbc6-119">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="5cbc6-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cbc6-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cbc6-120">Requirements</span></span>



| <span data-ttu-id="5cbc6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cbc6-121">Requirement</span></span> | <span data-ttu-id="5cbc6-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5cbc6-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5cbc6-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5cbc6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5cbc6-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5cbc6-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5cbc6-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5cbc6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5cbc6-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5cbc6-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5cbc6-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="5cbc6-127">Namespace</span></span><br/>                | <span data-ttu-id="5cbc6-128">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="5cbc6-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="5cbc6-129">MOF</span><span class="sxs-lookup"><span data-stu-id="5cbc6-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5cbc6-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5cbc6-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cbc6-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="5cbc6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cbc6-132">**MicrosoftDNS \_ MGType**</span><span class="sxs-lookup"><span data-stu-id="5cbc6-132">**MicrosoftDNS\_MGType**</span></span>](microsoftdns-mgtype.md)
</dt> <dt>

[<span data-ttu-id="5cbc6-133">**Método CreateInstanceFromPropertyData da \_ classe MGType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="5cbc6-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="5cbc6-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="5cbc6-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





