---
title: Classe MicrosoftDNS_AFSDBType
description: Subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro AFSDB (servidor de banco de dados do sistema de arquivos Andrew).
ms.assetid: 536f4df7-bd01-458b-b8f1-36f066e9ca04
keywords:
- MicrosoftDNS_AFSDBType de classe de DNS
- MicrosoftDNS_AFSDBType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType
- MicrosoftDNS_AFSDBType.CreateInstanceFromPropertyData
- MicrosoftDNS_AFSDBType.Modify
- MicrosoftDNS_AFSDBType.Subtype
- MicrosoftDNS_AFSDBType.ServerName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 836de50f4da9e613fb3e940b90971f38a634c804
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009384"
---
# <a name="microsoftdns_afsdbtype-class"></a><span data-ttu-id="63be1-105">\_Classe MicrosoftDNS AFSDBType</span><span class="sxs-lookup"><span data-stu-id="63be1-105">MicrosoftDNS\_AFSDBType class</span></span>

<span data-ttu-id="63be1-106">Subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro AFSDB (servidor de banco de dados do sistema de arquivos Andrew).</span><span class="sxs-lookup"><span data-stu-id="63be1-106">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an Andrew File System Database Server (AFSDB) record.</span></span>

<span data-ttu-id="63be1-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="63be1-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="63be1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63be1-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_AFSDBType : MicrosoftDNS_ResourceRecord
{
  uint16 Subtype;
  string ServerName;
};
```

## <a name="members"></a><span data-ttu-id="63be1-109">Membros</span><span class="sxs-lookup"><span data-stu-id="63be1-109">Members</span></span>

<span data-ttu-id="63be1-110">A classe **MicrosoftDNS \_ AFSDBType** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="63be1-110">The **MicrosoftDNS\_AFSDBType** class has these types of members:</span></span>

-   [<span data-ttu-id="63be1-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="63be1-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="63be1-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="63be1-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="63be1-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="63be1-113">Methods</span></span>

<span data-ttu-id="63be1-114">A classe **MicrosoftDNS \_ AFSDBType** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="63be1-114">The **MicrosoftDNS\_AFSDBType** class has these methods.</span></span>



| <span data-ttu-id="63be1-115">Método</span><span class="sxs-lookup"><span data-stu-id="63be1-115">Method</span></span>                             | <span data-ttu-id="63be1-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="63be1-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63be1-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="63be1-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="63be1-118">Cria uma instância de um registro de recurso AFSDB com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário/da célula, a classe (padrão = IN), o valor de vida útil e o subtipo e o nome do servidor AFS do host.</span><span class="sxs-lookup"><span data-stu-id="63be1-118">Instantiates an AFSDB Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/Cell Name, class (default = IN), time-to-live value, and host AFS server subtype and name.</span></span> <span data-ttu-id="63be1-119">Retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="63be1-119">Returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="63be1-120">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="63be1-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="63be1-121">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="63be1-121">**Modify**</span></span>                         | <span data-ttu-id="63be1-122">Esse método atualiza o TTL, o subtipo e o nome do servidor para os valores especificados como os parâmetros de entrada desse método.</span><span class="sxs-lookup"><span data-stu-id="63be1-122">This method updates the TTL, Subtype and Server Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="63be1-123">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="63be1-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="63be1-124">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="63be1-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="63be1-125">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="63be1-125">Qualifiers: Implemented</span></span><br/>   |



 

### <a name="properties"></a><span data-ttu-id="63be1-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="63be1-126">Properties</span></span>

<span data-ttu-id="63be1-127">A classe **MicrosoftDNS \_ AFSDBType** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="63be1-127">The **MicrosoftDNS\_AFSDBType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="63be1-128">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="63be1-128">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63be1-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="63be1-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63be1-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="63be1-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63be1-131">FQDN que especifica um host que tem um servidor para a célula AFS especificada no nome do proprietário.</span><span class="sxs-lookup"><span data-stu-id="63be1-131">FQDN specifying a host that has a server for the AFS cell specified in the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="63be1-132">**Subtipo**</span><span class="sxs-lookup"><span data-stu-id="63be1-132">**Subtype**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63be1-133">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63be1-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="63be1-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="63be1-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63be1-135">Subtipo do servidor host AFS.</span><span class="sxs-lookup"><span data-stu-id="63be1-135">Subtype of the host AFS server.</span></span> <span data-ttu-id="63be1-136">Para o subtipo 1 (valor = 1), o host tem um servidor de local de volume AFS versão 3,0 para a célula AFS nomeada.</span><span class="sxs-lookup"><span data-stu-id="63be1-136">For subtype 1 (value=1), the host has an AFS version 3.0 Volume Location Server for the named AFS cell.</span></span> <span data-ttu-id="63be1-137">No caso do subtipo 2 (valor = 2), o host tem um servidor de nomes autenticado que contém o nó do diretório raiz da célula para a célula de DCE/NCA nomeada.</span><span class="sxs-lookup"><span data-stu-id="63be1-137">In the case of subtype 2 (value=2), the host has an authenticated name server holding the cell-root directory node for the named DCE/NCA cell.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="63be1-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63be1-138">Requirements</span></span>



| <span data-ttu-id="63be1-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="63be1-139">Requirement</span></span> | <span data-ttu-id="63be1-140">Valor</span><span class="sxs-lookup"><span data-stu-id="63be1-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63be1-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63be1-141">Minimum supported client</span></span><br/> | <span data-ttu-id="63be1-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="63be1-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="63be1-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63be1-143">Minimum supported server</span></span><br/> | <span data-ttu-id="63be1-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="63be1-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="63be1-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="63be1-145">Namespace</span></span><br/>                | <span data-ttu-id="63be1-146">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="63be1-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="63be1-147">MOF</span><span class="sxs-lookup"><span data-stu-id="63be1-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63be1-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63be1-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63be1-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="63be1-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63be1-150">**Método CreateInstanceFromPropertyData da \_ classe AFSDBType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="63be1-150">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="63be1-151">**Método Modify da classe MicrosoftDNS \_ AFSDBType**</span><span class="sxs-lookup"><span data-stu-id="63be1-151">**Modify Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="63be1-152">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="63be1-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





