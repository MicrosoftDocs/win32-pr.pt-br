---
title: Método IDWriteInlineObject GetOverhangMetrics
description: IDWriteTextLayout chama essa função de retorno de chamada para obter as extensões visíveis (em DIPs) do objeto embutido. No caso de um bitmap simples, sem preenchimento e nenhuma folga, todas as Sobretravas serão simplesmente zeradas.
ms.assetid: b3b3e9f0-ee35-4117-9a62-a975c03b5ca9
keywords:
- Gravação direta do método GetOverhangMetrics
- Método GetOverhangMetrics Direct Write, interface IDWriteInlineObject
- IDWriteInlineObject interface de gravação direta, método GetOverhangMetrics
topic_type:
- apiref
api_name:
- IDWriteInlineObject.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 011794fc3804435dd565a00035247436814c41474c60b66f90c5cb5d9594f6c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928146"
---
# <a name="idwriteinlineobjectgetoverhangmetrics-method"></a>Método IDWriteInlineObject:: GetOverhangMetrics

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chama essa função de retorno de chamada para obter as extensões visíveis (em DIPs) do objeto embutido. No caso de um bitmap simples, sem preenchimento e nenhuma folga, todas as Sobretravas serão simplesmente zeradas.

Os sobretravamentos devem ser retornados em relação ao tamanho relatado do objeto (consulte [**\_ \_ \_ métricas de objeto embutido DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics)) e não devem ser ajustados de linha de base.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sobretravamentos* \[ fora\]
</dt> <dd>

Tipo: **[ **DWRITE \_ de \_ métricas de folga**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***

Exceder as extensões visíveis (em DIPs) fora do objeto.

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

[**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> <dt>

[**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> </dl>

 

