---
title: Método MoveNext IDWriteColorGlyphRunEnumerator
description: Mover para a próxima execução de glifo no enumerador.
ms.assetid: E6336C0E-F880-485C-9111-A102298257C1
keywords:
- Gravação direta do método MoveNext
- Método MoveNext Direct Write, interface IDWriteColorGlyphRunEnumerator
- Gravação direta da interface IDWriteColorGlyphRunEnumerator, método MoveNext
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator.MoveNext
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c9963916c07f1df8cf3cfedb49b9e3fd66d0df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499486"
---
# <a name="idwritecolorglyphrunenumeratormovenext-method"></a>Método IDWriteColorGlyphRunEnumerator:: MoveNext

Mover para a próxima execução de glifo no enumerador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT MoveNext(
  [out] BOOL *haveRun
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*haveRun* \[ fora\]
</dt> <dd>

Tipo: **bool \** _

Retorna _ *true** se houver uma próxima execução de glifo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]<br/>                          |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md)
</dt> </dl>

 

 





