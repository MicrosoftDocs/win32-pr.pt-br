---
description: A interface ITMediaCollection fornece acesso ao conjunto de informações de mídia em uma descrição de conferência SDP (RFC 2327).
ms.assetid: a7e7a07d-239e-432e-9984-7763f11c59ce
title: Interface ITMediaCollection (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21305e1d1729437b53c380b7712feee3827b3ba8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767751"
---
# <a name="itmediacollection-interface"></a>Interface ITMediaCollection

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A interface **ITMediaCollection** fornece acesso ao conjunto de informações de mídia em uma descrição de conferência SDP (RFC 2327). Cada descrição de mídia no SDP é descrita por uma interface [**ITMedia**](itmedia.md) . O **ITMediaCollection** permite a manipulação do conjunto de informações de **ITMEDIA** para o SDP, incluindo:

-   Permite o acesso à mídia por índice.
-   Habilita a criação e a exclusão de mídia.

O método [**ITSdp:: get \_ mediacollection**](itsdp-get-mediacollection.md) cria a interface **ITMediaCollection** .

## <a name="members"></a>Membros

A interface **ITMediaCollection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITMediaCollection** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITMediaCollection** tem esses métodos.



| Método                                                            | Descrição                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**Criada**](itmediacollection-create.md)                        | Cria uma nova mídia com propriedades padrão e a retorna.<br/> |
| [**Apagar**](itmediacollection-delete.md)                        | Exclui a mídia correspondente ao índice especificado.<br/>     |
| [**obter \_ \_ NewEnum**](itmediacollection-get--newenum.md)          | Retorna um enumerador para a coleção.<br/>                   |
| [**obter \_ contagem**](itmediacollection-get-count.md)                 | Obtém o número de mídia na sessão.<br/>                    |
| [**obter \_ EnumerationIf**](itmediacollection-get-enumerationif.md) | Obtém o ponteiro para a interface de enumeração.<br/>                      |
| [**obter \_ Item**](itmediacollection-get-item.md)                   | Retorna a mídia correspondente ao índice especificado.<br/>     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

