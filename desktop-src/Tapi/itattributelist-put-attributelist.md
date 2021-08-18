---
description: O \_ método Put atributolist define a lista de atributos.
ms.assetid: f7d57c0c-9114-42a4-b2bc-c812334d8136
title: 'ITAttributeList: método de ut_AttributeList de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c68ccbf8349b9f78f2893263345f7f76af2dec3e197daa73789a471887d685c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003474"
---
# <a name="itattributelistput_attributelist-method"></a>ITAttributeList::p método de atributo de UT \_

\[os controles e as interfaces de conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Put \_ atributolist** define a lista de atributos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_AttributeList(
  [in] VARIANT newVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*newVal* \[ no\]
</dt> <dd>

Matriz de atributos a ser definida.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *newVal* não é válido.<br/>                 |
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
</dt> <dt>

[**ITAttributeList:: obter \_ atributolist**](itattributelist-get-attributelist.md)
</dt> </dl>

 

 




