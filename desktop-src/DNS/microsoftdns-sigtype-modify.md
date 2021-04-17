---
title: Método Modify da classe MicrosoftDNS_SIGType
description: O método Modify atualiza um RR de assinatura (SIG).
ms.assetid: 6a7017da-d3f1-4aba-a53a-96f578518304
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_SIGType classe
- MicrosoftDNS_SIGType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80fbaa25ec3b6a52aae06f99ed02d50430745dca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454755"
---
# <a name="modify-method-of-the-microsoftdns_sigtype-class"></a><span data-ttu-id="3959e-106">Método Modify da classe MicrosoftDNS \_ SIGType</span><span class="sxs-lookup"><span data-stu-id="3959e-106">Modify method of the MicrosoftDNS\_SIGType class</span></span>

<span data-ttu-id="3959e-107">O método **Modify** atualiza um RR de assinatura (SIG).</span><span class="sxs-lookup"><span data-stu-id="3959e-107">The **Modify** method updates a Signature (SIG) RR.</span></span>

## <a name="syntax"></a><span data-ttu-id="3959e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3959e-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           uint16               TypeCovered,
  [in]           uint16               Algorithm,
  [in]           uint16               Labels,
  [in]           uint32               OriginalTTL,
  [in]           uint32               SignatureExpiration,
  [in]           uint32               SignatureInception,
  [in]           uint16               KeyTag,
  [in]           string               SignerName,
  [in]           string               Signature,
  [out, ref]     MicrosoftDNS_SIGType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="3959e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3959e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3959e-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3959e-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3959e-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="3959e-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="3959e-112">*TypeCovered* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3959e-112">*TypeCovered* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3959e-113">Tipo de RR coberto por essa SIG.</span><span class="sxs-lookup"><span data-stu-id="3959e-113">Type of RR covered by this SIG.</span></span>

</dd> <dt>

<span data-ttu-id="3959e-114">*Algoritmo* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="3959e-114">*Algorithm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3959e-115">Algoritmo usado com a chave especificada no registro de recurso.</span><span class="sxs-lookup"><span data-stu-id="3959e-115">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="3959e-116">Os valores atribuídos são mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3959e-116">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="3959e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3959e-117">Value</span></span>                                                                                                | <span data-ttu-id="3959e-118">Significado</span><span class="sxs-lookup"><span data-stu-id="3959e-118">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="3959e-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="3959e-119"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="3959e-120">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="3959e-120">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="3959e-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="3959e-121"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="3959e-122">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="3959e-122">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="3959e-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="3959e-123"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="3959e-124">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="3959e-124">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="3959e-125"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="3959e-125"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="3959e-126">Criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="3959e-126">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3959e-127">*Rótulos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3959e-127">*Labels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3959e-128">Contagem não assinada de rótulos no nome do proprietário do RR SIG original.</span><span class="sxs-lookup"><span data-stu-id="3959e-128">Unsigned count of labels in the original SIG RR owner name.</span></span> <span data-ttu-id="3959e-129">A contagem não inclui o rótulo nulo para a raiz nem qualquer caractere curinga inicial.</span><span class="sxs-lookup"><span data-stu-id="3959e-129">The count does not include the NULL label for the root, nor any initial wildcards.</span></span>

</dd> <dt>

<span data-ttu-id="3959e-130">*OriginalTTL* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3959e-130">*OriginalTTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3959e-131">TTL do conjunto de RRs assinado pelo SIG.</span><span class="sxs-lookup"><span data-stu-id="3959e-131">TTL of the RR set signed by the SIG.</span></span>

</dd> <dt>

<span data-ttu-id="3959e-132">*SignatureExpiration* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3959e-132">*SignatureExpiration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3959e-133">Data de expiração da assinatura, expressa em segundos desde o início de 1º de janeiro de 1970, hora de Greenwich (GMT), excluindo segundos bissextos.</span><span class="sxs-lookup"><span data-stu-id="3959e-133">Signature expiration date, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="3959e-134">*SignatureInception* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3959e-134">*SignatureInception* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3959e-135">Data e hora em que a assinatura se torna válida, expressa em segundos desde o início de 1º de janeiro de 1970, Greenwich Mean Time (GMT), excluindo segundos bissextos.</span><span class="sxs-lookup"><span data-stu-id="3959e-135">Date and time at which the Signature becomes valid, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="3959e-136">*Keytag* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3959e-136">*KeyTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3959e-137">Método usado para escolher uma chave que verifica um SIG.</span><span class="sxs-lookup"><span data-stu-id="3959e-137">Method used to choose a key that verifies a SIG.</span></span> <span data-ttu-id="3959e-138">Consulte RFC 2535, Apêndice C para o método usado para calcular um KeyTag.</span><span class="sxs-lookup"><span data-stu-id="3959e-138">See RFC 2535, Appendix C for the method used to calculate a KeyTag.</span></span>

</dd> <dt>

<span data-ttu-id="3959e-139">*Signatárioname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3959e-139">*SignerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3959e-140">Nome de domínio do signatário que gerou o RR SIG.</span><span class="sxs-lookup"><span data-stu-id="3959e-140">Domain name of the signer that generated the SIG RR.</span></span>

</dd> <dt>

<span data-ttu-id="3959e-141">*Assinatura* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="3959e-141">*Signature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3959e-142">Assinatura, representada na base 64, formatada conforme definido na RFC 2535, apêndice A.</span><span class="sxs-lookup"><span data-stu-id="3959e-142">Signature, represented in base 64, formatted as defined in RFC 2535, Appendix A.</span></span>

</dd> <dt>

<span data-ttu-id="3959e-143">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="3959e-143">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="3959e-144">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="3959e-144">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3959e-145">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3959e-145">Return value</span></span>

<span data-ttu-id="3959e-146">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3959e-146">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3959e-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="3959e-147">Remarks</span></span>

<span data-ttu-id="3959e-148">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="3959e-148">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="3959e-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3959e-149">Requirements</span></span>



| <span data-ttu-id="3959e-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="3959e-150">Requirement</span></span> | <span data-ttu-id="3959e-151">Valor</span><span class="sxs-lookup"><span data-stu-id="3959e-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3959e-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3959e-152">Minimum supported client</span></span><br/> | <span data-ttu-id="3959e-153">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3959e-153">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3959e-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3959e-154">Minimum supported server</span></span><br/> | <span data-ttu-id="3959e-155">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3959e-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3959e-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="3959e-156">Namespace</span></span><br/>                | <span data-ttu-id="3959e-157">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="3959e-157">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="3959e-158">MOF</span><span class="sxs-lookup"><span data-stu-id="3959e-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3959e-159"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3959e-159"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3959e-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="3959e-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3959e-161">**MicrosoftDNS \_ SIGType**</span><span class="sxs-lookup"><span data-stu-id="3959e-161">**MicrosoftDNS\_SIGType**</span></span>](microsoftdns-sigtype.md)
</dt> <dt>

[<span data-ttu-id="3959e-162">**Método CreateInstanceFromPropertyData da \_ classe SIGType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="3959e-162">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="3959e-163">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="3959e-163">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





