---
description: Especifica se o serviço de configuração automática para redes com fio requer o uso do 802.1 X para autenticação de porta.
ms.assetid: fb01be74-46ad-4d8c-be4c-50ae05a0c33b
title: Elemento OneXEnforced (segurança)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnforced
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e6656238b0745f8bfef9aff5bcb0b80775dd1da2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789748"
---
# <a name="onexenforced-security-element"></a><span data-ttu-id="ec3b0-103">Elemento OneXEnforced (segurança)</span><span class="sxs-lookup"><span data-stu-id="ec3b0-103">OneXEnforced (security) Element</span></span>

<span data-ttu-id="ec3b0-104">O elemento **OneXEnforced** (Security) especifica se o serviço de configuração automática para redes com fio requer o uso do 802.1 x para autenticação de porta.</span><span class="sxs-lookup"><span data-stu-id="ec3b0-104">The **OneXEnforced** (security) element specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <span data-ttu-id="ec3b0-105">Quando **OneXEnforced** é true, o serviço de configuração automática deve usar 802.1 x para autenticação de porta.</span><span class="sxs-lookup"><span data-stu-id="ec3b0-105">When **OneXEnforced** is TRUE, the automatic configuration service must use 802.1X for port authentication.</span></span> <span data-ttu-id="ec3b0-106">Quando **OneXEnforced** for false, o serviço de configuração automática tentará usar 802.1 x para autenticação de porta, mas o serviço fará o fallback para sem autenticação se a autenticação 802.1 x falhar por qualquer motivo.</span><span class="sxs-lookup"><span data-stu-id="ec3b0-106">When **OneXEnforced** is FALSE, then the automatic configuration service will attempt to use 802.1X for port authentication, but the service will fall back to no authentication if 802.1X authentication fails for any reason.</span></span>

<span data-ttu-id="ec3b0-107">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="ec3b0-107">This element is optional.</span></span> <span data-ttu-id="ec3b0-108">O valor padrão é FALSE.</span><span class="sxs-lookup"><span data-stu-id="ec3b0-108">The default value is FALSE.</span></span>

<span data-ttu-id="ec3b0-109">Esse elemento tem apenas um valor significativo se [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md) for true.</span><span class="sxs-lookup"><span data-stu-id="ec3b0-109">This element only has a meaningful value if [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md) is TRUE.</span></span> <span data-ttu-id="ec3b0-110">Se **OneXEnabled** for false, o valor desse elemento será ignorado.</span><span class="sxs-lookup"><span data-stu-id="ec3b0-110">If **OneXEnabled** is FALSE, then the value of this element is ignored.</span></span>

``` syntax
<xs:element name="OneXEnforced"
    type="boolean"
 />
```

<span data-ttu-id="ec3b0-111">O elemento **OneXEnforced** é definido pelo elemento [**Security**](lan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3b0-111">The **OneXEnforced** element is defined by the [**security**](lan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec3b0-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec3b0-112">Requirements</span></span>



| <span data-ttu-id="ec3b0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec3b0-113">Requirement</span></span> | <span data-ttu-id="ec3b0-114">Valor</span><span class="sxs-lookup"><span data-stu-id="ec3b0-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ec3b0-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec3b0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ec3b0-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ec3b0-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ec3b0-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec3b0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ec3b0-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ec3b0-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ec3b0-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec3b0-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="ec3b0-120">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="ec3b0-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ec3b0-121">**segurança**</span><span class="sxs-lookup"><span data-stu-id="ec3b0-121">**security**</span></span>](lan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="ec3b0-122">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="ec3b0-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ec3b0-123">**segurança (MSM)**</span><span class="sxs-lookup"><span data-stu-id="ec3b0-123">**security (MSM)**</span></span>](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




