---
description: A interface IEnumTime fornece métodos de enumeração padrão COM para a interface ITTime. O método ITTimeCollection::get \_ EnumerationIf retorna um ponteiro para IEnumTime.
ms.assetid: 395d7830-9a70-473a-8a89-4b4db48d5774
title: Interface IEnumTime (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c79d780374bcf121dcb5010aef51725f9836e511bed4b86c855970bb47b838e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992196"
---
# <a name="ienumtime-interface"></a>Interface IEnumTime

\[As interfaces e controles de conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

A interface **IEnumTime** fornece métodos de enumeração padrão COM para a interface [**ITTime.**](ittime.md) O [**método ITTimeCollection::get \_ EnumerationIf**](ittimecollection-get-enumerationif.md) retorna um ponteiro para **IEnumTime.**

## <a name="members"></a>Membros

A interface **IEnumTime** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IEnumTime** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IEnumTime** tem esses métodos.



| Método                           | Descrição                                                                                        |
|:---------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clone**](ienumtime-clone.md) | Cria outro enumerador que contém o mesmo estado de enumeração do atual.<br/> |
| [**Avançar**](ienumtime-next.md)   | Obtém o próximo número especificado de elementos na sequência de enumeração.<br/>                 |
| [**Redefinir**](ienumtime-reset.md) | Redefine para o início da sequência de enumeração.<br/>                                    |
| [**Ignorar**](ienumtime-skip.md)   | Ignora o próximo número especificado de elementos na sequência de enumeração.<br/>           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

