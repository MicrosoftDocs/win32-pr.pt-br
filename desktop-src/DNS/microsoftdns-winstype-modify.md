---
title: Método Modify da classe MicrosoftDNS_WINSType
description: O método Modify atualiza um registro de recurso WINS (serviço de cadastramento na Internet do Windows).
ms.assetid: b61c429a-6b01-4b17-9312-bc5b69d1e76a
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_WINSType classe
- MicrosoftDNS_WINSType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1469d1a9d50c72cdf3699bdc2ab9b96f51dfce86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824555"
---
# <a name="modify-method-of-the-microsoftdns_winstype-class"></a><span data-ttu-id="c6fcb-106">Método Modify da \_ classe winstype MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="c6fcb-106">Modify method of the MicrosoftDNS\_WINSType class</span></span>

<span data-ttu-id="c6fcb-107">O método **Modify** atualiza um registro de recurso WINS (serviço de cadastramento na Internet do Windows).</span><span class="sxs-lookup"><span data-stu-id="c6fcb-107">The **Modify** method updates a Windows Internet Name Service (WINS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6fcb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c6fcb-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint32                MappingFlag,
  [in, optional] uint32                LookupTimeout,
  [in, optional] uint32                CacheTimeout,
  [in, optional] string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="c6fcb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6fcb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6fcb-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c6fcb-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fcb-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="c6fcb-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="c6fcb-112">*MappingFlag* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c6fcb-112">*MappingFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fcb-113">Sinalizador de mapeamento WINS que especifica se o registro deve ser incluído na replicação de zona.</span><span class="sxs-lookup"><span data-stu-id="c6fcb-113">WINS mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="c6fcb-114">Ele pode ter apenas dois valores: 0x80000000 e 0x00010000 correspondentes aos sinalizadores de replicação e sem replicação (registro local), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c6fcb-114">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span> <span data-ttu-id="c6fcb-115">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="c6fcb-115">The following values are valid.</span></span>



| <span data-ttu-id="c6fcb-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c6fcb-116">Value</span></span>                                                                                                                                               | <span data-ttu-id="c6fcb-117">Significado</span><span class="sxs-lookup"><span data-stu-id="c6fcb-117">Meaning</span></span>                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <span data-ttu-id="c6fcb-118"><dt>**0x80000000**</dt></span><span class="sxs-lookup"><span data-stu-id="c6fcb-118"><dt>**0x80000000**</dt></span></span> </dl> | <span data-ttu-id="c6fcb-119">Sinalizador de replicação</span><span class="sxs-lookup"><span data-stu-id="c6fcb-119">Replication flag</span></span><br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <span data-ttu-id="c6fcb-120"><dt>**0x00010000**</dt></span><span class="sxs-lookup"><span data-stu-id="c6fcb-120"><dt>**0x00010000**</dt></span></span> </dl> | <span data-ttu-id="c6fcb-121">Sinalizador sem replicação (registro local)</span><span class="sxs-lookup"><span data-stu-id="c6fcb-121">No-replication (local record) flag</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c6fcb-122">*LookupTimeout* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c6fcb-122">*LookupTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fcb-123">Tempo, em segundos, que um servidor DNS tenta resolução usando a pesquisa WINS.</span><span class="sxs-lookup"><span data-stu-id="c6fcb-123">Time, in seconds, that a DNS Server attempts resolution using WINS Look up.</span></span>

</dd> <dt>

<span data-ttu-id="c6fcb-124">*CacheTimeout* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c6fcb-124">*CacheTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fcb-125">Tempo, em segundos, que um servidor DNS que usa a pesquisa WINS pode armazenar em cache a resposta do servidor WINS.</span><span class="sxs-lookup"><span data-stu-id="c6fcb-125">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="c6fcb-126">*WinsServers* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c6fcb-126">*WinsServers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fcb-127">Lista de endereços IP separados por vírgulas de servidores WINS usados na pesquisa WINS.</span><span class="sxs-lookup"><span data-stu-id="c6fcb-127">List of comma-separated IP addresses of WINS servers used in WINS Look ups.</span></span>

</dd> <dt>

<span data-ttu-id="c6fcb-128">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="c6fcb-128">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fcb-129">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="c6fcb-129">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6fcb-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c6fcb-130">Return value</span></span>

<span data-ttu-id="c6fcb-131">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c6fcb-131">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6fcb-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6fcb-132">Remarks</span></span>

<span data-ttu-id="c6fcb-133">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="c6fcb-133">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6fcb-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6fcb-134">Requirements</span></span>



| <span data-ttu-id="c6fcb-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6fcb-135">Requirement</span></span> | <span data-ttu-id="c6fcb-136">Valor</span><span class="sxs-lookup"><span data-stu-id="c6fcb-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6fcb-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6fcb-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c6fcb-138">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c6fcb-138">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c6fcb-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6fcb-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c6fcb-140">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c6fcb-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c6fcb-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="c6fcb-141">Namespace</span></span><br/>                | <span data-ttu-id="c6fcb-142">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="c6fcb-142">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c6fcb-143">MOF</span><span class="sxs-lookup"><span data-stu-id="c6fcb-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6fcb-144"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c6fcb-144"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6fcb-145">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c6fcb-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6fcb-146">**MicrosoftDNS \_ winstype**</span><span class="sxs-lookup"><span data-stu-id="c6fcb-146">**MicrosoftDNS\_WINSType**</span></span>](microsoftdns-winstype.md)
</dt> <dt>

[<span data-ttu-id="c6fcb-147">**Método CreateInstanceFromPropertyData da \_ classe winstype MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c6fcb-147">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="c6fcb-148">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="c6fcb-148">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





