---
title: Elemento config (EapHostConfig)
description: É usado quando a configuração do método está no formato de texto XML em vez de em um BLOB binário.
ms.assetid: f47bec23-745f-47db-84db-2556beb6a9e9
keywords:
- Elemento de configuração EAPHost
topic_type:
- apiref
api_name:
- Config
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a81c90063a57a9d55d8ab6d9c18486315c187f0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455297"
---
# <a name="config-eaphostconfig-element"></a><span data-ttu-id="1aded-104">Elemento config (EapHostConfig)</span><span class="sxs-lookup"><span data-stu-id="1aded-104">Config (EapHostConfig) Element</span></span>

<span data-ttu-id="1aded-105">O elemento **config (EapHostConfig)** é usado quando a configuração do método está no formato de texto XML em vez de em um blob binário.</span><span class="sxs-lookup"><span data-stu-id="1aded-105">The **Config (EapHostConfig)** element is used when the method configuration is in XML text form instead of a binary BLOB.</span></span>

``` syntax
<xs:element name="Config"
    type="BaseEapMethodConfig"
 />
```

<span data-ttu-id="1aded-106">O elemento **config** é definido pelo elemento [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="1aded-106">The **Config** element is defined by the [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="1aded-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="1aded-107">Remarks</span></span>

<span data-ttu-id="1aded-108">Os elementos **config** e [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) não podem ser usados simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="1aded-108">The **Config** and [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="1aded-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1aded-109">Requirements</span></span>



| <span data-ttu-id="1aded-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="1aded-110">Requirement</span></span> | <span data-ttu-id="1aded-111">Valor</span><span class="sxs-lookup"><span data-stu-id="1aded-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1aded-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1aded-112">Minimum supported client</span></span><br/> | <span data-ttu-id="1aded-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1aded-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1aded-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1aded-114">Minimum supported server</span></span><br/> | <span data-ttu-id="1aded-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1aded-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1aded-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="1aded-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="1aded-117">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="1aded-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="1aded-118">**EapHostConfig**</span><span class="sxs-lookup"><span data-stu-id="1aded-118">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

<span data-ttu-id="1aded-119">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="1aded-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="1aded-120">**EapHostConfig**</span><span class="sxs-lookup"><span data-stu-id="1aded-120">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

[<span data-ttu-id="1aded-121">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="1aded-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="1aded-122">Esquema eaphostconfig</span><span class="sxs-lookup"><span data-stu-id="1aded-122">eaphostconfig Schema</span></span>](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





