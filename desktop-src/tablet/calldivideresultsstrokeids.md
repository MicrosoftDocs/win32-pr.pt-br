---
description: Recupera as propriedades de ID dos objetos IInkStrokeDisp da palavra, da linha, do parágrafo ou do desenho correspondente determinado pela análise de tinta.
ms.assetid: f05ffa3b-2a47-46fe-bb8f-e682aa094b69
title: Função CallDivideResultsStrokeIds
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
ms.openlocfilehash: ee690c9564df3b8c75eca6eec8eeb88b7531f4ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105773013"
---
# <a name="calldivideresultsstrokeids-function"></a>Função CallDivideResultsStrokeIds

Recupera as propriedades de [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) dos objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) da palavra, da linha, do parágrafo ou do desenho correspondente determinado pela análise de tinta.

Esta função não se destina a ser usada pelo código do aplicativo.

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

*hDivider* \[ no\]
</dt> <dd>

Um identificador para o objeto [divisória](the-divider-object.md) .

</dd> <dt>

*\[ aWordStrokeIds \]* \[out\]
</dt> <dd>

Uma matriz das IDs de traço da tinta na palavra.

</dd> <dt>

*\[ aLineStrokeIds \]* \[out\]
</dt> <dd>

Uma matriz das IDs de traço da tinta na linha.

</dd> <dt>

*\[ aParagraphStrokeIds \]* \[out\]
</dt> <dd>

Uma matriz das IDs de traço da tinta no parágrafo.

</dd> <dt>

*\[ aDrawingStrokeIds \]* \[out\]
</dt> <dd>

Uma matriz das IDs de traço da tinta no desenho.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função pode retornar um desses valores.



| Código de retorno                                                                                  | Description                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | A função foi bem-sucedida.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O parâmetro *hDivider* é inválido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                         |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                             |
| Biblioteca<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




