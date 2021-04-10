---
description: Especifica o período de tempo, em segundos, a aguardar antes que um EAPOL-Start seja enviado.
ms.assetid: 6163eeb9-23a8-4e34-ad3f-016946e241e2
title: Elemento startPeriod (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- startPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a583403a354cbefe93387be2d5af06958bbf6b28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296718"
---
# <a name="startperiod-onex-element"></a><span data-ttu-id="05bd8-103">Elemento startPeriod (OneX)</span><span class="sxs-lookup"><span data-stu-id="05bd8-103">startPeriod (OneX) Element</span></span>

<span data-ttu-id="05bd8-104">O elemento startPeriod (OneX) especifica o período de tempo, em segundos, a aguardar antes de um EAPOL-Start ser enviado.</span><span class="sxs-lookup"><span data-stu-id="05bd8-104">The startPeriod (OneX) element specifies the length of time, in seconds, to wait before an EAPOL-Start is sent.</span></span> <span data-ttu-id="05bd8-105">Uma mensagem de EAPOL-Start é enviada para iniciar o processo de autenticação 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="05bd8-105">An EAPOL-Start message is sent to start the 802.1X authentication process.</span></span>

<span data-ttu-id="05bd8-106">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="05bd8-106">This element is optional.</span></span> <span data-ttu-id="05bd8-107">Quando startPeriod não é especificado em um perfil, é usado um valor de 5 segundos.</span><span class="sxs-lookup"><span data-stu-id="05bd8-107">When startPeriod is not specified in a profile, a value of 5 seconds is used.</span></span>

<span data-ttu-id="05bd8-108">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento será ignorado se estiver presente em um perfil.</span><span class="sxs-lookup"><span data-stu-id="05bd8-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="startPeriod">
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
```

<span data-ttu-id="05bd8-109">O elemento **startPeriod** é definido pelo elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="05bd8-109">The **startPeriod** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="05bd8-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05bd8-110">Requirements</span></span>



| <span data-ttu-id="05bd8-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="05bd8-111">Requirement</span></span> | <span data-ttu-id="05bd8-112">Valor</span><span class="sxs-lookup"><span data-stu-id="05bd8-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="05bd8-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05bd8-113">Minimum supported client</span></span><br/> | <span data-ttu-id="05bd8-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="05bd8-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="05bd8-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05bd8-115">Minimum supported server</span></span><br/> | <span data-ttu-id="05bd8-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="05bd8-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="05bd8-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="05bd8-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="05bd8-118">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="05bd8-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="05bd8-119">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="05bd8-119">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="05bd8-120">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="05bd8-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="05bd8-121">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="05bd8-121">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




