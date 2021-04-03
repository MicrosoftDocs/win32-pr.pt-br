---
description: Contém um SSID para uma LAN sem fio.
ms.assetid: fb3466c4-a586-424b-96e2-ba287c99a1d9
title: Elemento SSID (SSIDConfig)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSID
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 644a4afbd10fbfff870007befda964fc9babd593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828845"
---
# <a name="ssid-ssidconfig-element"></a><span data-ttu-id="f0235-103">Elemento SSID (SSIDConfig)</span><span class="sxs-lookup"><span data-stu-id="f0235-103">SSID (SSIDConfig) Element</span></span>

<span data-ttu-id="f0235-104">O elemento SSID (SSIDConfig) contém um SSID para uma LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="f0235-104">The SSID (SSIDConfig) element contains an SSID for a wireless LAN.</span></span>

<span data-ttu-id="f0235-105">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** No máximo um elemento **SSID** pode aparecer em um perfil.</span><span class="sxs-lookup"><span data-stu-id="f0235-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** At most one **SSID** element can appear in a profile.</span></span>

``` syntax
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
```

<span data-ttu-id="f0235-106">O elemento **SSID** é definido pelo elemento [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f0235-106">The **SSID** element is defined by the [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f0235-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f0235-107">Child elements</span></span>



| <span data-ttu-id="f0235-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="f0235-108">Element</span></span>                                              | <span data-ttu-id="f0235-109">Type</span><span class="sxs-lookup"><span data-stu-id="f0235-109">Type</span></span> | <span data-ttu-id="f0235-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f0235-110">Description</span></span>                                                           |
|------------------------------------------------------|------|-----------------------------------------------------------------------|
| [<span data-ttu-id="f0235-111">**hex**</span><span class="sxs-lookup"><span data-stu-id="f0235-111">**hex**</span></span>](wlan-profileschema-hex-ssid-element.md)   |      | <span data-ttu-id="f0235-112">Contém o SSID de uma LAN sem fio em formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="f0235-112">Contains the SSID of a wireless LAN in hexadecimal format.</span></span><br/> |
| [<span data-ttu-id="f0235-113">**nomes**</span><span class="sxs-lookup"><span data-stu-id="f0235-113">**name**</span></span>](wlan-profileschema-name-ssid-element.md) |      | <span data-ttu-id="f0235-114">Contém o SSID para uma LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="f0235-114">Contains the SSID for a wireless LAN.</span></span><br/>                      |



## <a name="remarks"></a><span data-ttu-id="f0235-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0235-115">Remarks</span></span>

<span data-ttu-id="f0235-116">Embora os elementos [**hex**](wlan-profileschema-hex-ssid-element.md) e [**Name**](wlan-profileschema-name-ssid-element.md) sejam opcionais, pelo menos um elemento **hex** ou [**Name**](wlan-profileschema-name-ssid-element.md) deve aparecer como um filho do elemento **SSID** .</span><span class="sxs-lookup"><span data-stu-id="f0235-116">Although the [**hex**](wlan-profileschema-hex-ssid-element.md) and [**name**](wlan-profileschema-name-ssid-element.md) elements are optional, at least one **hex** or [**name**](wlan-profileschema-name-ssid-element.md) element must appear as a child of the **SSID** element.</span></span>

<span data-ttu-id="f0235-117">Quando as informações de perfil são convertidas em um SSID, o elemento [**hex**](wlan-profileschema-hex-ssid-element.md) é convertido para o SSID (se presente) e o elemento [**Name**](wlan-profileschema-name-ssid-element.md) é ignorado.</span><span class="sxs-lookup"><span data-stu-id="f0235-117">When profile information is converted to an SSID, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is converted to the SSID (if present) and the [**name**](wlan-profileschema-name-ssid-element.md) element is ignored.</span></span> <span data-ttu-id="f0235-118">Se o elemento **hex** não estiver presente, o elemento [**Name**](wlan-profileschema-name-ssid-element.md) será convertido em um SSID usando a conversão de Unicode em ASCII.</span><span class="sxs-lookup"><span data-stu-id="f0235-118">If the **hex** element is not present, the [**name**](wlan-profileschema-name-ssid-element.md) element is converted to an SSID using Unicode to ASCII conversion.</span></span>

<span data-ttu-id="f0235-119">Quando um SSID é armazenado em um perfil, o elemento [**hex**](wlan-profileschema-hex-ssid-element.md) sempre é gerado.</span><span class="sxs-lookup"><span data-stu-id="f0235-119">When an SSID is stored in a profile, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is always generated.</span></span> <span data-ttu-id="f0235-120">O elemento [**Name**](wlan-profileschema-name-ssid-element.md) só será gerado se a conversão de ASCII para Unicode do SSID e a geração do perfil XML forem bem-sucedidas.</span><span class="sxs-lookup"><span data-stu-id="f0235-120">The [**name**](wlan-profileschema-name-ssid-element.md) element is only generated if the both the ASCII to Unicode conversion of the SSID and the XML profile generation are successful.</span></span> <span data-ttu-id="f0235-121">Algumas informações do SSID original podem ser perdidas quando são convertidas em um [**nome**](wlan-profileschema-name-ssid-element.md).</span><span class="sxs-lookup"><span data-stu-id="f0235-121">Some information from the original SSID may be lost when it is converted to a [**name**](wlan-profileschema-name-ssid-element.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f0235-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f0235-122">Examples</span></span>

<span data-ttu-id="f0235-123">Para exibir perfis de exemplo que usam o elemento **SSID** , consulte [amostras de perfil sem fio](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="f0235-123">To view sample profiles that use the **SSID** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0235-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0235-124">Requirements</span></span>



| <span data-ttu-id="f0235-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0235-125">Requirement</span></span> | <span data-ttu-id="f0235-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f0235-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f0235-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0235-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f0235-128">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="f0235-128">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f0235-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0235-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f0235-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f0235-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="f0235-131">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="f0235-131">Redistributable</span></span><br/>          | <span data-ttu-id="f0235-132">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="f0235-132">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="f0235-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0235-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="f0235-134">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="f0235-134">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f0235-135">**SSIDConfig**</span><span class="sxs-lookup"><span data-stu-id="f0235-135">**SSIDConfig**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="f0235-136">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="f0235-136">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f0235-137">**SSIDConfig (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="f0235-137">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




