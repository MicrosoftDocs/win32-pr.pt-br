---
description: A interface ITAttributeList fornece métodos para obter e definir atributos não interpretados.
ms.assetid: 12806c2e-615c-4d78-a4bb-5cc35ea21175
title: Interface ITAttributeList (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a8dd0ac143791a09eedbd3fe575dcecb894a1fb6dbb218c8ecfdcadf60ebd60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762422"
---
# <a name="itattributelist-interface"></a>Interface ITAttributeList

\[As interfaces e controles de Conferência de Telefonia IP de reunião não estão disponíveis para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

A interface **ITAttributeList** fornece métodos para obter e definir atributos não interpretados. Em relação à posição das cadeias de caracteres de atributo em um pacote do protocolo SDP, consulte RFC 2327), os métodos supõem que todas as cadeias de caracteres de atributo existem logo antes que os atributos de mídia sejam especificados e depois de todos os atributos comuns. A interface **ITAttributeList** é criada chamando **QueryInterface** [**em ITDirectoryObject.**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)

## <a name="members"></a>Membros

A interface **ITAttributeList** herda da interface [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITAttributeList** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITAttributeList** tem esses métodos.



| Método                                                          | Descrição                                             |
|:----------------------------------------------------------------|:--------------------------------------------------------|
| [**Adicionar**](itattributelist-add.md)                              | Adiciona o atributo ao índice especificado.<br/>   |
| [**Excluir**](itattributelist-delete.md)                        | Exclui o atributo no índice especificado<br/> |
| [**get \_ AttributeList**](itattributelist-get-attributelist.md) | Obtém a lista de atributos.<br/>                 |
| [**get \_ Count**](itattributelist-get-count.md)                 | Obtém o número de atributos.<br/>               |
| [**get \_ Item**](itattributelist-get-item.md)                   | Obtém o atributo especificado pelo índice.<br/>   |
| [**put \_ AttributeList**](itattributelist-put-attributelist.md) | Define a lista de atributos.<br/>                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

