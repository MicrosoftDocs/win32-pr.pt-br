---
title: Método IDWriteTextLayout3 GetLineSpacing
description: Obtém informações de espaçamento de linha.
ms.assetid: 6b93a3ec-c8ea-2e64-45b5-51565d6de173
keywords:
- Gravação direta do método GetLineSpacing
- Método GetLineSpacing Direct Write, interface IDWriteTextLayout3
- IDWriteTextLayout3 interface de gravação direta, método GetLineSpacing
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96444f0e50cbb79074c6fc6d8b041d91c0751616ec5afe7024704709a2240947
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964006"
---
# <a name="idwritetextlayout3getlinespacing-method"></a>Método IDWriteTextLayout3:: GetLineSpacing

Obtém informações de espaçamento de linha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetLineSpacing(
  [out] DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lineSpacingOptions* \[ fora\]
</dt> <dd>

Como gerenciar o espaço entre as linhas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Somente aplicativos da área de trabalho R2\]<br/>                                 |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteTextLayout3**](idwritetextlayout3.md)
</dt> </dl>

 

 





