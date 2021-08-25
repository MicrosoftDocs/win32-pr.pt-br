---
description: Os GUIDs a seguir são suportados por APIs de vídeo do Direct3D 12.
ms.assetid: CF2F3058-328A-4128-B5C6-29723B49AB1E
title: GUIDs de vídeo do Direct3D 12 (D3d11.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8c2411b2e9172323e544855cfd4ef0200c8043d365ac9b65afd9a2a1d8f83ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942686"
---
# <a name="direct3d-12-video-guids"></a>GUIDs de vídeo do Direct3D 12

Os GUIDs a seguir são suportados por APIs de vídeo do Direct3D 12.

## <a name="d3d12_video_decode_profile-guids"></a>D3D12 \\ _VIDEO \\ _DECODE \\ _PROFILE GUIDs

A tabela a seguir lista os GUIDs que identificam perfis de decodificação de vídeo do Direct3D 12. As descrições relacionam cada perfil de decodificador de vídeo do Direct3D 12 ao vídeo equivalente do Direct3D 11 ou ao perfil DXVA.

| Nome                                                 | Valor                                                                                | Descrição
|------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| PERFIL DE \_ DECODIFICADOR DE VÍDEO D3D12 \_ \_ \_ MPEG1 \_ E \_ MPEG2           | 0x86695f12, 0x340e, 0x4f04, 0x9f, 0xd3, 0x92, 0x53, 0xdd, 0x32, 0x74, 0x60 | Equivalente a DXVA2 \_ ModeMPEG2and1 \_ VLD.                 |
| PERFIL DE \_ DECODIFICADOR DE VÍDEO D3D12 \_ \_ \_ MPEG2                     | 0xee27417f, 0x5e28, 0x4e65, 0xbe, 0xea, 0x1d, 0x26, 0xb5, 0x08, 0xad, 0xc9           | Equivalente a D3D11 \_ DECODER \_ PROFILE \_ MPEG2 \_ VLD e DXVA2 \_ ModeMPEG2 \_ VLD.                 |
| PERFIL DE DECODIFICADOR DE VÍDEO D3D12 \_ \_ \_ \_ H264                      | 0x1b81be68, 0xa0c7, 0x11d3, 0xb9, 0x84, 0x00, 0xc0, 0x4f, 0x2e, 0x73, 0xc5       | Equivalente a D3D11 \_ DECODER \_ PROFILE \_ H264 \_ VLD \_ NOFGT e DXVA \_ ModeH264 \_ VLD \_ NoFGT. |
| PERFIL DE DECODIFICADOR DE VÍDEO D3D12 \_ \_ \_ \_ H264 \_ ESTÉREO \_ PROGRESSIVO   | 0xd79be8da, 0x0cf1, 0x4c81, 0xb8, 0x2a, 0x69, 0xa4, 0xe2, 0x36, 0xf4, 0x3d          | Equivalente a D3D11 \_ DECODER \_ PROFILE \_ H264 \_ VLD \_ STEREO PROGRESSIVE NOFGT e \_ \_ DXVA \_ ModeH264 \_ VLD \_ NoFGT Progressivo Estéreo. \_ \_ |
| PERFIL DE DECODIFICADOR DE VÍDEO D3D12 \_ \_ \_ \_ H264 \_ ESTÉREO               | 0xf9aaccbb, 0xc2b6, 0x4cfc, 0x87, 0x79, 0x57, 0x07, 0xb1, 0x76, 0x05, 0x52          | Equivalente a D3D11 \_ DECODER \_ PROFILE \_ H264 \_ VLD \_ ESTÉREO \_ NOFGT e Modo DXVAH264 \_ \_ VLD \_ Estéreo \_ NoFGT |
| PERFIL DE DECODIFICADOR DE VÍDEO D3D12 \_ \_ \_ \_ H264 \_ MULTIVIEW            | 0x705b9d82, 0x76cf, 0x49d6, 0xb7, 0xe6, 0xac, 0x88, 0x72, 0xdb, 0x01, 0x3c          | Equivalente a D3D11 \_ DECODER \_ PROFILE \_ H264 \_ \_ VLD MULTIVIEW \_ NOFGT e DXVA \_ ModeH264 \_ VLD \_ \_ NoFGT. |
| PERFIL DE DECODIFICAR VÍDEO D3D12 \_ \_ \_ \_ VC1                       | 0x1b81beA3, 0xa0c7, 0x11d3, 0xb9, 0x84, 0x00, 0xc0, 0x4f, 0x2e, 0x73, 0xc5          | Equivalente a D3D11 \_ DECODER \_ PROFILE \_ VC1 \_ VLD e DXVA \_ ModeVC1 \_ VLD. |
| PERFIL DE \_ DECODIFICADOR DE VÍDEO D3D12 \_ \_ \_ VC1 \_ D2010                 | 0x1b81beA4, 0xa0c7, 0x11d3, 0xb9, 0x84, 0x00, 0xc0, 0x4f, 0x2e, 0x73, 0xc5          | Equivalente a D3D11 \_ DECODER \_ PROFILE \_ VC1 \_ D2010 e DXVA \_ ModeVC1 \_ D2010. |
| PERFIL DE DECODIFICADOR DE VÍDEO D3D12 \_ \_ \_ \_ MPEG4PT2 \_ SIMPLES           | 0xefd64d74, 0xc9e8, 0x41d7, 0xa5, 0xe9, 0xe9, 0xb0, 0xe3, 0x9f, 0xa3, 0x19          | Equivalente a D3D11 \_ DECODER \_ PROFILE \_ MPEG4PT2 VLD SIMPLE e \_ \_ DXVA \_ ModeMPEG4pt2 \_ VLD \_ Simple. |
| PERFIL DE \_ DECODIFICADOR DE VÍDEO D3D12 \_ \_ \_ MPEG4PT2 \_ ADVSIMPLE \_ NOGMC  | 0xed418a9f, 0x010d, 0x4eda, 0x9a, 0xe3, 0x9a, 0x65, 0x35, 0x8d, 0x8d, 0x2e          | Equivalente a D3D11 \_ DECODER \_ PROFILE \_ MPEG4PT2 \_ VLD \_ ADVSIMPLE \_ NOGMC e DXVA \_ ModeMPEG4pt2 \_ VLD \_ AdvSimple \_ NogMC. |
| D3D12 \_ VIDEO \_ DECODE \_ PROFILE \_ HEVC \_ MAIN                 | 0x5b11d51b, 0x2f4c, 0x4452, 0xbc, 0xc3, 0x09, 0xf2, 0xa1, 0x16, 0x0c, 0xc0          | Equivalente a D3D11 \_ DECODER \_ PROFILE \_ HEVC \_ VLD \_ MAIN e DXVA \_ ModeHEVC \_ VLD \_ Main
| PERFIL DE DECODIFICADOR DE VÍDEO D3D12 \_ \_ \_ \_ HEVC \_ MAIN10               | 0x107af0e0, 0xef1a, 0x4d19, 0xab, 0xa8, 0x67, 0xa1, 0x63, 0x07, 0x3d, 0x13          | Equivalente a D3D11 \_ DECODER \_ PROFILE \_ HEVC \_ VLD \_ MAIN10 e DXVA \_ ModeHEVC \_ VLD \_ Main10.
| PERFIL DE DECODIFICADOR DE VÍDEO D3D12 \_ \_ \_ \_ VP9                       | 0x463707f8, 0xa1d0, 0x4585, 0x87, 0x6d, 0x83, 0xaa, 0x6d, 0x60, 0xb8, 0x9e | |
| PERFIL DE DECODIFICADOR DE VÍDEO D3D12 \_ \_ \_ \_ VP9 \_ 10BIT \_ PROFILE2        | 0xa4c749ef, 0x6ecf, 0x48aa, 0x84, 0x48, 0x50, 0xa7, 0xa1, 0x16, 0x5f, 0xf7           | |
| PERFIL DE DECODIFICADOR DE VÍDEO D3D12 \_ \_ \_ \_ VP8                       | 0x90b899ea, 0x3a62, 0x4705, 0x88, 0xb3, 0x8d, 0xf0, 0x4b, 0x27, 0x44, 0xe7 | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_PROFILE0                       | 0xb8be4ccb, 0xcf53, 0x46ba, 0x8d, 0x59, 0xd6, 0xb8, 0xa6, 0xda, 0x5d, 0x2a | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_PROFILE1                       | 0x6936ff0f, 0x45b1, 0x4163, 0x9c, 0xc1, 0x64, 0x6e, 0xf6, 0x94, 0x61, 0x08 | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_PROFILE2                       | 0x0c5f2aa1, 0xe541, 0x4089, 0xbb, 0x7b, 0x98, 0x11, 0x0a, 0x19, 0xd7, 0xc8 | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_12BIT_PROFILE2                 | 0x17127009, 0xa00f, 0x4ce1, 0x99, 0x4e, 0xbf, 0x40, 0x81, 0xf6, 0xf3, 0xf0 | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_12BIT_PROFILE2_420             | 0x2d80bed6, 0x9cac, 0x4835, 0x9e, 0x91, 0x32, 0x7b, 0xbc, 0x4f, 0x9e, 0xe8 | |

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>D3d11.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[APIs de vídeo do Direct3D 11](direct3d-11-video-apis.md)
</dt> </dl>

 

 




