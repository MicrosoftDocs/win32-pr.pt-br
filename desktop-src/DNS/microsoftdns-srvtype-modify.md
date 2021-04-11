---
title: Método Modify da classe MicrosoftDNS_SRVType
description: O método Modify atualiza um registro de recurso de serviço (SRV).
ms.assetid: 626483c9-4b36-4e62-b9ad-dd7bb18f2e1e
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_SRVType classe
- MicrosoftDNS_SRVType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1174e7a8096d70a3e6305a5d24b9ae1f4915096e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009699"
---
# <a name="modify-method-of-the-microsoftdns_srvtype-class"></a><span data-ttu-id="70e43-106">Método Modify da classe MicrosoftDNS \_ SRVType</span><span class="sxs-lookup"><span data-stu-id="70e43-106">Modify method of the MicrosoftDNS\_SRVType class</span></span>

<span data-ttu-id="70e43-107">O método **Modify** atualiza um registro de recurso de serviço (SRV).</span><span class="sxs-lookup"><span data-stu-id="70e43-107">The **Modify** method updates a Service (SRV) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="70e43-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70e43-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Priority,
  [in, optional] uint16               Weight,
  [in, optional] uint16               Port,
  [in, optional] string               SRVDomainName,
  [out, ref]     MicrosoftDNS_SRVType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="70e43-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70e43-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70e43-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="70e43-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="70e43-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="70e43-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="70e43-112">*Prioridade* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="70e43-112">*Priority* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="70e43-113">Prioridade do host de destino especificado no nome do proprietário.</span><span class="sxs-lookup"><span data-stu-id="70e43-113">Priority of the target host specified in the owner name.</span></span> <span data-ttu-id="70e43-114">Números inferiores implicam prioridades mais altas.</span><span class="sxs-lookup"><span data-stu-id="70e43-114">Lower numbers imply higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="70e43-115">*Peso* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="70e43-115">*Weight* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="70e43-116">Peso do host de destino.</span><span class="sxs-lookup"><span data-stu-id="70e43-116">Weight of the target host.</span></span> <span data-ttu-id="70e43-117">Isso é útil ao selecionar entre os hosts que têm a mesma prioridade.</span><span class="sxs-lookup"><span data-stu-id="70e43-117">This is useful when selecting among hosts that have the same priority.</span></span> <span data-ttu-id="70e43-118">As chances de usar esse host devem ser proporcionais ao seu peso.</span><span class="sxs-lookup"><span data-stu-id="70e43-118">The chances of using this host should be proportional to its weight.</span></span>

</dd> <dt>

<span data-ttu-id="70e43-119">*Porta* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="70e43-119">*Port* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="70e43-120">Porta usada no host de destino de um serviço de protocolo.</span><span class="sxs-lookup"><span data-stu-id="70e43-120">Port used on the target host of a protocol service.</span></span>

</dd> <dt>

<span data-ttu-id="70e43-121">*SRVDomainName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="70e43-121">*SRVDomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="70e43-122">FQDN do host de destino.</span><span class="sxs-lookup"><span data-stu-id="70e43-122">FQDN of the target host.</span></span> <span data-ttu-id="70e43-123">Um destino de \\ . \\ significa que o serviço está decididamente não disponível neste domínio.</span><span class="sxs-lookup"><span data-stu-id="70e43-123">A target of \\.\\ means that the service is decidedly not available at this domain.</span></span>

</dd> <dt>

<span data-ttu-id="70e43-124">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="70e43-124">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="70e43-125">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="70e43-125">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70e43-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="70e43-126">Return value</span></span>

<span data-ttu-id="70e43-127">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="70e43-127">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="70e43-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="70e43-128">Remarks</span></span>

<span data-ttu-id="70e43-129">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="70e43-129">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="70e43-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70e43-130">Requirements</span></span>



| <span data-ttu-id="70e43-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="70e43-131">Requirement</span></span> | <span data-ttu-id="70e43-132">Valor</span><span class="sxs-lookup"><span data-stu-id="70e43-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="70e43-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70e43-133">Minimum supported client</span></span><br/> | <span data-ttu-id="70e43-134">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="70e43-134">None supported</span></span><br/>                                                              |
| <span data-ttu-id="70e43-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70e43-135">Minimum supported server</span></span><br/> | <span data-ttu-id="70e43-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="70e43-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="70e43-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="70e43-137">Namespace</span></span><br/>                | <span data-ttu-id="70e43-138">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="70e43-138">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="70e43-139">MOF</span><span class="sxs-lookup"><span data-stu-id="70e43-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70e43-140"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70e43-140"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70e43-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="70e43-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70e43-142">**MicrosoftDNS \_ SRVType**</span><span class="sxs-lookup"><span data-stu-id="70e43-142">**MicrosoftDNS\_SRVType**</span></span>](microsoftdns-srvtype.md)
</dt> <dt>

[<span data-ttu-id="70e43-143">**Método CreateInstanceFromPropertyData da \_ classe SRVType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="70e43-143">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="70e43-144">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="70e43-144">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





