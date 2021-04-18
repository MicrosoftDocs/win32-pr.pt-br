---
description: Um ponto de extremidade de comunicação que pode se conectar a uma LAN para enviar e receber quadros de dados. Os pontos de extremidade de LAN incluem as interfaces Ethernet, token ring e FDDI.
ms.assetid: c69464cf-00a9-476d-a494-2d7d65776334
title: Classe CIM_LANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LANEndpoint
- CIM_LANEndpoint.LANID
- CIM_LANEndpoint.LANType
- CIM_LANEndpoint.OtherLANType
- CIM_LANEndpoint.MACAddress
- CIM_LANEndpoint.AliasAddresses
- CIM_LANEndpoint.GroupAddresses
- CIM_LANEndpoint.MaxDataSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c924d175cb48e53346daff59a6317a4a0f241f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780983"
---
# <a name="cim_lanendpoint-class"></a><span data-ttu-id="95352-104">\_Classe CIM LANEndpoint</span><span class="sxs-lookup"><span data-stu-id="95352-104">CIM\_LANEndpoint class</span></span>

<span data-ttu-id="95352-105">Um ponto de extremidade de comunicação que pode se conectar a uma LAN para enviar e receber quadros de dados.</span><span class="sxs-lookup"><span data-stu-id="95352-105">A communication endpoint that can connect to a LAN to send and receive data frames.</span></span> <span data-ttu-id="95352-106">Os pontos de extremidade de LAN incluem as interfaces Ethernet, token ring e FDDI.</span><span class="sxs-lookup"><span data-stu-id="95352-106">LAN endpoints include ethernet, token Ring, and FDDI interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="95352-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95352-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints"), AMENDMENT]
class CIM_LANEndpoint : CIM_ProtocolEndpoint
{
  string LANID;
  uint16 LANType;
  string OtherLANType;
  string MACAddress;
  string AliasAddresses[];
  string GroupAddresses[];
  uint32 MaxDataSize;
};
```

## <a name="members"></a><span data-ttu-id="95352-108">Membros</span><span class="sxs-lookup"><span data-stu-id="95352-108">Members</span></span>

<span data-ttu-id="95352-109">A classe **CIM \_ LANEndpoint** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="95352-109">The **CIM\_LANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="95352-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="95352-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="95352-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="95352-111">Properties</span></span>

<span data-ttu-id="95352-112">A classe **CIM \_ LANEndpoint** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="95352-112">The **CIM\_LANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="95352-113">**AliasAddresses**</span><span class="sxs-lookup"><span data-stu-id="95352-113">**AliasAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95352-114">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="95352-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="95352-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="95352-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95352-116">Uma matriz que contém outros endereços unicast que podem ser usados para se comunicar com o ponto de extremidade da LAN.</span><span class="sxs-lookup"><span data-stu-id="95352-116">An array that contains other unicast addresses that may be used to communicate with the LAN endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="95352-117">**GroupAddresses**</span><span class="sxs-lookup"><span data-stu-id="95352-117">**GroupAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95352-118">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="95352-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="95352-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="95352-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95352-120">Uma matriz que contém os endereços multicast para os quais o ponto de extremidade de LAN escuta.</span><span class="sxs-lookup"><span data-stu-id="95352-120">An array that contains the multicast addresses to which the LAN endpoint listens.</span></span>

</dd> <dt>

<span data-ttu-id="95352-121">**LANID**</span><span class="sxs-lookup"><span data-stu-id="95352-121">**LANID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95352-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="95352-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95352-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="95352-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95352-124">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ LANConnectivitySegment. LANID, CIM \_ LANSegment. LANID")</span><span class="sxs-lookup"><span data-stu-id="95352-124">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_LANConnectivitySegment.LANID, CIM\_LANSegment.LANID")</span></span>
</dt> </dl>

<span data-ttu-id="95352-125">Um rótulo ou identificador para o segmento de LAN ao qual o ponto de extremidade está conectado.</span><span class="sxs-lookup"><span data-stu-id="95352-125">A label or identifier for the LAN segment to which the endpoint is connected.</span></span> <span data-ttu-id="95352-126">Se o ponto de extremidade não estiver conectado no momento ou se essas informações forem desconhecidas, **LANID** será NULL.</span><span class="sxs-lookup"><span data-stu-id="95352-126">If the endpoint is not currently connected or if this information is unknown, then **LANID** is NULL.</span></span>

</dd> <dt>

<span data-ttu-id="95352-127">**LANType**</span><span class="sxs-lookup"><span data-stu-id="95352-127">**LANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95352-128">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95352-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="95352-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="95352-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95352-130">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md).**ProtocolType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ LANConnectivitySegment. connectivitytype, CIM \_ LANSegment. LANType ")</span><span class="sxs-lookup"><span data-stu-id="95352-130">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md).**ProtocolType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_LANConnectivitySegment.ConnectivityType, CIM\_LANSegment.LANType")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="95352-131">Descrição preterida: o tipo de tecnologia usado na LAN.</span><span class="sxs-lookup"><span data-stu-id="95352-131">Deprecated description: The kind of technology used on the LAN.</span></span>

 

<span data-ttu-id="95352-132">Essa propriedade é preterida.</span><span class="sxs-lookup"><span data-stu-id="95352-132">This property is deprecated.</span></span> <span data-ttu-id="95352-133">Em vez disso, recomendamos que você use a propriedade **ProtocolType** .</span><span class="sxs-lookup"><span data-stu-id="95352-133">Instead we recommend that you use the **ProtocolType** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="95352-134">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="95352-134">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="95352-135">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="95352-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="95352-136">**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="95352-136">**Ethernet** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TokenRing"></span><span id="tokenring"></span><span id="TOKENRING"></span>

<span data-ttu-id="95352-137">**Tokenring** (3)</span><span class="sxs-lookup"><span data-stu-id="95352-137">**TokenRing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="95352-138">**FDDI** (4)</span><span class="sxs-lookup"><span data-stu-id="95352-138">**FDDI** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="95352-139">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="95352-139">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95352-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="95352-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95352-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="95352-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95352-142">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (12)</span><span class="sxs-lookup"><span data-stu-id="95352-142">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12)</span></span>
</dt> </dl>

<span data-ttu-id="95352-143">O endereço unicast principal usado pelo ponto de extremidade da LAN.</span><span class="sxs-lookup"><span data-stu-id="95352-143">The principal unicast address used by the LAN endpoint.</span></span>

<span data-ttu-id="95352-144">O endereço MAC deve ser formatado com as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="95352-144">The MAC address must be formatted with the following characteristics:</span></span>

-   <span data-ttu-id="95352-145">O endereço consiste em doze dígitos hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="95352-145">The address consists of twelve hexadecimal digits.</span></span>
-   <span data-ttu-id="95352-146">Cada par de dígitos representa um dos seis octetos do endereço MAC.</span><span class="sxs-lookup"><span data-stu-id="95352-146">Each pair of digits represents one of the six octets of the MAC address.</span></span>
-   <span data-ttu-id="95352-147">Cada par de dígitos deve estar em ordem de bits canônica de acordo com a RFC 2469.</span><span class="sxs-lookup"><span data-stu-id="95352-147">Each pair of digits must be in canonical bit order according to RFC 2469.</span></span>

</dd> <dt>

<span data-ttu-id="95352-148">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="95352-148">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95352-149">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="95352-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="95352-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="95352-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95352-151">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="95352-151">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")</span></span>
</dt> </dl>

<span data-ttu-id="95352-152">O tamanho máximo, em bytes, dos campos de dados enviados ou recebidos pelo ponto de extremidade da LAN.</span><span class="sxs-lookup"><span data-stu-id="95352-152">The maximum size, in bytes, of data fields sent or received by the LAN endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="95352-153">**OtherLANType**</span><span class="sxs-lookup"><span data-stu-id="95352-153">**OtherLANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95352-154">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="95352-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95352-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="95352-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95352-156">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md).**OtherTypeDescription**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ LANConnectivitySegment. OtherTypeDescription ","**CIM \_ LANEndpoint**.**LANType**")</span><span class="sxs-lookup"><span data-stu-id="95352-156">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md).**OtherTypeDescription**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_LANConnectivitySegment.OtherTypeDescription", "**CIM\_LANEndpoint**.**LANType**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="95352-157">Descrição preterida: o tipo de tecnologia usado na LAN quando a propriedade **LANType** é definida como "1" (outra).</span><span class="sxs-lookup"><span data-stu-id="95352-157">Deprecated description: The type of technology used on the LAN when the **LANType** property is set to "1" (Other).</span></span>

 

<span data-ttu-id="95352-158">Essa propriedade é preterida.</span><span class="sxs-lookup"><span data-stu-id="95352-158">This property is deprecated.</span></span> <span data-ttu-id="95352-159">Em vez disso, recomendamos que você use a propriedade **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="95352-159">Instead we recommend that you use the **OtherTypeDescription** property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="95352-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95352-160">Requirements</span></span>



| <span data-ttu-id="95352-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="95352-161">Requirement</span></span> | <span data-ttu-id="95352-162">Valor</span><span class="sxs-lookup"><span data-stu-id="95352-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95352-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95352-163">Minimum supported client</span></span><br/> | <span data-ttu-id="95352-164">Windows 8</span><span class="sxs-lookup"><span data-stu-id="95352-164">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="95352-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95352-165">Minimum supported server</span></span><br/> | <span data-ttu-id="95352-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="95352-166">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="95352-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="95352-167">Namespace</span></span><br/>                | <span data-ttu-id="95352-168">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="95352-168">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="95352-169">MOF</span><span class="sxs-lookup"><span data-stu-id="95352-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95352-170"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="95352-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="95352-171">DLL</span><span class="sxs-lookup"><span data-stu-id="95352-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95352-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="95352-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="95352-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="95352-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95352-174">**CIM \_ ProtocolEndpoint**</span><span class="sxs-lookup"><span data-stu-id="95352-174">**CIM\_ProtocolEndpoint**</span></span>](cim-protocolendpoint.md)
</dt> </dl>

 

