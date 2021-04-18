---
description: Localiza o intervalo de texto na cadeia de caracteres reconhecida que corresponde a uma coleção de objetos IContextNode.
ms.assetid: 2c5bc4a1-08de-4872-b552-6d22924ce2a8
title: 'Método IInkAnalyzer:: GetTextRangeFromNodes (IACom. h)'
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
ms.openlocfilehash: da27206a33ca58cebd10192393c4cf2efd1d5919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768324"
---
# <a name="iinkanalyzergettextrangefromnodes-method"></a>Método IInkAnalyzer:: GetTextRangeFromNodes

Localiza o intervalo de texto na cadeia de caracteres reconhecida que corresponde a uma coleção de objetos [**IContextNode**](icontextnode.md) .

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

*plStart* \[ fora\]
</dt> <dd>

Um inteiro com sinal de 32 bits que indica o início do intervalo de texto. Este parâmetro é passado não inicializado.

</dd> <dt>

*plLength* \[ fora\]
</dt> <dd>

Um inteiro com sinal de 32 bits que indica o comprimento do intervalo de texto. Este parâmetro é passado não inicializado.

</dd> <dt>

*pNodesToSearch* \[ no\]
</dt> <dd>

A coleção de objetos [**IContextNode**](icontextnode.md) para os quais encontrar o intervalo de texto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Se *pNodesToSearch* contiver objetos [**IContextNode**](icontextnode.md) que não são adjacentes, esse método retornará o menor intervalo de texto que abrange todos os objetos **IContextNode** .

Esse método gera uma \_ exceção E INVALIDARG quando *pNodesToSearch* contém um [**IContextNode**](icontextnode.md) que não está associado ao [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> </dl>

 

 




