---
title: Classe MicrosoftDNS_KEYType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro de recurso de chave.
ms.assetid: d3fa1f35-fa0a-47ee-b2be-4464b9b21d80
keywords:
- MicrosoftDNS_KEYType de classe de DNS
- MicrosoftDNS_KEYType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType
- MicrosoftDNS_KEYType.CreateInstanceFromPropertyData
- MicrosoftDNS_KEYType.Modify
- MicrosoftDNS_KEYType.Flags
- MicrosoftDNS_KEYType.Protocol
- MicrosoftDNS_KEYType.Algorithm
- MicrosoftDNS_KEYType.PublicKey
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1e814af1d22820f1722e5812dd314dd1c7f6e0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824509"
---
# <a name="microsoftdns_keytype-class"></a><span data-ttu-id="ccd39-105">\_Classe KeyType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="ccd39-105">MicrosoftDNS\_KEYType class</span></span>

<span data-ttu-id="ccd39-106">A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro de recurso de chave.</span><span class="sxs-lookup"><span data-stu-id="ccd39-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a KEY Resource Record.</span></span>

<span data-ttu-id="ccd39-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="ccd39-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccd39-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ccd39-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_KEYType : MicrosoftDNS_ResourceRecord
{
  uint16 Flags;
  uint16 Protocol;
  uint16 Algorithm;
  string PublicKey;
};
```

## <a name="members"></a><span data-ttu-id="ccd39-109">Membros</span><span class="sxs-lookup"><span data-stu-id="ccd39-109">Members</span></span>

<span data-ttu-id="ccd39-110">A **classe \_ KeyType MicrosoftDNS** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ccd39-110">The **MicrosoftDNS\_KEYType** class has these types of members:</span></span>

-   [<span data-ttu-id="ccd39-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="ccd39-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="ccd39-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ccd39-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ccd39-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="ccd39-113">Methods</span></span>

<span data-ttu-id="ccd39-114">A **classe \_ KeyType MicrosoftDNS** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ccd39-114">The **MicrosoftDNS\_KEYType** class has these methods.</span></span>



| <span data-ttu-id="ccd39-115">Método</span><span class="sxs-lookup"><span data-stu-id="ccd39-115">Method</span></span>                             | <span data-ttu-id="ccd39-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="ccd39-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccd39-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="ccd39-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="ccd39-118">Cria uma instância de um registro de recurso principal com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário, a classe (padrão = IN), o valor de vida útil e o sinalizador de mapeamento do WINS, o tempo limite de pesquisa inversa, o tempo limite do cache WINS e o nome de domínio a acrescentar</span><span class="sxs-lookup"><span data-stu-id="ccd39-118">Instantiates a KEY Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out and domain name to append.</span></span> <span data-ttu-id="ccd39-119">Ele retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="ccd39-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="ccd39-120">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="ccd39-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="ccd39-121">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="ccd39-121">**Modify**</span></span>                         | <span data-ttu-id="ccd39-122">Atualiza o TTL, o sinalizador de mapeamento, o tempo limite de pesquisa, o tempo limite de cache e o domínio de resultado para os valores especificados como os parâmetros de entrada deste método.</span><span class="sxs-lookup"><span data-stu-id="ccd39-122">Updates the TTL, mapping flag, look-up time out, cache time out, and result domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="ccd39-123">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="ccd39-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="ccd39-124">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="ccd39-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="ccd39-125">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="ccd39-125">Qualifiers: Implemented</span></span><br/>                          |



 

### <a name="properties"></a><span data-ttu-id="ccd39-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ccd39-126">Properties</span></span>

<span data-ttu-id="ccd39-127">A **classe \_ KeyType MicrosoftDNS** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ccd39-127">The **MicrosoftDNS\_KEYType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ccd39-128">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="ccd39-128">**Algorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccd39-129">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ccd39-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ccd39-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ccd39-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccd39-131">Algoritmo usado com a chave especificada no registro de recurso.</span><span class="sxs-lookup"><span data-stu-id="ccd39-131">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="ccd39-132">Os valores atribuídos são mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ccd39-132">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="ccd39-133">Valor</span><span class="sxs-lookup"><span data-stu-id="ccd39-133">Value</span></span>                                                                                                | <span data-ttu-id="ccd39-134">Significado</span><span class="sxs-lookup"><span data-stu-id="ccd39-134">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="ccd39-135"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="ccd39-135"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="ccd39-136">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="ccd39-136">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="ccd39-137"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="ccd39-137"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="ccd39-138">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="ccd39-138">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="ccd39-139"><dt>**Beta**</dt></span><span class="sxs-lookup"><span data-stu-id="ccd39-139"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="ccd39-140">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="ccd39-140">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="ccd39-141"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="ccd39-141"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="ccd39-142">Criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="ccd39-142">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ccd39-143">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="ccd39-143">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccd39-144">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ccd39-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ccd39-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ccd39-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccd39-146">Sinalizadores usados para especificar o mapeamento, conforme descrito em IETF RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="ccd39-146">Flags used to specify mapping, as described in IETF RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="ccd39-147">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="ccd39-147">**Protocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccd39-148">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ccd39-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ccd39-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ccd39-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccd39-150">Protocolo para o qual a chave especificada no registro de recurso pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="ccd39-150">Protocol for which the key specified in the resource record can be used.</span></span> <span data-ttu-id="ccd39-151">Os valores atribuídos são mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ccd39-151">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="ccd39-152">Valor</span><span class="sxs-lookup"><span data-stu-id="ccd39-152">Value</span></span>                                                                                                    | <span data-ttu-id="ccd39-153">Significado</span><span class="sxs-lookup"><span data-stu-id="ccd39-153">Meaning</span></span>                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="ccd39-154"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="ccd39-154"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="ccd39-155">TLS</span><span class="sxs-lookup"><span data-stu-id="ccd39-155">TLS</span></span><br/>           |
| <span id="2"></span><dl> <span data-ttu-id="ccd39-156"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="ccd39-156"><dt>**2**</dt></span></span> </dl>     | <span data-ttu-id="ccd39-157">Email</span><span class="sxs-lookup"><span data-stu-id="ccd39-157">E-Mail</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="ccd39-158"><dt>**Beta**</dt></span><span class="sxs-lookup"><span data-stu-id="ccd39-158"><dt>**3**</dt></span></span> </dl>     | <span data-ttu-id="ccd39-159">DNSSEC</span><span class="sxs-lookup"><span data-stu-id="ccd39-159">DNSSEC</span></span><br/>        |
| <span id="4"></span><dl> <span data-ttu-id="ccd39-160"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="ccd39-160"><dt>**4**</dt></span></span> </dl>     | <span data-ttu-id="ccd39-161">IPsec</span><span class="sxs-lookup"><span data-stu-id="ccd39-161">IPsec</span></span><br/>         |
| <span id="255"></span><dl> <span data-ttu-id="ccd39-162"><dt>**255**</dt></span><span class="sxs-lookup"><span data-stu-id="ccd39-162"><dt>**255**</dt></span></span> </dl> | <span data-ttu-id="ccd39-163">Todos os protocolos</span><span class="sxs-lookup"><span data-stu-id="ccd39-163">All protocols</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ccd39-164">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="ccd39-164">**PublicKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccd39-165">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ccd39-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccd39-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ccd39-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccd39-167">Chave pública, representada na base 64, conforme descrito no apêndice A de RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="ccd39-167">Public key, represented in base 64 as described in Appendix A of RFC 2535.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ccd39-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccd39-168">Requirements</span></span>



| <span data-ttu-id="ccd39-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccd39-169">Requirement</span></span> | <span data-ttu-id="ccd39-170">Valor</span><span class="sxs-lookup"><span data-stu-id="ccd39-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccd39-171">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccd39-171">Minimum supported client</span></span><br/> | <span data-ttu-id="ccd39-172">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ccd39-172">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ccd39-173">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccd39-173">Minimum supported server</span></span><br/> | <span data-ttu-id="ccd39-174">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ccd39-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ccd39-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="ccd39-175">Namespace</span></span><br/>                | <span data-ttu-id="ccd39-176">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="ccd39-176">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ccd39-177">MOF</span><span class="sxs-lookup"><span data-stu-id="ccd39-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ccd39-178"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ccd39-178"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccd39-179">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ccd39-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccd39-180">**Método CreateInstanceFromPropertyData da \_ classe KeyType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ccd39-180">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="ccd39-181">**Método Modify da \_ classe KeyType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ccd39-181">**Modify Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-modify.md)
</dt> <dt>

[<span data-ttu-id="ccd39-182">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="ccd39-182">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





