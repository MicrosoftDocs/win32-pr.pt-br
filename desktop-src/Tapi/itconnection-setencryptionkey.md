---
description: O método SetEncryptionKey define a chave de criptografia necessária para descriptografar a sessão ou uma indicação para um mecanismo para obter uma chave utilizável por meios externos.
ms.assetid: 9efcf90e-3645-49f4-b27d-9a8246637310
title: 'Método ITConnection:: SetEncryptionKey (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91d0ce079d3815897c348e553df0af8dece8592b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757966"
---
# <a name="itconnectionsetencryptionkey-method"></a>Método ITConnection:: SetEncryptionKey

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **SetEncryptionKey** define a chave de criptografia necessária para descriptografar a sessão ou uma indicação para um mecanismo para obter uma chave utilizável por meios externos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetEncryptionKey(
  [in] BSTR pKeyType,
  [in] BSTR *ppKeyData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pKeyType* \[ no\]
</dt> <dd>

Ponteiro para um **BSTR** que contém o tipo de chave de criptografia.

</dd> <dt>

*ppKeyData* \[ no\]
</dt> <dd>

Ponteiro para um **BSTR** contendo informações de chave de criptografia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                          | Descrição                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

O aplicativo deve usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para alocar memória para os parâmetros *pKeyType* e *ppKeyData* . O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória quando as variáveis não forem mais necessárias.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 

