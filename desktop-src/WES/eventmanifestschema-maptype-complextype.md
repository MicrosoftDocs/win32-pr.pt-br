---
title: Tipo complexo MapType
description: Define uma lista de pares de nome/valor.
ms.assetid: 208ae219-8f79-4049-b946-a57b33c97b1b
keywords:
- Log de eventos do tipo complexo MapType
topic_type:
- apiref
api_name:
- MapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4daf6cfe677ab5585ac580e19c868f1bba17de45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644372"
---
# <a name="maptype-complex-type"></a><span data-ttu-id="0e20b-104">Tipo complexo MapType</span><span class="sxs-lookup"><span data-stu-id="0e20b-104">MapType Complex Type</span></span>

<span data-ttu-id="0e20b-105">Define uma lista de pares de nome/valor.</span><span class="sxs-lookup"><span data-stu-id="0e20b-105">Defines a list of name/value pairs.</span></span>

``` syntax
<xs:complexType name="MapType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="valueMap"
            type="ValueMapType"
         />
        <xs:element name="bitMap"
            type="BitMapType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="0e20b-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0e20b-106">Child elements</span></span>



| <span data-ttu-id="0e20b-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="0e20b-107">Element</span></span>                                                          | <span data-ttu-id="0e20b-108">Type</span><span class="sxs-lookup"><span data-stu-id="0e20b-108">Type</span></span>                                                                 | <span data-ttu-id="0e20b-109">Description</span><span class="sxs-lookup"><span data-stu-id="0e20b-109">Description</span></span>                                                                              |
|------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e20b-110">**bitMap**</span><span class="sxs-lookup"><span data-stu-id="0e20b-110">**bitMap**</span></span>](eventmanifestschema-bitmap-maptype-element.md)     | [<span data-ttu-id="0e20b-111">**BitMaptype**</span><span class="sxs-lookup"><span data-stu-id="0e20b-111">**BitMapType**</span></span>](eventmanifestschema-bitmaptype-complextype.md)     | <span data-ttu-id="0e20b-112">Define uma lista de pares de nome/valor que mapeia valores de bits e valores de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0e20b-112">Defines a list of name/value pairs that map bit values and string values.</span></span><br/>     |
| [<span data-ttu-id="0e20b-113">**valueMap**</span><span class="sxs-lookup"><span data-stu-id="0e20b-113">**valueMap**</span></span>](eventmanifestschema-valuemap-maptype-element.md) | [<span data-ttu-id="0e20b-114">**ValueMapType**</span><span class="sxs-lookup"><span data-stu-id="0e20b-114">**ValueMapType**</span></span>](eventmanifestschema-valuemaptype-complextype.md) | <span data-ttu-id="0e20b-115">Define uma lista de pares de nome/valor que mapeia valores inteiros e valores de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0e20b-115">Defines a list of name/value pairs that map integer values and string values.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0e20b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e20b-116">Remarks</span></span>

<span data-ttu-id="0e20b-117">Normalmente, você cria mapas para fornecer valores de cadeia de caracteres enumerados para dados de eventos.</span><span class="sxs-lookup"><span data-stu-id="0e20b-117">Typically, you create maps to provide enumerated string values for event data.</span></span>

## <a name="examples"></a><span data-ttu-id="0e20b-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0e20b-118">Examples</span></span>

<span data-ttu-id="0e20b-119">O exemplo a seguir mostra como especificar um mapa de valor e bitmap.</span><span class="sxs-lookup"><span data-stu-id="0e20b-119">The following example shows how to specify a value map and bitmap.</span></span>


```XML
<maps>
   <valueMap name="MyValueMap">
       <map value="5" message="$(string.value5)"/>
       <map value="45" message="$(string.value45)"/>
   </valueMap>
 
   <bitMap name="MyBitmap">
       <map value="0x8" message="$(string.bit3)/>
       <map value="0x80" message="$(string.bit7)/>
   </bitMap>
</maps>
```



## <a name="requirements"></a><span data-ttu-id="0e20b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e20b-120">Requirements</span></span>



| <span data-ttu-id="0e20b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e20b-121">Requirement</span></span> | <span data-ttu-id="0e20b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0e20b-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0e20b-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e20b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0e20b-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0e20b-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0e20b-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e20b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0e20b-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0e20b-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





