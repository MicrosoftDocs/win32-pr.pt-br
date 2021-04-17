---
title: Interface IReferenceClock
description: A interface IReferenceClock fornece acesso a um relógio externo. Essa interface é fornecida para permitir que todas as rotinas de renderização sejam sincronizadas com o mesmo relógio. Essa interface pode ser Obtida de um objeto leitor.
ms.assetid: 1424fd74-d56c-4338-801f-319ef975169f
keywords:
- Formato de mídia do Windows da interface IReferenceClock
- Formato de mídia do Windows da interface IReferenceClock, descrito
topic_type:
- apiref
api_name:
- IReferenceClock
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72d17ef362aa5436fe98443d86dff5ae31212650
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105773099"
---
# <a name="ireferenceclock-interface"></a>Interface IReferenceClock

A interface **IReferenceClock** fornece acesso a um relógio externo. Essa interface é fornecida para permitir que todas as rotinas de renderização sejam sincronizadas com o mesmo relógio.

Essa interface pode ser Obtida de um objeto leitor.

## <a name="members"></a>Membros

A interface **IReferenceClock** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IReferenceClock** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IReferenceClock** tem esses métodos.



| Método                                                   | Descrição                                                               |
|:---------------------------------------------------------|:--------------------------------------------------------------------------|
| [**AdvisePeriodic**](ireferenceclock-adviseperiodic.md) | Não implementado por este SDK.<br/>                                   |
| [**Aviso de**](ireferenceclock-advisetime.md)         | Solicita uma notificação assíncrona que um tempo decorreu.<br/> |
| [**GetTime**](ireferenceclock-gettime.md)               | Recupera o tempo de referência atual.<br/>                          |
| [**Cancelar**](ireferenceclock-unadvise.md)             | Cancela uma solicitação de notificação.<br/>                                |



 

## <a name="remarks"></a>Comentários

Para obter informações sobre outras interfaces que podem ser obtidas usando o método QueryInterface dessa interface, consulte leitor Object.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces**](interfaces.md)
</dt> </dl>

 

