---
description: O \_ método obter contagem Obtém o número de atributos.
ms.assetid: dc607f09-4cca-4ef0-8b86-dbc5e6edcfdd
title: 'Método ITAttributeList:: get_Count (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83033546b75e7dda9da26fa910404e2739f40d651e0be79338b49fb5c98b9415
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762442"
---
# <a name="itattributelistget_count-method"></a>Método de contagem ITAttributeList:: get \_

\[os controles e as interfaces de conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **obter \_ contagem** Obtém o número de atributos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Count(
  [out] LONG *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PVal* \[ fora\]
</dt> <dd>

Contagem dos atributos na lista.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *PVal* não é um ponteiro válido.<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ falha**</dt> </dl>        | Erro não especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITAttributeList**](itattributelist.md)
</dt> </dl>

 

 




