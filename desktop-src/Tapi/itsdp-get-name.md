---
description: O \_ método Get Name Obtém o nome da sessão.
ms.assetid: 97b44a01-585b-434c-ad59-51c35e8a1ceb
title: 'Método ITSdp:: get_Name (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 930aaa1edcfb93f6a02a4ebe97acbbfcc1cfd42e8187d0ea14cf661c7ad7f66c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012886"
---
# <a name="itsdpget_name-method"></a>Método de nome de ITSdp:: get \_

\[os controles e as interfaces de conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ Name** Obtém o nome da sessão. Isso deve ser uma cadeia de caracteres ASCII conversível se o conjunto de caracteres for ASCII. (Caso contrário, pode ser qualquer cadeia de caracteres **BSTR** .)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Name(
  [out] BSTR *ppName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppName* \[ fora\]
</dt> <dd>

Ponteiro para um **BSTR** que contém o nome da sessão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *ppName* não é um ponteiro válido.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ falha**</dt> </dl>        | Erro não especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                  |



 

## <a name="remarks"></a>Comentários

O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada para o parâmetro *ppName* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITSdp: nome de:p UT \_**](itsdp-put-name.md)
</dt> </dl>

 

