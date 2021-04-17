---
title: Método SetParam IConfigAsfWriter2
description: O método SetParam define o valor do parâmetro de configuração de filtro especificado.
ms.assetid: b8067fb2-c379-4b26-b4f7-c790604e3edc
keywords:
- Método SetParam Windows Media Format
- Método SetParam Windows Media Format, interface IConfigAsfWriter2
- IConfigAsfWriter2 interface formato Windows Media, método SetParam
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.SetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f123bf11c8297f3a7ce0d4b0047874d8d7b31b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105811536"
---
# <a name="iconfigasfwriter2setparam-method"></a>Método IConfigAsfWriter2:: SetParam

O método **SetParam** define o valor do parâmetro de configuração de filtro especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetParam(
  [in] DWORD dwParam,
  [in] DWORD dwParam1,
  [in] DWORD dwParam2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwParam* \[ no\]
</dt> <dd>

Especifica o parâmetro a ser definido. Ele deve ser um valor definido na enumeração do [ \_ \_ \_ parâmetro am ASFWRITERCONFIG](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) .

</dd> <dt>

*dwParam1* \[ no\]
</dt> <dd>

Especifica o valor a ser atribuído ao parâmetro *dwParam* .

</dd> <dt>

*dwParam2* \[ no\]
</dt> <dd>

Não usado; deve ser 0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem sucedido, ele retornará S \_ OK. Se falhar, ele retornará um código de erro **HRESULT** .

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> <dt>

[**IConfigAsfWriter2:: GetParam**](iconfigasfwriter2-getparam.md)
</dt> </dl>

 

 