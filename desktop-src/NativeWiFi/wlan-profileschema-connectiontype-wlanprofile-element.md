---
description: Indica o modo de operação da rede.
ms.assetid: b71de38a-6373-4d96-90dd-a3ad4a7de074
title: Elemento ConnectionType (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectionType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1e7b456260c656ebb3d64b6a3732fe97ca3ca488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827504"
---
# <a name="connectiontype-wlanprofile-element"></a><span data-ttu-id="fce75-103">Elemento ConnectionType (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="fce75-103">connectionType (WLANProfile) Element</span></span>

<span data-ttu-id="fce75-104">O elemento ConnectionType (WLANProfile) indica o modo de operação da rede.</span><span class="sxs-lookup"><span data-stu-id="fce75-104">The connectionType (WLANProfile) element indicates the operating mode of the network.</span></span>

<span data-ttu-id="fce75-105">Um valor de **ESS** indica uma rede de infraestrutura, enquanto **IBSS** indica uma rede ad hoc.</span><span class="sxs-lookup"><span data-stu-id="fce75-105">A value of **ESS** indicates an infrastructure network, while **IBSS** indicates an ad-hoc network.</span></span>

``` syntax
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
```

<span data-ttu-id="fce75-106">O elemento **ConnectionType** é definido pelo elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="fce75-106">The **connectionType** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="fce75-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fce75-107">Examples</span></span>

<span data-ttu-id="fce75-108">Para exibir perfis de exemplo que usam o elemento **ConnectionType** , consulte [amostras de perfil sem fio](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="fce75-108">To view sample profiles that use the **connectionType** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fce75-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fce75-109">Requirements</span></span>



| <span data-ttu-id="fce75-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="fce75-110">Requirement</span></span> | <span data-ttu-id="fce75-111">Valor</span><span class="sxs-lookup"><span data-stu-id="fce75-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fce75-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fce75-112">Minimum supported client</span></span><br/> | <span data-ttu-id="fce75-113">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="fce75-113">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fce75-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fce75-114">Minimum supported server</span></span><br/> | <span data-ttu-id="fce75-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fce75-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="fce75-116">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="fce75-116">Redistributable</span></span><br/>          | <span data-ttu-id="fce75-117">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="fce75-117">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="fce75-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="fce75-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="fce75-119">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="fce75-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="fce75-120">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="fce75-120">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="fce75-121">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="fce75-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="fce75-122">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="fce75-122">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




