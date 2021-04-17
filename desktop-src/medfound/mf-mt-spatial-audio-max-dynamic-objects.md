---
description: Especifica o número máximo de objetos de áudio dinâmicos que podem ser processados pelo ponto de extremidade de áudio simulataneously.
ms.assetid: 6B6D73C1-C2E6-4C23-BBAD-7B51E8441C71
title: Atributo MF_MT_SPATIAL_AUDIO_MAX_DYNAMIC_OBJECTS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358045079fb9cf52ad1fd0c8969f54723c7f02d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749516"
---
# <a name="mf_mt_spatial_audio_max_dynamic_objects-attribute"></a><span data-ttu-id="811d3-103">\_Atributo de \_ máximo \_ de \_ \_ objetos dinâmicos de áudio \_ do MF MT</span><span class="sxs-lookup"><span data-stu-id="811d3-103">MF\_MT\_SPATIAL\_AUDIO\_MAX\_DYNAMIC\_OBJECTS attribute</span></span>

<span data-ttu-id="811d3-104">Especifica o número máximo de objetos de áudio dinâmicos que podem ser processados pelo ponto de extremidade de áudio simulataneously.</span><span class="sxs-lookup"><span data-stu-id="811d3-104">Specifies the maximum number of dynamic audio objects that can be rendered by the audio endpoint simulataneously.</span></span>

## <a name="data-type"></a><span data-ttu-id="811d3-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="811d3-105">Data type</span></span>

<span data-ttu-id="811d3-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="811d3-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="811d3-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="811d3-107">Remarks</span></span>

<span data-ttu-id="811d3-108">Um [**IMFSpatialAudioSample**](/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample) pode conter menos amostras do que o número especificado por esse atributo.</span><span class="sxs-lookup"><span data-stu-id="811d3-108">An [**IMFSpatialAudioSample**](/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample) may contain fewer samples than the number specified by this attribute.</span></span> <span data-ttu-id="811d3-109">Se um exemplo contiver mais objetos de áudio do que o especificado por esse atributo, o comportamento será indefinido.</span><span class="sxs-lookup"><span data-stu-id="811d3-109">If a sample contains more audio objects than specified by this attribute, the behavior is undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="811d3-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="811d3-110">Requirements</span></span>



| <span data-ttu-id="811d3-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="811d3-111">Requirement</span></span> | <span data-ttu-id="811d3-112">Valor</span><span class="sxs-lookup"><span data-stu-id="811d3-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="811d3-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="811d3-113">Minimum supported client</span></span><br/> | <span data-ttu-id="811d3-114">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="811d3-114">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="811d3-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="811d3-115">Minimum supported server</span></span><br/> | <span data-ttu-id="811d3-116">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="811d3-116">None supported</span></span><br/>                                                          |
| <span data-ttu-id="811d3-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="811d3-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="811d3-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="811d3-118"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




