---
description: 'A interface IEnumTime fornece métodos de enumeração de padrão COM para a interface ITTime. O método ITTimeCollection:: get \_ EnumerationIf retorna um ponteiro para IEnumTime.'
ms.assetid: 395d7830-9a70-473a-8a89-4b4db48d5774
title: Interface IEnumTime (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2336f435ec322694847c776ac92ade93e8791207
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769419"
---
# <a name="ienumtime-interface"></a>Interface IEnumTime

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A interface **IEnumTime** fornece métodos de enumeração de padrão com para a interface [**ITTime**](ittime.md) . O método [**ITTimeCollection:: get \_ EnumerationIf**](ittimecollection-get-enumerationif.md) retorna um ponteiro para **IEnumTime**.

## <a name="members"></a>Membros

A interface **IEnumTime** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IEnumTime** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IEnumTime** tem esses métodos.



| Método                           | Descrição                                                                                        |
|:---------------------------------|:---------------------------------------------------------------------------------------------------|
| [**8i**](ienumtime-clone.md) | Cria outro enumerador que contém o mesmo estado de enumeração do atual.<br/> |
| [**Avançar**](ienumtime-next.md)   | Obtém o próximo número especificado de elementos na sequência de enumeração.<br/>                 |
| [**Redefinir**](ienumtime-reset.md) | Redefine para o início da sequência de enumeração.<br/>                                    |
| [**Ignorar**](ienumtime-skip.md)   | Ignora o próximo número especificado de elementos na sequência de enumeração.<br/>           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

