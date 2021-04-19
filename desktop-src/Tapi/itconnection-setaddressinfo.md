---
description: O método SetAddressInfo define as informações de endereço.
ms.assetid: 100b96af-e6ba-4496-9978-4df133e1c2b5
title: 'Método ITConnection:: SetAddressInfo (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae181911527c22639c8c2da3038c0377734fd1da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767757"
---
# <a name="itconnectionsetaddressinfo-method"></a>Método ITConnection:: SetAddressInfo

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **SetAddressInfo** define as informações de endereço.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetAddressInfo(
  [in] BSTR          pStartAddress,
  [in] LONG          NumAddresses,
  [in] unsigned char Ttl
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStartAddress* \[ no\]
</dt> <dd>

Ponteiro para um **BSTR** que contém o endereço inicial.

</dd> <dt>

*NumAddresses* \[ no\]
</dt> <dd>

Número de endereços a serem usados para a sessão.

</dd> <dt>

*TTL* \[ no\]
</dt> <dd>

escopo [*TTL (vida útil)*](t-tapgloss.md) para transmissões nos endereços.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                         | Significado                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *pStartAddress*, *NumAddresses* ou *TTL* não é válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/>                  |
| <dl> <dt>**E \_ falha**</dt> </dl>        | Erro não especificado.<br/>                                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                                   |



 

## <a name="remarks"></a>Comentários

O aplicativo deve usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para alocar memória para o parâmetro *PStartAddress* e usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória quando a variável não for mais necessária.

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

 

