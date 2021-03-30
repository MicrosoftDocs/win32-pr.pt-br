---
title: Elemento ConfigBlob (EapHostConfig)
description: É usado quando a configuração do método está em formato de BLOB binário em vez de formulário de cadeia de caracteres de texto.
ms.assetid: 2820e0b8-2cd1-40e8-ac0c-a62e73ac3847
keywords:
- Elemento ConfigBlob EAPHost
topic_type:
- apiref
api_name:
- ConfigBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b220c74c6439b4b2cbb0d05a1d540d673e1bd17b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644198"
---
# <a name="configblob-eaphostconfig-element"></a><span data-ttu-id="5d4a0-104">Elemento ConfigBlob (EapHostConfig)</span><span class="sxs-lookup"><span data-stu-id="5d4a0-104">ConfigBlob (EapHostConfig) Element</span></span>

<span data-ttu-id="5d4a0-105">O elemento **ConfigBlob (EapHostConfig)** é usado quando a configuração do método está em formato de blob binário em vez de formulário de cadeia de texto.</span><span class="sxs-lookup"><span data-stu-id="5d4a0-105">The **ConfigBlob (EapHostConfig)** element is used when the method configuration is in binary BLOB form instead of text string form.</span></span>

``` syntax
<xs:element name="ConfigBlob"
    type="hexBinary"
 />
```

<span data-ttu-id="5d4a0-106">O elemento **ConfigBlob** é definido pelo elemento [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5d4a0-106">The **ConfigBlob** element is defined by the [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d4a0-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d4a0-107">Remarks</span></span>

<span data-ttu-id="5d4a0-108">Os elementos [**config**](eaphostconfigschema-config-eaphostconfig-element.md) e **ConfigBlob** não podem ser usados simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="5d4a0-108">The [**Config**](eaphostconfigschema-config-eaphostconfig-element.md) and **ConfigBlob** elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d4a0-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d4a0-109">Requirements</span></span>



| <span data-ttu-id="5d4a0-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d4a0-110">Requirement</span></span> | <span data-ttu-id="5d4a0-111">Valor</span><span class="sxs-lookup"><span data-stu-id="5d4a0-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5d4a0-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d4a0-112">Minimum supported client</span></span><br/> | <span data-ttu-id="5d4a0-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5d4a0-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5d4a0-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d4a0-114">Minimum supported server</span></span><br/> | <span data-ttu-id="5d4a0-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5d4a0-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5d4a0-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5d4a0-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="5d4a0-117">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="5d4a0-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5d4a0-118">**EapHostConfig**</span><span class="sxs-lookup"><span data-stu-id="5d4a0-118">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

<span data-ttu-id="5d4a0-119">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="5d4a0-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="5d4a0-120">**EapHostConfig**</span><span class="sxs-lookup"><span data-stu-id="5d4a0-120">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

[<span data-ttu-id="5d4a0-121">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="5d4a0-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="5d4a0-122">Esquema eaphostconfig</span><span class="sxs-lookup"><span data-stu-id="5d4a0-122">eaphostconfig Schema</span></span>](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





