---
description: Contém várias configurações de MSM (módulo específico de mídia).
ms.assetid: 31f98af8-a577-4f6a-9a0a-b182b5a89cc3
title: Elemento MSM (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSM
api_type:
- Schema
api_location: ''
ms.openlocfilehash: b2e1ffdc5ad27524d3d2fc5b37b3a060a90c7575
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759672"
---
# <a name="msm-wlanprofile-element"></a><span data-ttu-id="2459c-103">Elemento MSM (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="2459c-103">MSM (WLANProfile) Element</span></span>

<span data-ttu-id="2459c-104">O elemento MSM (WLANProfile) contém várias configurações do módulo de mídia específica (MSM).</span><span class="sxs-lookup"><span data-stu-id="2459c-104">The MSM (WLANProfile) element contains various media-specific module (MSM) settings.</span></span>

``` syntax
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
```

<span data-ttu-id="2459c-105">O elemento é definido pelo elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2459c-105">The element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2459c-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2459c-106">Child elements</span></span>



| <span data-ttu-id="2459c-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="2459c-107">Element</span></span>                                                                            | <span data-ttu-id="2459c-108">Type</span><span class="sxs-lookup"><span data-stu-id="2459c-108">Type</span></span>                                                              | <span data-ttu-id="2459c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="2459c-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2459c-110">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="2459c-110">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)       |                                                                   | <span data-ttu-id="2459c-111">Especifica o par de autenticação e criptografia a ser usado para este perfil.</span><span class="sxs-lookup"><span data-stu-id="2459c-111">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="2459c-112">**Authentication**</span><span class="sxs-lookup"><span data-stu-id="2459c-112">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="2459c-113">Especifica o par de autenticação e criptografia a ser usado para este perfil.</span><span class="sxs-lookup"><span data-stu-id="2459c-113">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="2459c-114">**conectividade**</span><span class="sxs-lookup"><span data-stu-id="2459c-114">**connectivity**</span></span>](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | <span data-ttu-id="2459c-115">Contém várias configurações de conectividade.</span><span class="sxs-lookup"><span data-stu-id="2459c-115">Contains various connectivity settings.</span></span> <span data-ttu-id="2459c-116">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="2459c-116">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="2459c-117">**encripta**</span><span class="sxs-lookup"><span data-stu-id="2459c-117">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="2459c-118">Define a criptografia de dados a ser usada para se conectar à LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="2459c-118">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="2459c-119">**keyIndex**</span><span class="sxs-lookup"><span data-stu-id="2459c-119">**keyIndex**</span></span>](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | <span data-ttu-id="2459c-120">Especifica qual índice de chave deve ser usado para criptografar o tráfego sem fio.</span><span class="sxs-lookup"><span data-stu-id="2459c-120">Specifies which key index must be used to encrypt wireless traffic.</span></span> <span data-ttu-id="2459c-121">Isso só é usado quando KeyType está definido como networkKey.</span><span class="sxs-lookup"><span data-stu-id="2459c-121">This is only used when keyType is set to networkKey.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="2459c-122">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="2459c-122">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)            | [<span data-ttu-id="2459c-123">cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="2459c-123">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="2459c-124">Contém a chave de rede ou frase secreta.</span><span class="sxs-lookup"><span data-stu-id="2459c-124">Contains the network key or passphrase.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="2459c-125">**keyType**</span><span class="sxs-lookup"><span data-stu-id="2459c-125">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | <span data-ttu-id="2459c-126">Tipo de chave.</span><span class="sxs-lookup"><span data-stu-id="2459c-126">Type of key.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="2459c-127">**phyType**</span><span class="sxs-lookup"><span data-stu-id="2459c-127">**phyType**</span></span>](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | <span data-ttu-id="2459c-128">Especifica o padrão de LAN sem fio 802,11 usado na LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="2459c-128">Specifies the 802.11 wireless LAN standard used on the wireless LAN.</span></span> <span data-ttu-id="2459c-129">O valor "n" só tem suporte no Windows Vista com SP1 e em versões posteriores do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="2459c-129">The value "n" is only supported on Windows Vista with SP1 and later versions of the operating system.</span></span><br/> <span data-ttu-id="2459c-130">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="2459c-130">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="2459c-131">**PMKCacheMode**</span><span class="sxs-lookup"><span data-stu-id="2459c-131">**PMKCacheMode**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | <span data-ttu-id="2459c-132">Indica se o cache PMK será usado.</span><span class="sxs-lookup"><span data-stu-id="2459c-132">Indicates whether PMK caching will be used.</span></span> <span data-ttu-id="2459c-133">Esse elemento é válido somente para redes definidas por WPA2.</span><span class="sxs-lookup"><span data-stu-id="2459c-133">This element is valid only for WPA2-defined networks.</span></span><br/> <span data-ttu-id="2459c-134">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="2459c-134">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="2459c-135">**PMKCacheSize**</span><span class="sxs-lookup"><span data-stu-id="2459c-135">**PMKCacheSize**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | <span data-ttu-id="2459c-136">Especifica o número de entradas no cache OMK no cliente.</span><span class="sxs-lookup"><span data-stu-id="2459c-136">Specifies the number of entries in the OMK cache on the client.</span></span> <span data-ttu-id="2459c-137">Esse elemento é válido somente para redes definidas por WPA2 com o modo PMKCache definido como habilitado.</span><span class="sxs-lookup"><span data-stu-id="2459c-137">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="2459c-138">Se o modo PMKCache estiver habilitado e esse elemento estiver ausente, o tamanho do cache será padronizado para 128 entradas.</span><span class="sxs-lookup"><span data-stu-id="2459c-138">If PMKCache mode is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span><br/> <span data-ttu-id="2459c-139">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="2459c-139">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                   |
| [<span data-ttu-id="2459c-140">**PMKCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="2459c-140">**PMKCacheTTL**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | <span data-ttu-id="2459c-141">Indica o período de tempo, em minutos, que um cache de PMK será mantido.</span><span class="sxs-lookup"><span data-stu-id="2459c-141">Indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="2459c-142">Esse elemento é válido somente para redes definidas por WPA2 com o modo PMKCache definido como habilitado.</span><span class="sxs-lookup"><span data-stu-id="2459c-142">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span><br/> <span data-ttu-id="2459c-143">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="2459c-143">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="2459c-144">**preAuthMode**</span><span class="sxs-lookup"><span data-stu-id="2459c-144">**preAuthMode**</span></span>](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | <span data-ttu-id="2459c-145">Determina se a pré-autenticação será usada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="2459c-145">Determines if pre-authentication will be used by the client.</span></span> <span data-ttu-id="2459c-146">A pré-autenticação habilita o roaming rápido seguro de WPA2.</span><span class="sxs-lookup"><span data-stu-id="2459c-146">Pre-authentication enables WPA2 secure fast roaming.</span></span> <span data-ttu-id="2459c-147">Esse elemento é válido somente para redes definidas por WPA2 com o modo PMKCache definido como habilitado.</span><span class="sxs-lookup"><span data-stu-id="2459c-147">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="2459c-148">Se o modo PMKCache estiver habilitado e esse elemento estiver ausente, o valor padrão será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="2459c-148">If PMKCache mode is enabled, and this element is absent, the default value is disabled.</span></span><br/> <span data-ttu-id="2459c-149">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="2459c-149">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/> |
| [<span data-ttu-id="2459c-150">**preAuthThrottle**</span><span class="sxs-lookup"><span data-stu-id="2459c-150">**preAuthThrottle**</span></span>](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | <span data-ttu-id="2459c-151">Indica o número de tentativas ao se autenticar em APs vizinhos.</span><span class="sxs-lookup"><span data-stu-id="2459c-151">Indicates the number of tries when preauthenticating to neighboring APs.</span></span> <span data-ttu-id="2459c-152">Esse elemento é válido somente para redes definidas por WPA2 com o modo PMKCache definido como habilitado.</span><span class="sxs-lookup"><span data-stu-id="2459c-152">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="2459c-153">Se o modo PMKCache estiver habilitado e esse elemento estiver ausente, o número de tentativas padrão será 3.</span><span class="sxs-lookup"><span data-stu-id="2459c-153">If PMKCache mode is enabled, and this element is absent, the number of tries defaults to 3.</span></span><br/> <span data-ttu-id="2459c-154">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="2459c-154">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="2459c-155">**protected**</span><span class="sxs-lookup"><span data-stu-id="2459c-155">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)                | [<span data-ttu-id="2459c-156">booleano</span><span class="sxs-lookup"><span data-stu-id="2459c-156">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="2459c-157">Indica se a chave está criptografada.</span><span class="sxs-lookup"><span data-stu-id="2459c-157">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="2459c-158">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento deve ter um valor de FALSE.</span><span class="sxs-lookup"><span data-stu-id="2459c-158">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of FALSE.</span></span><br/>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="2459c-159">**segurança**</span><span class="sxs-lookup"><span data-stu-id="2459c-159">**security**</span></span>](wlan-profileschema-security-msm-element.md)                        |                                                                   | <span data-ttu-id="2459c-160">Contém várias configurações de segurança.</span><span class="sxs-lookup"><span data-stu-id="2459c-160">Contains various security settings.</span></span> <span data-ttu-id="2459c-161">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="2459c-161">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="2459c-162">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="2459c-162">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | <span data-ttu-id="2459c-163">Contém as informações de chave compartilhada.</span><span class="sxs-lookup"><span data-stu-id="2459c-163">Contains the shared key information.</span></span> <span data-ttu-id="2459c-164">Esse elemento só será necessário se as chaves WEP ou PSK forem necessárias para o par de autenticação e criptografia.</span><span class="sxs-lookup"><span data-stu-id="2459c-164">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span><br/>                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="2459c-165">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="2459c-165">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="2459c-166">booleano</span><span class="sxs-lookup"><span data-stu-id="2459c-166">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="2459c-167">Indica se 802.1 X é usado.</span><span class="sxs-lookup"><span data-stu-id="2459c-167">Indicates whether 802.1X is used.</span></span> <span data-ttu-id="2459c-168">Esse sinalizador é opcional.</span><span class="sxs-lookup"><span data-stu-id="2459c-168">This flag is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="2459c-169">Comentários</span><span class="sxs-lookup"><span data-stu-id="2459c-169">Remarks</span></span>

<span data-ttu-id="2459c-170">O elemento [**fipsmode**](wlan-profileschema-fipsmode-authencryption-element.md) pode ser inserido como um filho do elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2459c-170">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span> <span data-ttu-id="2459c-171">O elemento [**Onex**](onexschema-onex-element.md) pode ser inserido como um filho do elemento [**Security (MSM)**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2459c-171">The [**OneX**](onexschema-onex-element.md) element can be inserted as a child of the [**security (MSM)**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="2459c-172">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2459c-172">Examples</span></span>

<span data-ttu-id="2459c-173">Para exibir perfis de exemplo que usam o elemento **msm** , consulte [amostras de perfil sem fio](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="2459c-173">To view sample profiles that use the **MSM** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2459c-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2459c-174">Requirements</span></span>



| <span data-ttu-id="2459c-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="2459c-175">Requirement</span></span> | <span data-ttu-id="2459c-176">Valor</span><span class="sxs-lookup"><span data-stu-id="2459c-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="2459c-177">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2459c-177">Minimum supported client</span></span><br/> | <span data-ttu-id="2459c-178">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="2459c-178">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2459c-179">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2459c-179">Minimum supported server</span></span><br/> | <span data-ttu-id="2459c-180">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2459c-180">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="2459c-181">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="2459c-181">Redistributable</span></span><br/>          | <span data-ttu-id="2459c-182">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="2459c-182">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="2459c-183">Confira também</span><span class="sxs-lookup"><span data-stu-id="2459c-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2459c-184">Exemplos de perfil sem fio</span><span class="sxs-lookup"><span data-stu-id="2459c-184">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

<span data-ttu-id="2459c-185">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="2459c-185">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2459c-186">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="2459c-186">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="2459c-187">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="2459c-187">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2459c-188">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="2459c-188">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
