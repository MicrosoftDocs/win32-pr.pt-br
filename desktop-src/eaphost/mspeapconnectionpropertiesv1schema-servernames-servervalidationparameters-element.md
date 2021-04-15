---
title: Elemento servernames (ServerValidationParameters) (PEAP)
description: Saiba mais sobre o elemento Servernames (ServerValidationParameters). Esse elemento representa uma lista de nomes de servidor delimitados por ponto e vírgula. | Elemento servernames (ServerValidationParameters) (PEAP)
ms.assetid: 2595daa1-9f1b-40cf-9219-0e7295fdd5c3
keywords:
- Elemento servernames EAPHost
topic_type:
- apiref
api_name:
- ServerNames
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 40aa7ba317b7ba7c3f7a06cce87ef57c2906fe4b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105747262"
---
# <a name="servernames-servervalidationparameters-element-peap"></a><span data-ttu-id="b0cb8-106">Elemento servernames (ServerValidationParameters) (PEAP)</span><span class="sxs-lookup"><span data-stu-id="b0cb8-106">ServerNames (ServerValidationParameters) element (PEAP)</span></span>

<span data-ttu-id="b0cb8-107">O elemento **servernames (ServerValidationParameters)** representa uma lista de nomes de servidor delimitados por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="b0cb8-107">The **ServerNames (ServerValidationParameters)** element represents a list of semicolon delimited server names.</span></span>

``` syntax
<xs:element name="ServerNames"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="b0cb8-108">O elemento **servernames** é definido pelo tipo complexo [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b0cb8-108">The **ServerNames** element is defined by the [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0cb8-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0cb8-109">Remarks</span></span>

<span data-ttu-id="b0cb8-110">Cada nome de servidor é delimitado por ponto e vírgula e pode ser representado por expressões regulares.</span><span class="sxs-lookup"><span data-stu-id="b0cb8-110">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span> <span data-ttu-id="b0cb8-111">O elemento **servernames** é opcional.</span><span class="sxs-lookup"><span data-stu-id="b0cb8-111">The **ServerNames** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0cb8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0cb8-112">Requirements</span></span>



| <span data-ttu-id="b0cb8-113">Função</span><span class="sxs-lookup"><span data-stu-id="b0cb8-113">Role</span></span> | <span data-ttu-id="b0cb8-114">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="b0cb8-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="b0cb8-115">Cliente</span><span class="sxs-lookup"><span data-stu-id="b0cb8-115">Client</span></span><br/> | <span data-ttu-id="b0cb8-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b0cb8-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b0cb8-117">Servidor</span><span class="sxs-lookup"><span data-stu-id="b0cb8-117">Server</span></span><br/> | <span data-ttu-id="b0cb8-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b0cb8-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b0cb8-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0cb8-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="b0cb8-120">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="b0cb8-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b0cb8-121">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="b0cb8-121">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="b0cb8-122">**Possíveis elementos pai imediatos na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="b0cb8-122">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b0cb8-123">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="b0cb8-123">**ServerValidation (EapType)**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="b0cb8-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="b0cb8-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="b0cb8-125">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="b0cb8-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="b0cb8-126">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="b0cb8-126">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="b0cb8-127">Elementos do esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="b0cb8-127">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





