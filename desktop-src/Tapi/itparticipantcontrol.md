---
description: A interface ITParticipantControl é implementada pelo IPConf MSP.
ms.assetid: e617f2a4-6be8-4cb1-9f03-470c5100b834
title: Interface ITParticipantControl (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96075748f0c35cbc5af3c6cd07277d15222e0658
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780123"
---
# <a name="itparticipantcontrol-interface"></a>Interface ITParticipantControl

\[O **ITParticipantControl** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A interface **ITParticipantControl** é implementada pelo IPConf msp. Essa interface é exposta no objeto de chamada. Essa interface permite que um aplicativo recupere ponteiros para os participantes em uma conferência. A interface **ITParticipantControl** é criada chamando **QueryInterface** no [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).

## <a name="members"></a>Membros

A interface **ITParticipantControl** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITParticipantControl** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITParticipantControl** tem esses métodos.



| Método                                                                      | Descrição                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) | Enumera os participantes atualmente envolvidos na conferência.<br/>                                                                                                    |
| [**obter \_ participantes**](itparticipantcontrol-get-participants.md)          | Cria uma coleção de participantes associados à conferência atual. Fornecido para aplicativos cliente de automação, como aqueles escritos em Visual Basic.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

