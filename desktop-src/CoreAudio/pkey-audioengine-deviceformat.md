---
description: A \_ Propriedade PKEY AudioEngine \_ DeviceFormat especifica o formato de dispositivo, que é o formato que o usuário selecionou para o fluxo que flui entre o mecanismo de áudio e o dispositivo de ponto de extremidade de áudio quando o dispositivo opera no modo compartilhado.
ms.assetid: eb3c734f-0bb8-47cc-a01f-99569f472cde
title: PKEY_AudioEngine_DeviceFormat (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13245d23095c25173a894a7a4c7cc11b2cdc534f6ae7198508b725d0fd1cf0b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018324"
---
# <a name="pkey_audioengine_deviceformat"></a>PKEY \_ AudioEngine \_ DeviceFormat

A propriedade **PKEY \_ AudioEngine \_ DeviceFormat** especifica o formato de dispositivo, que é o formato que o usuário selecionou para o fluxo que flui entre o mecanismo de áudio e o dispositivo de ponto de extremidade de áudio quando o dispositivo opera no modo compartilhado. Esse formato pode não ser o melhor formato padrão para o uso de um aplicativo de modo exclusivo. Normalmente, um aplicativo de modo exclusivo encontra um formato de dispositivo adequado fazendo algumas chamadas para o método [**IAudioClient:: IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) . Para obter mais informações, consulte [formatos de dispositivo](device-formats.md).

O membro **VT** da estrutura **PROPVARIANT** é definido como blob VT \_ .

O membro de **blob** da estrutura **PROPVARIANT** é uma estrutura do tipo **blob** que contém dois membros. Member **BLOB. cbSize** é um **DWORD** que especifica o número de bytes na descrição do formato. Member **BLOB. pBlobData** aponta para uma estrutura **WAVEFORMATEX** que contém a descrição do formato. para obter mais informações sobre **BLOB**, consulte a documentação do SDK do Windows. para obter mais informações sobre o **WAVEFORMATEX**, consulte a documentação do Windows DDK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades do ponto de extremidade de áudio**](audio-endpoint-properties.md)
</dt> <dt>

[Propriedades de áudio de núcleo](core-audio-properties.md)
</dt> </dl>

 

 




