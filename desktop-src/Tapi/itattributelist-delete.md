---
description: O método Delete exclui o atributo no índice especificado.
ms.assetid: 6bc6f3d2-d630-4a00-9d74-fb5fa7626e3f
title: Método ITAttributeList::D elete (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8391b1e505f08227bc28351b698f2ab97371a93b89e2850f2befee67b2461c47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061034"
---
# <a name="itattributelistdelete-method"></a>Método ITAttributeList::D elete

\[As interfaces e controles de Conferência de Telefonia IP de reunião não estão disponíveis para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método Delete** exclui o atributo no índice especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Índice* \[ Em\]
</dt> <dd>

Índice do atributo a ser excluído.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O *parâmetro Index* não é válido.<br/>                  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Erro não especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITAttributeList**](itattributelist.md)
</dt> </dl>

 

 




