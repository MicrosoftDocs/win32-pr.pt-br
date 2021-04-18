---
description: O método Init Inicializa o blob de conferência com base em uma cadeia de caracteres textual. Se pBlob for NULL, os valores padrão serão usados.
ms.assetid: ba492503-90ff-45dd-a39f-6d4451e57339
title: 'Método ITConferenceBlob:: init (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81bdd512ffeb4b380da04e59deb17315d00b7285
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789459"
---
# <a name="itconferenceblobinit-method"></a>Método ITConferenceBlob:: init

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **init** Inicializa o blob de conferência com base em uma cadeia de caracteres textual. Se *pBlob* for **NULL**, os valores padrão serão usados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Init(
  [in] BSTR               pName,
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* \[ no\]
</dt> <dd>

Ponteiro para uma representação **BSTR** do nome da conferência.

</dd> <dt>

*CharacterSet* \[ no\]
</dt> <dd>

[**Blob \_ do \_**](blob-character-set.md) Descritor do conjunto de caracteres do conjunto de caracteres.

</dd> <dt>

*pBlob* \[ no\]
</dt> <dd>

Ponteiro para um **BSTR** que contém o blob de conferência. Se for **NULL**, o blob de conferência será inicializado com valores padrão. Atualmente, os valores de conferência padrão só estarão disponíveis se o parâmetro *CharacterSet* estiver definido como BCS \_ ASCII.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                         | Significado                                                                    |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *pname*, *CharacterSet* ou *pBlob* não é válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/>            |
| <dl> <dt>**E \_ falha**</dt> </dl>        | Erro não especificado.<br/>                                              |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                             |



 

## <a name="remarks"></a>Comentários

**ITConferenceBlob:: init** retornará uma falha se o blob já tiver sido inicializado.

O aplicativo deve usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para alocar memória para os parâmetros *pname* e *pBlob* . O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória quando as variáveis não forem mais necessárias.

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

 

