---
description: A interface ITMediaCollection fornece acesso ao conjunto de informações de mídia em uma descrição de conferência SDP (RFC 2327).
ms.assetid: a7e7a07d-239e-432e-9984-7763f11c59ce
title: Interface ITMediaCollection (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2425ae89f376d5cb2d7cc23e70abd33f87750d3d1b5343a17c8ecb05d7de760d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034606"
---
# <a name="itmediacollection-interface"></a>Interface ITMediaCollection

\[As interfaces e controles de Conferência de Telefonia IP de reunião não estão disponíveis para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

A interface **ITMediaCollection** fornece acesso ao conjunto de informações de mídia em uma descrição de conferência SDP (RFC 2327). Cada descrição de mídia no SDP é descrita por uma interface [**ITMedia.**](itmedia.md) **ITMediaCollection** permite a manipulação do conjunto de informações **de ITMedia** para o SDP, incluindo:

-   Permite o acesso à mídia por índice.
-   Habilita a criação e a exclusão de mídia.

O [**método ITSdp::get \_ MediaCollection**](itsdp-get-mediacollection.md) cria a interface **ITMediaCollection.**

## <a name="members"></a>Membros

A **interface ITMediaCollection** herda da interface [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITMediaCollection** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A **interface ITMediaCollection** tem esses métodos.



| Método                                                            | Descrição                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**Criar**](itmediacollection-create.md)                        | Cria uma nova mídia com propriedades padrão e a retorna.<br/> |
| [**Excluir**](itmediacollection-delete.md)                        | Exclui a mídia correspondente ao índice especificado.<br/>     |
| [**get \_ \_ NewEnum**](itmediacollection-get--newenum.md)          | Retorna um enumerador para a coleção.<br/>                   |
| [**get \_ Count**](itmediacollection-get-count.md)                 | Obtém o número de mídias na sessão.<br/>                    |
| [**get \_ EnumerationIf**](itmediacollection-get-enumerationif.md) | Obtém o ponteiro para a interface de enumeração.<br/>                      |
| [**get \_ Item**](itmediacollection-get-item.md)                   | Retorna a mídia correspondente ao índice especificado.<br/>     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

