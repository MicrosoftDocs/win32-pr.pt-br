---
description: O \_ método Get MediaTitle recupera um título textual para a mídia que o aplicativo pode usar para fins informativos ou de exibição. Isso deve ser uma cadeia de caracteres ASCII conversível se o conjunto de caracteres for ASCII. Caso contrário, pode ser qualquer cadeia de caracteres BSTR.
ms.assetid: c5567672-54f0-45d6-81d2-5a501a33c25f
title: 'Método ITMedia:: get_MediaTitle (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f2ec4bf16fc27c23277113ee13c8fe02f89c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810136"
---
# <a name="itmediaget_mediatitle-method"></a>Método ITMedia:: get \_ MediaTitle

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ MediaTitle** recupera um título textual para a mídia que o aplicativo pode usar para fins informativos ou de exibição. Isso deve ser uma cadeia de caracteres ASCII conversível se o conjunto de caracteres for ASCII. Caso contrário, pode ser qualquer cadeia de caracteres **BSTR** .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_MediaTitle(
  [out] BSTR *ppMediaTitle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppMediaTitle* \[ fora\]
</dt> <dd>

Ponteiro para um **BSTR** que contém o título da mídia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *ppMediaTitle* não é um ponteiro válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ falha**</dt> </dl>        | Erro não especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                  |



 

## <a name="remarks"></a>Comentários

O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada para o parâmetro *ppMediaTitle* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMedia::P UT \_ MediaTitle**](itmedia-put-mediatitle.md)
</dt> </dl>

 

