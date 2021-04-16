---
description: Recupera informações de análise do objeto InkDivider.
ms.assetid: 1b073da4-80f4-48f4-8ff6-b21793c173a8
title: Função CallDivide
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivide
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 0084811ee471bee8fe67653dace49fa83642a7fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501138"
---
# <a name="calldivide-function"></a>Função CallDivide

Recupera informações de análise do objeto [**InkDivider**](inkdivider-class.md) .

Esta função não se destina a ser usada pelo código do aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI CallDivide(
  _In_  INT_PTR hDivider,
  _In_  int     *pWordSize,
  _In_  int     *pLineSize,
  _In_  int     *pParagraphSize,
  _In_  int     *pDrawingSize,
  _Out_ int     *pWordCount,
  _Out_ int     *pLineCount,
  _Out_ int     *pParagraphCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDivider* \[ no\]
</dt> <dd>

Um identificador para o objeto [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*pWordSize* \[ no\]
</dt> <dd>

O tamanho da palavra retornada pelo objeto [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*pLineSize* \[ no\]
</dt> <dd>

O tamanho da linha retornada pelo objeto [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*pParagraphSize* \[ no\]
</dt> <dd>

O tamanho do parágrafo retornado pelo objeto [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*pDrawingSize* \[ no\]
</dt> <dd>

O tamanho do desenho retornado pelo objeto [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*pWordCount* \[ fora\]
</dt> <dd>

O número de palavras retornadas pela análise de tinta.

</dd> <dt>

*pLineCount* \[ fora\]
</dt> <dd>

O número de linhas retornadas pela análise de tinta.

</dd> <dt>

*pParagraphCount* \[ fora\]
</dt> <dd>

O número de parágrafos retornados pela análise de tinta.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função pode retornar um desses valores.



| Código de retorno                                                                                  | Descrição                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | A função bem-sucedido.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Um ou mais parâmetros são inválidos.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                         |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                             |
| Biblioteca<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




