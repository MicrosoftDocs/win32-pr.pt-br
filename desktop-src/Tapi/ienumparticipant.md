---
description: 'A interface IEnumParticipant fornece métodos de enumeração de padrão COM para a interface ITParticipant. O método ITParticipantControl:: EnumerateParticipants retorna um ponteiro para IEnumParticipant.'
ms.assetid: 8534d102-06ce-4e82-8f9c-9ab9f0d14df9
title: Interface IEnumParticipant (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a20a2cd8e72c5c44b054fc4658b304c8b4fa41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783369"
---
# <a name="ienumparticipant-interface"></a>Interface IEnumParticipant

\[O **IEnumParticipant** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A interface **IEnumParticipant** fornece métodos de enumeração de padrão com para a interface [**ITParticipant**](itparticipant.md) . O método [**ITParticipantControl:: EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) retorna um ponteiro para **IEnumParticipant**.

A interface **IEnumParticipant** está oculta das linguagens de Visual Basic e script.

## <a name="members"></a>Membros

A interface **IEnumParticipant** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IEnumParticipant** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IEnumParticipant** tem esses métodos.



| Método                                  | Descrição                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**8i**](ienumparticipant-clone.md) | Cria outro enumerador que contém o mesmo estado de enumeração do atual.<br/> |
| [**Avançar**](ienumparticipant-next.md)   | Obtém o próximo número especificado de elementos na sequência de enumeração.<br/>                 |
| [**Redefinir**](ienumparticipant-reset.md) | Redefine para o início da sequência de enumeração.<br/>                                    |
| [**Ignorar**](ienumparticipant-skip.md)   | Ignora o próximo número especificado de elementos na sequência de enumeração.<br/>           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

