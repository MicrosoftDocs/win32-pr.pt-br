---
description: A interface IKeyFrameControl é implementada pelo H. 323 MSP e está disponível somente em objetos de fluxo H. 323.
ms.assetid: 68cb1df1-f7fa-447a-8ea5-80dc1e802760
title: Interface IKeyFrameControl (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c326c6a492777d7c41ae450a1c502c343aeb8cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788065"
---
# <a name="ikeyframecontrol-interface"></a>Interface IKeyFrameControl

\[O **IKeyFrameControl** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A interface **IKeyFrameControl** é implementada pelo [H. 323 MSP](h323-msp.md) e está disponível somente em objetos de fluxo h. 323. Essa interface expõe métodos que permitem a criação e manipulação de terminais que podem se comunicar entre clientes do H323 e do SDP. Ele tem dois métodos que permitem que o aplicativo peça ao ponto de extremidade remoto para atualizar a imagem de vídeo com um quadro-chave.

## <a name="members"></a>Membros

A interface **IKeyFrameControl** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IKeyFrameControl** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IKeyFrameControl** tem esses métodos.



| Método                                                                  | Descrição                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**PeriodicUpdatePicture**](ikeyframecontrol-periodicupdatepicture.md) | Configura um temporizador no fluxo que solicitará atualizações de imagem periodicamente.<br/> |
| [**UpdatePicture**](ikeyframecontrol-updatepicture.md)                 | Solicita que o remetente do vídeo atualize a imagem.<br/>                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[H323 MSP](h323-msp.md)
</dt> </dl>

 

