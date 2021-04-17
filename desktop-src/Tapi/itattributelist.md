---
description: A interface ITAttributeList fornece métodos para obter e definir atributos não interpretados.
ms.assetid: 12806c2e-615c-4d78-a4bb-5cc35ea21175
title: Interface ITAttributeList (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2afbc7ab447188943c0f02e6c5a664bbcc4c6d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761963"
---
# <a name="itattributelist-interface"></a>Interface ITAttributeList

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A interface **ITAttributeList** fornece métodos para obter e definir atributos não interpretados. Sobre a posição das cadeias de caracteres de atributo em um pacote de protocolo de descritor de sessão (SDP, consulte RFC 2327), os métodos pressupõem que todas as cadeias de caracteres de atributo existam logo antes que os atributos de mídia sejam especificados e depois de todos os atributos comuns. A interface **ITAttributeList** é criada chamando **QueryInterface** no [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).

## <a name="members"></a>Membros

A interface **ITAttributeList** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITAttributeList** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITAttributeList** tem esses métodos.



| Método                                                          | Descrição                                             |
|:----------------------------------------------------------------|:--------------------------------------------------------|
| [**Agrega**](itattributelist-add.md)                              | Adiciona o atributo no índice especificado.<br/>   |
| [**Apagar**](itattributelist-delete.md)                        | Exclui o atributo no índice especificado<br/> |
| [**obter \_ atributolist**](itattributelist-get-attributelist.md) | Obtém a lista de atributos.<br/>                 |
| [**obter \_ contagem**](itattributelist-get-count.md)                 | Obtém o número de atributos.<br/>               |
| [**obter \_ Item**](itattributelist-get-item.md)                   | Obtém o atributo especificado pelo índice.<br/>   |
| [**colocar \_ atributolist**](itattributelist-put-attributelist.md) | Define a lista de atributos.<br/>                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

