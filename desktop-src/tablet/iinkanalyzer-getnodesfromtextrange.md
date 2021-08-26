---
description: Recupera uma coleção de objetos IContextNode relevantes para o intervalo de texto especificado para os nós de contexto especificados.
ms.assetid: 39a5dd52-7007-4395-8668-261eca78a090
title: Método IInkAnalyzer::GetNodesFromTextRange (IACom.h)
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
ms.openlocfilehash: df9eb6e1e748088abaa4780aedfded4e26977018d70dd79f518159185594a90b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057816"
---
# <a name="iinkanalyzergetnodesfromtextrange-method"></a>Método IInkAnalyzer::GetNodesFromTextRange

Recupera uma coleção de [**objetos IContextNode**](icontextnode.md) relevantes para o intervalo de texto especificado para os nós de contexto especificados.

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

*plStart* \[ in, out\]
</dt> <dd>

Uma referência ao início do intervalo de texto na parte *pNodesToSearch* da cadeia de caracteres reconhecida.

</dd> <dt>

*plLength* \[ in, out\]
</dt> <dd>

Uma referência ao comprimento do intervalo de texto na parte *pNodesToSearch* da cadeia de caracteres reconhecida.

</dd> <dt>

*ppContextNodes* \[ out\]
</dt> <dd>

Um ponteiro para os [**objetos IContextNode**](icontextnode.md) que são relevantes para o intervalo de texto especificado para os nós de contexto especificados.

</dd> <dt>

*pNodesToSearch* \[ Em\]
</dt> <dd>

Os [**objetos IContextNode**](icontextnode.md) aos quais limitar a pesquisa.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

O intervalo de texto especificado deve ser relativo à parte *pNodesToSearch* da cadeia de caracteres reconhecida do [**IInkAnalyzer,**](iinkanalyzer.md)em vez da cadeia de caracteres reconhecida de **todo o IInkAnalyzer.**

Esse método modifica os valores dos parâmetros *plStart* e *plLength* expandindo o intervalo de texto para os limites de palavra mais próximos.

Por exemplo, se a cadeia de caracteres reconhecida for "Estou atrasado" e você chamar esse método usando os valores de parâmetro de 6 para *plStart* e 1 para *plLength*, que corresponde à letra "a" em "late", esse método retornará uma coleção que contém um único [**IContextNode**](icontextnode.md), o InkWord ou TextWord que corresponde à palavra "late". Para este exemplo, esse método também modifica o valor de *plStart* como 5 e o valor de *plLength* como 4, que corresponde à palavra "late".

> [!Note]  
> O *parâmetro plStart* é relativo à cadeia de caracteres reconhecida do *parâmetro pNodesToSearch.*

 

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

 

 




