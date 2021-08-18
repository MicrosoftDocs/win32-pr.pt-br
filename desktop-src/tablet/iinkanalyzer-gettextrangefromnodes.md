---
description: Localiza o intervalo de texto na cadeia de caracteres reconhecida que corresponde a uma coleção de objetos IContextNode.
ms.assetid: 2c5bc4a1-08de-4872-b552-6d22924ce2a8
title: Método IInkAnalyzer::GetTextRangeFromNodes (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetTextRangeFromNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 147877ef8871f7b07e2aa501a107c1e40bd75e80009e5bee97dca03346bb853a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092126"
---
# <a name="iinkanalyzergettextrangefromnodes-method"></a>Método IInkAnalyzer::GetTextRangeFromNodes

Localiza o intervalo de texto na cadeia de caracteres reconhecida que corresponde a uma coleção de [**objetos IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTextRangeFromNodes(
  [out] LONG          *plStart,
  [out] LONG          *plLength,
  [in]  IContextNodes *pNodesToSearch
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*plStart* \[ out\]
</dt> <dd>

Um inteiro com sinal de 32 bits que indica o início do intervalo de texto. Este parâmetro é passado não inicializado.

</dd> <dt>

*plLength* \[ out\]
</dt> <dd>

Um inteiro com sinal de 32 bits que indica o comprimento do intervalo de texto. Este parâmetro é passado não inicializado.

</dd> <dt>

*pNodesToSearch* \[ Em\]
</dt> <dd>

A coleção de [**objetos IContextNode**](icontextnode.md) para os quais encontrar o intervalo de texto.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

Se *pNodesToSearch* contiver objetos [**IContextNode**](icontextnode.md) que não são adjacentes, esse método retornará o menor intervalo de texto que abrange todos os **objetos IContextNode.**

Esse método lança uma exceção E \_ INVALIDARG quando *pNodesToSearch* contém um [**IContextNode**](icontextnode.md) que não está associado ao [**IInkAnalyzer.**](iinkanalyzer.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> </dl>

 

 




