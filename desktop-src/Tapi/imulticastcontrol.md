---
description: A interface IMulticastControl é implementada pelo IPConf MSP e está disponível somente em objetos de chamada multicast.
ms.assetid: 9bdb4ab9-30b3-46fb-b13a-de9c294c8046
title: Interface IMulticastControl (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7469ca26a49bc25b36ae87727a1fdcf324bcf54e8a253805ed56f252c7f062
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905946"
---
# <a name="imulticastcontrol-interface"></a>Interface IMulticastControl

\[**IMulticastControl** não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

A interface **IMulticastControl** é implementada pelo IPConf MSP e está disponível somente em objetos de chamada multicast. Essa interface expõe métodos que permitem a criação e a manipulação de terminais que podem se comunicar entre clientes H323 e SDP. A interface **IMulticastControl** controla o modo de loopback multicast.

No modo MM \_ NO LOOPBACK, o loopback multicast está desabilitado, o que significa que dois aplicativos no mesmo computador que ingressarem no mesmo grupo multicast obterão os pacotes uns dos \_ outros. Esse modo terá o melhor desempenho se houver sempre apenas um aplicativo in joining ao grupo multicast no computador. O \_ modo MM NO \_ LOOPBACK é o modo padrão.

O modo MM \_ FULL \_ LOOPBACK é bom apenas para teste. Todos os pacotes enviados são enviados em loop de volta também. Isso pode ser usado para testar se os dispositivos estão funcionando.

O modo MM SELECTIVE LOOPBACK é usado para habilitar vários aplicativos em um \_ computador a ingressar no mesmo grupo \_ multicast. Os pacotes são loops de volta da pilha e cada sessão RTP é responsável por filtrar pacotes indesejados.

## <a name="members"></a>Membros

A interface **IMulticastControl** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMulticastControl** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IMulticastControl** tem esses métodos.



| Método                                                          | Descrição                                  |
|:----------------------------------------------------------------|:---------------------------------------------|
| [**get \_ LoopbackMode**](imulticastcontrol-get-loopbackmode.md) | Obtém o modo de loopback multicast.<br/> |
| [**put \_ LoopbackMode**](imulticastcontrol-put-loopbackmode.md) | Define o modo de loopback multicast.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> </dl>

 

