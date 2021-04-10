---
description: Especifica se o serviço de configuração automática para redes com fio tentará a autenticação de porta usando 802.1 X.
ms.assetid: ab6cfc59-9cfd-45d3-ad27-306ad4f6d4e1
title: Elemento OneXEnabled (segurança)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnabled
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9c76fce3b42cff648d03f520ddeb569a39e99f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170411"
---
# <a name="onexenabled-security-element"></a><span data-ttu-id="af965-103">Elemento OneXEnabled (segurança)</span><span class="sxs-lookup"><span data-stu-id="af965-103">OneXEnabled (security) Element</span></span>

<span data-ttu-id="af965-104">O elemento **OneXEnabled** (Security) especifica se o serviço de configuração automática para redes com fio tentará a autenticação de porta usando 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="af965-104">The **OneXEnabled** (security) element specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span> <span data-ttu-id="af965-105">Quando **OneXEnabled** é false, o serviço de configuração automática nunca usa 802.1 x para autenticação de porta.</span><span class="sxs-lookup"><span data-stu-id="af965-105">When **OneXEnabled** is FALSE, the automatic configuration service never uses 802.1X for port authentication.</span></span> <span data-ttu-id="af965-106">Quando **OneXEnabled** é true, o serviço de configuração automática tenta a autenticação de porta usando 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="af965-106">When **OneXEnabled** is TRUE, then the automatic configuration service attempts port authentication using 802.1X.</span></span>

<span data-ttu-id="af965-107">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="af965-107">This element is optional.</span></span> <span data-ttu-id="af965-108">O valor padrão é TRUE.</span><span class="sxs-lookup"><span data-stu-id="af965-108">The default value is TRUE.</span></span> <span data-ttu-id="af965-109">Quando **OneXEnabled** não é especificado em um perfil, o 802.1 x pode ser usado para autenticação de porta.</span><span class="sxs-lookup"><span data-stu-id="af965-109">When **OneXEnabled** is not specified in a profile, then 802.1X may be used for port authentication.</span></span>

``` syntax
<xs:element name="OneXEnabled"
    type="boolean"
 />
```

<span data-ttu-id="af965-110">O elemento **OneXEnabled** é definido pelo elemento [**Security**](lan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="af965-110">The **OneXEnabled** element is defined by the [**security**](lan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="af965-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af965-111">Requirements</span></span>



| <span data-ttu-id="af965-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="af965-112">Requirement</span></span> | <span data-ttu-id="af965-113">Valor</span><span class="sxs-lookup"><span data-stu-id="af965-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="af965-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af965-114">Minimum supported client</span></span><br/> | <span data-ttu-id="af965-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="af965-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="af965-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af965-116">Minimum supported server</span></span><br/> | <span data-ttu-id="af965-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="af965-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="af965-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="af965-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="af965-119">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="af965-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="af965-120">**segurança**</span><span class="sxs-lookup"><span data-stu-id="af965-120">**security**</span></span>](lan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="af965-121">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="af965-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="af965-122">**segurança (MSM)**</span><span class="sxs-lookup"><span data-stu-id="af965-122">**security (MSM)**</span></span>](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




