---
description: O \_ método Get StartAddress Obtém o primeiro endereço a ser usado para a sessão.
ms.assetid: 3c4fec19-1b7d-4052-afd8-7aaf095907d0
title: 'Método ITConnection:: get_StartAddress (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0c21f704d734c1d0cdccd7f796898e3770cfab19e0f3ab7ee728e86810b2a2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140349"
---
# <a name="itconnectionget_startaddress-method"></a>Método StartAddress ITConnection:: get \_

\[os controles e as interfaces de conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ StartAddress** Obtém o primeiro endereço a ser usado para a sessão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_StartAddress(
  [out] BSTR *ppStartAddress
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppStartAddress* \[ fora\]
</dt> <dd>

Ponteiro para um **BSTR** que contém o endereço inicial da sessão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                      |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *ppStartAddress* não é um ponteiro válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/>   |
| <dl> <dt>**E \_ falha**</dt> </dl>        | Erro não especificado.<br/>                                     |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                    |



 

## <a name="remarks"></a>Comentários

O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada para o parâmetro *ppStartAddress* .

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

 

