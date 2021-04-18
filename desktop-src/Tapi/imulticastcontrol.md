---
description: A interface IMulticastControl é implementada pelo IPConf MSP e disponível somente em objetos de chamada multicast.
ms.assetid: 9bdb4ab9-30b3-46fb-b13a-de9c294c8046
title: Interface IMulticastControl (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98ad006ea41034d6d4da32359d1ecbcdd250ab6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761964"
---
# <a name="imulticastcontrol-interface"></a>Interface IMulticastControl

\[O **IMulticastControl** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A interface **IMulticastControl** é implementada pelo IPConf msp e disponível somente em objetos de chamada multicast. Essa interface expõe métodos que permitem a criação e manipulação de terminais que podem se comunicar entre clientes do H323 e do SDP. A interface **IMulticastControl** controla o modo de loopback multicast.

No modo MM \_ sem \_ loopback, o loopback multicast está desabilitado, o que significa que dois aplicativos no mesmo computador que ingressam no mesmo grupo de multicast receberão os pacotes uns dos outros. Esse modo tem o melhor desempenho se sempre houver apenas um aplicativo ingressando no grupo de multicast no computador. MM \_ nenhum \_ modo de loopback é o modo padrão.

O \_ modo de \_ auto-retorno completo mm é bom apenas para teste. Todos os pacotes enviados também são reproduzidos em loop. Isso pode ser usado para testar se os dispositivos estão funcionando.

O \_ modo de \_ auto-retorno seletivo mm é usado para permitir que vários aplicativos em um computador ingressem no mesmo grupo de multicast. Os pacotes são reproduzidos em loop da pilha e cada sessão RTP é responsável por filtrar pacotes indesejados.

## <a name="members"></a>Membros

A interface **IMulticastControl** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMulticastControl** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IMulticastControl** tem esses métodos.



| Método                                                          | Descrição                                  |
|:----------------------------------------------------------------|:---------------------------------------------|
| [**obter \_ loopbackmode**](imulticastcontrol-get-loopbackmode.md) | Obtém o modo de loopback multicast.<br/> |
| [**colocar \_ loopbackmode**](imulticastcontrol-put-loopbackmode.md) | Define o modo de loopback multicast.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> </dl>

 

