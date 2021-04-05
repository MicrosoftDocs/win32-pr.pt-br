---
title: Método Modify da classe MicrosoftDNS_WINSRType
description: O método Modify atualiza um registro de recurso WINSr (pesquisa inversa do WINS).
ms.assetid: 28be0045-5b0d-4434-a2a9-b56191f1e213
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_WINSRType classe
- MicrosoftDNS_WINSRType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02d89c3cd191262136035f9006853e2f1a7f7dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086307"
---
# <a name="modify-method-of-the-microsoftdns_winsrtype-class"></a><span data-ttu-id="9cf45-106">Método Modify da classe MicrosoftDNS \_ WINSRType</span><span class="sxs-lookup"><span data-stu-id="9cf45-106">Modify method of the MicrosoftDNS\_WINSRType class</span></span>

<span data-ttu-id="9cf45-107">O método **Modify** atualiza um registro de recurso WINSR (pesquisa inversa do WINS).</span><span class="sxs-lookup"><span data-stu-id="9cf45-107">The **Modify** method updates a WINS Reverse Look up (WINSR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cf45-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9cf45-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint32                 MappingFlag,
  [in, optional] uint32                 LookupTimeout,
  [in, optional] uint32                 CacheTimeout,
  [in, optional] string                 ResultDomain,
  [out, ref]     MicrosoftDNS_WINSRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="9cf45-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9cf45-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cf45-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9cf45-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9cf45-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="9cf45-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="9cf45-112">*MappingFlag* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9cf45-112">*MappingFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9cf45-113">Sinalizador de mapeamento WINSr que especifica se o registro deve ser incluído na replicação de zona.</span><span class="sxs-lookup"><span data-stu-id="9cf45-113">WINSR mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="9cf45-114">Ele pode ter apenas dois valores: 0x80000000 e 0x00010000 correspondentes aos sinalizadores de replicação e sem replicação (registro local), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9cf45-114">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="9cf45-115">*LookupTimeout* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9cf45-115">*LookupTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9cf45-116">Tempo limite, em segundos, para um servidor DNS usando a pesquisa inversa do WINS.</span><span class="sxs-lookup"><span data-stu-id="9cf45-116">Time out, in seconds, for a DNS Server using WINS Reverse Look up.</span></span>

</dd> <dt>

<span data-ttu-id="9cf45-117">*CacheTimeout* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9cf45-117">*CacheTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9cf45-118">Tempo, em segundos, um servidor DNS usando a pesquisa WINS pode armazenar em cache a resposta do servidor WINS.</span><span class="sxs-lookup"><span data-stu-id="9cf45-118">Time, in seconds, a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="9cf45-119">*ResultDomain* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9cf45-119">*ResultDomain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9cf45-120">Nome de domínio a ser anexado aos nomes NetBIOS retornados.</span><span class="sxs-lookup"><span data-stu-id="9cf45-120">Domain name to append to returned NetBIOS names.</span></span>

</dd> <dt>

<span data-ttu-id="9cf45-121">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="9cf45-121">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="9cf45-122">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="9cf45-122">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cf45-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9cf45-123">Return value</span></span>

<span data-ttu-id="9cf45-124">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9cf45-124">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cf45-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="9cf45-125">Remarks</span></span>

<span data-ttu-id="9cf45-126">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="9cf45-126">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cf45-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cf45-127">Requirements</span></span>



| <span data-ttu-id="9cf45-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cf45-128">Requirement</span></span> | <span data-ttu-id="9cf45-129">Valor</span><span class="sxs-lookup"><span data-stu-id="9cf45-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9cf45-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cf45-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9cf45-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9cf45-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9cf45-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cf45-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9cf45-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9cf45-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9cf45-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="9cf45-134">Namespace</span></span><br/>                | <span data-ttu-id="9cf45-135">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="9cf45-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="9cf45-136">MOF</span><span class="sxs-lookup"><span data-stu-id="9cf45-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9cf45-137"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9cf45-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cf45-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="9cf45-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cf45-139">**MicrosoftDNS \_ WINSRType**</span><span class="sxs-lookup"><span data-stu-id="9cf45-139">**MicrosoftDNS\_WINSRType**</span></span>](microsoftdns-winsrtype.md)
</dt> <dt>

[<span data-ttu-id="9cf45-140">**Método CreateInstanceFromPropertyData da \_ classe WINSRType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9cf45-140">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="9cf45-141">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="9cf45-141">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





