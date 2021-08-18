---
description: 'Método IInkAnalyzer:: Search – fornece uma pesquisa com base em frases difusas e sem diferenciação de maiúsculas e minúsculas para os traços de escrita analisados e os traços de desenho analisados que têm tipos reconhecidos.'
ms.assetid: 5b5ce4b5-45ef-42ef-866b-2f38c32d8c86
title: 'Método IInkAnalyzer:: Search (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Search
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a5ebbec010d84f510d9bd2786b20fee1deaa34039720d842df77cbe0f1ca9825
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091486"
---
# <a name="iinkanalyzersearch-method"></a>Método IInkAnalyzer:: Search

Fornece uma pesquisa difusa, sem diferenciação de maiúsculas e minúsculas, para os traços de escrita analisado e os traços de desenho analisados que têm tipos reconhecidos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Search(
  [in]      BSTR  bstrPhraseToMatch,
  [in, out] ULONG *pulSearchResultCount,
  [out]     ULONG **ppulStrokeCountPerResult,
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     ULONG **ppulStrokeIds
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrPhraseToMatch* \[ no\]
</dt> <dd>

A frase que será encontrada nas alternativas para os traços analisados no momento.

</dd> <dt>

*pulSearchResultCount* \[ entrada, saída\]
</dt> <dd>

O número máximo de resultados retornados da pesquisa.

</dd> <dt>

*ppulStrokeCountPerResult* \[ fora\]
</dt> <dd>

Ponteiro para uma matriz do número de traços em cada resultado da pesquisa.

</dd> <dt>

*pulStrokeIdsCount* \[ entrada, saída\]
</dt> <dd>

O número de IDs de traço em *ppulStrokeIds*.

</dd> <dt>

*ppulStrokeIds* \[ fora\]
</dt> <dd>

Ponteiro para uma matriz de IDs de traço que representa um conjunto de conjuntos de traços.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Esta pesquisa localiza subcadeias de caracteres de várias palavras e de palavras únicas. Os resultados de reconhecimento alternativos e as segmentações alternativas são pesquisados.

Todas as cadeias de caracteres de entrada serão convertidas em uma única caixa para comparação, utilizando o LCID do thread atual para fazer essa conversão para respeitar as convenções de casos culturais.

A cadeia de caracteres passada é tratada como uma frase. Palavras e caracteres devem aparecer no alterantes para os traços na ordem especificada. A primeira e última palavras da frase podem ser correspondidas como subcadeias de caracteres (a primeira palavra que aparece no final de uma alternativa e a última palavra que aparece no begginging de uma), mas quaisquer outras palavras (aquelas dentro da frase) devem aparecer como palavras inteiras.

Se a cadeia de caracteres passada não tiver espaço em branco entre os caracteres, a subcadeia de caracteres poderá ser encontrada em qualquer lugar dentro de uma única palavra em uma alternativa.

Somente a presença ou a ausência de espaço em branco entre caracteres altera os resultados da pesquisa. O espaço em branco que não está entre caracteres é ignorado. O tipo de espaço em branco é ignorado (uma guia ou um espaço entre os caracteres fornecerá o mesmo resultado). A quantidade de espaço em branco não importa, um espaço ou dois espaços entre caracteres fornecerá o mesmo resultado.

A pesquisa não gera eventos PopulateContextNode. Somente os traços que já foram preenchidos serão pesquisados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> </dl>

 

 




