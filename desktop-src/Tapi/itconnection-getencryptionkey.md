---
description: O método GetEncryptionKey Obtém a chave de criptografia.
ms.assetid: a80d8660-d13e-483f-b1d7-ee2043ef5cab
title: 'Método ITConnection:: GetEncryptionKey (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a237073d4842cd26797b046a4d973390ff5ef254b574bcafbc6f10abca932aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060974"
---
# <a name="itconnectiongetencryptionkey-method"></a>Método ITConnection:: GetEncryptionKey

\[os controles e as interfaces de conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **GetEncryptionKey** Obtém a chave de criptografia.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetEncryptionKey(
  [out] BSTR         *ppKeyType,
  [out] VARIANT_BOOL *pfValidKeyData,
  [out] BSTR         *ppKeyData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppKeyType* \[ fora\]
</dt> <dd>

Ponteiro para um **BSTR** que contém o tipo de chave de criptografia.

</dd> <dt>

*pfValidKeyData* \[ fora\]
</dt> <dd>

Indica a validade dos dados de chave de criptografia.

</dd> <dt>

*ppKeyData* \[ fora\]
</dt> <dd>

Ponteiro para um **BSTR** que contém os dados da chave de criptografia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                                                 |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *ppKeyType, pfValidKeyData* ou *ppKeyData* não é um ponteiro válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/>                              |
| <dl> <dt>**E \_ falha**</dt> </dl>        | Erro não especificado.<br/>                                                                |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                                               |



 

## <a name="remarks"></a>Comentários

O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada para os parâmetros *ppKeyType* e *ppKeyData* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 

