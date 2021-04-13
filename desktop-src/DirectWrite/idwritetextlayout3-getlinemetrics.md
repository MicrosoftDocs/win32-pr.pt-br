---
title: Método IDWriteTextLayout3 GetLineMetrics
description: Recupera as propriedades de cada linha.
ms.assetid: 352ca3e3-7b08-823c-0881-0b051d4ce574
keywords:
- Gravação direta do método GetLineMetrics
- Método GetLineMetrics Direct Write, interface IDWriteTextLayout3
- IDWriteTextLayout3 interface de gravação direta, método GetLineMetrics
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d10a06cbf123b71e1308b45c747ac8a840a5fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455413"
---
# <a name="idwritetextlayout3getlinemetrics-method"></a>Método IDWriteTextLayout3:: GetLineMetrics

Recupera as propriedades de cada linha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetLineMetrics(
  [out] DWRITE_LINE_METRICS1 *lineMetrics,
        UINT32               maxLineCount,
  [out] UINT32               *actualLineCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lineMetrics* \[ fora\]
</dt> <dd>

A matriz a ser preenchida com informações de linha.

</dd> <dt>

*maxLineCount* 
</dt> <dd>

O tamanho máximo da matriz lineMetrics.

</dd> <dt>

*actualLineCount* \[ fora\]
</dt> <dd>

O tamanho real da matriz lineMetrics necessária.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Se maxLineCount não for suficientemente grande E \_ não for \_ suficiente \_ buffer, o que é equivalente a HRESULT \_ do \_ Win32 (erro \_ buffer insuficiente \_ ), é retornado e actualLineCount é definido como o número de linhas necessárias.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                 |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteTextLayout3**](idwritetextlayout3.md)
</dt> </dl>

 

 





