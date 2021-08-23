---
description: Códigos de erro específicos do XAudio2 retornados por métodos XAudio2.
ms.assetid: 42a1c21c-4b14-114a-d79e-15a61eb2139b
title: Códigos de erro XAudio2 (Xaudio2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bbfb29153ca55064c1019e9cfb8fd1019caaa0ffe17dfa103f123faa812f762
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119545396"
---
# <a name="xaudio2-error-codes"></a>Códigos de erro XAudio2

Códigos de erro específicos do XAudio2 retornados por métodos XAudio2.



| Constante/valor                                                                                                                                                                                                                                                                      | Descrição                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_E_INVALID_CALL"></span><span id="xaudio2_e_invalid_call"></span><dl> <dt>**XAudio2 \_ E & 0x88960001 de \_ \_ chamada inválida**</dt> <dt></dt> </dl>                          | Retornado por XAudio2 para determinados erros de uso de API (chamadas inválidas e assim por diante) que são difíceis de evitar completamente e devem ser manipulados por um título em tempo de execução. (Os erros de uso da API que são completamente podem ser evitados, como parâmetros inválidos, causam uma ASSERÇÃO em compilações de depuração e comportamento indefinido em compilações de varejo, portanto, nenhum código de erro é definido para eles.)<br/> |
| <span id="XAUDIO2_E_XMA_DECODER_ERROR"></span><span id="xaudio2_e_xma_decoder_error"></span><dl> <dt>**XAudio2 \_ \_ \_ \_ Erro de decodificador E XMA**</dt> <dt>0x88960002</dt> </dl>          | O hardware do Xbox 360 XMA sofreu um erro irrecuperável.<br/>                                                                                                                                                                                                                                                                                             |
| <span id="XAUDIO2_E_XAPO_CREATION_FAILED"></span><span id="xaudio2_e_xapo_creation_failed"></span><dl> <dt>**XAudio2 \_ \_ \_ \_ Falha na criação do E XAPO**</dt> <dt>0x88960003</dt> </dl> | Falha ao criar uma instância de um efeito.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="XAUDIO2_E_DEVICE_INVALIDATED"></span><span id="xaudio2_e_device_invalidated"></span><dl> <dt>**XAudio2 \_ Dispositivo E 0x88960004 \_ \_ invalidados**</dt> <dt></dt> </dl>        | Um dispositivo de áudio tornou-se inutilizável por ser desconectado ou algum outro evento.<br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a>Comentários

### <a name="platform-requirements"></a>Requisitos de plataforma

Windows 10 (xaudio 2.9); Windows 8, Windows Phone 8 (XAudio 2,8); SDK do DirectX (XAudio 2,7)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Xaudio2. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[XAudio2:: Constants](constants.md)
</dt> </dl>

 

 




