---
description: Especifica os parâmetros necessários para configurar uma conexão de dados.
ms.assetid: 7a3d3b9d-f799-4927-9c18-04b025788a4a
title: Elemento Context (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Context
api_type:
- Schema
ms.openlocfilehash: dac98101dade85fbbaa63275933885241ef206fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781090"
---
# <a name="context-mbnprofile-element"></a><span data-ttu-id="00acc-103">Elemento Context (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="00acc-103">Context (MBNProfile) Element</span></span>

<span data-ttu-id="00acc-104">O elemento **Context (MBNProfile)** especifica os parâmetros necessários para configurar uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="00acc-104">The **Context (MBNProfile)** element specifies the parameters required to setup a data connection.</span></span>

<span data-ttu-id="00acc-105">O elemento pode ter os seguintes elementos filho.</span><span class="sxs-lookup"><span data-stu-id="00acc-105">The element can have the following child elements.</span></span>

-   [<span data-ttu-id="00acc-106">**AccessString**</span><span class="sxs-lookup"><span data-stu-id="00acc-106">**AccessString**</span></span>](schema-accessstring-contexttype-element.md)
-   [<span data-ttu-id="00acc-107">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="00acc-107">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)
-   [<span data-ttu-id="00acc-108">**Compactação**</span><span class="sxs-lookup"><span data-stu-id="00acc-108">**Compression**</span></span>](schema-compression-contexttype-element.md)
-   [<span data-ttu-id="00acc-109">**AuthProtocol**</span><span class="sxs-lookup"><span data-stu-id="00acc-109">**AuthProtocol**</span></span>](schema-authprotocol-contexttype-element.md)

<span data-ttu-id="00acc-110">Esse elemento pode ter um máximo de uma ocorrência.</span><span class="sxs-lookup"><span data-stu-id="00acc-110">This element can have a maximum of one occurrence.</span></span>

``` syntax
<xs:element name="Context"
    type="contextType"
 />
```

<span data-ttu-id="00acc-111">O elemento **Context** é definido pelo elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="00acc-111">The **Context** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="00acc-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00acc-112">Requirements</span></span>



| <span data-ttu-id="00acc-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="00acc-113">Requirement</span></span> | <span data-ttu-id="00acc-114">Valor</span><span class="sxs-lookup"><span data-stu-id="00acc-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="00acc-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00acc-115">Minimum supported client</span></span><br/> | <span data-ttu-id="00acc-116">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="00acc-116">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="00acc-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00acc-117">Minimum supported server</span></span><br/> | <span data-ttu-id="00acc-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="00acc-118">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="00acc-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="00acc-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="00acc-120">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="00acc-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="00acc-121">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="00acc-121">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="00acc-122">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="00acc-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="00acc-123">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="00acc-123">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




