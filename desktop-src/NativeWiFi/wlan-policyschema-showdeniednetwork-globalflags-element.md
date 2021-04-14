---
description: Especifica se as redes negadas aparecem no assistente conectar-se a uma rede.
ms.assetid: d0a13a80-2532-4383-8946-2536cc1f5e12
title: Elemento showDeniedNetwork (globalFlags)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- showDeniedNetwork
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33049dad00e5fda22e3f739d3dc200a282481a8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502238"
---
# <a name="showdeniednetwork-globalflags-element"></a><span data-ttu-id="48eec-103">Elemento showDeniedNetwork (globalFlags)</span><span class="sxs-lookup"><span data-stu-id="48eec-103">showDeniedNetwork (globalFlags) Element</span></span>

<span data-ttu-id="48eec-104">O elemento **showDeniedNetwork** (globalFlags) especifica se as redes negadas aparecem no assistente **conectar a uma rede** .</span><span class="sxs-lookup"><span data-stu-id="48eec-104">The **showDeniedNetwork** (globalFlags) element specifies whether denied networks appear in the **Connect to a Network** wizard.</span></span> <span data-ttu-id="48eec-105">As redes podem ser negadas pela política de grupo ou pelas configurações do usuário.</span><span class="sxs-lookup"><span data-stu-id="48eec-105">Networks may be denied by group policy or by user settings.</span></span> <span data-ttu-id="48eec-106">Quando **showDeniedNetwork** tem um valor de true, redes negadas aparecem no assistente **conectar-se a uma rede** ; caso contrário, as redes negadas não aparecerão no assistente.</span><span class="sxs-lookup"><span data-stu-id="48eec-106">When **showDeniedNetwork** has a value of TRUE, denied networks appear in the **Connect to a Network** wizard; otherwise, denied networks do not appear in the wizard.</span></span>

<span data-ttu-id="48eec-107">Esse elemento é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="48eec-107">This element is mandatory.</span></span> <span data-ttu-id="48eec-108">Quando um perfil é criado pelo serviço de configuração automática, esse elemento assumirá o valor padrão de FALSE.</span><span class="sxs-lookup"><span data-stu-id="48eec-108">When a profile is created by the AutoConfig service, this element will take the default value of FALSE.</span></span>

``` syntax
<xs:element name="showDeniedNetwork"
    type="boolean"
 />
```

<span data-ttu-id="48eec-109">O elemento **showDeniedNetwork** é definido pelo elemento [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="48eec-109">The **showDeniedNetwork** element is defined by the [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="48eec-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48eec-110">Requirements</span></span>



| <span data-ttu-id="48eec-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="48eec-111">Requirement</span></span> | <span data-ttu-id="48eec-112">Valor</span><span class="sxs-lookup"><span data-stu-id="48eec-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="48eec-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48eec-113">Minimum supported client</span></span><br/> | <span data-ttu-id="48eec-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="48eec-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="48eec-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48eec-115">Minimum supported server</span></span><br/> | <span data-ttu-id="48eec-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="48eec-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="48eec-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="48eec-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="48eec-118">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="48eec-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="48eec-119">**globalFlags**</span><span class="sxs-lookup"><span data-stu-id="48eec-119">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="48eec-120">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="48eec-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="48eec-121">**globalFlags (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="48eec-121">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




