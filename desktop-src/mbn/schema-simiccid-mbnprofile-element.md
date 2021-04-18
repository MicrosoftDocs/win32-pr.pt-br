---
description: Identifica o número de identificação do SIM para dispositivos GSM.
ms.assetid: 980afba4-fc31-4da0-ba01-6eb8e3db0ac8
title: Elemento SimIccID (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SimIccID
api_type:
- Schema
ms.openlocfilehash: f566253ad3e86b4f7ee7317cf125d9e649034847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750722"
---
# <a name="simiccid-mbnprofile-element"></a><span data-ttu-id="95cd6-103">Elemento SimIccID (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="95cd6-103">SimIccID (MBNProfile) Element</span></span>

<span data-ttu-id="95cd6-104">O elemento **SimIccID (MBNProfile)** identifica o número de identificação do sim para dispositivos GSM.</span><span class="sxs-lookup"><span data-stu-id="95cd6-104">The **SimIccID (MBNProfile)** element identifies the SIM Identification number for GSM devices.</span></span>

<span data-ttu-id="95cd6-105">Esse elemento é opcional e é definido pelo serviço de banda larga móvel para uso interno.</span><span class="sxs-lookup"><span data-stu-id="95cd6-105">This element is optional and is set by the Mobile Broadband service for internal use.</span></span> <span data-ttu-id="95cd6-106">Um aplicativo não deve definir esse campo durante a criação ou atualização de um perfil.</span><span class="sxs-lookup"><span data-stu-id="95cd6-106">An application should not set this field while creating or updating a profile.</span></span>

``` syntax
<xs:element name="SimIccID"
    type="simIccIDType"
 />
```

<span data-ttu-id="95cd6-107">O elemento **SimIccID** é definido pelo elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="95cd6-107">The **SimIccID** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="95cd6-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95cd6-108">Requirements</span></span>



| <span data-ttu-id="95cd6-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="95cd6-109">Requirement</span></span> | <span data-ttu-id="95cd6-110">Valor</span><span class="sxs-lookup"><span data-stu-id="95cd6-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="95cd6-111">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95cd6-111">Minimum supported client</span></span><br/> | <span data-ttu-id="95cd6-112">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="95cd6-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="95cd6-113">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95cd6-113">Minimum supported server</span></span><br/> | <span data-ttu-id="95cd6-114">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="95cd6-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="95cd6-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="95cd6-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="95cd6-116">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="95cd6-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="95cd6-117">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="95cd6-117">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="95cd6-118">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="95cd6-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="95cd6-119">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="95cd6-119">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




