---
description: O \_ método Put MediaTitle define um título textual para a mídia que o aplicativo pode usar para fins informativos ou de exibição. Isso deve ser uma cadeia de caracteres ASCII conversível se o conjunto de caracteres for ASCII. Caso contrário, pode ser qualquer cadeia de caracteres BSTR.
ms.assetid: bbab033b-bd37-4ef6-9e84-1d0b17ecbd4e
title: 'ITMedia: método de ut_MediaTitle de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d1abee91b08555f79437e5e26710761429e4f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760163"
---
# <a name="itmediaput_mediatitle-method"></a>ITMedia: método UT \_ MediaTitle:p

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Put \_ MediaTitle** define um título textual para a mídia que o aplicativo pode usar para fins informativos ou de exibição. Isso deve ser uma cadeia de caracteres ASCII conversível se o conjunto de caracteres for ASCII. Caso contrário, pode ser qualquer cadeia de caracteres **BSTR** .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_MediaTitle(
  [in] BSTR pMediaTitle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMediaTitle* \[ no\]
</dt> <dd>

Ponteiro para um **BSTR** que contém o título da mídia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *pMediaTitle* não é um ponteiro válido.<br/>  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *pMediaTitle* não é válido.<br/>            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ falha**</dt> </dl>        | Erro não especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                  |



 

## <a name="remarks"></a>Comentários

O aplicativo deve usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para alocar memória para o parâmetro *PMediaTitle* e usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória quando a variável não for mais necessária.

Essa função pode enviar dados pela transmissão em formato não criptografado; Portanto, alguém que está interceptando na rede pode ser capaz de ler os dados. O risco de segurança de enviar os dados em texto não criptografado deve ser considerado antes de usar esse método.

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

[**ITMedia:: obter \_ MediaTitle**](itmedia-get-mediatitle.md)
</dt> </dl>

 

