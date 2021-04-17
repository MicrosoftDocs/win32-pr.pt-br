---
description: Representa um acelerador de hardware para o DXVA (DirectX Video Acceleration) 1,0.
ms.assetid: 63f77cf9-4c04-4ddb-9582-cfcf86f66a2a
title: Interface IDirect3DDXVADevice9 (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 192f47b8161893f9517bc976452eb8836da4bb53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766437"
---
# <a name="idirect3ddxvadevice9-interface"></a>Interface IDirect3DDXVADevice9

Representa um acelerador de hardware para o DXVA (DirectX Video Acceleration) 1,0.

## <a name="members"></a>Membros

A interface **IDirect3DDXVADevice9** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDirect3DDXVADevice9** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDirect3DDXVADevice9** tem esses métodos.



| Método                                                  | Descrição                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------|
| [**BeginFrame**](idirect3ddxvadevice9-beginframe.md)   | Inicia o processamento para criar uma imagem decodificada.<br/>         |
| [**Quadro de fim**](idirect3ddxvadevice9-endframe.md)       | Encerra o processamento para criar uma imagem decodificada.<br/>           |
| [**Execute (executar)**](idirect3ddxvadevice9-execute.md)         | Executa uma operação de decodificação de DXVA. <br/>                       |
| [**QueryStatus**](idirect3ddxvadevice9-querystatus.md) | Consulta o status de leitura/gravação de uma superfície de decodificação de DXVA. <br/> |



 

## <a name="remarks"></a>Comentários

Para obter um ponteiro para essa interface, chame [**IDirect3DVideoDevice9:: CreateDXVADevice**](idirect3dvideodevice9-createdxvadevice.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces de vídeo Direct3D](direct3d-video-interfaces.md)
</dt> </dl>

 

 
