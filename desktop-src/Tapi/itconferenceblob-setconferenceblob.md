---
description: O método SetConferenceBlob confirma as alterações no blob de conferência. Para inicializar o blob de conferência pela primeira vez, use o método Init em vez disso.
ms.assetid: 4a65edb9-77de-42d9-85a1-1e3c41706417
title: 'Método ITConferenceBlob:: SetConferenceBlob (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47779807e5bde6a070b4600aec903309c7679dc8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769416"
---
# <a name="itconferenceblobsetconferenceblob-method"></a>Método ITConferenceBlob:: SetConferenceBlob

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **SetConferenceBlob** confirma as alterações no blob de conferência. Para inicializar o blob de conferência pela primeira vez, use o método [**init**](itconferenceblob-init.md) em vez disso.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetConferenceBlob(
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CharacterSet* \[ no\]
</dt> <dd>

[**Blob \_ do \_**](blob-character-set.md) Descritor do conjunto de caracteres do conjunto de caracteres do blob de conferência.

</dd> <dt>

*pBlob* \[ no\]
</dt> <dd>

Ponteiro para um **BSTR** que contém o blob de conferência.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *CharacterSet* ou *pBlob* não é válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/>  |
| <dl> <dt>**E \_ falha**</dt> </dl>        | Erro não especificado.<br/>                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                   |



 

## <a name="remarks"></a>Comentários

O aplicativo deve usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para alocar memória para o parâmetro *PBlob* e usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória quando a variável não for mais necessária.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITConferenceBlob**](itconferenceblob.md)
</dt> <dt>

[**\_conjunto de caracteres de blob \_**](blob-character-set.md)
</dt> </dl>

 

