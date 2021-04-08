---
description: Obtém ou define a velocidade de decodificação de vídeo.
ms.assetid: 76F7013D-C172-4D31-93BC-EA3D186EB14C
title: Propriedade AVDecVideoFastDecodeMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355c085731befedbcb9245a67870d9d609a92c6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087854"
---
# <a name="avdecvideofastdecodemode-property"></a><span data-ttu-id="d2c44-103">Propriedade AVDecVideoFastDecodeMode</span><span class="sxs-lookup"><span data-stu-id="d2c44-103">AVDecVideoFastDecodeMode property</span></span>

<span data-ttu-id="d2c44-104">Obtém ou define a velocidade de decodificação de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d2c44-104">Gets or sets the video decoding speed.</span></span>

## <a name="data-type"></a><span data-ttu-id="d2c44-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d2c44-105">Data type</span></span>

<span data-ttu-id="d2c44-106">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="d2c44-106">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d2c44-107">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="d2c44-107">Property GUID</span></span>

<span data-ttu-id="d2c44-108">**CODECAPI \_ AVDecVideoFastDecodeMode**</span><span class="sxs-lookup"><span data-stu-id="d2c44-108">**CODECAPI\_AVDecVideoFastDecodeMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="d2c44-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d2c44-109">Property value</span></span>

<span data-ttu-id="d2c44-110">O valor dessa propriedade pode variar de 0 a 32, onde 0 indica que a decodificação normal e 32 é o modo de decodificação mais rápida.</span><span class="sxs-lookup"><span data-stu-id="d2c44-110">The value of this property can range from 0 to 32, where 0 indicates normal decoding and 32 is the fastest decoding mode.</span></span> <span data-ttu-id="d2c44-111">O comportamento exato depende da implementação do decodificador.</span><span class="sxs-lookup"><span data-stu-id="d2c44-111">The exact behavior depends on the decoder implementation.</span></span> <span data-ttu-id="d2c44-112">Nem todo incremento entre 1 e 32 define necessariamente é um modo distinto.</span><span class="sxs-lookup"><span data-stu-id="d2c44-112">Not every increment between 1 and 32 necessarily defines is a distinct mode.</span></span>

<span data-ttu-id="d2c44-113">A enumeração [**eAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode) contém alguns modos predefinidos para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d2c44-113">The [**eAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode) enumeration contains some predefined modes for this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2c44-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2c44-114">Requirements</span></span>



| <span data-ttu-id="d2c44-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2c44-115">Requirement</span></span> | <span data-ttu-id="d2c44-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d2c44-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2c44-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2c44-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d2c44-118">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d2c44-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d2c44-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2c44-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d2c44-120">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d2c44-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d2c44-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2c44-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2c44-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2c44-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2c44-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2c44-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2c44-124">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="d2c44-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="d2c44-125">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="d2c44-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




