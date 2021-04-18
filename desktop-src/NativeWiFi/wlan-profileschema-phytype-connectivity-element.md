---
description: Especifica o padrão de LAN sem fio 802,11 usado em uma LAN sem fio.
ms.assetid: 19582ff0-59bd-4c93-8c92-0135e6e025d2
title: Elemento phyType (conectividade)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- phyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 71a58e464528136244cec745aed2e59c6fea737d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810530"
---
# <a name="phytype-connectivity-element"></a><span data-ttu-id="b3c9a-103">Elemento phyType (conectividade)</span><span class="sxs-lookup"><span data-stu-id="b3c9a-103">phyType (connectivity) Element</span></span>

<span data-ttu-id="b3c9a-104">O elemento phyType (conectividade) especifica o padrão de LAN sem fio 802,11 usado em uma LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="b3c9a-104">The phyType (connectivity) element specifies the 802.11 wireless LAN standard used on a wireless LAN.</span></span>

<span data-ttu-id="b3c9a-105">Você pode especificar vários **phyType** s.</span><span class="sxs-lookup"><span data-stu-id="b3c9a-105">You can specify multiple **phyType** s.</span></span> <span data-ttu-id="b3c9a-106">Se nenhum **phyType** for especificado, o perfil poderá ser usado para se conectar a qualquer **phyType**.</span><span class="sxs-lookup"><span data-stu-id="b3c9a-106">If no **phyType** is specified, the profile can be used to connect to any **phyType**.</span></span> <span data-ttu-id="b3c9a-107">O valor "n" só tem suporte no Windows Vista com Service Pack 1 (SP1) e versões posteriores do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b3c9a-107">The value "n" is only supported on Windows Vista with Service Pack 1 (SP1) and later versions of the operating system.</span></span>

<span data-ttu-id="b3c9a-108">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="b3c9a-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
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
```

<span data-ttu-id="b3c9a-109">O elemento é definido pelo elemento de [**conectividade**](wlan-profileschema-connectivity-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b3c9a-109">The element is defined by the [**connectivity**](wlan-profileschema-connectivity-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3c9a-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3c9a-110">Requirements</span></span>



| <span data-ttu-id="b3c9a-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3c9a-111">Requirement</span></span> | <span data-ttu-id="b3c9a-112">Valor</span><span class="sxs-lookup"><span data-stu-id="b3c9a-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b3c9a-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3c9a-113">Minimum supported client</span></span><br/> | <span data-ttu-id="b3c9a-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3c9a-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b3c9a-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3c9a-115">Minimum supported server</span></span><br/> | <span data-ttu-id="b3c9a-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b3c9a-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b3c9a-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3c9a-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="b3c9a-118">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="b3c9a-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b3c9a-119">**conectividade**</span><span class="sxs-lookup"><span data-stu-id="b3c9a-119">**connectivity**</span></span>](wlan-profileschema-connectivity-msm-element.md)
</dt> <dt>

<span data-ttu-id="b3c9a-120">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="b3c9a-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b3c9a-121">**conectividade (MSM)**</span><span class="sxs-lookup"><span data-stu-id="b3c9a-121">**connectivity (MSM)**</span></span>](wlan-profileschema-connectivity-msm-element.md)
</dt> </dl>

 

 




