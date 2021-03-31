---
description: Contém o SSID de uma LAN sem fio.
ms.assetid: ed23ccd0-9b44-4c97-a5ed-93e86632b819
title: Elemento Name (SSID)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- name
api_type:
- Schema
api_location: ''
ms.openlocfilehash: dbb1301de2a2d70edf8c61de002c28e48b00a5d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829469"
---
# <a name="name-ssid-element"></a><span data-ttu-id="3bf3b-103">Elemento Name (SSID)</span><span class="sxs-lookup"><span data-stu-id="3bf3b-103">name (SSID) Element</span></span>

<span data-ttu-id="3bf3b-104">O elemento Name (SSID) contém o SSID de uma LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="3bf3b-104">The name (SSID) element contains the SSID of a wireless LAN.</span></span>

``` syntax
<xs:element name="name">
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
```

<span data-ttu-id="3bf3b-105">O elemento é definido pelo elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3bf3b-105">The element is defined by the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bf3b-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="3bf3b-106">Remarks</span></span>

<span data-ttu-id="3bf3b-107">Os nomes diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3bf3b-107">Names are case-sensitive.</span></span>

<span data-ttu-id="3bf3b-108">Embora os elementos [**hex**](wlan-profileschema-hex-ssid-element.md) e **Name** sejam opcionais, pelo menos um elemento **hex** ou **Name** deve aparecer como um filho do elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3bf3b-108">Although the [**hex**](wlan-profileschema-hex-ssid-element.md) and **name** elements are optional, at least one **hex** or **name** element must appear as a child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

<span data-ttu-id="3bf3b-109">Quando as informações de perfil são convertidas em um SSID, o elemento [**hex**](wlan-profileschema-hex-ssid-element.md) é convertido para o SSID (se presente) e o elemento **Name** é ignorado.</span><span class="sxs-lookup"><span data-stu-id="3bf3b-109">When profile information is converted to an SSID, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is converted to the SSID (if present) and the **name** element is ignored.</span></span> <span data-ttu-id="3bf3b-110">Se o elemento **hex** não estiver presente, o elemento **Name** será convertido em um SSID usando a conversão de Unicode em ASCII.</span><span class="sxs-lookup"><span data-stu-id="3bf3b-110">If the **hex** element is not present, the **name** element is converted to an SSID using Unicode to ASCII conversion.</span></span>

<span data-ttu-id="3bf3b-111">Quando um SSID é armazenado em um perfil, o elemento [**hex**](wlan-profileschema-hex-ssid-element.md) sempre é gerado.</span><span class="sxs-lookup"><span data-stu-id="3bf3b-111">When an SSID is stored in a profile, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is always generated.</span></span> <span data-ttu-id="3bf3b-112">O elemento **Name** só será gerado se a conversão de ASCII para Unicode do SSID e a geração do perfil XML forem bem-sucedidas.</span><span class="sxs-lookup"><span data-stu-id="3bf3b-112">The **name** element is only generated if the both the ASCII to Unicode conversion of the SSID and the XML profile generation are successful.</span></span> <span data-ttu-id="3bf3b-113">Algumas informações do SSID original podem ser perdidas quando são convertidas em um **nome**.</span><span class="sxs-lookup"><span data-stu-id="3bf3b-113">Some information from the original SSID may be lost when it is converted to a **name**.</span></span>

<span data-ttu-id="3bf3b-114">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Os caracteres de escape XML, como &, não são exibidos.</span><span class="sxs-lookup"><span data-stu-id="3bf3b-114">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** XML escape characters, such as &, are not displayed.</span></span> <span data-ttu-id="3bf3b-115">Evite usar caracteres de escape XML em nomes SSID para perfis implantados no Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2.</span><span class="sxs-lookup"><span data-stu-id="3bf3b-115">Avoid using XML escape characters in SSID names for profiles deployed on Windows XP with SP3 and Wireless LAN API for Windows XP with SP2.</span></span>

## <a name="examples"></a><span data-ttu-id="3bf3b-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3bf3b-116">Examples</span></span>

<span data-ttu-id="3bf3b-117">Para exibir perfis de exemplo que usam o elemento **Name** , consulte [amostras de perfil sem fio](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="3bf3b-117">To view sample profiles that use the **name** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3bf3b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bf3b-118">Requirements</span></span>



| <span data-ttu-id="3bf3b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bf3b-119">Requirement</span></span> | <span data-ttu-id="3bf3b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3bf3b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="3bf3b-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3bf3b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3bf3b-122">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="3bf3b-122">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3bf3b-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3bf3b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3bf3b-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3bf3b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="3bf3b-125">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="3bf3b-125">Redistributable</span></span><br/>          | <span data-ttu-id="3bf3b-126">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="3bf3b-126">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="3bf3b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="3bf3b-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="3bf3b-128">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="3bf3b-128">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3bf3b-129">**SSID**</span><span class="sxs-lookup"><span data-stu-id="3bf3b-129">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

<span data-ttu-id="3bf3b-130">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="3bf3b-130">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3bf3b-131">**SSID (SSIDConfig)**</span><span class="sxs-lookup"><span data-stu-id="3bf3b-131">**SSID (SSIDConfig)**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




