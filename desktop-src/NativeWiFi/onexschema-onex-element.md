---
description: Especifica as informações de configuração 802.1 X para um perfil de LAN com ou sem fio.
ms.assetid: 4528fcb5-ee8e-4824-a69e-8d67622c4b4d
title: Elemento OneX
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4b3e3d91087a394efb7909d36d6244bfbf6115e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778711"
---
# <a name="onex-element"></a><span data-ttu-id="90cd3-103">Elemento OneX</span><span class="sxs-lookup"><span data-stu-id="90cd3-103">OneX Element</span></span>

<span data-ttu-id="90cd3-104">O elemento OneX especifica informações de configuração 802.1 X para um perfil de LAN com ou sem fio.</span><span class="sxs-lookup"><span data-stu-id="90cd3-104">The OneX element specifies 802.1X configuration information for a wired or wireless LAN profile.</span></span> <span data-ttu-id="90cd3-105">Esse é o elemento raiz exclusivo para um perfil 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="90cd3-105">This element is the unique root element for an 802.1X profile.</span></span>

<span data-ttu-id="90cd3-106">O namespace de destino para o elemento OneX é `https://www.microsoft.com/networking/OneX/v1` .</span><span class="sxs-lookup"><span data-stu-id="90cd3-106">The target namespace for the OneX element is `https://www.microsoft.com/networking/OneX/v1`.</span></span> <span data-ttu-id="90cd3-107">A maioria dos elementos filho do elemento OneX está no `OneX` namespace.</span><span class="sxs-lookup"><span data-stu-id="90cd3-107">Most child elements of the OneX element are in the `OneX` namespace.</span></span> <span data-ttu-id="90cd3-108">Há uma exceção: o elemento [**EAPConfig**](onexschema-eapconfig-onex-element.md) está no `https://www.microsoft.com/provisioning/EapHostConfig` namespace.</span><span class="sxs-lookup"><span data-stu-id="90cd3-108">There is one exception: the [**EAPConfig**](onexschema-eapconfig-onex-element.md) element is in the `https://www.microsoft.com/provisioning/EapHostConfig` namespace.</span></span>

<span data-ttu-id="90cd3-109">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Somente o elemento [**EAPConfig**](onexschema-eapconfig-onex-element.md) tem suporte.</span><span class="sxs-lookup"><span data-stu-id="90cd3-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** Only the [**EAPConfig**](onexschema-eapconfig-onex-element.md) element is supported.</span></span> <span data-ttu-id="90cd3-110">Outros elementos, se presentes em um perfil, serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="90cd3-110">Other elements, if present in a profile, will be ignored.</span></span>

``` syntax
<xs:element name="OneX">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="cacheUserData"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="heldPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="authPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="startPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxStart"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="100"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxAuthFailures"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="100"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="supplicantMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="inhibitTransmission"
                         />
                        <xs:enumeration
                            value="includeLearning"
                         />
                        <xs:enumeration
                            value="compliant"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="authMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="machineOrUser"
                         />
                        <xs:enumeration
                            value="machine"
                         />
                        <xs:enumeration
                            value="user"
                         />
                        <xs:enumeration
                            value="guest"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="singleSignOn"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="type"
                            minOccurs="1"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:enumeration
                                        value="preLogon"
                                     />
                                    <xs:enumeration
                                        value="postLogon"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="maxDelay"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="integer"
                                >
                                    <xs:enumeration
                                        value="0"
                                     />
                                    <xs:enumeration
                                        value="120"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="userBasedVirtualLan"
                            type="boolean"
                            minOccurs="0"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="EAPConfig">
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            minOccurs="1"
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

## <a name="child-elements"></a><span data-ttu-id="90cd3-111">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="90cd3-111">Child elements</span></span>



| <span data-ttu-id="90cd3-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="90cd3-112">Element</span></span>                                                                            | <span data-ttu-id="90cd3-113">Type</span><span class="sxs-lookup"><span data-stu-id="90cd3-113">Type</span></span>    | <span data-ttu-id="90cd3-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="90cd3-114">Description</span></span>                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90cd3-115">**AuthMode**</span><span class="sxs-lookup"><span data-stu-id="90cd3-115">**authMode**</span></span>](onexschema-authmode-onex-element.md)                               |         | <span data-ttu-id="90cd3-116">Especifica o tipo de credenciais usadas para autenticação.</span><span class="sxs-lookup"><span data-stu-id="90cd3-116">Specifies the type of credentials used for authentication.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="90cd3-117">**authPeriod**</span><span class="sxs-lookup"><span data-stu-id="90cd3-117">**authPeriod**</span></span>](onexschema-authperiod-onex-element.md)                           |         | <span data-ttu-id="90cd3-118">Especifica o período máximo de tempo, em segundos, no qual um cliente aguarda uma resposta do autenticador.</span><span class="sxs-lookup"><span data-stu-id="90cd3-118">Specifies the maximum length of time, in seconds, in which a client waits for a response from the authenticator.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="90cd3-119">**cacheUserData**</span><span class="sxs-lookup"><span data-stu-id="90cd3-119">**cacheUserData**</span></span>](onexschema-cacheuserdata-onex-element.md)                     | <span data-ttu-id="90cd3-120">booleano</span><span class="sxs-lookup"><span data-stu-id="90cd3-120">boolean</span></span> | <span data-ttu-id="90cd3-121">Especifica se as credenciais do usuário são armazenadas em cache para as conexões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="90cd3-121">Specifies whether the user credentials are cached for subsequent connections.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="90cd3-122">**EAPConfig**</span><span class="sxs-lookup"><span data-stu-id="90cd3-122">**EAPConfig**</span></span>](onexschema-eapconfig-onex-element.md)                             |         | <span data-ttu-id="90cd3-123">Especifica a configuração do EAPHost.</span><span class="sxs-lookup"><span data-stu-id="90cd3-123">Specifies the EAPHost configuration.</span></span><br/>                                                                                                                                                                              |
| [<span data-ttu-id="90cd3-124">**heldPeriod**</span><span class="sxs-lookup"><span data-stu-id="90cd3-124">**heldPeriod**</span></span>](onexschema-heldperiod-onex-element.md)                           |         | <span data-ttu-id="90cd3-125">Especifica o período de tempo, em segundos, no qual um cliente não tentará realizar a autenticação novamente após uma tentativa de autenticação com falha.</span><span class="sxs-lookup"><span data-stu-id="90cd3-125">Specifies the length of time, in seconds, in which a client will not re-attempt authentication after a failed authentication attempt.</span></span><br/>                                                                             |
| [<span data-ttu-id="90cd3-126">**maxAuthFailures**</span><span class="sxs-lookup"><span data-stu-id="90cd3-126">**maxAuthFailures**</span></span>](onexschema-maxauthfailures-onex-element.md)                 |         | <span data-ttu-id="90cd3-127">Especifica o número máximo de falhas de autenticação permitidas para um conjunto de credenciais.</span><span class="sxs-lookup"><span data-stu-id="90cd3-127">Specifies the maximum number of authentication failures allowed for a set of credentials.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="90cd3-128">**maxDelay**</span><span class="sxs-lookup"><span data-stu-id="90cd3-128">**maxDelay**</span></span>](onexschema-maxdelay-singlesignon-element.md)                       |         | <span data-ttu-id="90cd3-129">Especifica, em segundos, o atraso máximo antes da tentativa de conexão de logon único falhar.</span><span class="sxs-lookup"><span data-stu-id="90cd3-129">Specifies, in seconds, the maximum delay before the single sign-on connection attempt fails.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="90cd3-130">**maxStart**</span><span class="sxs-lookup"><span data-stu-id="90cd3-130">**maxStart**</span></span>](onexschema-maxstart-onex-element.md)                               |         | <span data-ttu-id="90cd3-131">Especifica o número máximo de EAPOL-Start mensagens enviadas.</span><span class="sxs-lookup"><span data-stu-id="90cd3-131">Specifies the maximum number of EAPOL-Start messages sent.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="90cd3-132">**Logon único**</span><span class="sxs-lookup"><span data-stu-id="90cd3-132">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)                       |         | <span data-ttu-id="90cd3-133">Especifica as informações de configuração de rede de logon único.</span><span class="sxs-lookup"><span data-stu-id="90cd3-133">Specifies single sign-on network configuration information.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="90cd3-134">**startPeriod**</span><span class="sxs-lookup"><span data-stu-id="90cd3-134">**startPeriod**</span></span>](onexschema-startperiod-onex-element.md)                         |         | <span data-ttu-id="90cd3-135">Especifica o período de tempo, em segundos, a aguardar antes que um EAPOL-Start seja enviado.</span><span class="sxs-lookup"><span data-stu-id="90cd3-135">Specifies the length of time, in seconds, to wait before an EAPOL-Start is sent.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="90cd3-136">**suplicable**</span><span class="sxs-lookup"><span data-stu-id="90cd3-136">**supplicantMode**</span></span>](onexschema-supplicantmode-onex-element.md)                   |         | <span data-ttu-id="90cd3-137">Especifica o método de transmissão usado para pacotes EAPOL.</span><span class="sxs-lookup"><span data-stu-id="90cd3-137">Specifies the method of transmission used for EAPOL packets.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="90cd3-138">**Escreva**</span><span class="sxs-lookup"><span data-stu-id="90cd3-138">**type**</span></span>](onexschema-type-singlesignon-element.md)                               |         | <span data-ttu-id="90cd3-139">Especifica quando o logon único é executado.</span><span class="sxs-lookup"><span data-stu-id="90cd3-139">Specifies when single sign-on is performed.</span></span> <span data-ttu-id="90cd3-140">Quando definido como `preLogon` , o logon único é executado antes de o usuário fazer logon.</span><span class="sxs-lookup"><span data-stu-id="90cd3-140">When set to `preLogon`, single sign-on is performed before the user logs on.</span></span> <span data-ttu-id="90cd3-141">Quando definido como `postLogon` , o logon único é executado imediatamente após o usuário fazer logon.</span><span class="sxs-lookup"><span data-stu-id="90cd3-141">When set to `postLogon`, single sign-on is performed immediately after the user logs on.</span></span><br/> |
| [<span data-ttu-id="90cd3-142">**userBasedVirtualLan**</span><span class="sxs-lookup"><span data-stu-id="90cd3-142">**userBasedVirtualLan**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md) | <span data-ttu-id="90cd3-143">booleano</span><span class="sxs-lookup"><span data-stu-id="90cd3-143">boolean</span></span> | <span data-ttu-id="90cd3-144">Especifica se a LAN virtual (VLAN) usada pelo dispositivo é alterada com base nas credenciais do usuário.</span><span class="sxs-lookup"><span data-stu-id="90cd3-144">Specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span><br/>                                                                                                                   |



## <a name="remarks"></a><span data-ttu-id="90cd3-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="90cd3-145">Remarks</span></span>

<span data-ttu-id="90cd3-146">Para exibir a lista de elementos filho em uma estrutura do tipo árvore, consulte [elementos do esquema Onex](onexschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="90cd3-146">To view the list of child elements in a tree-like structure, see [OneX Schema Elements](onexschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="90cd3-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90cd3-147">Requirements</span></span>



| <span data-ttu-id="90cd3-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="90cd3-148">Requirement</span></span> | <span data-ttu-id="90cd3-149">Valor</span><span class="sxs-lookup"><span data-stu-id="90cd3-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="90cd3-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90cd3-150">Minimum supported client</span></span><br/> | <span data-ttu-id="90cd3-151">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="90cd3-151">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="90cd3-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90cd3-152">Minimum supported server</span></span><br/> | <span data-ttu-id="90cd3-153">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="90cd3-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="90cd3-154">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="90cd3-154">Redistributable</span></span><br/>          | <span data-ttu-id="90cd3-155">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="90cd3-155">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



 

 




