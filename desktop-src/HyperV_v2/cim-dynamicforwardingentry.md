---
description: Representa uma entrada no banco de dados de encaminhamento associado à \_ classe CIM TransparentBridgingService.
ms.assetid: 4c3afe7c-f7e5-4a83-8ba1-f0b1909cee52
title: Classe CIM_DynamicForwardingEntry
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DynamicForwardingEntry
- CIM_DynamicForwardingEntry.SystemCreationClassName
- CIM_DynamicForwardingEntry.SystemName
- CIM_DynamicForwardingEntry.ServiceCreationClassName
- CIM_DynamicForwardingEntry.ServiceName
- CIM_DynamicForwardingEntry.CreationClassName
- CIM_DynamicForwardingEntry.MACAddress
- CIM_DynamicForwardingEntry.DynamicStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65cf4f1bc5e678089d54dd99a09a6d3b7aeb3dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759252"
---
# <a name="cim_dynamicforwardingentry-class"></a><span data-ttu-id="11870-103">\_Classe CIM DynamicForwardingEntry</span><span class="sxs-lookup"><span data-stu-id="11870-103">CIM\_DynamicForwardingEntry class</span></span>

<span data-ttu-id="11870-104">Representa uma entrada no banco de dados de encaminhamento associado à classe [**CIM \_ TransparentBridgingService**](cim-transparentbridgingservice.md) .</span><span class="sxs-lookup"><span data-stu-id="11870-104">Represents an entry in the forwarding database associated with the [**CIM\_TransparentBridgingService**](cim-transparentbridgingservice.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="11870-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11870-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_DynamicForwardingEntry : CIM_LogicalElement
{
  string SystemCreationClassName;
  string SystemName;
  string ServiceCreationClassName;
  string ServiceName;
  string CreationClassName;
  string MACAddress;
  uint16 DynamicStatus;
};
```

## <a name="members"></a><span data-ttu-id="11870-106">Membros</span><span class="sxs-lookup"><span data-stu-id="11870-106">Members</span></span>

<span data-ttu-id="11870-107">A classe **CIM \_ DynamicForwardingEntry** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="11870-107">The **CIM\_DynamicForwardingEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="11870-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="11870-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="11870-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="11870-109">Properties</span></span>

<span data-ttu-id="11870-110">A classe **CIM \_ DynamicForwardingEntry** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="11870-110">The **CIM\_DynamicForwardingEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="11870-111">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="11870-111">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11870-112">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="11870-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11870-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11870-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11870-114">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="11870-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="11870-115">O nome da classe ou da subclasse usada para criar a instância.</span><span class="sxs-lookup"><span data-stu-id="11870-115">The name of the class or the subclass used to create the instance.</span></span> <span data-ttu-id="11870-116">Quando usado com as outras propriedades de chave dessa classe, essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="11870-116">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="11870-117">**DynamicStatus**</span><span class="sxs-lookup"><span data-stu-id="11870-117">**DynamicStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11870-118">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="11870-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="11870-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11870-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11870-120">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dTpFdbStatus ")</span><span class="sxs-lookup"><span data-stu-id="11870-120">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpFdbStatus")</span></span>
</dt> </dl>

<span data-ttu-id="11870-121">O status da entrada.</span><span class="sxs-lookup"><span data-stu-id="11870-121">The status of the entry.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="11870-122">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="11870-122">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>

<span data-ttu-id="11870-123">**Inválido** (2)</span><span class="sxs-lookup"><span data-stu-id="11870-123">**Invalid** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>

<span data-ttu-id="11870-124">**Aprendido** (3)</span><span class="sxs-lookup"><span data-stu-id="11870-124">**Learned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Self"></span><span id="self"></span><span id="SELF"></span>

<span data-ttu-id="11870-125">Por **conta própria** (4)</span><span class="sxs-lookup"><span data-stu-id="11870-125">**Self** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>

<span data-ttu-id="11870-126">**Gerenciamento** (5)</span><span class="sxs-lookup"><span data-stu-id="11870-126">**Mgmt** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="11870-127">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="11870-127">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11870-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="11870-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11870-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11870-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11870-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (12), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dTpFdbAddress ")</span><span class="sxs-lookup"><span data-stu-id="11870-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpFdbAddress")</span></span>
</dt> </dl>

<span data-ttu-id="11870-131">O endereço MAC unicast para o qual o serviço de ponte filtra informações.</span><span class="sxs-lookup"><span data-stu-id="11870-131">The Unicast MAC address for which the bridging service filters information.</span></span> <span data-ttu-id="11870-132">O endereço MAC é formatado como doze dígitos hexadecimais, como 010203040506, com cada par que representa um dos seis octetos do endereço MAC na ordem de bits canônica de acordo com a RFC 2469.</span><span class="sxs-lookup"><span data-stu-id="11870-132">The MAC address is formatted as twelve hexadecimal digits, such as 010203040506, with each pair representing one of the six octets of the MAC address in canonical bit order according to RFC 2469.</span></span>

</dd> <dt>

<span data-ttu-id="11870-133">**ServiceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="11870-133">**ServiceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11870-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="11870-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11870-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11870-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11870-136">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ serviço CIM**](cim-service.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="11870-136">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Service**](cim-service.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="11870-137">O valor de **CreationClassName** do objeto de serviço de escopo.</span><span class="sxs-lookup"><span data-stu-id="11870-137">The **CreationClassName** value of the scoping service object.</span></span>

</dd> <dt>

<span data-ttu-id="11870-138">**ServiceName**</span><span class="sxs-lookup"><span data-stu-id="11870-138">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11870-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="11870-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11870-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11870-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11870-141">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ serviço CIM**](cim-service.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="11870-141">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Service**](cim-service.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="11870-142">O nome do serviço de escopo.</span><span class="sxs-lookup"><span data-stu-id="11870-142">The name of the scoping service.</span></span>

</dd> <dt>

<span data-ttu-id="11870-143">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="11870-143">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11870-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="11870-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11870-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11870-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11870-146">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="11870-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="11870-147">O valor de **CreationClassName** do objeto do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="11870-147">The **CreationClassName** value of the scoping system object.</span></span>

</dd> <dt>

<span data-ttu-id="11870-148">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="11870-148">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11870-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="11870-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11870-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11870-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11870-151">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="11870-151">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="11870-152">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="11870-152">The name of the scoping system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11870-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11870-153">Requirements</span></span>



| <span data-ttu-id="11870-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="11870-154">Requirement</span></span> | <span data-ttu-id="11870-155">Valor</span><span class="sxs-lookup"><span data-stu-id="11870-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11870-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11870-156">Minimum supported client</span></span><br/> | <span data-ttu-id="11870-157">Windows 8</span><span class="sxs-lookup"><span data-stu-id="11870-157">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="11870-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11870-158">Minimum supported server</span></span><br/> | <span data-ttu-id="11870-159">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="11870-159">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="11870-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="11870-160">Namespace</span></span><br/>                | <span data-ttu-id="11870-161">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="11870-161">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="11870-162">MOF</span><span class="sxs-lookup"><span data-stu-id="11870-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11870-163"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11870-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="11870-164">DLL</span><span class="sxs-lookup"><span data-stu-id="11870-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11870-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="11870-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="11870-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="11870-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11870-167">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="11870-167">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

