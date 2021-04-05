---
title: Método Modify da classe MicrosoftDNS_KEYType
description: O método Modify atualiza um registro de recurso de chave.
ms.assetid: 0ea1e0e5-ccd1-4800-b0c3-27795c36250c
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_KEYType classe
- MicrosoftDNS_KEYType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ee9182925f3f1d53fb90a4beefeb421f01c24f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086371"
---
# <a name="modify-method-of-the-microsoftdns_keytype-class"></a><span data-ttu-id="33e1f-106">Método Modify da \_ classe KeyType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="33e1f-106">Modify method of the MicrosoftDNS\_KEYType class</span></span>

<span data-ttu-id="33e1f-107">O método **Modify** atualiza um registro de recurso de chave.</span><span class="sxs-lookup"><span data-stu-id="33e1f-107">The **Modify** method updates a KEY Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="33e1f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33e1f-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Flags,
  [in, optional] uint16               Protocol,
  [in, optional] uint16               Algorithm,
  [in, optional] string               PublicKey,
  [out, ref]     MicrosoftDNS_KEYType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="33e1f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33e1f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33e1f-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="33e1f-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="33e1f-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="33e1f-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="33e1f-112">*Sinalizadores* \[ de em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="33e1f-112">*Flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="33e1f-113">Sinalizadores usados para especificar o mapeamento, conforme descrito em IETF RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="33e1f-113">Flags used to specify mapping, as described in IETF RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="33e1f-114">*Protocolo* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="33e1f-114">*Protocol* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="33e1f-115">Protocolo para o qual a chave especificada no RR pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="33e1f-115">Protocol for which the key specified in the RR can be used.</span></span> <span data-ttu-id="33e1f-116">Os valores atribuídos são mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="33e1f-116">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="33e1f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="33e1f-117">Value</span></span>                                                                                                    | <span data-ttu-id="33e1f-118">Significado</span><span class="sxs-lookup"><span data-stu-id="33e1f-118">Meaning</span></span>                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="33e1f-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="33e1f-119"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="33e1f-120">TLS</span><span class="sxs-lookup"><span data-stu-id="33e1f-120">TLS</span></span><br/>           |
| <span id="2"></span><dl> <span data-ttu-id="33e1f-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="33e1f-121"><dt>**2**</dt></span></span> </dl>     | <span data-ttu-id="33e1f-122">Email</span><span class="sxs-lookup"><span data-stu-id="33e1f-122">E-Mail</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="33e1f-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="33e1f-123"><dt>**3**</dt></span></span> </dl>     | <span data-ttu-id="33e1f-124">DNSSEC</span><span class="sxs-lookup"><span data-stu-id="33e1f-124">dnssec</span></span><br/>        |
| <span id="4"></span><dl> <span data-ttu-id="33e1f-125"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="33e1f-125"><dt>**4**</dt></span></span> </dl>     | <span data-ttu-id="33e1f-126">IPsec</span><span class="sxs-lookup"><span data-stu-id="33e1f-126">IPsec</span></span><br/>         |
| <span id="255"></span><dl> <span data-ttu-id="33e1f-127"><dt>**255**</dt></span><span class="sxs-lookup"><span data-stu-id="33e1f-127"><dt>**255**</dt></span></span> </dl> | <span data-ttu-id="33e1f-128">Todos os protocolos</span><span class="sxs-lookup"><span data-stu-id="33e1f-128">All protocols</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="33e1f-129">*Algoritmo* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="33e1f-129">*Algorithm* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="33e1f-130">Algoritmo usado com a chave especificada no registro de recurso.</span><span class="sxs-lookup"><span data-stu-id="33e1f-130">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="33e1f-131">Os valores atribuídos são mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="33e1f-131">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="33e1f-132">Valor</span><span class="sxs-lookup"><span data-stu-id="33e1f-132">Value</span></span>                                                                                                | <span data-ttu-id="33e1f-133">Significado</span><span class="sxs-lookup"><span data-stu-id="33e1f-133">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="33e1f-134"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="33e1f-134"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="33e1f-135">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="33e1f-135">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="33e1f-136"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="33e1f-136"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="33e1f-137">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="33e1f-137">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="33e1f-138"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="33e1f-138"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="33e1f-139">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="33e1f-139">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="33e1f-140"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="33e1f-140"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="33e1f-141">Criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="33e1f-141">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="33e1f-142">*PublicKey* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="33e1f-142">*PublicKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="33e1f-143">Chave pública, representada na base 64, conforme descrito no apêndice A de RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="33e1f-143">Public key, represented in base 64 as described in Appendix A of RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="33e1f-144">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="33e1f-144">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="33e1f-145">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="33e1f-145">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33e1f-146">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33e1f-146">Return value</span></span>

<span data-ttu-id="33e1f-147">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="33e1f-147">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="33e1f-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="33e1f-148">Remarks</span></span>

<span data-ttu-id="33e1f-149">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="33e1f-149">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="33e1f-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33e1f-150">Requirements</span></span>



| <span data-ttu-id="33e1f-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="33e1f-151">Requirement</span></span> | <span data-ttu-id="33e1f-152">Valor</span><span class="sxs-lookup"><span data-stu-id="33e1f-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33e1f-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33e1f-153">Minimum supported client</span></span><br/> | <span data-ttu-id="33e1f-154">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="33e1f-154">None supported</span></span><br/>                                                              |
| <span data-ttu-id="33e1f-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33e1f-155">Minimum supported server</span></span><br/> | <span data-ttu-id="33e1f-156">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="33e1f-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="33e1f-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="33e1f-157">Namespace</span></span><br/>                | <span data-ttu-id="33e1f-158">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="33e1f-158">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="33e1f-159">MOF</span><span class="sxs-lookup"><span data-stu-id="33e1f-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33e1f-160"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33e1f-160"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33e1f-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="33e1f-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33e1f-162">**KeyType MicrosoftDNS \_**</span><span class="sxs-lookup"><span data-stu-id="33e1f-162">**MicrosoftDNS\_KEYType**</span></span>](microsoftdns-keytype.md)
</dt> <dt>

[<span data-ttu-id="33e1f-163">**Método CreateInstanceFromPropertyData da \_ classe KeyType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="33e1f-163">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="33e1f-164">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="33e1f-164">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





