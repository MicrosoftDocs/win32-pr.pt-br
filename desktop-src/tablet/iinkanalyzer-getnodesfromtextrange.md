---
description: Recupera uma coleção de objetos IContextNode que são relevantes para o intervalo de texto especificado para os nós de contexto especificados.
ms.assetid: 39a5dd52-7007-4395-8668-261eca78a090
title: 'Método IInkAnalyzer:: GetNodesFromTextRange (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetNodesFromTextRange
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ada60a64bb4e7d8b4604b18982630dabd7e44256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647227"
---
# <a name="iinkanalyzergetnodesfromtextrange-method"></a>Método IInkAnalyzer:: GetNodesFromTextRange

Recupera uma coleção de objetos [**IContextNode**](icontextnode.md) que são relevantes para o intervalo de texto especificado para os nós de contexto especificados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetNodesFromTextRange(
  [in, out] LONG          *plStart,
  [in, out] LONG          *plLength,
  [out]     IContextNodes **ppContextNodes,
  [in]      IContextNodes *pNodesToSearch = defaultvalue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*plStart* \[ entrada, saída\]
</dt> <dd>

Uma referência ao início do intervalo de texto na parte *pNodesToSearch* da cadeia de caracteres reconhecida.

</dd> <dt>

*plLength* \[ entrada, saída\]
</dt> <dd>

Uma referência ao comprimento do intervalo de texto na parte *pNodesToSearch* da cadeia de caracteres reconhecida.

</dd> <dt>

*ppContextNodes* \[ fora\]
</dt> <dd>

Um ponteiro para os objetos [**IContextNode**](icontextnode.md) que são relevantes para o intervalo de texto especificado para os nós de contexto especificados.

</dd> <dt>

*pNodesToSearch* \[ no\]
</dt> <dd>

Os objetos [**IContextNode**](icontextnode.md) para limitar a pesquisa.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

O intervalo de texto especificado deve ser relativo à parte *pNodesToSearch* da cadeia de caracteres reconhecida do [**IInkAnalyzer**](iinkanalyzer.md), e não à cadeia de caracteres reconhecida do **IInkAnalyzer** inteiro.

Esse método modifica os valores dos parâmetros *plStart* e *plLength* expandindo o intervalo de texto para os limites de palavras mais próximos.

Por exemplo, se a cadeia de caracteres reconhecida for "Estou atrasado" e você chamar esse método usando os valores de parâmetro de 6 para *plStart* e 1 para *plLength*, que corresponde à letra "a" em "tardia", esse método retornará uma coleção que contém um único [**IContextNode**](icontextnode.md), o InkWord ou o textword que corresponde à palavra "tardia". Para este exemplo, esse método também modifica o valor de *plStart* para 5 e o valor de *plLength* para 4, que corresponde à palavra "tardia".

> [!Note]  
> O parâmetro *plStart* é relativo à cadeia de caracteres reconhecida do parâmetro *pNodesToSearch* .

 

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

 

 




