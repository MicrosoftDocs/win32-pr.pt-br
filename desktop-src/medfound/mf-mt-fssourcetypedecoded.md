---
description: Especifica se um decodificador pode usar os carimbos de data/hora (DTS) ao definir carimbos de data/hora.
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ad80b0b7b29677ed0bee2f86a2c12c56c08441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790437"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a><span data-ttu-id="cea97-103">\_ \_ Atributo FSSourceTypeDecoded MF MT</span><span class="sxs-lookup"><span data-stu-id="cea97-103">MF\_MT\_FSSourceTypeDecoded attribute</span></span>

<span data-ttu-id="cea97-104">Especifica que um tipo de mídia é decodificado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="cea97-104">Specifies that a media type is auto-decoded.</span></span>

## <a name="data-type"></a><span data-ttu-id="cea97-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="cea97-105">Data type</span></span>

<span data-ttu-id="cea97-106">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="cea97-106">**BOOL** stored as **UINT32**</span></span>


## <a name="remarks"></a><span data-ttu-id="cea97-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="cea97-107">Remarks</span></span>
<span data-ttu-id="cea97-108">Um tipo de mídia é marcado como um atributo para indicar que isso não existe na origem física e é sintetizado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="cea97-108">A media type is marked an attribute to indicate this doesn't exist on the physical source and is synthesized by the pipeline.</span></span> <span data-ttu-id="cea97-109">Um valor de 1 (TRUE) indica que o tipo de mídia está sintetizado.</span><span class="sxs-lookup"><span data-stu-id="cea97-109">A value of 1 (TRUE) indicates that the media type is synthesized.</span></span> <span data-ttu-id="cea97-110">Um valor de 0 (FALSE) ou o valor não está presente, indica que ele não é.</span><span class="sxs-lookup"><span data-stu-id="cea97-110">A value of 0 (FALSE), or the value not being present, indicates that it is not.</span></span>

<span data-ttu-id="cea97-111">Na versão atual, esse atributo deve ser especificado usando o seguinte valor de GUID em vez da constante de MD_MT_FSSourceTypeDecoded:</span><span class="sxs-lookup"><span data-stu-id="cea97-111">In the current release, this attribute should be specified using the following GUID value rather than the MD_MT_FSSourceTypeDecoded constant:</span></span>

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a><span data-ttu-id="cea97-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cea97-112">Requirements</span></span>



| <span data-ttu-id="cea97-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="cea97-113">Requirement</span></span> | <span data-ttu-id="cea97-114">Valor</span><span class="sxs-lookup"><span data-stu-id="cea97-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cea97-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cea97-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cea97-116">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cea97-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="cea97-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cea97-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cea97-118">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cea97-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |



## <a name="see-also"></a><span data-ttu-id="cea97-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="cea97-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cea97-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cea97-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




