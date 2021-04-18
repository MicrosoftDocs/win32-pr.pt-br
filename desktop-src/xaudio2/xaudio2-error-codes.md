---
description: Códigos de erro específicos do XAudio2 retornados por métodos XAudio2.
ms.assetid: 42a1c21c-4b14-114a-d79e-15a61eb2139b
title: Códigos de erro XAudio2 (Xaudio2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7011786c3db7f660dee7a3323861abd88c57835
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781308"
---
# <a name="xaudio2-error-codes"></a><span data-ttu-id="e7a99-103">Códigos de erro XAudio2</span><span class="sxs-lookup"><span data-stu-id="e7a99-103">XAudio2 Error Codes</span></span>

<span data-ttu-id="e7a99-104">Códigos de erro específicos do XAudio2 retornados por métodos XAudio2.</span><span class="sxs-lookup"><span data-stu-id="e7a99-104">XAudio2 specific error codes returned by XAudio2 methods.</span></span>



| <span data-ttu-id="e7a99-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="e7a99-105">Constant/value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="e7a99-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="e7a99-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_E_INVALID_CALL"></span><span id="xaudio2_e_invalid_call"></span><dl> <span data-ttu-id="e7a99-107"><dt>**XAudio2 \_ E & 0x88960001 de \_ \_ chamada inválida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e7a99-107"><dt>**XAUDIO2\_E\_INVALID\_CALL**</dt> <dt>0x88960001</dt></span></span> </dl>                          | <span data-ttu-id="e7a99-108">Retornado por XAudio2 para determinados erros de uso de API (chamadas inválidas e assim por diante) que são difíceis de evitar completamente e devem ser manipulados por um título em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="e7a99-108">Returned by XAudio2 for certain API usage errors (invalid calls and so on) that are hard to avoid completely and should be handled by a title at runtime.</span></span> <span data-ttu-id="e7a99-109">(Os erros de uso da API que são completamente podem ser evitados, como parâmetros inválidos, causam uma ASSERÇÃO em compilações de depuração e comportamento indefinido em compilações de varejo, portanto, nenhum código de erro é definido para eles.)</span><span class="sxs-lookup"><span data-stu-id="e7a99-109">(API usage errors that are completely avoidable, such as invalid parameters, cause an ASSERT in debug builds and undefined behavior in retail builds, so no error code is defined for them.)</span></span><br/> |
| <span id="XAUDIO2_E_XMA_DECODER_ERROR"></span><span id="xaudio2_e_xma_decoder_error"></span><dl> <span data-ttu-id="e7a99-110"><dt>**XAudio2 \_ \_ \_ \_ Erro de decodificador E XMA**</dt> <dt>0x88960002</dt></span><span class="sxs-lookup"><span data-stu-id="e7a99-110"><dt>**XAUDIO2\_E\_XMA\_DECODER\_ERROR**</dt> <dt>0x88960002</dt></span></span> </dl>          | <span data-ttu-id="e7a99-111">O hardware do Xbox 360 XMA sofreu um erro irrecuperável.</span><span class="sxs-lookup"><span data-stu-id="e7a99-111">The Xbox 360 XMA hardware suffered an unrecoverable error.</span></span><br/>                                                                                                                                                                                                                                                                                             |
| <span id="XAUDIO2_E_XAPO_CREATION_FAILED"></span><span id="xaudio2_e_xapo_creation_failed"></span><dl> <span data-ttu-id="e7a99-112"><dt>**XAudio2 \_ \_ \_ \_ Falha na criação do E XAPO**</dt> <dt>0x88960003</dt></span><span class="sxs-lookup"><span data-stu-id="e7a99-112"><dt>**XAUDIO2\_E\_XAPO\_CREATION\_FAILED**</dt> <dt>0x88960003</dt></span></span> </dl> | <span data-ttu-id="e7a99-113">Falha ao criar uma instância de um efeito.</span><span class="sxs-lookup"><span data-stu-id="e7a99-113">An effect failed to instantiate.</span></span><br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="XAUDIO2_E_DEVICE_INVALIDATED"></span><span id="xaudio2_e_device_invalidated"></span><dl> <span data-ttu-id="e7a99-114"><dt>**XAudio2 \_ Dispositivo E 0x88960004 \_ \_ invalidados**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e7a99-114"><dt>**XAUDIO2\_E\_DEVICE\_INVALIDATED**</dt> <dt>0x88960004</dt></span></span> </dl>        | <span data-ttu-id="e7a99-115">Um dispositivo de áudio tornou-se inutilizável por ser desconectado ou algum outro evento.</span><span class="sxs-lookup"><span data-stu-id="e7a99-115">An audio device became unusable through being unplugged or some other event.</span></span><br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="e7a99-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7a99-116">Remarks</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="e7a99-117">Requisitos de plataforma</span><span class="sxs-lookup"><span data-stu-id="e7a99-117">Platform Requirements</span></span>

<span data-ttu-id="e7a99-118">Windows 10 (XAudio 2.9); Windows 8, Windows Phone 8 (XAudio 2,8); SDK do DirectX (XAudio 2,7)</span><span class="sxs-lookup"><span data-stu-id="e7a99-118">Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)</span></span>

## <a name="requirements"></a><span data-ttu-id="e7a99-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7a99-119">Requirements</span></span>



| <span data-ttu-id="e7a99-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7a99-120">Requirement</span></span> | <span data-ttu-id="e7a99-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e7a99-121">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e7a99-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7a99-122">Header</span></span><br/> | <dl> <span data-ttu-id="e7a99-123"><dt>Xaudio2. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7a99-123"><dt>Xaudio2.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7a99-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7a99-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7a99-125">XAudio2:: Constants</span><span class="sxs-lookup"><span data-stu-id="e7a99-125">XAudio2::Constants</span></span>](constants.md)
</dt> </dl>

 

 




