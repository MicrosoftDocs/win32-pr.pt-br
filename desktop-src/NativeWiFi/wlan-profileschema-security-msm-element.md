---
description: Contém várias configurações de segurança.
ms.assetid: 1d912fb1-8fb4-4761-8991-5a50ffb0399e
title: Elemento Security (MSM) (LAN_policy) (WLAN)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: f6ea42a83d39c328db88e992555e5d593cc778b6
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "105779976"
---
# <a name="security-msm-element-lan_policy-for-wlan"></a><span data-ttu-id="e5979-103">Elemento Security (MSM) (LAN_policy) para WLAN</span><span class="sxs-lookup"><span data-stu-id="e5979-103">Security (MSM) Element (LAN_policy) for WLAN</span></span>

<span data-ttu-id="e5979-104">O elemento Security (MSM) contém várias configurações de segurança.</span><span class="sxs-lookup"><span data-stu-id="e5979-104">The security (MSM) element contains various security settings.</span></span>

``` syntax
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
```

<span data-ttu-id="e5979-105">O elemento é definido pelo elemento [**msm**](wlan-profileschema-msm-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e5979-105">The element is defined by the [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e5979-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="e5979-106">Child elements</span></span>



| <span data-ttu-id="e5979-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="e5979-107">Element</span></span>                                                                            | <span data-ttu-id="e5979-108">Type</span><span class="sxs-lookup"><span data-stu-id="e5979-108">Type</span></span>                                                              | <span data-ttu-id="e5979-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5979-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5979-110">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="e5979-110">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)       |                                                                   | <span data-ttu-id="e5979-111">Especifica o par de autenticação e criptografia a ser usado para este perfil.</span><span class="sxs-lookup"><span data-stu-id="e5979-111">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="e5979-112">**Authentication**</span><span class="sxs-lookup"><span data-stu-id="e5979-112">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="e5979-113">Especifica o par de autenticação e criptografia a ser usado para este perfil.</span><span class="sxs-lookup"><span data-stu-id="e5979-113">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="e5979-114">**encripta**</span><span class="sxs-lookup"><span data-stu-id="e5979-114">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="e5979-115">Define a criptografia de dados a ser usada para se conectar à LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="e5979-115">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="e5979-116">**keyIndex**</span><span class="sxs-lookup"><span data-stu-id="e5979-116">**keyIndex**</span></span>](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | <span data-ttu-id="e5979-117">Especifica qual índice de chave deve ser usado para criptografar o tráfego sem fio.</span><span class="sxs-lookup"><span data-stu-id="e5979-117">Specifies which key index must be used to encrypt wireless traffic.</span></span> <span data-ttu-id="e5979-118">Isso só é usado quando KeyType está definido como networkKey.</span><span class="sxs-lookup"><span data-stu-id="e5979-118">This is only used when keyType is set to networkKey.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="e5979-119">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="e5979-119">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)            | [<span data-ttu-id="e5979-120">cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="e5979-120">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="e5979-121">Contém a chave de rede ou frase secreta.</span><span class="sxs-lookup"><span data-stu-id="e5979-121">Contains the network key or passphrase.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="e5979-122">**keyType**</span><span class="sxs-lookup"><span data-stu-id="e5979-122">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | <span data-ttu-id="e5979-123">Tipo de chave.</span><span class="sxs-lookup"><span data-stu-id="e5979-123">Type of key.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="e5979-124">**PMKCacheMode**</span><span class="sxs-lookup"><span data-stu-id="e5979-124">**PMKCacheMode**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | <span data-ttu-id="e5979-125">Indica se o cache PMK será usado.</span><span class="sxs-lookup"><span data-stu-id="e5979-125">Indicates whether PMK caching will be used.</span></span> <span data-ttu-id="e5979-126">Esse elemento é válido somente para redes definidas por WPA2.</span><span class="sxs-lookup"><span data-stu-id="e5979-126">This element is valid only for WPA2-defined networks.</span></span><br/> <span data-ttu-id="e5979-127">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="e5979-127">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="e5979-128">**PMKCacheSize**</span><span class="sxs-lookup"><span data-stu-id="e5979-128">**PMKCacheSize**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | <span data-ttu-id="e5979-129">Especifica o número de entradas no cache OMK no cliente.</span><span class="sxs-lookup"><span data-stu-id="e5979-129">Specifies the number of entries in the OMK cache on the client.</span></span> <span data-ttu-id="e5979-130">Esse elemento é válido somente para redes definidas por WPA2 com o modo PMKCache definido como habilitado.</span><span class="sxs-lookup"><span data-stu-id="e5979-130">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="e5979-131">Se o modo PMKCache estiver habilitado e esse elemento estiver ausente, o tamanho do cache será padronizado para 128 entradas.</span><span class="sxs-lookup"><span data-stu-id="e5979-131">If PMKCache mode is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span><br/> <span data-ttu-id="e5979-132">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="e5979-132">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                   |
| [<span data-ttu-id="e5979-133">**PMKCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="e5979-133">**PMKCacheTTL**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | <span data-ttu-id="e5979-134">Indica o período de tempo, em minutos, que um cache de PMK será mantido.</span><span class="sxs-lookup"><span data-stu-id="e5979-134">Indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="e5979-135">Esse elemento é válido somente para redes definidas por WPA2 com o modo PMKCache definido como habilitado.</span><span class="sxs-lookup"><span data-stu-id="e5979-135">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span><br/> <span data-ttu-id="e5979-136">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="e5979-136">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="e5979-137">**preAuthMode**</span><span class="sxs-lookup"><span data-stu-id="e5979-137">**preAuthMode**</span></span>](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | <span data-ttu-id="e5979-138">Determina se a pré-autenticação será usada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="e5979-138">Determines if pre-authentication will be used by the client.</span></span> <span data-ttu-id="e5979-139">A pré-autenticação habilita o roaming rápido seguro de WPA2.</span><span class="sxs-lookup"><span data-stu-id="e5979-139">Pre-authentication enables WPA2 secure fast roaming.</span></span> <span data-ttu-id="e5979-140">Esse elemento é válido somente para redes definidas por WPA2 com o modo PMKCache definido como habilitado.</span><span class="sxs-lookup"><span data-stu-id="e5979-140">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="e5979-141">Se o modo PMKCache estiver habilitado e esse elemento estiver ausente, o valor padrão será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="e5979-141">If PMKCache mode is enabled, and this element is absent, the default value is disabled.</span></span><br/> <span data-ttu-id="e5979-142">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="e5979-142">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/> |
| [<span data-ttu-id="e5979-143">**preAuthThrottle**</span><span class="sxs-lookup"><span data-stu-id="e5979-143">**preAuthThrottle**</span></span>](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | <span data-ttu-id="e5979-144">Indica o número de tentativas ao se autenticar em APs vizinhos.</span><span class="sxs-lookup"><span data-stu-id="e5979-144">Indicates the number of tries when preauthenticating to neighboring APs.</span></span> <span data-ttu-id="e5979-145">Esse elemento é válido somente para redes definidas por WPA2 com o modo PMKCache definido como habilitado.</span><span class="sxs-lookup"><span data-stu-id="e5979-145">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="e5979-146">Se o modo PMKCache estiver habilitado e esse elemento estiver ausente, o número de tentativas padrão será 3.</span><span class="sxs-lookup"><span data-stu-id="e5979-146">If PMKCache mode is enabled, and this element is absent, the number of tries defaults to 3.</span></span><br/> <span data-ttu-id="e5979-147">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="e5979-147">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="e5979-148">**protected**</span><span class="sxs-lookup"><span data-stu-id="e5979-148">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)                | [<span data-ttu-id="e5979-149">booleano</span><span class="sxs-lookup"><span data-stu-id="e5979-149">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="e5979-150">Indica se a chave está criptografada.</span><span class="sxs-lookup"><span data-stu-id="e5979-150">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="e5979-151">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento deve ter um valor de **false**.</span><span class="sxs-lookup"><span data-stu-id="e5979-151">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of **FALSE**.</span></span><br/>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="e5979-152">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="e5979-152">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | <span data-ttu-id="e5979-153">Contém as informações de chave compartilhada.</span><span class="sxs-lookup"><span data-stu-id="e5979-153">Contains the shared key information.</span></span> <span data-ttu-id="e5979-154">Esse elemento só será necessário se as chaves WEP ou PSK forem necessárias para o par de autenticação e criptografia.</span><span class="sxs-lookup"><span data-stu-id="e5979-154">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span><br/>                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="e5979-155">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="e5979-155">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="e5979-156">booleano</span><span class="sxs-lookup"><span data-stu-id="e5979-156">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="e5979-157">Indica se 802.1 X é usado.</span><span class="sxs-lookup"><span data-stu-id="e5979-157">Indicates whether 802.1X is used.</span></span> <span data-ttu-id="e5979-158">Esse sinalizador é opcional.</span><span class="sxs-lookup"><span data-stu-id="e5979-158">This flag is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="e5979-159">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5979-159">Remarks</span></span>

<span data-ttu-id="e5979-160">O elemento [**fipsmode**](wlan-profileschema-fipsmode-authencryption-element.md) pode ser inserido como um filho do elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e5979-160">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span> <span data-ttu-id="e5979-161">O elemento [**Onex**](onexschema-onex-element.md) pode ser inserido como um filho do elemento **Security (MSM)** .</span><span class="sxs-lookup"><span data-stu-id="e5979-161">The [**OneX**](onexschema-onex-element.md) element can be inserted as a child of the **security (MSM)** element.</span></span>

## <a name="examples"></a><span data-ttu-id="e5979-162">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e5979-162">Examples</span></span>

<span data-ttu-id="e5979-163">Para exibir perfis de exemplo que usam o elemento de **segurança** , consulte [exemplos de perfil sem fio](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="e5979-163">To view sample profiles that use the **security** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5979-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5979-164">Requirements</span></span>



| <span data-ttu-id="e5979-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5979-165">Requirement</span></span> | <span data-ttu-id="e5979-166">Valor</span><span class="sxs-lookup"><span data-stu-id="e5979-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="e5979-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5979-167">Minimum supported client</span></span><br/> | <span data-ttu-id="e5979-168">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="e5979-168">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e5979-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5979-169">Minimum supported server</span></span><br/> | <span data-ttu-id="e5979-170">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e5979-170">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="e5979-171">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="e5979-171">Redistributable</span></span><br/>          | <span data-ttu-id="e5979-172">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="e5979-172">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="e5979-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5979-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5979-174">Exemplos de perfil sem fio</span><span class="sxs-lookup"><span data-stu-id="e5979-174">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

<span data-ttu-id="e5979-175">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="e5979-175">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e5979-176">**MSM**</span><span class="sxs-lookup"><span data-stu-id="e5979-176">**MSM**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="e5979-177">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="e5979-177">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e5979-178">**MSM (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="e5979-178">**MSM (WLANProfile)**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> </dl>

 

 
