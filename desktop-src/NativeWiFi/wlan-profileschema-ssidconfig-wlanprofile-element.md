---
description: Contém um ou mais SSIDs para LANs sem fio.
ms.assetid: f9c46db8-2933-48e1-8cb3-effeb13c43ed
title: Elemento SSIDConfig (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSIDConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5665b385c3264ff9d36e79ad671c8f9e8377d4bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828699"
---
# <a name="ssidconfig-wlanprofile-element"></a><span data-ttu-id="6f6cc-103">Elemento SSIDConfig (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="6f6cc-103">SSIDConfig (WLANProfile) Element</span></span>

<span data-ttu-id="6f6cc-104">O elemento SSIDConfig (WLANProfile) contém um ou mais SSIDs para LANs sem fio.</span><span class="sxs-lookup"><span data-stu-id="6f6cc-104">The SSIDConfig (WLANProfile) element contains one or more SSIDs for wireless LANs.</span></span>

``` syntax
<xs:element name="SSIDConfig"
    maxOccurs="256"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="SSID"
                maxOccurs="256"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="hex"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:minLength
                                        value="1"
                                     />
                                    <xs:maxLength
                                        value="32"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="name"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:minLength
                                        value="1"
                                     />
                                    <xs:maxLength
                                        value="32"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="nonBroadcast"
                type="boolean"
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

<span data-ttu-id="6f6cc-105">O elemento **SSIDConfig** é definido pelo elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6f6cc-105">The **SSIDConfig** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6f6cc-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6f6cc-106">Child elements</span></span>



| <span data-ttu-id="6f6cc-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="6f6cc-107">Element</span></span>                                                                    | <span data-ttu-id="6f6cc-108">Type</span><span class="sxs-lookup"><span data-stu-id="6f6cc-108">Type</span></span>                                                              | <span data-ttu-id="6f6cc-109">Description</span><span class="sxs-lookup"><span data-stu-id="6f6cc-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f6cc-110">**hex**</span><span class="sxs-lookup"><span data-stu-id="6f6cc-110">**hex**</span></span>](wlan-profileschema-hex-ssid-element.md)                         |                                                                   | <span data-ttu-id="6f6cc-111">Contém o SSID de uma LAN sem fio em formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="6f6cc-111">Contains the SSID of a wireless LAN in hexadecimal format.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="6f6cc-112">**nomes**</span><span class="sxs-lookup"><span data-stu-id="6f6cc-112">**name**</span></span>](wlan-profileschema-name-ssid-element.md)                       |                                                                   | <span data-ttu-id="6f6cc-113">Contém o nome (diferencia maiúsculas de minúsculas) do SSID de uma LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="6f6cc-113">Contains the (case-sensitive) name of the SSID of a wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="6f6cc-114">**sem difusão**</span><span class="sxs-lookup"><span data-stu-id="6f6cc-114">**nonBroadcast**</span></span>](wlan-profileschema-nonbroadcast-ssidconfig-element.md) | [<span data-ttu-id="6f6cc-115">booleano</span><span class="sxs-lookup"><span data-stu-id="6f6cc-115">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="6f6cc-116">Indica se a rede transmite seu SSID.</span><span class="sxs-lookup"><span data-stu-id="6f6cc-116">Indicates whether the network broadcasts its SSID.</span></span><br/> <span data-ttu-id="6f6cc-117">Se [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) for definido como ESS, esse valor poderá ser **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="6f6cc-117">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to ESS, this value can be either **TRUE** or **FALSE**.</span></span> <span data-ttu-id="6f6cc-118">O valor padrão será **true** se esse elemento estiver ausente.</span><span class="sxs-lookup"><span data-stu-id="6f6cc-118">The default value is **TRUE** if this element is absent.</span></span><br/> <span data-ttu-id="6f6cc-119">Se [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) for definido como IBSS, esse valor deverá ser **false**.</span><span class="sxs-lookup"><span data-stu-id="6f6cc-119">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to IBSS, this value must be **FALSE**.</span></span><br/> <span data-ttu-id="6f6cc-120">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="6f6cc-120">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/> |
| [<span data-ttu-id="6f6cc-121">**SSID**</span><span class="sxs-lookup"><span data-stu-id="6f6cc-121">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)                 |                                                                   | <span data-ttu-id="6f6cc-122">Contém um SSID para uma LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="6f6cc-122">Contains an SSID for a wireless LAN.</span></span><br/> <span data-ttu-id="6f6cc-123">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** No máximo um elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) pode aparecer em um perfil.</span><span class="sxs-lookup"><span data-stu-id="6f6cc-123">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** At most one [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element can appear in a profile.</span></span><br/>                                                                                                                                                                                                                                                                                                        |



## <a name="examples"></a><span data-ttu-id="6f6cc-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6f6cc-124">Examples</span></span>

<span data-ttu-id="6f6cc-125">Para exibir perfis de exemplo que usam o elemento **SSIDConfig** , consulte [amostras de perfil sem fio](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="6f6cc-125">To view sample profiles that use the **SSIDConfig** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f6cc-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f6cc-126">Requirements</span></span>



| <span data-ttu-id="6f6cc-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f6cc-127">Requirement</span></span> | <span data-ttu-id="6f6cc-128">Valor</span><span class="sxs-lookup"><span data-stu-id="6f6cc-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6f6cc-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f6cc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6f6cc-130">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="6f6cc-130">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6f6cc-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f6cc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6f6cc-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6f6cc-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="6f6cc-133">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="6f6cc-133">Redistributable</span></span><br/>          | <span data-ttu-id="6f6cc-134">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="6f6cc-134">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="6f6cc-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f6cc-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="6f6cc-136">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="6f6cc-136">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6f6cc-137">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="6f6cc-137">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="6f6cc-138">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="6f6cc-138">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6f6cc-139">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="6f6cc-139">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
