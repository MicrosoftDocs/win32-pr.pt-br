---
title: Classe MicrosoftDNS_WKSType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro de serviços de Well-Known (WKS).
ms.assetid: 7bbfd518-d473-4127-949b-9133a43ac7a7
keywords:
- MicrosoftDNS_WKSType de classe de DNS
- MicrosoftDNS_WKSType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType
- MicrosoftDNS_WKSType.CreateInstanceFromPropertyData
- MicrosoftDNS_WKSType.Modify
- MicrosoftDNS_WKSType.InternetAddress
- MicrosoftDNS_WKSType.IPProtocol
- MicrosoftDNS_WKSType.Services
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f7fde08721bb8bb62b93f72b792060b06c15dad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918688"
---
# <a name="microsoftdns_wkstype-class"></a><span data-ttu-id="d122d-105">\_Classe MicrosoftDNS WKSType</span><span class="sxs-lookup"><span data-stu-id="d122d-105">MicrosoftDNS\_WKSType class</span></span>

<span data-ttu-id="d122d-106">A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro de serviços de Well-Known (WKS).</span><span class="sxs-lookup"><span data-stu-id="d122d-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Well-Known Services (WKS) record.</span></span>

<span data-ttu-id="d122d-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="d122d-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d122d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d122d-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_WKSType : MicrosoftDNS_ResourceRecord
{
  string InternetAddress;
  string IPProtocol;
  string Services;
};
```

## <a name="members"></a><span data-ttu-id="d122d-109">Membros</span><span class="sxs-lookup"><span data-stu-id="d122d-109">Members</span></span>

<span data-ttu-id="d122d-110">A classe **MicrosoftDNS \_ WKSType** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d122d-110">The **MicrosoftDNS\_WKSType** class has these types of members:</span></span>

-   [<span data-ttu-id="d122d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="d122d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="d122d-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d122d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d122d-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="d122d-113">Methods</span></span>

<span data-ttu-id="d122d-114">A classe **MicrosoftDNS \_ WKSType** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d122d-114">The **MicrosoftDNS\_WKSType** class has these methods.</span></span>



| <span data-ttu-id="d122d-115">Método</span><span class="sxs-lookup"><span data-stu-id="d122d-115">Method</span></span>                             | <span data-ttu-id="d122d-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d122d-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d122d-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="d122d-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="d122d-118">Cria uma instância de um tipo WKS de RR com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário, a classe (padrão = IN), o valor de vida útil e o endereço de Internet do proprietário, o protocolo IP e a máscara de bits de porta.</span><span class="sxs-lookup"><span data-stu-id="d122d-118">Instantiates a WKS Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the owner's Internet Address, IP protocol and port bit mask.</span></span> <span data-ttu-id="d122d-119">Ele retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="d122d-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="d122d-120">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="d122d-120">Qualifiers: Implemented, static</span></span><br/>  |
| <span data-ttu-id="d122d-121">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="d122d-121">**Modify**</span></span>                         | <span data-ttu-id="d122d-122">Esse método atualiza a TTL, o endereço da Internet, o protocolo IP e os serviços para os valores especificados como os parâmetros de entrada desse método.</span><span class="sxs-lookup"><span data-stu-id="d122d-122">This method updates the TTL, Internet Address, IP Protocol, and Services to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="d122d-123">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="d122d-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="d122d-124">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="d122d-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="d122d-125">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="d122d-125">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d122d-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d122d-126">Properties</span></span>

<span data-ttu-id="d122d-127">A classe **MicrosoftDNS \_ WKSType** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d122d-127">The **MicrosoftDNS\_WKSType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d122d-128">**InternetAddress**</span><span class="sxs-lookup"><span data-stu-id="d122d-128">**InternetAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d122d-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d122d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d122d-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d122d-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d122d-131">Endereço IP da Internet para o proprietário do registro.</span><span class="sxs-lookup"><span data-stu-id="d122d-131">Internet IP address for the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="d122d-132">**IPProtocol**</span><span class="sxs-lookup"><span data-stu-id="d122d-132">**IPProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d122d-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d122d-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d122d-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d122d-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d122d-135">Cadeia de caracteres que representa o protocolo IP para este registro.</span><span class="sxs-lookup"><span data-stu-id="d122d-135">String representing the IP protocol for this record.</span></span> <span data-ttu-id="d122d-136">Os valores válidos são UDP ou TCP.</span><span class="sxs-lookup"><span data-stu-id="d122d-136">Valid values are UDP or TCP.</span></span>

</dd> <dt>

<span data-ttu-id="d122d-137">**Serviços**</span><span class="sxs-lookup"><span data-stu-id="d122d-137">**Services**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d122d-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d122d-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d122d-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d122d-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d122d-140">Cadeia de caracteres que contém todos os serviços usados pelo registro WKS (serviço bem conhecido).</span><span class="sxs-lookup"><span data-stu-id="d122d-140">String containing all services used by the Well Known Service (WKS) record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d122d-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d122d-141">Requirements</span></span>



| <span data-ttu-id="d122d-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="d122d-142">Requirement</span></span> | <span data-ttu-id="d122d-143">Valor</span><span class="sxs-lookup"><span data-stu-id="d122d-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d122d-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d122d-144">Minimum supported client</span></span><br/> | <span data-ttu-id="d122d-145">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d122d-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d122d-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d122d-146">Minimum supported server</span></span><br/> | <span data-ttu-id="d122d-147">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d122d-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d122d-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="d122d-148">Namespace</span></span><br/>                | <span data-ttu-id="d122d-149">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="d122d-149">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d122d-150">MOF</span><span class="sxs-lookup"><span data-stu-id="d122d-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d122d-151"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d122d-151"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d122d-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="d122d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d122d-153">**Método CreateInstanceFromPropertyData da \_ classe WKSType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="d122d-153">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="d122d-154">**Método Modify da classe MicrosoftDNS \_ WKSType**</span><span class="sxs-lookup"><span data-stu-id="d122d-154">**Modify Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-modify.md)
</dt> <dt>

[<span data-ttu-id="d122d-155">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="d122d-155">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





