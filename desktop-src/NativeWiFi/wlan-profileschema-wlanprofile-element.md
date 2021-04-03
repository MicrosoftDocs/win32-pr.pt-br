---
description: Contém um perfil de LAN sem fio.
ms.assetid: bc97cb49-3891-4a4a-aab4-895cd9ce6908
title: Elemento WLANProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLANProfile
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 227d912128bf3f656fca7aecbaf0fe0640659465
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837197"
---
# <a name="wlanprofile-element"></a><span data-ttu-id="7eb6b-103">Elemento WLANProfile</span><span class="sxs-lookup"><span data-stu-id="7eb6b-103">WLANProfile Element</span></span>

<span data-ttu-id="7eb6b-104">O elemento **WLANProfile** contém um perfil de LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-104">The **WLANProfile** element contains a wireless LAN profile.</span></span> <span data-ttu-id="7eb6b-105">Esse é o elemento raiz exclusivo para um perfil sem fio.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-105">This element is the unique root element for a wireless profile.</span></span>

<span data-ttu-id="7eb6b-106">O namespace de destino para o elemento WLANProfile é `https://www.microsoft.com/networking/WLAN/profile/v1` .</span><span class="sxs-lookup"><span data-stu-id="7eb6b-106">The target namespace for the WLANProfile element is `https://www.microsoft.com/networking/WLAN/profile/v1`.</span></span>

``` syntax
<xs:element name="WLANProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
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
            <xs:element name="connectionType">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="IBSS"
                         />
                        <xs:enumeration
                            value="ESS"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="connectionMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="auto"
                         />
                        <xs:enumeration
                            value="manual"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="autoSwitch"
                type="boolean"
                minOccurs="0"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
            <xs:element name="MSM"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="connectivity"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="phyType"
                                        minOccurs="0"
                                        maxOccurs="4"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:enumeration
                                                    value="a"
                                                 />
                                                <xs:enumeration
                                                    value="b"
                                                 />
                                                <xs:enumeration
                                                    value="g"
                                                 />
                                                <xs:enumeration
                                                    value="n"
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
                        <xs:element name="security"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="authEncryption">
                                        <xs:complexType>
                                            <xs:sequence>
                                                <xs:element name="authentication">
                                                    <xs:simpleType>
                                                        <xs:restriction
                                                            base="string"
                                                        >
                                                            <xs:enumeration
                                                                value="open"
                                                             />
                                                            <xs:enumeration
                                                                value="shared"
                                                             />
                                                            <xs:enumeration
                                                                value="WPA"
                                                             />
                                                            <xs:enumeration
                                                                value="WPAPSK"
                                                             />
                                                            <xs:enumeration
                                                                value="WPA2"
                                                             />
                                                            <xs:enumeration
                                                                value="WPA2PSK"
                                                             />
                                                        </xs:restriction>
                                                    </xs:simpleType>
                                                </xs:element>
                                                <xs:element name="encryption">
                                                    <xs:simpleType>
                                                        <xs:restriction
                                                            base="string"
                                                        >
                                                            <xs:enumeration
                                                                value="none"
                                                             />
                                                            <xs:enumeration
                                                                value="WEP"
                                                             />
                                                            <xs:enumeration
                                                                value="TKIP"
                                                             />
                                                            <xs:enumeration
                                                                value="AES"
                                                             />
                                                        </xs:restriction>
                                                    </xs:simpleType>
                                                </xs:element>
                                                <xs:element name="useOneX"
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
                                    <xs:element name="sharedKey"
                                        minOccurs="0"
                                    >
                                        <xs:complexType>
                                            <xs:sequence>
                                                <xs:element name="keyType">
                                                    <xs:simpleType>
                                                        <xs:restriction
                                                            base="string"
                                                        >
                                                            <xs:enumeration
                                                                value="networkKey"
                                                             />
                                                            <xs:enumeration
                                                                value="passPhrase"
                                                             />
                                                        </xs:restriction>
                                                    </xs:simpleType>
                                                </xs:element>
                                                <xs:element name="protected"
                                                    type="boolean"
                                                 />
                                                <xs:element name="keyMaterial"
                                                    type="string"
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
                                    <xs:element name="keyIndex"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="integer"
                                            >
                                                <xs:minInclusive
                                                    value="0"
                                                 />
                                                <xs:maxInclusive
                                                    value="3"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="PMKCacheMode"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:enumeration
                                                    value="disabled"
                                                 />
                                                <xs:enumeration
                                                    value="enabled"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="PMKCacheTTL"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="integer"
                                            >
                                                <xs:minInclusive
                                                    value="5"
                                                 />
                                                <xs:maxInclusive
                                                    value="1400"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="PMKCacheSize"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="integer"
                                            >
                                                <xs:minInclusive
                                                    value="1"
                                                 />
                                                <xs:maxInclusive
                                                    value="255"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="preAuthMode"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:enumeration
                                                    value="disabled"
                                                 />
                                                <xs:enumeration
                                                    value="enabled"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="preAuthThrottle"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="integer"
                                            >
                                                <xs:minInclusive
                                                    value="1"
                                                 />
                                                <xs:maxInclusive
                                                    value="16"
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
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="IHV"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="OUIHeader">
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="OUI">
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="hexBinary"
                                            >
                                                <xs:length
                                                    value="3"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="type">
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="hexBinary"
                                            >
                                                <xs:length
                                                    value="1"
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
                        <xs:element name="connectivity"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:any
                                        processContents="lax"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="security"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:any
                                        processContents="lax"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="useMSOneX"
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

## <a name="child-elements"></a><span data-ttu-id="7eb6b-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7eb6b-107">Child elements</span></span>



| <span data-ttu-id="7eb6b-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="7eb6b-108">Element</span></span>                                                                            | <span data-ttu-id="7eb6b-109">Type</span><span class="sxs-lookup"><span data-stu-id="7eb6b-109">Type</span></span>                                                              | <span data-ttu-id="7eb6b-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="7eb6b-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7eb6b-111">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-111">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)       |                                                                   | <span data-ttu-id="7eb6b-112">Especifica o par de autenticação e criptografia a ser usado para este perfil.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-112">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="7eb6b-113">**Authentication**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-113">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="7eb6b-114">Especifica o método de autenticação a ser usado para se conectar à LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-114">Specifies the authentication method to be used to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="7eb6b-115">**autocomutação**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-115">**autoSwitch**</span></span>](wlan-profileschema-autoswitch-wlanprofile-element.md)            | [<span data-ttu-id="7eb6b-116">booleano</span><span class="sxs-lookup"><span data-stu-id="7eb6b-116">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="7eb6b-117">Determina o comportamento de roaming de uma rede conectada automaticamente quando uma rede preferencial está no intervalo.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-117">Determines the roaming behavior of an auto-connected network when a more preferred network is in range.</span></span> <span data-ttu-id="7eb6b-118">Esse elemento é opcional e não tem nenhum efeito em uma rede conectada manualmente.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-118">This element is optional and has no effect on a manually connected network.</span></span><br/> <span data-ttu-id="7eb6b-119">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-119">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="7eb6b-120">**connectionMode**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-120">**connectionMode**</span></span>](wlan-profileschema-connectionmode-wlanprofile-element.md)    |                                                                   | <span data-ttu-id="7eb6b-121">Indica se a conexão com a LAN sem fio deve ser automática ("automática") ou iniciada ("manual") pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-121">Indicates whether connection to the wireless LAN should be automatic ("auto") or initiated ("manual") by user.</span></span> <span data-ttu-id="7eb6b-122">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-122">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="7eb6b-123">**connectionType**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-123">**connectionType**</span></span>](wlan-profileschema-connectiontype-wlanprofile-element.md)    |                                                                   | <span data-ttu-id="7eb6b-124">Indica se a rede é infraestrutura ("ESS") ou ad-hoc ("IBSS").</span><span class="sxs-lookup"><span data-stu-id="7eb6b-124">Indicates whether the network is infrastructure ("ESS") or ad-hoc ("IBSS").</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="7eb6b-125">**conectividade**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-125">**connectivity**</span></span>](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | <span data-ttu-id="7eb6b-126">Contém várias configurações de conectividade.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-126">Contains various connectivity settings.</span></span> <span data-ttu-id="7eb6b-127">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-127">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="7eb6b-128">**conectividade**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-128">**connectivity**</span></span>](wlan-profileschema-connectivity-ihv-element.md)                |                                                                   | <span data-ttu-id="7eb6b-129">Contém configurações de conectividade relacionadas a IHV.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-129">Contains IHV-related connectivity settings.</span></span><br/> <span data-ttu-id="7eb6b-130">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-130">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="7eb6b-131">**encripta**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-131">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="7eb6b-132">Define a criptografia de dados a ser usada para se conectar à LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-132">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="7eb6b-133">**hex**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-133">**hex**</span></span>](wlan-profileschema-hex-ssid-element.md)                                 |                                                                   | <span data-ttu-id="7eb6b-134">Contém o SSID de uma LAN sem fio em formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-134">Contains the SSID of a wireless LAN in hexadecimal format.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="7eb6b-135">**IHV**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-135">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)                          |                                                                   | <span data-ttu-id="7eb6b-136">Contém configurações opcional do fornecedor de hardware independente (IHV).</span><span class="sxs-lookup"><span data-stu-id="7eb6b-136">Contains optional independent hardware vendor (IHV) settings.</span></span><br/> <span data-ttu-id="7eb6b-137">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-137">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="7eb6b-138">**keyIndex**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-138">**keyIndex**</span></span>](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | <span data-ttu-id="7eb6b-139">Especifica qual índice de chave deve ser usado para criptografar o tráfego sem fio.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-139">Specifies which key index should be used to encrypt wireless traffic.</span></span> <span data-ttu-id="7eb6b-140">Isso só é usado quando [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) está definido como "networkKey".</span><span class="sxs-lookup"><span data-stu-id="7eb6b-140">This is only used when [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) is set to "networkKey".</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="7eb6b-141">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-141">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)            | [<span data-ttu-id="7eb6b-142">cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="7eb6b-142">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="7eb6b-143">Contém a chave de rede ou frase secreta.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-143">Contains the network key or passphrase.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="7eb6b-144">**keyType**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-144">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | <span data-ttu-id="7eb6b-145">Tipo de chave.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-145">Type of key.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="7eb6b-146">**MSM**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-146">**MSM**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)                          |                                                                   | <span data-ttu-id="7eb6b-147">Contém várias configurações de MSM.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-147">Contains various MSM settings.</span></span> <span data-ttu-id="7eb6b-148">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-148">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="7eb6b-149">**nomes**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-149">**name**</span></span>](wlan-profileschema-name-wlanprofile-element.md)                        | [<span data-ttu-id="7eb6b-150">**nometype**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-150">**nameType**</span></span>](wlan-profileschema-nametype-simpletype.md)        | <span data-ttu-id="7eb6b-151">Nome do perfil de WLAN.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-151">Name of the WLAN profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="7eb6b-152">**nomes**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-152">**name**</span></span>](wlan-profileschema-name-ssid-element.md)                               |                                                                   | <span data-ttu-id="7eb6b-153">Contém o SSID de uma LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-153">Contains the SSID of a wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="7eb6b-154">**sem difusão**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-154">**nonBroadcast**</span></span>](wlan-profileschema-nonbroadcast-ssidconfig-element.md)         | [<span data-ttu-id="7eb6b-155">booleano</span><span class="sxs-lookup"><span data-stu-id="7eb6b-155">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="7eb6b-156">Indica se a rede transmite seu SSID.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-156">Indicates whether the network broadcasts its SSID.</span></span><br/> <span data-ttu-id="7eb6b-157">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-157">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="7eb6b-158">**OUI**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-158">**OUI**</span></span>](wlan-profileschema-oui-ouiheader-element.md)                            |                                                                   | <span data-ttu-id="7eb6b-159">Contém um hexBinary de 3 bytes que identifica o IHV.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-159">Contains a 3 byte hexBinary that identifies the IHV.</span></span><br/> <span data-ttu-id="7eb6b-160">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-160">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="7eb6b-161">**OUIHeader**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-161">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)                      |                                                                   | <span data-ttu-id="7eb6b-162">Identifica o IHV.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-162">Identifies the IHV.</span></span><br/> <span data-ttu-id="7eb6b-163">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-163">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="7eb6b-164">**phyType**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-164">**phyType**</span></span>](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | <span data-ttu-id="7eb6b-165">Especifica o padrão de LAN sem fio 802,11 usado na LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-165">Specifies the 802.11 wireless LAN standard used on the wireless LAN.</span></span> <span data-ttu-id="7eb6b-166">O valor "n" só tem suporte no Windows Vista com SP1 e em versões posteriores do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-166">The value "n" is only supported on Windows Vista with SP1 and later versions of the operating system.</span></span><br/> <span data-ttu-id="7eb6b-167">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-167">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="7eb6b-168">**PMKCacheMode**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-168">**PMKCacheMode**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | <span data-ttu-id="7eb6b-169">Indica se o cache PMK será usado.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-169">Indicates whether PMK caching will be used.</span></span> <span data-ttu-id="7eb6b-170">Esse elemento é válido somente para redes definidas por WPA2.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-170">This element is valid only for WPA2-defined networks.</span></span><br/> <span data-ttu-id="7eb6b-171">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-171">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="7eb6b-172">**PMKCacheSize**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-172">**PMKCacheSize**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | <span data-ttu-id="7eb6b-173">Especifica o número de entradas no cache PMK no cliente.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-173">Specifies the number of entries in the PMK cache on the client.</span></span> <span data-ttu-id="7eb6b-174">Esse elemento é válido somente para redes definidas por WPA2 com [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) definido como "habilitado".</span><span class="sxs-lookup"><span data-stu-id="7eb6b-174">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="7eb6b-175">Se **PMKCacheMode** estiver habilitado e esse elemento estiver ausente, o tamanho do cache será padronizado para 128 entradas.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-175">If **PMKCacheMode** is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span><br/> <span data-ttu-id="7eb6b-176">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-176">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="7eb6b-177">**PMKCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-177">**PMKCacheTTL**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | <span data-ttu-id="7eb6b-178">Indica o período de tempo, em minutos, que um cache de PMK será mantido.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-178">Indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="7eb6b-179">Esse elemento é válido somente para redes definidas por WPA2 com [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) definido como "habilitado".</span><span class="sxs-lookup"><span data-stu-id="7eb6b-179">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span><br/> <span data-ttu-id="7eb6b-180">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-180">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="7eb6b-181">**preAuthMode**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-181">**preAuthMode**</span></span>](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | <span data-ttu-id="7eb6b-182">Determina se a pré-autenticação será usada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-182">Determines if pre-authentication will be used by the client.</span></span> <span data-ttu-id="7eb6b-183">A pré-autenticação habilita o roaming rápido seguro de WPA2.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-183">Pre-authentication enables WPA2 secure fast roaming.</span></span> <span data-ttu-id="7eb6b-184">Esse elemento é válido somente para redes definidas por WPA2 com [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) definido como "habilitado".</span><span class="sxs-lookup"><span data-stu-id="7eb6b-184">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="7eb6b-185">Se **PMKCacheMode** estiver habilitado e esse elemento estiver ausente, o valor padrão será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-185">If **PMKCacheMode** is enabled, and this element is absent, the default value is disabled.</span></span><br/> <span data-ttu-id="7eb6b-186">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-186">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="7eb6b-187">**preAuthThrottle**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-187">**preAuthThrottle**</span></span>](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | <span data-ttu-id="7eb6b-188">Indica o número de tentativas ao se autenticar em APs vizinhos.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-188">Indicates the number of tries when preauthenticating to neighboring APs.</span></span> <span data-ttu-id="7eb6b-189">Esse elemento é válido somente para redes definidas por WPA2 com [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) definido como "habilitado".</span><span class="sxs-lookup"><span data-stu-id="7eb6b-189">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="7eb6b-190">Se **PMKCacheMode** estiver habilitado e esse elemento estiver ausente, o número de tentativas padrão será 3.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-190">If **PMKCacheMode** is enabled, and this element is absent, the number of tries defaults to 3.</span></span><br/> <span data-ttu-id="7eb6b-191">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-191">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="7eb6b-192">**protected**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-192">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)                | [<span data-ttu-id="7eb6b-193">booleano</span><span class="sxs-lookup"><span data-stu-id="7eb6b-193">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="7eb6b-194">Indica se a chave está criptografada.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-194">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="7eb6b-195">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento deve ter um valor de **false**.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-195">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of **FALSE**.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="7eb6b-196">**segurança**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-196">**security**</span></span>](wlan-profileschema-security-msm-element.md)                        |                                                                   | <span data-ttu-id="7eb6b-197">Contém várias configurações de segurança.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-197">Contains various security settings.</span></span> <span data-ttu-id="7eb6b-198">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-198">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="7eb6b-199">**segurança**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-199">**security**</span></span>](wlan-profileschema-security-ihv-element.md)                        |                                                                   | <span data-ttu-id="7eb6b-200">Contém configurações de segurança específicas de IHV.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-200">Contains IHV-specific security settings.</span></span> <span data-ttu-id="7eb6b-201">As configurações de segurança da Microsoft e as configurações de segurança de IHV são mutuamente exclusivas.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-201">Microsoft security settings and IHV security settings are mutually exclusive.</span></span> <span data-ttu-id="7eb6b-202">Se os dois conjuntos de configurações de segurança estiverem presentes no mesmo perfil, o perfil será inválido.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-202">If both sets of security settings are present in the same profile, the profile is invalid.</span></span><br/> <span data-ttu-id="7eb6b-203">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-203">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="7eb6b-204">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-204">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | <span data-ttu-id="7eb6b-205">Contém as informações de chave compartilhada.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-205">Contains the shared key information.</span></span> <span data-ttu-id="7eb6b-206">Esse elemento só será necessário se as chaves WEP ou PSK forem necessárias para o par de autenticação e criptografia.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-206">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="7eb6b-207">**SSID**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-207">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)                         |                                                                   | <span data-ttu-id="7eb6b-208">Especifica o SSID de uma LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-208">Specifies the SSID of a wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="7eb6b-209">**SSIDConfig**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-209">**SSIDConfig**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)            |                                                                   | <span data-ttu-id="7eb6b-210">Contém um ou mais SSIDs juntamente com outras configurações comuns.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-210">Contains one or more SSIDs along with other common settings.</span></span> <br/> <span data-ttu-id="7eb6b-211">Um perfil pode ter vários elementos [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) e cada elemento [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) pode ter vários elementos [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7eb6b-211">A profile can have multiple [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) elements and each [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element can have multiple [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) elements.</span></span> <span data-ttu-id="7eb6b-212">No entanto, o Windows apenas considera o primeiro elemento [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) em um elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7eb6b-212">However, Windows only ever considers the first [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element in a [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span><br/> <span data-ttu-id="7eb6b-213">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** No máximo um elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) pode aparecer em um perfil.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-213">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** At most one [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element can appear in a profile.</span></span><br/> |
| [<span data-ttu-id="7eb6b-214">**Escreva**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-214">**type**</span></span>](wlan-profileschema-type-ouiheader-element.md)                          |                                                                   | <span data-ttu-id="7eb6b-215">Contém um **hexBinary** de 1 byte que é usado para diferenciar NICs pelo mesmo IHV.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-215">Contains a 1 byte **hexBinary** that is used to differentiate NICs by the same IHV.</span></span><br/> <span data-ttu-id="7eb6b-216">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-216">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="7eb6b-217">**useMSOneX**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-217">**useMSOneX**</span></span>](wlan-profileschema-usemsonex-ihv-element.md)                      | [<span data-ttu-id="7eb6b-218">booleano</span><span class="sxs-lookup"><span data-stu-id="7eb6b-218">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="7eb6b-219">Especifica a origem das configurações de segurança 802.1 X usadas por um componente de segurança do IHV.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-219">Specifies the origin of 802.1X security settings used by an IHV security component.</span></span> <span data-ttu-id="7eb6b-220">Quando [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) é verdadeiro, os componentes de segurança de IHV usam configurações 802.1 x definidas pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-220">When [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) is true, IHV security components use Microsoft-defined 802.1X settings.</span></span> <span data-ttu-id="7eb6b-221">Quando **useMSOneX** é false, os componentes de segurança de IHV usam configurações 802.1 x fornecidas pelo fornecedor.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-221">When **useMSOneX** is false, IHV security components use vendor-supplied 802.1X settings.</span></span> <span data-ttu-id="7eb6b-222">Por padrão, **useMSOneX** é false.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-222">By default, **useMSOneX** is false.</span></span> <span data-ttu-id="7eb6b-223">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-223">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="7eb6b-224">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="7eb6b-224">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="7eb6b-225">booleano</span><span class="sxs-lookup"><span data-stu-id="7eb6b-225">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="7eb6b-226">Indica se 802.1 X é usado.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-226">Indicates whether 802.1X is used.</span></span> <span data-ttu-id="7eb6b-227">Esse sinalizador é opcional.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-227">This flag is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="7eb6b-228">Comentários</span><span class="sxs-lookup"><span data-stu-id="7eb6b-228">Remarks</span></span>

<span data-ttu-id="7eb6b-229">A maioria dos elementos filho do elemento WLANProfile está no `https://www.microsoft.com/networking/WLAN/profile/v1` namespace.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-229">Most child elements of the WLANProfile element are in the `https://www.microsoft.com/networking/WLAN/profile/v1` namespace.</span></span> <span data-ttu-id="7eb6b-230">Há duas exceções: o elemento [**fipsmode**](wlan-profileschema-fipsmode-authencryption-element.md) está no `https://www.microsoft.com/networking/WLAN/profile/v2` namespace e o elemento [**Onex**](onexschema-onex-element.md) está no `https://www.microsoft.com/networking/OneX/v1` namespace.</span><span class="sxs-lookup"><span data-stu-id="7eb6b-230">There are two exceptions: the [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element is in the `https://www.microsoft.com/networking/WLAN/profile/v2` namespace and the [**OneX**](onexschema-onex-element.md) element is in the `https://www.microsoft.com/networking/OneX/v1` namespace.</span></span>

<span data-ttu-id="7eb6b-231">O elemento [**fipsmode**](wlan-profileschema-fipsmode-authencryption-element.md) pode ser inserido como um filho do elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7eb6b-231">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span> <span data-ttu-id="7eb6b-232">O elemento [**Onex**](onexschema-onex-element.md) pode ser inserido como um filho do elemento [**Security (MSM)**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7eb6b-232">The [**OneX**](onexschema-onex-element.md) element can be inserted as a child of the [**security (MSM)**](wlan-profileschema-security-msm-element.md) element.</span></span>

<span data-ttu-id="7eb6b-233">Para exibir a lista de elementos filho em uma estrutura do tipo árvore, consulte [ \_ elementos do esquema do perfil WLAN](wlan-profileschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="7eb6b-233">To view the list of child elements in a tree-like structure, see [WLAN\_profile Schema Elements](wlan-profileschema-elements.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7eb6b-234">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7eb6b-234">Examples</span></span>

<span data-ttu-id="7eb6b-235">Para exibir perfis de exemplo, consulte [amostras de perfil sem fio](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="7eb6b-235">To view sample profiles, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7eb6b-236">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7eb6b-236">Requirements</span></span>



| <span data-ttu-id="7eb6b-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="7eb6b-237">Requirement</span></span> | <span data-ttu-id="7eb6b-238">Valor</span><span class="sxs-lookup"><span data-stu-id="7eb6b-238">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7eb6b-239">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7eb6b-239">Minimum supported client</span></span><br/> | <span data-ttu-id="7eb6b-240">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="7eb6b-240">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7eb6b-241">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7eb6b-241">Minimum supported server</span></span><br/> | <span data-ttu-id="7eb6b-242">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7eb6b-242">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="7eb6b-243">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="7eb6b-243">Redistributable</span></span><br/>          | <span data-ttu-id="7eb6b-244">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="7eb6b-244">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="7eb6b-245">Confira também</span><span class="sxs-lookup"><span data-stu-id="7eb6b-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eb6b-246">Exemplos de perfil sem fio</span><span class="sxs-lookup"><span data-stu-id="7eb6b-246">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 
