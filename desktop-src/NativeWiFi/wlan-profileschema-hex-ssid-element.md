---
description: Contém o SSID de uma LAN sem fio em formato hexadecimal.
ms.assetid: 6c49a3e6-f167-408b-a96f-5b6032108f34
title: Elemento Hex (SSID)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- hex
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6bc214f50788fdc6965a1ce429c5c2919846cf72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762050"
---
# <a name="hex-ssid-element"></a><span data-ttu-id="6e0ab-103">Elemento Hex (SSID)</span><span class="sxs-lookup"><span data-stu-id="6e0ab-103">hex (SSID) Element</span></span>

<span data-ttu-id="6e0ab-104">O elemento Hex (SSID) contém o SSID de uma LAN sem fio no formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-104">The hex (SSID) element contains the SSID of a wireless LAN in hexadecimal format.</span></span>

``` syntax
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
```

<span data-ttu-id="6e0ab-105">O elemento é definido pelo elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6e0ab-105">The element is defined by the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e0ab-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e0ab-106">Remarks</span></span>

<span data-ttu-id="6e0ab-107">Embora os elementos **hex** e [**Name**](wlan-profileschema-name-ssid-element.md) sejam opcionais, pelo menos um elemento **hex** ou [**Name**](wlan-profileschema-name-ssid-element.md) deve aparecer como um filho do elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6e0ab-107">Although the **hex** and [**name**](wlan-profileschema-name-ssid-element.md) elements are optional, at least one **hex** or [**name**](wlan-profileschema-name-ssid-element.md) element must appear as a child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

<span data-ttu-id="6e0ab-108">Quando as informações de perfil são convertidas em um SSID, o elemento **hex** é convertido para o SSID (se presente) e o elemento [**Name**](wlan-profileschema-name-ssid-element.md) é ignorado.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-108">When profile information is converted to an SSID, the **hex** element is converted to the SSID (if present) and the [**name**](wlan-profileschema-name-ssid-element.md) element is ignored .</span></span> <span data-ttu-id="6e0ab-109">Se o elemento **hex** não estiver presente, o elemento [**Name**](wlan-profileschema-name-ssid-element.md) será convertido em um SSID usando a conversão de Unicode em ASCII.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-109">If the **hex** element is not present, the [**name**](wlan-profileschema-name-ssid-element.md) element is converted to an SSID using Unicode to ASCII conversion.</span></span>

<span data-ttu-id="6e0ab-110">Quando um SSID é armazenado em um perfil, o elemento **hex** sempre é gerado.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-110">When an SSID is stored in a profile, the **hex** element is always generated.</span></span> <span data-ttu-id="6e0ab-111">O elemento [**Name**](wlan-profileschema-name-ssid-element.md) só será gerado se a conversão de ASCII para Unicode do SSID e a geração do perfil XML forem bem-sucedidas.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-111">The [**name**](wlan-profileschema-name-ssid-element.md) element is only generated if the both the ASCII to Unicode conversion of the SSID and the XML profile generation are successful.</span></span> <span data-ttu-id="6e0ab-112">Algumas informações do SSID original podem ser perdidas quando são convertidas em um [**nome**](wlan-profileschema-name-ssid-element.md).</span><span class="sxs-lookup"><span data-stu-id="6e0ab-112">Some information from the original SSID may be lost when it is converted to a [**name**](wlan-profileschema-name-ssid-element.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6e0ab-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6e0ab-113">Examples</span></span>

<span data-ttu-id="6e0ab-114">Para exibir um perfil de exemplo que usa o elemento **hex** , consulte [exemplo de perfil FIPS](fips-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="6e0ab-114">To view a sample profile that uses the **hex** element, see [FIPS Profile Sample](fips-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e0ab-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e0ab-115">Requirements</span></span>



| <span data-ttu-id="6e0ab-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e0ab-116">Requirement</span></span> | <span data-ttu-id="6e0ab-117">Valor</span><span class="sxs-lookup"><span data-stu-id="6e0ab-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6e0ab-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e0ab-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6e0ab-119">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="6e0ab-119">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6e0ab-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e0ab-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6e0ab-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6e0ab-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="6e0ab-122">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="6e0ab-122">Redistributable</span></span><br/>          | <span data-ttu-id="6e0ab-123">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="6e0ab-123">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="6e0ab-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e0ab-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="6e0ab-125">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="6e0ab-125">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6e0ab-126">**SSID**</span><span class="sxs-lookup"><span data-stu-id="6e0ab-126">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

<span data-ttu-id="6e0ab-127">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="6e0ab-127">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6e0ab-128">**SSID (SSIDConfig)**</span><span class="sxs-lookup"><span data-stu-id="6e0ab-128">**SSID (SSIDConfig)**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




