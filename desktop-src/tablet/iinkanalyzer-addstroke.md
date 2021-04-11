---
description: Adiciona dados de traço para um único traço para o IInkAnalyzer e atribui o identificador de cultura do thread de entrada ativo ao traço.
ms.assetid: 0e603e5a-d722-4ab8-bc59-605e131c863b
title: 'Método IInkAnalyzer:: addstroke (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc946e7975772eb7be6fff54d01bb1a6dae8ebe7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164545"
---
# <a name="iinkanalyzeraddstroke-method"></a>Método IInkAnalyzer:: addstroke

Adiciona dados de traço para um único traço para o [**IInkAnalyzer**](iinkanalyzer.md) e atribui o identificador de cultura do thread de entrada ativo ao traço.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddStroke(
  [in]  LONG         lStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lStrokeId* \[ no\]
</dt> <dd>

O identificador do traço a ser adicionado.

</dd> <dt>

*ulStrokePacketDataCount* \[ no\]
</dt> <dd>

O número de pacotes no traço.

</dd> <dt>

*plStrokePacketData* \[ no\]
</dt> <dd>

Uma matriz que contém os dados de pacote para o traço.

</dd> <dt>

*ulStrokePacketDescriptionCount* \[ no\]
</dt> <dd>

O número de propriedades do pacote em cada pacote.

</dd> <dt>

*pStrokePacketDescriptionGuids* \[ no\]
</dt> <dd>

Uma matriz que contém os identificadores de Propriedade do pacote.

</dd> <dt>

*ppContextNodeStrokeAddedTo* \[ fora\]
</dt> <dd>

Um ponteiro para o [**IContextNode**](icontextnode.md) para o qual o [**IInkAnalyzer**](iinkanalyzer.md) adicionou o traço.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodeStrokeAddedTo* quando você não precisar mais usar o objeto.

 

Quando *ppContextNodeStrokeAddedTo* é **nulo**, ele indica que o chamador não está interessado no valor de retorno do método.

O [**IInkAnalyzer**](iinkanalyzer.md) adiciona o traço a um [**IContextNode**](icontextnode.md) do tipo UnclassifiedInk (consulte [tipos de nó de contexto](context-node-types.md)). Esse nó está na coleção de subnós do nó raiz (consulte os métodos [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) ).

O [**IInkAnalyzer**](iinkanalyzer.md) atribui o identificador de cultura do thread de entrada ativo ao traço e adiciona o traço ao primeiro nó de contexto UnclassifiedInk no nó raiz do analisador de tinta que contém traços com o mesmo identificador de cultura. Se o analisador de tinta não tiver um nó com o mesmo identificador de cultura, ele criará um novo nó de contexto UnclassifiedInk sob seu nó raiz e adicionará o traço ao novo nó de contexto UnclassifiedInk.

*plStrokePacketData* contém dados de pacote para todos os pontos no traço. *pStrokePacketDescriptionGuids* contém os identificadores globalmente exclusivos (GUIDs) que descrevem os tipos de dados de pacote incluídos para cada ponto no traço. Para obter uma lista completa das propriedades de pacote disponíveis, consulte [constantes PacketPropertyGuids](packetpropertyguids-constants.md).

Esse método expande a região suja para a União do valor atual da região e a caixa delimitadora do traço adicionado.

Se o [**IInkAnalyzer**](iinkanalyzer.md) já contiver um traço com o mesmo identificador de traço, o **IInkAnalyzer** retornará um **HRESULT** de **E \_ INVALIDARG**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**InkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Método IInkAnalyzer:: RemoveStroke**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**Método IInkAnalyzer:: RemoveStrokes**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

