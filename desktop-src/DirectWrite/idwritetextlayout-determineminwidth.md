---
title: Método IDWriteTextLayout DetermineMinWidth
description: Determina a largura mínima possível em que o layout pode ser definido sem a interrupção de emergência entre os caracteres de palavras inteiras que estão ocorrendo.
ms.assetid: 8efa1471-1b74-46d4-ac6d-fb1839ce2e74
keywords:
- Gravação direta do método DetermineMinWidth
- Método DetermineMinWidth Direct Write, interface IDWriteTextLayout
- IDWriteTextLayout interface de gravação direta, método DetermineMinWidth
topic_type:
- apiref
api_name:
- IDWriteTextLayout.DetermineMinWidth
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41123f2a5d584341c344248d0af936f34fc04e49c9aabc1cb73ecea0eacc84ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075526"
---
# <a name="idwritetextlayoutdetermineminwidth-method"></a>IDWriteTextLayout: método etermineMinWidth de:D

Determina a largura mínima possível em que o layout pode ser definido sem a interrupção de emergência entre os caracteres de palavras inteiras que estão ocorrendo.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT DetermineMinWidth(
  [out] FLOAT *minWidth
) = 0;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*minWidth* \[ fora\]
</dt> <dd>

Tipo: **float \***

Largura mínima.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

