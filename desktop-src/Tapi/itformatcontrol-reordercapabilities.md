---
description: O método ReOrderCapabilities define um novo pedido para recursos de formato.
ms.assetid: 05785d64-a22f-411f-9fae-318828d30c52
title: 'Método ITFormatControl:: ReOrderCapabilities (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d6f7800e4a04dbd70c5b270778cd7eb0ff540b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759470"
---
# <a name="itformatcontrolreordercapabilities-method"></a>Método ITFormatControl:: ReOrderCapabilities

\[ Esse método não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **ReOrderCapabilities** define um novo pedido para recursos de formato.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReOrderCapabilities(
  [in] DWORD *pdwIndices,
  [in] BOOL  *pfEnabled,
  [in] BOOL  *pfPublicize,
  [in] DWORD dwNumIndices
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pdwIndices* \[ no\]
</dt> <dd>

Índice do formato que está sendo reordenado.

</dd> <dt>

*pfEnabled* \[ no\]
</dt> <dd>

Indica se o formato deve ser habilitado ou desabilitado.

</dd> <dt>

*pfPublicize* \[ no\]
</dt> <dd>

Indica se o formato deve ser disponibilizado.

</dd> <dt>

*dwNumIndices* \[ no\]
</dt> <dd>

Novo número de índice para o formato.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

O método [**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) deve ser chamado antes do uso desse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,1<br/>                                                         |
| parâmetro<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITFormatControl**](itformatcontrol.md)
</dt> <dt>

[**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md)
</dt> </dl>

 

 




