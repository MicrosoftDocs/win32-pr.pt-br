---
description: Contém várias configurações para fornecedores de hardware independentes.
ms.assetid: 4ad8c991-7849-41d6-9852-1ecadc372a2d
title: Elemento IHV (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IHV
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d2d2902522c84ebe2939d42301a491521ac8a70f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789515"
---
# <a name="ihv-wlanprofile-element"></a><span data-ttu-id="5a1f6-103">Elemento IHV (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="5a1f6-103">IHV (WLANProfile) Element</span></span>

<span data-ttu-id="5a1f6-104">O elemento IHV (WLANProfile) contém várias configurações para fornecedores de hardware independentes.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-104">The IHV (WLANProfile) element contains various settings for independent hardware vendors.</span></span> <span data-ttu-id="5a1f6-105">Se um perfil incluir configurações de segurança de IHV, eles substituirão qualquer segurança definida pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-105">If a profile includes IHV security settings, they override any Microsoft-defined security.</span></span>

<span data-ttu-id="5a1f6-106">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-106">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
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
```

<span data-ttu-id="5a1f6-107">O elemento é definido pelo elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5a1f6-107">The element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="5a1f6-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5a1f6-108">Child elements</span></span>



| <span data-ttu-id="5a1f6-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="5a1f6-109">Element</span></span>                                                             | <span data-ttu-id="5a1f6-110">Type</span><span class="sxs-lookup"><span data-stu-id="5a1f6-110">Type</span></span>                                                              | <span data-ttu-id="5a1f6-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a1f6-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a1f6-112">**conectividade**</span><span class="sxs-lookup"><span data-stu-id="5a1f6-112">**connectivity**</span></span>](wlan-profileschema-connectivity-ihv-element.md) |                                                                   | <span data-ttu-id="5a1f6-113">Contém configurações de conectividade relacionadas a IHV.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-113">Contains IHV-related connectivity settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="5a1f6-114">**OUI**</span><span class="sxs-lookup"><span data-stu-id="5a1f6-114">**OUI**</span></span>](wlan-profileschema-oui-ouiheader-element.md)             |                                                                   | <span data-ttu-id="5a1f6-115">Contém um hexBinary de 3 bytes que identifica o IHV.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-115">Contains a 3 byte hexBinary that identifies the IHV.</span></span><br/>                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="5a1f6-116">**OUIHeader**</span><span class="sxs-lookup"><span data-stu-id="5a1f6-116">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)       |                                                                   | <span data-ttu-id="5a1f6-117">Identifica o IHV.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-117">Identifies the IHV.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="5a1f6-118">**segurança**</span><span class="sxs-lookup"><span data-stu-id="5a1f6-118">**security**</span></span>](wlan-profileschema-security-ihv-element.md)         |                                                                   | <span data-ttu-id="5a1f6-119">Contém configurações de segurança específicas de IHV.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-119">Contains IHV-specific security settings.</span></span> <span data-ttu-id="5a1f6-120">As configurações de segurança da Microsoft e as configurações de segurança de IHV são mutuamente exclusivas.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-120">Microsoft security settings and IHV security settings are mutually exclusive.</span></span> <span data-ttu-id="5a1f6-121">O perfil inteiro será inválido se ambas as configurações de segurança estiverem presentes.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-121">The entire profile is invalid if both security settings are present.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="5a1f6-122">**Escreva**</span><span class="sxs-lookup"><span data-stu-id="5a1f6-122">**type**</span></span>](wlan-profileschema-type-ouiheader-element.md)           |                                                                   | <span data-ttu-id="5a1f6-123">Contém um hexBinary de 1 byte que é usado para diferenciar NICs pelo mesmo IHV.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-123">Contains a 1 byte hexBinary that is used to differentiate NICs by the same IHV.</span></span><br/>                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="5a1f6-124">**useMSOneX**</span><span class="sxs-lookup"><span data-stu-id="5a1f6-124">**useMSOneX**</span></span>](wlan-profileschema-usemsonex-ihv-element.md)       | [<span data-ttu-id="5a1f6-125">booleano</span><span class="sxs-lookup"><span data-stu-id="5a1f6-125">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="5a1f6-126">Especifica a origem das configurações de segurança 802.1 X usadas por um componente de segurança do IHV.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-126">Specifies the origin of 802.1X security settings used by an IHV security component.</span></span> <span data-ttu-id="5a1f6-127">Quando [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) é verdadeiro, os componentes de segurança de IHV usam configurações 802.1 x definidas pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-127">When [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) is true, IHV security components use Microsoft-defined 802.1X settings.</span></span> <span data-ttu-id="5a1f6-128">Quando **useMSOneX** é false, os componentes de segurança de IHV usam configurações 802.1 x fornecidas pelo fornecedor.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-128">When **useMSOneX** is false, IHV security components use vendor-supplied 802.1X settings.</span></span> <span data-ttu-id="5a1f6-129">Por padrão, **useMSOneX** é false.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-129">By default, **useMSOneX** is false.</span></span> <span data-ttu-id="5a1f6-130">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-130">This element is optional.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5a1f6-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a1f6-131">Requirements</span></span>



| <span data-ttu-id="5a1f6-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a1f6-132">Requirement</span></span> | <span data-ttu-id="5a1f6-133">Valor</span><span class="sxs-lookup"><span data-stu-id="5a1f6-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5a1f6-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a1f6-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5a1f6-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5a1f6-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5a1f6-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a1f6-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5a1f6-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5a1f6-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a1f6-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a1f6-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="5a1f6-139">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="5a1f6-139">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5a1f6-140">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="5a1f6-140">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="5a1f6-141">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="5a1f6-141">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="5a1f6-142">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="5a1f6-142">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
