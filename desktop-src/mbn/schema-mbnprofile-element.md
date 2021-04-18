---
description: É o elemento raiz que identifica um perfil de banda larga móvel.
ms.assetid: 08302e7f-3024-439b-a2ad-a4ae9487b82b
title: Elemento MBNProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MBNProfile
api_type:
- Schema
ms.openlocfilehash: 7016d492a70192a7d6accdcb3aaa57a9c564960e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785243"
---
# <a name="mbnprofile-element"></a><span data-ttu-id="57ee2-103">Elemento MBNProfile</span><span class="sxs-lookup"><span data-stu-id="57ee2-103">MBNProfile Element</span></span>

<span data-ttu-id="57ee2-104">O elemento **MBNProfile** é o elemento raiz que identifica um perfil de banda larga móvel.</span><span class="sxs-lookup"><span data-stu-id="57ee2-104">The **MBNProfile** element is the root element that identifies a Mobile Broadband profile.</span></span>

<span data-ttu-id="57ee2-105">Só pode haver um elemento desse tipo por documento.</span><span class="sxs-lookup"><span data-stu-id="57ee2-105">There can only be one element of this type per document.</span></span>

``` syntax
<xs:element name="MBNProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Name"
                type="nameType"
             />
            <xs:element name="Description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="ICONFilePath"
                type="iconFileType"
                minOccurs="0"
             />
            <xs:element name="IsDefault"
                type="boolean"
             />
            <xs:element name="ProfileCreationType"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="token"
                    >
                        <xs:enumeration
                            value="UserProvisioned"
                         />
                        <xs:enumeration
                            value="AdminProvisioned"
                         />
                        <xs:enumeration
                            value="OperatorProvisioned"
                         />
                        <xs:enumeration
                            value="DeviceProvisioned"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="SubscriberID"
                type="subscriberIdType"
             />
            <xs:element name="SimIccID"
                type="simIccIDType"
                minOccurs="0"
             />
            <xs:element name="HomeProviderName"
                type="providerNameType"
                minOccurs="0"
             />
            <xs:element name="AutoConnectOnInternet"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="ConnectionMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="manual"
                         />
                        <xs:enumeration
                            value="auto"
                         />
                        <xs:enumeration
                            value="auto-home"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="Context"
                type="contextType"
                minOccurs="0"
             />
            <xs:element name="DataRoamingPartners"
                minOccurs="0"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="57ee2-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="57ee2-106">Child elements</span></span>



| <span data-ttu-id="57ee2-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="57ee2-107">Element</span></span>                                                                          | <span data-ttu-id="57ee2-108">Type</span><span class="sxs-lookup"><span data-stu-id="57ee2-108">Type</span></span>                                                           | <span data-ttu-id="57ee2-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="57ee2-109">Description</span></span>                                               |
|----------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="57ee2-110">**AutoConnectOnInternet**</span><span class="sxs-lookup"><span data-stu-id="57ee2-110">**AutoConnectOnInternet**</span></span>](schema-autoconnectoninternet-mbnprofile-element.md) | <span data-ttu-id="57ee2-111">booleano</span><span class="sxs-lookup"><span data-stu-id="57ee2-111">boolean</span></span>                                                        | <span data-ttu-id="57ee2-112">Se o dispositivo será conectado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="57ee2-112">Whether the device will automatically connect.</span></span><br/> |
| [<span data-ttu-id="57ee2-113">**ConnectionMode**</span><span class="sxs-lookup"><span data-stu-id="57ee2-113">**ConnectionMode**</span></span>](schema-connectionmode-mbnprofile-element.md)               |                                                                | <span data-ttu-id="57ee2-114">As configurações de conexão automática do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57ee2-114">The device auto connection settings.</span></span><br/>           |
| [<span data-ttu-id="57ee2-115">**Contexto**</span><span class="sxs-lookup"><span data-stu-id="57ee2-115">**Context**</span></span>](schema-context-mbnprofile-element.md)                             | [<span data-ttu-id="57ee2-116">**contextType**</span><span class="sxs-lookup"><span data-stu-id="57ee2-116">**contextType**</span></span>](schema-contexttype-complextype.md)          | <span data-ttu-id="57ee2-117">Parâmetros de configuração de conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="57ee2-117">Data connection setup parameters.</span></span><br/>              |
| [<span data-ttu-id="57ee2-118">**DataRoamingPartners**</span><span class="sxs-lookup"><span data-stu-id="57ee2-118">**DataRoamingPartners**</span></span>](schema-dataroamingpartners-mbnprofile-element.md)     |                                                                | <span data-ttu-id="57ee2-119">Provedores de rede preferenciais para roaming.</span><span class="sxs-lookup"><span data-stu-id="57ee2-119">Preferred network providers for roaming.</span></span><br/>       |
| [<span data-ttu-id="57ee2-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="57ee2-120">**Description**</span></span>](schema-description-mbnprofile-element.md)                     | [<span data-ttu-id="57ee2-121">**nometype**</span><span class="sxs-lookup"><span data-stu-id="57ee2-121">**nameType**</span></span>](schema-nametype-simpletype.md)                 | <span data-ttu-id="57ee2-122">Descrição do perfil.</span><span class="sxs-lookup"><span data-stu-id="57ee2-122">Description of the profile.</span></span><br/>                    |
| [<span data-ttu-id="57ee2-123">**HomeProviderName**</span><span class="sxs-lookup"><span data-stu-id="57ee2-123">**HomeProviderName**</span></span>](schema-homeprovidername-mbnprofile-element.md)           | [<span data-ttu-id="57ee2-124">**providerNametype**</span><span class="sxs-lookup"><span data-stu-id="57ee2-124">**providerNameType**</span></span>](schema-providernametype-simpletype.md) | <span data-ttu-id="57ee2-125">Nome do provedor de início.</span><span class="sxs-lookup"><span data-stu-id="57ee2-125">Name of the home provider.</span></span><br/>                     |
| [<span data-ttu-id="57ee2-126">**ICONFilePath**</span><span class="sxs-lookup"><span data-stu-id="57ee2-126">**ICONFilePath**</span></span>](schema-iconfilepath-mbnprofile-element.md)                   | [<span data-ttu-id="57ee2-127">**iconFileType**</span><span class="sxs-lookup"><span data-stu-id="57ee2-127">**iconFileType**</span></span>](schema-iconfiletype-simpletype.md)         | <span data-ttu-id="57ee2-128">Caminho para o arquivo de ícone.</span><span class="sxs-lookup"><span data-stu-id="57ee2-128">Path to the icon file.</span></span><br/>                         |
| [<span data-ttu-id="57ee2-129">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="57ee2-129">**IsDefault**</span></span>](schema-isdefault-mbnprofile-element.md)                         | <span data-ttu-id="57ee2-130">booleano</span><span class="sxs-lookup"><span data-stu-id="57ee2-130">boolean</span></span>                                                        | <span data-ttu-id="57ee2-131">Se o perfil é o padrão.</span><span class="sxs-lookup"><span data-stu-id="57ee2-131">Whether the profile is the default.</span></span><br/>            |
| [<span data-ttu-id="57ee2-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="57ee2-132">**Name**</span></span>](schema-name-mbnprofile-element.md)                                   | [<span data-ttu-id="57ee2-133">**nometype**</span><span class="sxs-lookup"><span data-stu-id="57ee2-133">**nameType**</span></span>](schema-nametype-simpletype.md)                 | <span data-ttu-id="57ee2-134">Nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="57ee2-134">Name of the profile.</span></span><br/>                           |
| [<span data-ttu-id="57ee2-135">**ProfileCreationType**</span><span class="sxs-lookup"><span data-stu-id="57ee2-135">**ProfileCreationType**</span></span>](schema-profilecreationtype-mbnprofile-element.md)     |                                                                | <span data-ttu-id="57ee2-136">Informações sobre o criador do perfil.</span><span class="sxs-lookup"><span data-stu-id="57ee2-136">Information about the profile creator.</span></span><br/>         |
| [<span data-ttu-id="57ee2-137">**SimIccID**</span><span class="sxs-lookup"><span data-stu-id="57ee2-137">**SimIccID**</span></span>](schema-simiccid-mbnprofile-element.md)                           | [<span data-ttu-id="57ee2-138">**simIccIDType**</span><span class="sxs-lookup"><span data-stu-id="57ee2-138">**simIccIDType**</span></span>](schema-simiccidtype-simpletype.md)         | <span data-ttu-id="57ee2-139">Número de identificação do SIM para dispositivos GSM.</span><span class="sxs-lookup"><span data-stu-id="57ee2-139">SIM identification number for GSM devices.</span></span><br/>     |
| [<span data-ttu-id="57ee2-140">**Subscriberid**</span><span class="sxs-lookup"><span data-stu-id="57ee2-140">**SubscriberID**</span></span>](schema-subscriberid-mbnprofile-element.md)                   | [<span data-ttu-id="57ee2-141">**subscriberIdType**</span><span class="sxs-lookup"><span data-stu-id="57ee2-141">**subscriberIdType**</span></span>](schema-subscriberidtype-simpletype.md) | <span data-ttu-id="57ee2-142">Identificador exclusivo do perfil.</span><span class="sxs-lookup"><span data-stu-id="57ee2-142">Unique identifier of the profile.</span></span><br/>              |



## <a name="requirements"></a><span data-ttu-id="57ee2-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57ee2-143">Requirements</span></span>



| <span data-ttu-id="57ee2-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="57ee2-144">Requirement</span></span> | <span data-ttu-id="57ee2-145">Valor</span><span class="sxs-lookup"><span data-stu-id="57ee2-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="57ee2-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57ee2-146">Minimum supported client</span></span><br/> | <span data-ttu-id="57ee2-147">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="57ee2-147">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="57ee2-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57ee2-148">Minimum supported server</span></span><br/> | <span data-ttu-id="57ee2-149">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="57ee2-149">None supported</span></span><br/>                         |



 

 




