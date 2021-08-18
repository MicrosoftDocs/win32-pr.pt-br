---
description: Adiciona dados de traço para vários traços ao IInkAnalyzer e atribui o identificador de cultura especificado aos traços.
ms.assetid: 1274b24f-204b-4a84-a7c0-0205b6068ae8
title: Método IInkAnalyzer::AddRogkesForLanguage (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokesForLanguage
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 52e2dc742dc91b37bce29d477cf91f7178f2ae2a62ce3a329d2b9bf79c46b33a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719604"
---
# <a name="iinkanalyzeraddstrokesforlanguage-method"></a>Método IInkAnalyzer::AddRogkesForLanguage

Adiciona dados de traço para vários traços ao [**IInkAnalyzer**](iinkanalyzer.md) e atribui o identificador de cultura especificado aos traços.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddStrokesForLanguage(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plIdofStrokesToAdd,
  [in]  LONG         lStrokesLCID,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ulStrokeIdsCount* \[ Em\]
</dt> <dd>

O número de traços a adicionar.

</dd> <dt>

*plIdofStrkesToAdd* \[ Em\]
</dt> <dd>

Uma matriz que contém os identificadores de traço.

</dd> <dt>

*lRogkesLCID* \[ Em\]
</dt> <dd>

Um valor que representa o identificador de cultura a ser atribuído aos traços.

</dd> <dt>

*ulRogkePacketDescriptionCount* \[ Em\]
</dt> <dd>

O número de propriedades em cada pacote.

</dd> <dt>

*pRogkePacketDescriptionGuids* \[ Em\]
</dt> <dd>

Uma matriz que contém os identificadores de propriedade do pacote.

</dd> <dt>

*pulPacketDataCountPerStrke* \[ Em\]
</dt> <dd>

Uma matriz que contém o número de pacotes em cada traço.

</dd> <dt>

*plRogkePacketData* \[ Em\]
</dt> <dd>

Uma matriz que contém os dados do pacote para os traços.

</dd> <dt>

*ppContextNodeStrkeAddedTo* \[ out\]
</dt> <dd>

O [**IContextNode ao**](icontextnode.md) qual o analisador de tinta adicionou os traços.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar uma perda de memória, chame [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodeStrkeAddedTo* quando você não precisar mais usar o objeto .

 

Quando *ppContextNodeStrkeAddedTo* é **NULL**, indica que o chamador não está interessado no valor de retorno do método .

O [**IInkAnalyzer**](iinkanalyzer.md) adiciona os traços a [**um IContextNode**](icontextnode.md) do tipo UnclassifiedInk (consulte [Tipos de nó de contexto).](context-node-types.md) Esse nó está na coleção de subnodos do nó raiz (consulte Métodos [**IInkAnalyzer::GetRootNode**](iinkanalyzer-getrootnode.md) e [**IContextNode::GetSubNodes).**](icontextnode-getsubnodes.md)

O [**IInkAnalyzer**](iinkanalyzer.md) atribui o identificador de cultura *lStrkeLCID* aos traços e adiciona os traços ao primeiro nó de contexto UnclassifiedInk no nó raiz do analisador de tinta que contém traços com o mesmo identificador de cultura. Se o analisador de tinta não tiver um nó com o mesmo identificador de cultura, ele criará um novo nó de contexto UnclassifiedInk em seu nó raiz e adiciona os traços ao novo nó de contexto UnclassifiedInk.

*plRogkePacketData* contém dados de pacote para todos os traços. *pRogkePacketDescriptionGuids* contém os GUIDs (identificadores globalmente exclusivos) que descrevem os tipos de dados de pacote incluídos para cada ponto em cada traço. Para ver uma lista completa das propriedades de pacote disponíveis, consulte [Constantes PacketPropertyGuids](packetpropertyguids-constants.md).

> [!Note]  
> Somente traços com as mesmas descrições de pacote podem ser adicionados em uma única chamada ao [**Método IInkAnalyzer::AddStrkes**](iinkanalyzer-addstrokes.md).

 

Esse método expande a região suja para a união do valor atual da região e a caixa delimitativa dos traços adicionados.

Se [**o IInkAnalyzer**](iinkanalyzer.md) já contiver um traço com o mesmo identificador que um dos traços a serem adicionados, **o IInkAnalyzer** retornará um **HRESULT** **de E \_ INVALIDARG.**

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
</dt> <dt>

[**Método IInkAnalyzer::AddStrke**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Método IInkAnalyzer::AddRogkeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Método IInkAnalyzer::AddStrkes**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Método IInkAnalyzer::RemoveStrke**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**Método IInkAnalyzer::RemoveStrkes**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

