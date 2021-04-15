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
ms.openlocfilehash: be4045e01ac890471536d95768668b633d8f2249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761640"
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

## <a name="return-value"></a>Retornar valor

Essa função pode retornar um desses valores.



| Código de retorno                                                                                  | Descrição                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | A função foi bem-sucedida.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O parâmetro *pDivider* é inválido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                         |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                             |
| Biblioteca<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 
