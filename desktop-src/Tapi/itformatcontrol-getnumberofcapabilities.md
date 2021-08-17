---
description: O método GetNumberOfCapabilities recupera o número de recursos associados ao formato atual.
ms.assetid: 26e51c0d-c1cb-410f-ab19-eb884afa8431
title: Método ITFormatControl::GetNumberOfCapabilities (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57bd79b61f8c41893ec8d99ffc9bfadcc3887631c885d5caa430a6fb723396a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117945271"
---
# <a name="itformatcontrolgetnumberofcapabilities-method"></a>Método ITFormatControl::GetNumberOfCapabilities

\[Esse método não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método GetNumberOfCapabilities** recupera o número de recursos associados ao formato atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetNumberOfCapabilities(
  [out] DWORD *pdwCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pdwCount* \[ out\]
</dt> <dd>

Contagem dos recursos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.1<br/>                                                         |
| Cabeçalho<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITFormatControl**](itformatcontrol.md)
</dt> </dl>

 

 




