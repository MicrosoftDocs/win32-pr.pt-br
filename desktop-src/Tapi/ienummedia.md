---
description: 'A interface IEnumMedia fornece métodos de enumeração de padrão COM para a interface ITMedia. O método ITMediaCollection:: get \_ EnumerationIf retorna um ponteiro para IEnumMedia.'
ms.assetid: 827f8866-2445-4b7c-88fe-eed19f48c93b
title: Interface IEnumMedia (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7127e7d1d751ee487ad5b86326602cfcfe5aae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759971"
---
# <a name="ienummedia-interface"></a>Interface IEnumMedia

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A interface **IEnumMedia** fornece métodos de enumeração de padrão com para a interface [**ITMedia**](itmedia.md) . O método [**ITMediaCollection:: get \_ EnumerationIf**](itmediacollection-get-enumerationif.md) retorna um ponteiro para **IEnumMedia**.

## <a name="members"></a>Membros

A interface **IEnumMedia** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IEnumMedia** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IEnumMedia** tem esses métodos.



| Método                            | Descrição                                                                                        |
|:----------------------------------|:---------------------------------------------------------------------------------------------------|
| [**8i**](ienummedia-clone.md) | Cria outro enumerador que contém o mesmo estado de enumeração do atual.<br/> |
| [**Avançar**](ienummedia-next.md)   | Obtém o próximo número especificado de elementos na sequência de enumeração.<br/>                 |
| [**Redefinir**](ienummedia-reset.md) | Redefine para o início da sequência de enumeração.<br/>                                    |
| [**Ignorar**](ienummedia-skip.md)   | Ignora o próximo número especificado de elementos na sequência de enumeração.<br/>           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

