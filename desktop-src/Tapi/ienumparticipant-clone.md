---
description: O método clone cria outro enumerador que contém o mesmo estado de enumeração que o atual. Esse método é ocultado das linguagens de Visual Basic e script.
ms.assetid: 551e0ddc-7ebf-4fc2-a155-0c9ee2f406d4
title: 'Método IEnumParticipant:: clone (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5b094f47738fd23f2762b7012a4e23c8b89da57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780606"
---
# <a name="ienumparticipantclone-method"></a>Método IEnumParticipant:: clone

\[O **clone** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **clone** cria outro enumerador que contém o mesmo estado de enumeração que o atual. Esse método é ocultado das linguagens de Visual Basic e script.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Clone(
  [out] IEnumParticipant **ppEnum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppEnum* \[ fora\]
</dt> <dd>

Ponteiro para a nova interface [**IEnumParticipant**](ienumparticipant.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *ppEnum* não é um ponteiro válido.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ inesperado**</dt> </dl>  | Falha por motivos desconhecidos.<br/>                          |



 

## <a name="remarks"></a>Comentários

A TAPI chama o método [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) na interface [**IEnumParticipant**](ienumparticipant.md) retornada por **IEnumParticipant:: clone**. O aplicativo deve chamar [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) na interface **IEnumParticipant** para liberar recursos associados a ela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumParticipant**](ienumparticipant.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

