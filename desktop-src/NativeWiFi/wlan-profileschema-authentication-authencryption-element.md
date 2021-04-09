---
description: Especifica o método de autenticação a ser usado para se conectar à LAN sem fio.
ms.assetid: fb6c5cce-05d6-41a2-acf4-9ae2713079dd
title: Elemento Authentication (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authentication
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 02895da685c78484c907af51745264abb81086da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164872"
---
# <a name="authentication-authencryption-element"></a><span data-ttu-id="6f85d-103">Elemento Authentication (authEncryption)</span><span class="sxs-lookup"><span data-stu-id="6f85d-103">authentication (authEncryption) Element</span></span>

<span data-ttu-id="6f85d-104">O elemento Authentication (authEncryption) especifica o método de autenticação a ser usado para conectar-se à LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="6f85d-104">The authentication (authEncryption) element specifies the authentication method to be used to connect to the wireless LAN.</span></span>

``` syntax
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
```

<span data-ttu-id="6f85d-105">O elemento é definido pelo elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6f85d-105">The element is defined by the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f85d-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f85d-106">Remarks</span></span>

<span data-ttu-id="6f85d-107">A tabela a seguir descreve os valores de enumeração.</span><span class="sxs-lookup"><span data-stu-id="6f85d-107">The following table describes the enumeration values.</span></span>



| <span data-ttu-id="6f85d-108">Valor</span><span class="sxs-lookup"><span data-stu-id="6f85d-108">Value</span></span>   | <span data-ttu-id="6f85d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f85d-109">Description</span></span>                            |
|---------|----------------------------------------|
| <span data-ttu-id="6f85d-110">Abrir</span><span class="sxs-lookup"><span data-stu-id="6f85d-110">open</span></span>    | <span data-ttu-id="6f85d-111">Abra a autenticação 802,11.</span><span class="sxs-lookup"><span data-stu-id="6f85d-111">Open 802.11 authentication.</span></span>            |
| <span data-ttu-id="6f85d-112">shared</span><span class="sxs-lookup"><span data-stu-id="6f85d-112">shared</span></span>  | <span data-ttu-id="6f85d-113">Autenticação compartilhada 802,11.</span><span class="sxs-lookup"><span data-stu-id="6f85d-113">Shared 802.11 authentication.</span></span>          |
| <span data-ttu-id="6f85d-114">WPA</span><span class="sxs-lookup"><span data-stu-id="6f85d-114">WPA</span></span>     | <span data-ttu-id="6f85d-115">WPA-Enterprise a autenticação 802,11.</span><span class="sxs-lookup"><span data-stu-id="6f85d-115">WPA-Enterprise 802.11 authentication.</span></span>  |
| <span data-ttu-id="6f85d-116">WPAPSK</span><span class="sxs-lookup"><span data-stu-id="6f85d-116">WPAPSK</span></span>  | <span data-ttu-id="6f85d-117">WPA-Personal a autenticação 802,11.</span><span class="sxs-lookup"><span data-stu-id="6f85d-117">WPA-Personal 802.11 authentication.</span></span>    |
| <span data-ttu-id="6f85d-118">WPA2</span><span class="sxs-lookup"><span data-stu-id="6f85d-118">WPA2</span></span>    | <span data-ttu-id="6f85d-119">WPA2-Enterprise a autenticação 802,11.</span><span class="sxs-lookup"><span data-stu-id="6f85d-119">WPA2-Enterprise 802.11 authentication.</span></span> |
| <span data-ttu-id="6f85d-120">WPA2PSK</span><span class="sxs-lookup"><span data-stu-id="6f85d-120">WPA2PSK</span></span> | <span data-ttu-id="6f85d-121">WPA2-Personal a autenticação 802,11.</span><span class="sxs-lookup"><span data-stu-id="6f85d-121">WPA2-Personal 802.11 authentication.</span></span>   |



 

<span data-ttu-id="6f85d-122">Para obter mais informações sobre os métodos de autenticação 802,11, consulte as especificações de [WPA](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access), [802.1 x](https://ieeexplore.ieee.org/document/1438730)e [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="6f85d-122">For more information about 802.11 authentication methods, see the [WPA](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access), [802.1X](https://ieeexplore.ieee.org/document/1438730), and [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specifications.</span></span>

## <a name="examples"></a><span data-ttu-id="6f85d-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6f85d-123">Examples</span></span>

<span data-ttu-id="6f85d-124">Para exibir perfis de exemplo que usam o elemento de **autenticação** , consulte [amostras de perfil sem fio](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="6f85d-124">To view sample profiles that use the **authentication** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f85d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f85d-125">Requirements</span></span>



| <span data-ttu-id="6f85d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f85d-126">Requirement</span></span> | <span data-ttu-id="6f85d-127">Valor</span><span class="sxs-lookup"><span data-stu-id="6f85d-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6f85d-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f85d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6f85d-129">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="6f85d-129">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6f85d-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f85d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6f85d-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6f85d-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="6f85d-132">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="6f85d-132">Redistributable</span></span><br/>          | <span data-ttu-id="6f85d-133">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="6f85d-133">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="6f85d-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f85d-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="6f85d-135">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="6f85d-135">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6f85d-136">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="6f85d-136">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

<span data-ttu-id="6f85d-137">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="6f85d-137">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6f85d-138">**authEncryption (segurança)**</span><span class="sxs-lookup"><span data-stu-id="6f85d-138">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




