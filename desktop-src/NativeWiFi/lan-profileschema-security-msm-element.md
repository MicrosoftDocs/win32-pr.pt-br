---
description: Contém configurações de segurança para redes com fio.
ms.assetid: 08470cf4-3722-4cb9-9877-13eca2f7d04e
title: Elemento Security (MSM) (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 2bd052679f207cd0778f212a73663d4dfd8ce165
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105775683"
---
# <a name="security-msm-element-lan_policy"></a><span data-ttu-id="9494f-103">Elemento Security (MSM) (LAN_policy)</span><span class="sxs-lookup"><span data-stu-id="9494f-103">Security (MSM) Element (LAN_policy)</span></span>

<span data-ttu-id="9494f-104">O elemento Security (MSM) contém configurações de segurança para redes com fio.</span><span class="sxs-lookup"><span data-stu-id="9494f-104">The security (MSM) element contains security settings for wired networks.</span></span> <span data-ttu-id="9494f-105">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="9494f-105">This element is optional.</span></span>

``` syntax
<xs:element name="security">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OneXEnforced"
                type="boolean"
             />
            <xs:element name="OneXEnabled"
                type="boolean"
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

<span data-ttu-id="9494f-106">O elemento **Security** é definido pelo elemento [**msm**](lan-profileschema-msm-lanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="9494f-106">The **security** element is defined by the [**MSM**](lan-profileschema-msm-lanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9494f-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="9494f-107">Child elements</span></span>



| <span data-ttu-id="9494f-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="9494f-108">Element</span></span>                                                                 | <span data-ttu-id="9494f-109">Type</span><span class="sxs-lookup"><span data-stu-id="9494f-109">Type</span></span>    | <span data-ttu-id="9494f-110">Description</span><span class="sxs-lookup"><span data-stu-id="9494f-110">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9494f-111">**OneXEnabled**</span><span class="sxs-lookup"><span data-stu-id="9494f-111">**OneXEnabled**</span></span>](lan-profileschema-onexenabled-security-element.md)   | <span data-ttu-id="9494f-112">booleano</span><span class="sxs-lookup"><span data-stu-id="9494f-112">boolean</span></span> | <span data-ttu-id="9494f-113">Especifica se o serviço de configuração automática para redes com fio tentará a autenticação de porta usando 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="9494f-113">Specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span> <br/>      |
| [<span data-ttu-id="9494f-114">**OneXEnforced**</span><span class="sxs-lookup"><span data-stu-id="9494f-114">**OneXEnforced**</span></span>](lan-profileschema-onexenforced-security-element.md) | <span data-ttu-id="9494f-115">booleano</span><span class="sxs-lookup"><span data-stu-id="9494f-115">boolean</span></span> | <span data-ttu-id="9494f-116">Especifica se o serviço de configuração automática para redes com fio requer o uso do 802.1 X para autenticação de porta.</span><span class="sxs-lookup"><span data-stu-id="9494f-116">Specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="9494f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9494f-117">Requirements</span></span>



| <span data-ttu-id="9494f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9494f-118">Requirement</span></span> | <span data-ttu-id="9494f-119">Valor</span><span class="sxs-lookup"><span data-stu-id="9494f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9494f-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9494f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9494f-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9494f-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9494f-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9494f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9494f-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9494f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9494f-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="9494f-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="9494f-125">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="9494f-125">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="9494f-126">**MSM**</span><span class="sxs-lookup"><span data-stu-id="9494f-126">**MSM**</span></span>](lan-profileschema-msm-lanprofile-element.md)
</dt> <dt>

<span data-ttu-id="9494f-127">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="9494f-127">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="9494f-128">**MSM (LANProfile)**</span><span class="sxs-lookup"><span data-stu-id="9494f-128">**MSM (LANProfile)**</span></span>](lan-profileschema-msm-lanprofile-element.md)
</dt> </dl>

 

 




