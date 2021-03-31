---
description: Indica se a conexão com uma LAN sem fio deve ser automática ou iniciada pelo usuário.
ms.assetid: 0fad8392-3053-494b-9b30-1db85408a437
title: Elemento ConnectionMode (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectionMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 3dafb9561bf8b5e3c5c66eb23bd5e286cbd38118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647713"
---
# <a name="connectionmode-wlanprofile-element"></a><span data-ttu-id="7abe5-103">Elemento ConnectionMode (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="7abe5-103">connectionMode (WLANProfile) Element</span></span>

<span data-ttu-id="7abe5-104">O elemento ConnectionMode (WLANProfile) indica se a conexão com uma LAN sem fio deve ser automática ou iniciada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="7abe5-104">The connectionMode (WLANProfile) element indicates whether connection to a wireless LAN should be automatic or initiated by user.</span></span>

<span data-ttu-id="7abe5-105">Se [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) for definido como ESS, esse valor poderá ser automático ou manual.</span><span class="sxs-lookup"><span data-stu-id="7abe5-105">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to ESS, this value can be either auto or manual.</span></span> <span data-ttu-id="7abe5-106">O valor padrão será auto se esse elemento estiver ausente.</span><span class="sxs-lookup"><span data-stu-id="7abe5-106">The default value is auto if this element is absent.</span></span>

<span data-ttu-id="7abe5-107">Se [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) for definido como IBSS, esse valor deverá ser manual.</span><span class="sxs-lookup"><span data-stu-id="7abe5-107">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to IBSS, this value must be manual.</span></span>

``` syntax
<xs:element name="connectionMode">
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
```

<span data-ttu-id="7abe5-108">O elemento **ConnectionMode** é definido pelo elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7abe5-108">The **connectionMode** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="7abe5-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="7abe5-109">Remarks</span></span>

<span data-ttu-id="7abe5-110">A tabela a seguir descreve os valores de enumeração.</span><span class="sxs-lookup"><span data-stu-id="7abe5-110">The following table describes the enumeration values.</span></span>



| <span data-ttu-id="7abe5-111">Valor</span><span class="sxs-lookup"><span data-stu-id="7abe5-111">Value</span></span>  | <span data-ttu-id="7abe5-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="7abe5-112">Description</span></span>                                                                                                |
|--------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7abe5-113">auto</span><span class="sxs-lookup"><span data-stu-id="7abe5-113">auto</span></span>   | <span data-ttu-id="7abe5-114">A conexão com a rede sem fio deve ser iniciada automaticamente sempre que a rede estiver no intervalo.</span><span class="sxs-lookup"><span data-stu-id="7abe5-114">The connection to the wireless network should be initiated automatically whenever the network is in range.</span></span> |
| <span data-ttu-id="7abe5-115">manual</span><span class="sxs-lookup"><span data-stu-id="7abe5-115">manual</span></span> | <span data-ttu-id="7abe5-116">A conexão com a rede sem fio só é iniciada peloda mediante a solicitação explícita de um usuário.</span><span class="sxs-lookup"><span data-stu-id="7abe5-116">The connection to the wireless network is only initated upon the explicit request of a user.</span></span>               |



 

## <a name="examples"></a><span data-ttu-id="7abe5-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7abe5-117">Examples</span></span>

<span data-ttu-id="7abe5-118">Para exibir perfis de exemplo que usam o elemento **ConnectionMode** , consulte [amostras de perfil sem fio](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="7abe5-118">To view sample profiles that use the **connectionMode** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7abe5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7abe5-119">Requirements</span></span>



| <span data-ttu-id="7abe5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7abe5-120">Requirement</span></span> | <span data-ttu-id="7abe5-121">Valor</span><span class="sxs-lookup"><span data-stu-id="7abe5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7abe5-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7abe5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7abe5-123">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="7abe5-123">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7abe5-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7abe5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7abe5-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7abe5-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="7abe5-126">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="7abe5-126">Redistributable</span></span><br/>          | <span data-ttu-id="7abe5-127">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="7abe5-127">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="7abe5-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="7abe5-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="7abe5-129">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="7abe5-129">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="7abe5-130">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="7abe5-130">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="7abe5-131">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="7abe5-131">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="7abe5-132">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="7abe5-132">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




