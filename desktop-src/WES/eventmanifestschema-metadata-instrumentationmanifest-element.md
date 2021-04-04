---
title: Elemento Metadata (instrumentationManifest)
description: Contém valores globais que você pode referenciar em outros manifestos.
ms.assetid: 5bf3bb1e-47c9-4d6e-86e3-3316e21b76b3
keywords:
- EventLog de elemento de metadados
topic_type:
- apiref
api_name:
- metadata
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c14dc8772dee66fcce9ff07e9918c11b463aa414
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085189"
---
# <a name="metadata-instrumentationmanifest-element"></a><span data-ttu-id="ce831-104">Elemento Metadata (instrumentationManifest)</span><span class="sxs-lookup"><span data-stu-id="ce831-104">metadata (instrumentationManifest) Element</span></span>

<span data-ttu-id="ce831-105">Contém valores globais que você pode referenciar em outros manifestos.</span><span class="sxs-lookup"><span data-stu-id="ce831-105">Contains global values that you can reference in other manifests.</span></span> <span data-ttu-id="ce831-106">Para obter um exemplo, consulte o arquivo Winmeta.xml incluído na \\ pasta include do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="ce831-106">For an example, see the Winmeta.xml file included in the \\Include folder of the Windows SDK.</span></span>

``` syntax
<xs:element name="metadata"
    type="MetadataType"
 />
```

<span data-ttu-id="ce831-107">O elemento de **metadados** é definido pelo elemento [**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ce831-107">The **metadata** element is defined by the [**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce831-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce831-108">Remarks</span></span>

<span data-ttu-id="ce831-109">Embora você possa criar um manifesto que contenha uma seção de metadados, o serviço não o usará; os únicos metadados que o serviço reconhece são os metadados encontrados no arquivo de Winmeta.xml.</span><span class="sxs-lookup"><span data-stu-id="ce831-109">Although you can create a manifest that contains a metadata section, the service will not use it; the only metadata that the service recognizes is the metadata found in the Winmeta.xml file.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce831-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce831-110">Requirements</span></span>



| <span data-ttu-id="ce831-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce831-111">Requirement</span></span> | <span data-ttu-id="ce831-112">Valor</span><span class="sxs-lookup"><span data-stu-id="ce831-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ce831-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce831-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ce831-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ce831-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ce831-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce831-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ce831-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ce831-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ce831-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce831-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="ce831-118">**Elemento pai**</span><span class="sxs-lookup"><span data-stu-id="ce831-118">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="ce831-119">**instrumentationManifest**</span><span class="sxs-lookup"><span data-stu-id="ce831-119">**instrumentationManifest**</span></span>](eventmanifestschema-instrumentationmanifest-element.md)
</dt> </dl>

 

 





