---
title: Interfaces de vídeo Direct3D
description: Este tópico lista as interfaces de vídeo do Direct3D que estão disponíveis no Direct3D 9Ex e que têm suporte no Windows 7 e em versões posteriores dos sistemas operacionais cliente Windows e no Windows Server 2008 R2 e em versões posteriores dos sistemas operacionais Windows Server.
ms.assetid: 922AC983-B9C0-494C-BADD-CEF20931FC26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d20c86e172308d4be6f4c6218a110f49b033ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454119"
---
# <a name="direct3d-video-interfaces"></a>Interfaces de vídeo Direct3D

Este tópico lista as interfaces de vídeo do Direct3D que estão disponíveis no Direct3D 9Ex e que têm suporte no Windows 7 e em versões posteriores dos sistemas operacionais cliente Windows e no Windows Server 2008 R2 e em versões posteriores dos sistemas operacionais Windows Server. Você pode usar essas interfaces e seus métodos para obter os recursos de proteção de conteúdo de vídeo do driver de gráficos e os recursos de hardware de sobreposição de um dispositivo Direct3D. Você também pode usar essas interfaces e seus métodos para proteger o conteúdo de vídeo. Essas interfaces e seus métodos são definidos em D3d9. h e descritos na seção [Microsoft Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) .



| Interface                                                                                                                                                                                                                             | Descrição                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="IDirect3D9ExOverlayExtension"></span><span id="idirect3d9exoverlayextension"></span><span id="IDIRECT3D9EXOVERLAYEXTENSION"></span>[**IDirect3D9ExOverlayExtension**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9exoverlayextension)<br/>           | Consulta a sobreposição de recursos de hardware de um dispositivo Direct3D.<br/>                                                     |
| <span id="IDirect3DAuthenticatedChannel9"></span><span id="idirect3dauthenticatedchannel9"></span><span id="IDIRECT3DAUTHENTICATEDCHANNEL9"></span>[**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9)<br/> | Fornece um canal de comunicação com o driver de gráficos ou o tempo de execução do Direct3D.<br/>                                  |
| <span id="IDirect3DCryptoSession9"></span><span id="idirect3dcryptosession9"></span><span id="IDIRECT3DCRYPTOSESSION9"></span>[**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)<br/>                                    | Representa uma sessão criptográfica que é usada para acessar uma superfície protegida.<br/>                                      |
| <span id="IDirect3DDevice9Video"></span><span id="idirect3ddevice9video"></span><span id="IDIRECT3DDEVICE9VIDEO"></span>[**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video)<br/>                                              | Permite que um aplicativo use a proteção de conteúdo e os serviços de criptografia que são implementados por um driver de gráficos.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[Guia de programação para Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

