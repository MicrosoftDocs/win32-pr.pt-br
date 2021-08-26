---
description: Recupera as propriedades de ID para os objetos IInkStrkeDisp da palavra, linha, parágrafo ou desenho correspondentes determinados pela análise de tinta.
ms.assetid: f05ffa3b-2a47-46fe-bb8f-e682aa094b69
title: Função CallDivideResultsRogkeIds
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResultsStrokeIds
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 64b3e4180a34c45890408f8ba92cc79465fffa7f1028152e27f8d5c0aa40e3e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009126"
---
# <a name="calldivideresultsstrokeids-function"></a>Função CallDivideResultsRogkeIds

Recupera as [**propriedades de ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) para os [**objetos IInkStrkeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) da palavra, linha, parágrafo ou desenho correspondentes determinados pela análise de tinta.

Essa função não se destina a ser usada pelo código do aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI CallDivideResultsStrokeIds(
  _In_  INT_PTR hDivider,
  _Out_ int     aWordStrokeIds[],
  _Out_ int     aLineStrokeIds[],
  _Out_ int     aParagraphStrokeIds[],
  _Out_ int     aDrawingStrokeIds[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDivider* \[ Em\]
</dt> <dd>

Um identificador para o [objeto Divisor.](the-divider-object.md)

</dd> <dt>

*aWordStrokeIds \[ \]* \[out\]
</dt> <dd>

Uma matriz das IDs de traço da tinta na palavra.

</dd> <dt>

*aLineStrkeIds \[ \]* \[out\]
</dt> <dd>

Uma matriz das IDs de traço da tinta na linha.

</dd> <dt>

*aParagraphStrkeIds \[ \]* \[out\]
</dt> <dd>

Uma matriz das IDs de traço da tinta no parágrafo.

</dd> <dt>

*aDrawingStrkeIds \[ \]* \[out\]
</dt> <dd>

Uma matriz das IDs de traço da tinta no desenho.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa função pode retornar um desses valores.



| Código de retorno                                                                                  | Descrição                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | A função foi bem-sucedida.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O *parâmetro hDivider* é inválido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                         |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                             |
| Biblioteca<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




