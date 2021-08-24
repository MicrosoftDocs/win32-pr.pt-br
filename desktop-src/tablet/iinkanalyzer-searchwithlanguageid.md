---
description: Método IInkAnalyzer::SearchWithLanguageId – fornece uma pesquisa com base em frase difusa e sem reconhecimento de maiúsculas e minúsculas para a escrita de traços analisados e traços de desenho analisados que têm tipos reconhecidos.
ms.assetid: dfd481f9-38fd-433f-b1fc-697c735c13da
title: Método IInkAnalyzer::SearchWithLanguageId (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SearchWithLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 922cbd2110149ac27041be41ccd24a601e87b5355351e0774a80eb636461c21f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590346"
---
# <a name="iinkanalyzersearchwithlanguageid-method"></a>Método IInkAnalyzer::SearchWithLanguageId

Fornece uma pesquisa com base em frases difusas e sem reconhecimento de maiúsculas e minúsculas para traços de escrita analisados e traços de desenho analisados que têm tipos reconhecidos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SearchWithLanguageId(
  [in]      BSTR  bstrPhraseToMatch,
  [in]      LONG  lSearchStringLanguageId,
  [in, out] ULONG *pulSearchResultCount,
  [out]     ULONG **ppulStrokeCountPerResult,
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     ULONG **ppulStrokeIds
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrPhraseToMatch* \[ Em\]
</dt> <dd>

A frase que será encontrada nas alternativas para os traços analisados no momento.

</dd> <dt>

*lSearchStringLanguageId* \[ Em\]
</dt> <dd>

O LCID associado à cadeia de caracteres passada. Usado para converter o caso internamente para dar suporte a comparações sem maiúsculas e minúsculas.

</dd> <dt>

*pulSearchResultCount* \[ in, out\]
</dt> <dd>

O número máximo de resultados retornados da pesquisa.

</dd> <dt>

*ppulRogkeCountPerResult* \[ out\]
</dt> <dd>

Ponteiro para uma matriz do número de traços em cada resultado da pesquisa.

</dd> <dt>

*pulStrokeIdsCount* \[ in, out\]
</dt> <dd>

O número de IDs de traço em *ppulRogkeIds.*

</dd> <dt>

*ppulRogkeIds* \[ out\]
</dt> <dd>

Ponteiro para uma matriz de IDs de traço que representam um conjunto de conjuntos de traços.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

Essa pesquisa localiza substrings de palavra única e de várias palavras. Os resultados de reconhecimento alternativos e as segmentações alternativas são pesquisados.

Todas as cadeias de caracteres de entrada serão convertidas em uma única caixa para comparação utilizando o LCID do thread atual para fazer essa conversão para respeitar as convenções de caso culturais.

A cadeia de caracteres passada é tratada como uma frase. Palavras e caracteres devem aparecer nas alterantes para os traços na ordem especificada. As primeiras e as últimas palavras da frase podem ser combinadas como substrings (a primeira palavra que aparece no final de uma alternativa e a última palavra que aparece no ataque de uma), mas qualquer outra palavra (aquelas dentro da frase) deve aparecer como palavras inteiras.

Se a cadeia de caracteres passada não tiver espaço em branco entre caracteres, a substring poderá ser encontrada em qualquer lugar dentro de uma única palavra em uma alternativa.

Somente a presença ou a ausência de espaço em branco entre caracteres altera os resultados da pesquisa. O espaço em branco que não está entre caracteres é ignorado. O tipo do espaço em branco é ignorado (uma guia ou um espaço entre caracteres dará o mesmo resultado). A quantidade de espaço em branco não importa– um espaço ou dois espaços entre caracteres darão o mesmo resultado.

A pesquisa não gera eventos PopulateContextNode. Somente os traços que já foram preenchidos serão pesquisados.

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

 

 




