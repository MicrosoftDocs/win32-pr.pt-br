---
description: O \_ método Get Description obtém a descrição da sessão (BSTR).
ms.assetid: 09a372fe-0dcd-4daf-8f13-c4c89b1ecd16
title: 'Método ITSdp:: get_Description (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f60f7aefcfac852a1665f54a59ff0541b1d82a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810134"
---
# <a name="itsdpget_description-method"></a>Método de descrição de ITSdp:: get \_

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ Description** Obtém a descrição da sessão (**BSTR**). Isso deve ser uma cadeia de caracteres ASCII conversível se o conjunto de caracteres for ASCII. (Caso contrário, pode ser qualquer cadeia de caracteres **BSTR** .)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Description(
  [out] BSTR *ppDescription
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppDescription* \[ fora\]
</dt> <dd>

Ponteiro para um **BSTR** que contém a descrição da sessão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                     |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *ppDescription* não é um ponteiro válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/>  |
| <dl> <dt>**E \_ falha**</dt> </dl>        | Erro não especificado.<br/>                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                   |



 

## <a name="remarks"></a>Comentários

O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar o parâmetro *ppDescription* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**Descrição do ITSdp::p UT \_**](itsdp-put-description.md)
</dt> </dl>

 

