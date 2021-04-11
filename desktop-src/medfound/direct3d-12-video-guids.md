---
description: Os GUIDs a seguir dão suporte a APIs de vídeo do Direct3D 12.
ms.assetid: CF2F3058-328A-4128-B5C6-29723B49AB1E
title: GUIDs de vídeo do Direct3D 12 (D3d11. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05f7a56227ccc2953504d8466a34d6b2160ce1e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164193"
---
# <a name="direct3d-12-video-guids"></a>GUIDs de vídeo do Direct3D 12

Os GUIDs a seguir dão suporte a APIs de vídeo do Direct3D 12.

## <a name="d3d12_video_decode_profile-guids"></a>D3D12 \\ _VIDEO \\ _DECODE \\ _PROFILE GUIDs

A tabela a seguir lista os GUIDs que identificam os perfis de decodificação de vídeo do Direct3D 12. As descrições relacionam cada perfil de decodificação de vídeo do Direct3D 12 ao perfil de vídeo ou DXVA equivalente do Direct3D 11.

| Nome                                                 | Valor                                                                                | Descrição
|------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| \_ \_ Perfil de decodificação de vídeo D3D12 \_ \_ MPEG1 \_ e \_ MPEG2           | 0x86695f12, 0x340e, 0x4f04, 0x9f, 0xd3, 0x92, 0x53, 0xdd, 0x32, 0x74, 0x60 | Equivalente a DXVA2 \_ ModeMPEG2and1 \_ VLD.                 |
| \_MPEG2 do \_ perfil de decodificação de vídeo D3D12 \_ \_                     | 0xee27417f, 0x5e28, 0x4e65, 0xbe, 0xea, 0x1d, 0x26, 0xb5, 0x08, 0xad, 0xc9           | Equivalente ao D3D11 de \_ decodificador \_ \_ MPEG2 \_ VLD e DXVA2 \_ ModeMPEG2 \_ VLD.                 |
| D3D12 \_ de \_ perfil de decodificação de vídeo em \_ \_ H264                      | 0x1b81be68, 0xa0c7, 0x11d3, 0xb9, 0x84, 0x00, 0xC0, 0x4F, 0x2e, 0x73, 0xC5       | Equivalente ao \_ perfil de decodificador D3D11 \_ \_ H264 \_ VLD \_ NOFGT e DXVA \_ ModeH264 \_ VLD \_ NOFGT. |
| \_Perfil de \_ decodificação de vídeo D3D12 \_ \_ H264 \_ estéreo \_ progressivo   | 0xd79be8da, 0x0cf1, 0x4c81, 0xb8, 0x2a, 0x69, 0xa4, 0xe2, 0x36, 0xf4, 0x3d          | Equivalente ao \_ perfil de decodificador D3D11 \_ \_ H264 \_ VLD \_ estéreo \_ progressivo \_ NOFGT e DXVA \_ ModeH264 \_ VLD \_ estéreo \_ progressivo NOFGT \_ . |
| \_Perfil de \_ decodificação de vídeo D3D12 \_ \_ H264 \_ estéreo               | 0xf9aaccbb, 0xc2b6, 0x4cfc, 0x87, 0x79, 0x57, 0x07, 0xB1, 0x76, 0x05, 0x52          | Equivalente ao \_ perfil de decodificador D3D11 \_ \_ H264 \_ VLD \_ estéreo \_ NOFGT e DXVA \_ ModeH264 \_ VLD \_ estéreo \_ NOFGT |
| D3D12 \_ de \_ perfil de decodificação de vídeo \_ \_ H264 \_ MULTIVIEW            | 0x705b9d82, 0x76cf, 0x49d6, 0xb7, 0xE6, 0xAC, 0x88, 0x72, 0xdb, 0x01, 0x3C          | Equivalente ao \_ perfil de decodificador D3D11 \_ \_ H264 \_ VLD \_ MultiView \_ NOFGT e DXVA \_ ModeH264 \_ VLD \_ MULTIVIEW \_ NOFGT. |
| \_Perfil de \_ decodificação de vídeo D3D12 \_ \_ VC1                       | 0x1b81beA3, 0xa0c7, 0x11d3, 0xb9, 0x84, 0x00, 0xC0, 0x4F, 0x2e, 0x73, 0xC5          | Equivalente ao \_ perfil de decodificador D3D11 \_ \_ VC1 \_ VLD e DXVA \_ ModeVC1 \_ VLD. |
| \_Perfil de \_ decodificação de vídeo D3D12 \_ \_ VC1 \_ D2010                 | 0x1b81beA4, 0xa0c7, 0x11d3, 0xb9, 0x84, 0x00, 0xC0, 0x4F, 0x2e, 0x73, 0xC5          | Equivalente ao \_ perfil de decodificador D3D11 \_ \_ VC1 \_ D2010 e DXVA \_ ModeVC1 \_ D2010. |
| \_Perfil de \_ decodificação de vídeo D3D12 \_ \_ MPEG4PT2 \_ simples           | 0xefd64d74, 0xc9e8, 0x41d7, 0xa5, 0xe9, 0xe9, 0xb0, 0xe3, 0x9f, 0xa3, 0x19          | Equivalente a D3D11 \_ perfil de decodificador \_ \_ MPEG4PT2 \_ VLD \_ simples e DXVA \_ ModeMPEG4pt2 \_ VLD \_ simples. |
| \_Perfil de \_ decodificação de vídeo D3D12 \_ \_ MPEG4PT2 \_ ADVSIMPLE \_ NOGMC  | 0xed418a9f, 0x010d, 0x4eda, 0x9a, 0xe3, 0x9a, 0x65, 0x35, 0x8d, 0x8d, 0x2e          | Equivalente ao \_ perfil de decodificador D3D11 \_ \_ MPEG4PT2 \_ VLD \_ ADVSIMPLE \_ NOGMC e DXVA \_ ModeMPEG4pt2 \_ \_ \_ VLD ADVSIMPLE NOGMC. |
| \_Perfil de \_ decodificação de vídeo D3D12 \_ \_ HEVC \_ principal                 | 0x5b11d51b, 0x2f4c, 0x4452, 0xbc, 0xc3, 0x09, 0xf2, 0xa1, 0x16, 0x0c, 0xc0          | Equivalente ao \_ perfil de decodificador D3D11 \_ \_ HEVC \_ VLD \_ Main e DXVA \_ ModeHEVC \_ VLD \_ Main
| \_Perfil de \_ decodificação de vídeo D3D12 \_ \_ HEVC \_ MAIN10               | 0x107af0e0, 0xef1a, 0x4d19, 0xab, 0xa8, 0x67, 0xa1, 0x63, 0x07, 0x3d, 0x13          | Equivalente ao \_ perfil de decodificador D3D11 \_ \_ HEVC \_ VLD \_ MAIN10 e DXVA \_ ModeHEVC \_ \_ VLD MAIN10.
| \_Perfil de \_ decodificação de vídeo D3D12 \_ \_ VP9                       | 0x463707f8, 0xa1d0, 0x4585, 0x87, 0x6d, 0x83, 0xaa, 0x6d, 0x60, 0xb8, 0x9e | |
| \_Perfil de \_ decodificação de vídeo D3D12 \_ \_ VP9 \_ descompactado \_ proarquivo2        | 0xa4c749ef, 0x6ecf, 0x48aa, 0x84, 0x48, 0x50, 0xa7, 0xA1, 0x16, 0x5F, 0xf7           | |
| \_Perfil de \_ decodificação de vídeo D3D12 \_ \_ VP8                       | 0x90b899ea, 0x3a62, 0x4705, 0x88, 0xb3, 0x8d, 0xf0, 0x4b, 0x27, 0x44, 0xe7 | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_PROFILE0                       | 0xb8be4ccb, 0xcf53, 0x46ba, 0x8d, 0x59, 0xd6, 0xb8, 0xa6, 0xda, 0x5d, 0x2a | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_PROFILE1                       | 0x6936ff0f, 0x45b1, 0x4163, 0x9c, 0xc1, 0x64, 0x6e, 0xf6, 0x94, 0x61, 0x08 | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_PROFILE2                       | 0x0c5f2aa1, 0xe541, 0x4089, 0xBB, 0x7B, 0x98, 0x11, 0x0A, 0x19, 0xd7, 0xC8 | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_12BIT_PROFILE2                 | 0x17127009, 0xa00f, 0x4ce1, 0x99, 0x4e, 0xbf, 0x40, 0x81, 0xF6, 0xf3, 0xF0 | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_12BIT_PROFILE2_420             | 0x2d80bed6, 0x9cac, 0x4835, 0x9e, 0x91, 0x32, 0x7B, 0xbc, 0x4F, 0x9e, 0xe8 | |

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>D3d11. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[APIs de vídeo do Direct3D 11](direct3d-11-video-apis.md)
</dt> </dl>

 

 




