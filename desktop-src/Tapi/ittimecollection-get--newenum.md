---
description: 'Método ITTimeCollection:: get__NewEnum-o \_ \_ método Get NewEnum retorna um enumerador para a coleção.'
ms.assetid: 0c2d739d-736d-4773-9747-1107546a973c
title: 'Método ITTimeCollection:: get__NewEnum (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ba76f1d10e2cb9ee937ec688af3e87e0bb9310df9fc39afaef64e60ea55b1dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991896"
---
# <a name="ittimecollectionget__newenum-method"></a>\_Método NewEnum ITTimeCollection:: get \_

\[os controles e as interfaces de conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ \_ NewEnum** retorna um enumerador para a coleção.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get__NewEnum(
  [out] IUnknown **pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PVal* \[ fora\]
</dt> <dd>

Ponteiro para uma interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) em um objeto enumerador para a coleção.

Chame o método [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) na interface **IUnknown** retornada para obter um ponteiro para uma interface de enumeração [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) na coleção. O **IEnumVARIANT** fornece vários métodos que você pode usar para iterar pela coleção.

Para obter mais informações, consulte a seção Comentários a seguir.

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



 

## <a name="remarks"></a>Comentários

Esse método é intercambiável com [**Get \_ EnumerationIf**](ittimecollection-get-enumerationif.md) , exceto pelo fato de que ele retorna **IUnknown** em vez de [**IEnumTime**](ienumtime.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITTimeCollection**](ittimecollection.md)
</dt> <dt>

[**ITTime**](ittime.md)
</dt> </dl>

 

