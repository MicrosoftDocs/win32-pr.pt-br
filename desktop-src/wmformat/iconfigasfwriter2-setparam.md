---
title: Método IConfigAsfWriter2 SetParam
description: O método SetParam define o valor do parâmetro de configuração de filtro especificado.
ms.assetid: b8067fb2-c379-4b26-b4f7-c790604e3edc
keywords:
- Formato de mídia do windows do método SetParam
- Formato de mídia do windows do método SetParam, interface IConfigAsfWriter2
- Formato de mídia da interface IConfigAsfWriter2 , método SetParam
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.SetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e7c73831ec45e6e0b65444e93e976fe349a2d4576d578f3399c60c399628cbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847494"
---
# <a name="iconfigasfwriter2setparam-method"></a>Método IConfigAsfWriter2::SetParam

O **método SetParam** define o valor do parâmetro de configuração de filtro especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetParam(
  [in] DWORD dwParam,
  [in] DWORD dwParam1,
  [in] DWORD dwParam2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwParam* \[ Em\]
</dt> <dd>

Especifica o parâmetro a ser definido. Ele deve ser um valor definido na [ \_ \_ enumeração AM ASFWRITERCONFIG \_ PARAM.](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85))

</dd> <dt>

*dwParam1* \[ Em\]
</dt> <dd>

Especifica o valor a ser atribuído ao *parâmetro dwParam.*

</dd> <dt>

*dwParam2* \[ Em\]
</dt> <dd>

Não usado; deve ser 0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará S \_ OK. Se falhar, ele retornará um código **de erro HRESULT.**

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> <dt>

[**IConfigAsfWriter2::GetParam**](iconfigasfwriter2-getparam.md)
</dt> </dl>

 

 