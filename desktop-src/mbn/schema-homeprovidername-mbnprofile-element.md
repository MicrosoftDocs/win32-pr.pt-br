---
description: Identifica o nome do provedor de página inicial para o cartão SIM/dispositivo especificado.
ms.assetid: 05d65091-5a1d-427a-8f51-1e1b9d189571
title: Elemento HomeProviderName (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HomeProviderName
api_type:
- Schema
ms.openlocfilehash: 3d0af51e4873915838f2d55f683d07e9098aad3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647097"
---
# <a name="homeprovidername-mbnprofile-element"></a><span data-ttu-id="704f8-103">Elemento HomeProviderName (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="704f8-103">HomeProviderName (MBNProfile) Element</span></span>

<span data-ttu-id="704f8-104">O elemento **HomeProviderName (MBNProfile)** identifica o nome do provedor de Home para o cartão Sim/dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="704f8-104">The **HomeProviderName (MBNProfile)** element identifies the name of Home provider for the given SIM/Device.</span></span>

<span data-ttu-id="704f8-105">Esse elemento é opcional e é definido pelo serviço de banda larga móvel para uso interno.</span><span class="sxs-lookup"><span data-stu-id="704f8-105">This element is optional and is set by the Mobile Broadband service for internal use.</span></span> <span data-ttu-id="704f8-106">Um aplicativo não deve definir esse campo durante a criação ou atualização de um perfil.</span><span class="sxs-lookup"><span data-stu-id="704f8-106">An application should not set this field while creating or updating a profile.</span></span>

``` syntax
<xs:element name="HomeProviderName"
    type="providerNameType"
 />
```

<span data-ttu-id="704f8-107">O elemento **HomeProviderName** é definido pelo elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="704f8-107">The **HomeProviderName** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="704f8-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="704f8-108">Requirements</span></span>



| <span data-ttu-id="704f8-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="704f8-109">Requirement</span></span> | <span data-ttu-id="704f8-110">Valor</span><span class="sxs-lookup"><span data-stu-id="704f8-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="704f8-111">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="704f8-111">Minimum supported client</span></span><br/> | <span data-ttu-id="704f8-112">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="704f8-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="704f8-113">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="704f8-113">Minimum supported server</span></span><br/> | <span data-ttu-id="704f8-114">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="704f8-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="704f8-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="704f8-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="704f8-116">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="704f8-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="704f8-117">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="704f8-117">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="704f8-118">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="704f8-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="704f8-119">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="704f8-119">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




