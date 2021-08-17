---
description: Define a propriedade LineHeight no objeto InkDivider.
ms.assetid: ce5e40c5-faa1-4d66-94f4-d5bd1a11ee4c
title: Função SetLineHeight
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetLineHeight
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 2c6a176b5878b7aaee4a0e51a5a366302b13a1a643453ad2c6d57e103362c4fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966815"
---
# <a name="setlineheight-function"></a>Função SetLineHeight

Define a propriedade [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) no objeto [**InkDivider**](inkdivider-class.md) .

Essa função auxiliar não se destina a ser usada pelo código do aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI SetLineHeight(
  _In_ INT_PTR hDivider,
  _In_ LONG    lLineHeight
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDivider* \[ no\]
</dt> <dd>

Um identificador para o objeto [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*lLineHeight* \[ no\]
</dt> <dd>

A propriedade [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) do objeto [**InkDivider**](inkdivider-class.md) , em unidades HIMETRIC.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa função pode retornar um desses valores.



| Código de retorno                                                                                  | Descrição                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | A função foi bem-sucedida.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O parâmetro *pDivider* é inválido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                         |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                             |
| Biblioteca<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 
