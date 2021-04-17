---
description: Adiciona dados de traço para vários traços ao IInkAnalyzer e atribui o identificador de cultura do thread de entrada ativo aos traços.
ms.assetid: 4a8d6828-699b-465d-b057-197866ff069f
title: 'Método IInkAnalyzer:: AddStrokes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc616f8a388010df2b3d39ea55622d81fa5ce3a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811529"
---
# <a name="iinkanalyzeraddstrokes-method"></a>Método IInkAnalyzer:: AddStrokes

Adiciona dados de traço para vários traços ao [**IInkAnalyzer**](iinkanalyzer.md) e atribui o identificador de cultura do thread de entrada ativo aos traços.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddStrokes(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plStrokeIds,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ulStrokeIdsCount* \[ no\]
</dt> <dd>

O número de traços a serem adicionados.

</dd> <dt>

*plStrokeIds* \[ no\]
</dt> <dd>

Uma matriz que contém os identificadores de traço.

</dd> <dt>

*ulStrokePacketDescriptionCount* \[ no\]
</dt> <dd>

O número de propriedades em cada pacote.

</dd> <dt>

*pStrokePacketDescriptionGuids* \[ no\]
</dt> <dd>

Uma matriz que contém os identificadores de Propriedade do pacote.

</dd> <dt>

*pulPacketDataCountPerStroke* \[ no\]
</dt> <dd>

Uma matriz que contém o número de pacotes em cada traço.

</dd> <dt>

*plStrokePacketData* \[ no\]
</dt> <dd>

Uma matriz que contém os dados de pacote para os traços.

</dd> <dt>

*ppContextNodeStrokeAddedTo* \[ fora\]
</dt> <dd>

O [**IContextNode**](icontextnode.md) para o qual o analisador de tinta adicionou os traços.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodeStrokeAddedTo* quando você não precisar mais usar o objeto.

 

Quando *ppContextNodeStrokeAddedTo* é **nulo**, ele indica que o chamador não está interessado no valor de retorno do método.

O [**IInkAnalyzer**](iinkanalyzer.md) adiciona os traços a um [**IContextNode**](icontextnode.md) do tipo UnclassifiedInk (consulte [tipos de nó de contexto](context-node-types.md)). Esse nó está na coleção de subnós do nó raiz (consulte os métodos [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) ).

O [**IInkAnalyzer**](iinkanalyzer.md) atribui o identificador de cultura do thread de entrada ativo aos traços e adiciona os traços ao primeiro nó de contexto UnclassifiedInk no nó raiz do analisador de tinta que contém traços com o mesmo identificador de cultura. Se o analisador de tinta não tiver um nó com o mesmo identificador de cultura, ele criará um novo nó de contexto UnclassifiedInk sob seu nó raiz e adicionará os traços ao novo nó de contexto UnclassifiedInk.

*plStrokePacketData* contém dados de pacote para todos os traços. *pStrokePacketDescriptionGuids* contém os identificadores globalmente exclusivos (GUIDs) que descrevem os tipos de dados de pacote incluídos para cada ponto em cada traço. Para obter uma lista completa das propriedades de pacote disponíveis, consulte [constantes PacketPropertyGuids](packetpropertyguids-constants.md).

> [!Note]  
> Somente traços com as mesmas descrições de pacote podem ser adicionados em uma única chamada para o **método IInkAnalyzer:: AddStrokes**.

 

Esse método expande a região suja para a União do valor atual da região e a caixa delimitadora dos traços adicionados.

Se o [**IInkAnalyzer**](iinkanalyzer.md) já contiver um traço com o mesmo identificador de um dos traços a serem adicionados, o **IInkAnalyzer** retornará um **HRESULT** de **E \_ INVALIDARG**.

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
</dt> <dt>

[**Método IInkAnalyzer:: addstroke**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Método IInkAnalyzer:: RemoveStroke**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**Método IInkAnalyzer:: RemoveStrokes**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

