---
description: Especifica se as credenciais do usuário são armazenadas em cache para as conexões subsequentes.
ms.assetid: 65ed03f1-f61e-46f8-a666-91b393618de3
title: Elemento cacheUserData (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- cacheUserData
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8650bb2e5899e96f921d57460c8ba49ffab0ea66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921633"
---
# <a name="cacheuserdata-onex-element"></a><span data-ttu-id="bcfbf-103">Elemento cacheUserData (OneX)</span><span class="sxs-lookup"><span data-stu-id="bcfbf-103">cacheUserData (OneX) Element</span></span>

<span data-ttu-id="bcfbf-104">O elemento cacheUserData (OneX) especifica se as credenciais do usuário são armazenadas em cache para conexões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-104">The cacheUserData (OneX) element specifies whether the user credentials are cached for subsequent connections.</span></span> <span data-ttu-id="bcfbf-105">Quando cacheUserData é TRUE, as credenciais são armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-105">When cacheUserData is TRUE, the credentials are cached.</span></span> <span data-ttu-id="bcfbf-106">Quando cacheUserData é FALSE, as credenciais não são armazenadas em cache e o usuário pode ser solicitado a fornecer credenciais em tentativas de conexão subsequentes.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-106">When cacheUserData is FALSE, the credentials are not cached and the user may be prompted for credentials on subsequent connection attempts.</span></span>

<span data-ttu-id="bcfbf-107">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-107">This element is optional.</span></span> <span data-ttu-id="bcfbf-108">Quando cacheUserData não é especificado em um perfil, as credenciais do usuário são armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-108">When cacheUserData is not specified in a profile, the user credentials are cached.</span></span>

<span data-ttu-id="bcfbf-109">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento será ignorado se estiver presente em um perfil.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="cacheUserData"
    type="boolean"
 />
```

<span data-ttu-id="bcfbf-110">O elemento **cacheUserData** é definido pelo elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="bcfbf-110">The **cacheUserData** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcfbf-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcfbf-111">Requirements</span></span>



| <span data-ttu-id="bcfbf-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcfbf-112">Requirement</span></span> | <span data-ttu-id="bcfbf-113">Valor</span><span class="sxs-lookup"><span data-stu-id="bcfbf-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bcfbf-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcfbf-114">Minimum supported client</span></span><br/> | <span data-ttu-id="bcfbf-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bcfbf-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bcfbf-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcfbf-116">Minimum supported server</span></span><br/> | <span data-ttu-id="bcfbf-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bcfbf-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bcfbf-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="bcfbf-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="bcfbf-119">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="bcfbf-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bcfbf-120">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="bcfbf-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="bcfbf-121">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="bcfbf-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bcfbf-122">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="bcfbf-122">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




