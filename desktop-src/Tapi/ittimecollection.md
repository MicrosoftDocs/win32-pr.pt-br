---
description: A interface ITTimeCollection é uma interface específica de provedor para o objeto de blob de conferência SDP (Session Descriptor Protocol).
ms.assetid: 6309e9f2-8a73-4d42-ae0a-2165352d6244
title: Interface ITTimeCollection (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d086dcf0df7fb4d55552c734798244209fc3e9f52a2f2462693f6aaad7110347
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762289"
---
# <a name="ittimecollection-interface"></a>Interface ITTimeCollection

\[os controles e as interfaces de conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A interface **ITTimeCollection** é uma interface específica de provedor para o objeto de blob de conferência SDP (Session Descriptor Protocol). Essa interface permite o acesso a interfaces [**ITTime**](ittime.md) por índice e também permite a criação e a exclusão de componentes de tempo. O método [**ITSdp:: get \_ timecollection**](itsdp-get-timecollection.md) cria a interface **ITTimeCollection** .

## <a name="members"></a>Membros

A interface **ITTimeCollection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITTimeCollection** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITTimeCollection** tem esses métodos.



| Método                                                           | Descrição                                                                                                           |
|:-----------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**Criar**](ittimecollection-create.md)                        | Cria um componente [**ITTime**](ittime.md) .<br/>                                                             |
| [**Excluir**](ittimecollection-delete.md)                        | Exclui um componente [**ITTime**](ittime.md) .<br/>                                                             |
| [**obter \_ \_ NewEnum**](ittimecollection-get--newenum.md)          | Retorna um enumerador para a coleção.<br/>                                                                  |
| [**obter \_ contagem**](ittimecollection-get-count.md)                 | Obtém o número de itens na coleção.<br/>                                                                        |
| [**obter \_ EnumerationIf**](ittimecollection-get-enumerationif.md) | Retorna a interface de enumeração [**IEnumTime**](ienumtime.md) que enumera [**ITTime**](ittime.md).<br/> |
| [**obter \_ Item**](ittimecollection-get-item.md)                   | Dado um índice, retorna um item na coleção.<br/>                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

