---
description: Habilita a decodificação acelerada por hardware de um dispositivo Direct3D 9, usando a versão 1,0 do DirectX Video Acceleration (DXVA).
ms.assetid: abe3beac-f3f8-413d-8b83-9da3340b19ac
title: Interface IDirect3DVideoDevice9 (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 89afef6f39b3aa196d8b1013e3d8873e329ce6ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090966"
---
# <a name="idirect3dvideodevice9-interface"></a>Interface IDirect3DVideoDevice9

Habilita a decodificação acelerada por hardware de um dispositivo Direct3D 9, usando a versão 1,0 do DirectX Video Acceleration (DXVA).

## <a name="when-to-use"></a>Quando usar

Essa interface não é destinada ao uso geral do aplicativo. Os filtros do decodificador do DirectShow devem usar a interface [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) , não **IDirect3DVideoDevice9**. Os Pins de entrada do filtro de processador de mixagem de vídeo (VMR) e o filtro de mixagem de sobreposição expõem **IAMVideoAccelerator**.

## <a name="members"></a>Membros

A interface **IDirect3DVideoDevice9** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDirect3DVideoDevice9** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDirect3DVideoDevice9** tem esses métodos.



| Método                                                                                   | Descrição                                                                                                                       |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDXVADevice**](idirect3dvideodevice9-createdxvadevice.md)                       | Cria um dispositivo de decodificador DXVA.<br/>                                                                                         |
| [**CreateSurface**](idirect3dvideodevice9-createsurface.md)                             | Cria uma superfície compactada para a decodificação de DXVA.<br/>                                                                        |
| [**GetDXVACompressedBufferInfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) | Obtém informações sobre os buffers compactados necessários para a decodificação acelerada por hardware.<br/>                                |
| [**GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md)                               | Obtém uma lista dos perfis de DXVA com suporte no driver de vídeo.<br/>                                             |
| [**GetDXVAInternalInfo**](idirect3dvideodevice9-getdxvainternalinfo.md)                 | Consulta a quantidade de memória temporária que a HAL (camada de abstração de hardware) alocará para seu uso particular. <br/> |
| [**GetUncompressedDXVAFormats**](idirect3dvideodevice9-getuncompresseddxvaformats.md)   | Obtém uma lista de formatos de pixel não compactados que podem ser renderizados usando um perfil de DXVA especificado.<br/>                         |



 

## <a name="remarks"></a>Comentários

Para obter um ponteiro para essa interface, chame **QueryInterface** em um ponteiro [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) ou [**IDirect3DDevice9Ex**](/windows/win32/api/d3d9/nn-d3d9-idirect3ddevice9ex) .

Esta interface dá suporte apenas a DXVA 1,0. Ele não dá suporte a DXVA 2,0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces de vídeo Direct3D](direct3d-video-interfaces.md)
</dt> <dt>

[Aceleração de vídeo do DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Especificação de DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
