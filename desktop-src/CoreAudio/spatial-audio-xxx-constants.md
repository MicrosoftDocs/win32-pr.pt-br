---
description: As \_ constantes de áudio espacial \_ xxx definem valores relacionados a recursos de som espaciais.
ms.assetid: F1A01BDB-0CC2-45ED-A423-8CC7F54D4E55
title: Constantes de SPATIAL_AUDIO_XXX (SpatialAudioMetadata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd2c92b970f69cf84e0744f21a41932a8851efed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748932"
---
# <a name="spatial_audio_xxx-constants"></a><span data-ttu-id="d52a7-103">\_Constantes de áudio espacial \_ xxx</span><span class="sxs-lookup"><span data-stu-id="d52a7-103">SPATIAL\_AUDIO\_XXX Constants</span></span>

<span data-ttu-id="d52a7-104">As \_ constantes de áudio espacial \_ xxx definem valores relacionados a recursos de som espaciais.</span><span class="sxs-lookup"><span data-stu-id="d52a7-104">The SPATIAL\_AUDIO\_XXX constants define values related to spatial sound features.</span></span>



| <span data-ttu-id="d52a7-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="d52a7-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="d52a7-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="d52a7-106">Description</span></span>                                                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPATIAL_AUDIO_POSITION"></span><span id="spatial_audio_position"></span><dl> <span data-ttu-id="d52a7-107"><dt>**Espacial \_ \_Posição de áudio**</dt> <dt>200</dt></span><span class="sxs-lookup"><span data-stu-id="d52a7-107"><dt>**SPATIAL\_AUDIO\_POSITION**</dt> <dt>200</dt></span></span> </dl>                                                   | <span data-ttu-id="d52a7-108">Um comando padrão de metadados de áudio espacial definido pela Microsoft que representa a posição do ouvinte no modelo padrão usado por [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) , em que a cabeça do ouvinte é a posição em coordenadas (0, 0, 0), definida em metros.</span><span class="sxs-lookup"><span data-stu-id="d52a7-108">A standard Microsoft-defined spatial audio metadata command which represents the listener position in the standard model used by [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) where the listener's head is position at coordinates (0,0,0), defined in meters.</span></span><br/> |
| <span id="SPATIAL_AUDIO_POSITION_BYTE_COUNT"></span><span id="spatial_audio_position_byte_count"></span><dl> <span data-ttu-id="d52a7-109"><dt>**Espacial \_ Posição de áudio- \_ \_ \_ contagem de bytes**</dt> <dt>sizeof (float) \* 3</dt></span><span class="sxs-lookup"><span data-stu-id="d52a7-109"><dt>**SPATIAL\_AUDIO\_POSITION\_BYTE\_COUNT**</dt> <dt>sizeof(float) \* 3</dt></span></span> </dl> | <span data-ttu-id="d52a7-110">Especifica o tamanho do valor **da \_ \_ posição de áudio espacial** .</span><span class="sxs-lookup"><span data-stu-id="d52a7-110">Specifies the size of the **SPATIAL\_AUDIO\_POSITION** value.</span></span><br/>                                                                                                                                                                                                        |
| <span id="SPATIAL_AUDIO_STANDARD_COMMANDS_START"></span><span id="spatial_audio_standard_commands_start"></span><dl> <span data-ttu-id="d52a7-111"><dt>**Espacial \_ \_Comandos padrão de áudio \_ \_ início**</dt> <dt>200</dt></span><span class="sxs-lookup"><span data-stu-id="d52a7-111"><dt>**SPATIAL\_AUDIO\_STANDARD\_COMMANDS\_START**</dt> <dt>200</dt></span></span> </dl>    | <span data-ttu-id="d52a7-112">Especifica o início do intervalo de comandos de metadados de áudio espacial reservado da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d52a7-112">Specifies the start of the range of Microsoft-reserved spatial audio metadata commands.</span></span> <span data-ttu-id="d52a7-113">Os comandos de metadados personalizados são restritos às IDs de comando 0-199.</span><span class="sxs-lookup"><span data-stu-id="d52a7-113">Custom metadata commands are restricted to command IDs 0 - 199.</span></span> <span data-ttu-id="d52a7-114">Os comandos 200-255 são reservados para uso da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d52a7-114">Commands 200 - 255 are reserved for Microsoft use.</span></span><br/>                                                           |



## <a name="requirements"></a><span data-ttu-id="d52a7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d52a7-115">Requirements</span></span>



| <span data-ttu-id="d52a7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d52a7-116">Requirement</span></span> | <span data-ttu-id="d52a7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d52a7-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d52a7-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d52a7-118">Header</span></span><br/> | <dl> <span data-ttu-id="d52a7-119"><dt>SpatialAudioMetadata. h</dt></span><span class="sxs-lookup"><span data-stu-id="d52a7-119"><dt>SpatialAudioMetadata.h</dt></span></span> </dl> |



 

 




