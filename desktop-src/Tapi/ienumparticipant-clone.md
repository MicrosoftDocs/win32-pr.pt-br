---
description: O método Clone cria outro enumerador que contém o mesmo estado de enumeração que o atual. Esse método está oculto de linguagens Visual Basic script e de script.
ms.assetid: 551e0ddc-7ebf-4fc2-a155-0c9ee2f406d4
title: Método IEnumParticipant::Clone (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eccd4bd29442daa01e632ae83510a87eebb06cb72beafc206b04d47c3dd761db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140489"
---
# <a name="ienumparticipantclone-method"></a>Método IEnumParticipant::Clone

\[**O** clone não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método Clone** cria outro enumerador que contém o mesmo estado de enumeração que o atual. Esse método está oculto de linguagens Visual Basic script e de script.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Clone(
  [out] IEnumParticipant **ppEnum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppEnum* \[ out\]
</dt> <dd>

Ponteiro para a nova interface [**IEnumParticipant.**](ienumparticipant.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | O *parâmetro ppEnum* não é um ponteiro válido.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>  | Falha por motivos desconhecidos.<br/>                          |



 

## <a name="remarks"></a>Comentários

TAPI chama o [**método AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) na interface [**IEnumParticipant**](ienumparticipant.md) retornada por **IEnumParticipant::Clone.** O aplicativo deve chamar [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) na interface **IEnumParticipant** para liberar recursos associados a ele.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumParticipant**](ienumparticipant.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

