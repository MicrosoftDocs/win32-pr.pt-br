---
description: O método put MediaTitle define um título textual para a mídia que o aplicativo pode usar para \_ fins informacionais ou de exibição. Deve ser uma cadeia de caracteres conversível ASCII se o conjunto de caracteres for ASCII. Caso contrário, pode ser qualquer cadeia de caracteres BSTR.
ms.assetid: bbab033b-bd37-4ef6-9e84-1d0b17ecbd4e
title: Método ITMedia::p ut_MediaTitle (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd07111cfa737be7ec5750a147ffd8d598e68b819f27f03a901a01fd66fbfdb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682746"
---
# <a name="itmediaput_mediatitle-method"></a>Método ITMedia::p Ut \_ MediaTitle

\[As interfaces e controles de Conferência de Telefonia IP de reunião não estão disponíveis para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método \_ put MediaTitle** define um título textual para a mídia que o aplicativo pode usar para fins informacionais ou de exibição. Deve ser uma cadeia de caracteres conversível ASCII se o conjunto de caracteres for ASCII. Caso contrário, pode ser qualquer cadeia **de caracteres BSTR.**

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_MediaTitle(
  [in] BSTR pMediaTitle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMediaTitle* \[ Em\]
</dt> <dd>

Ponteiro para um **BSTR** que contém o título da mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | O *parâmetro pMediaTitle* não é um ponteiro válido.<br/>  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O *parâmetro pMediaTitle* não é válido.<br/>            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Erro não especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                  |



 

## <a name="remarks"></a>Comentários

O aplicativo deve usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para alocar memória para o parâmetro *pMediaTitle* e usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória quando a variável não for mais necessária.

Essa função pode enviar dados pela transmissão em formato não criptografado; portanto, alguém que está escutando na rede pode conseguir ler os dados. O risco de segurança de enviar os dados em texto não claro deve ser considerado antes de usar esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Itmedia**](itmedia.md)
</dt> <dt>

[**ITMedia::get \_ MediaTitle**](itmedia-get-mediatitle.md)
</dt> </dl>

 

