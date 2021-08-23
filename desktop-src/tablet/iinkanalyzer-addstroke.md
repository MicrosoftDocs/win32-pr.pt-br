---
description: Adiciona dados de traço para um único traço ao IInkAnalyzer e atribui o identificador de cultura do thread de entrada ativo ao traço.
ms.assetid: 0e603e5a-d722-4ab8-bc59-605e131c863b
title: Método IInkAnalyzer::AddStrke (IACom.h)
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
ms.openlocfilehash: f7ba08e779e115c243918d94e5b41e8a7d77f54fab92b045274135ead2ae0264
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590586"
---
# <a name="iinkanalyzeraddstroke-method"></a>Método IInkAnalyzer::AddStrke

Adiciona dados de traço para um único traço ao [**IInkAnalyzer**](iinkanalyzer.md) e atribui o identificador de cultura do thread de entrada ativo ao traço.

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

*lStrkeId* \[ Em\]
</dt> <dd>

O identificador do traço a ser acrescentado.

</dd> <dt>

*ulRogkePacketDataCount* \[ Em\]
</dt> <dd>

O número de pacotes no traço.

</dd> <dt>

*plRogkePacketData* \[ Em\]
</dt> <dd>

Uma matriz que contém os dados de pacote para o traço.

</dd> <dt>

*ulRogkePacketDescriptionCount* \[ Em\]
</dt> <dd>

O número de propriedades de pacote em cada pacote.

</dd> <dt>

*pRogkePacketDescriptionGuids* \[ Em\]
</dt> <dd>

Uma matriz que contém os identificadores de propriedade do pacote.

</dd> <dt>

*ppContextNodeStrkeAddedTo* \[ out\]
</dt> <dd>

Um ponteiro para [**o IContextNode**](icontextnode.md) ao qual [**o IInkAnalyzer adicionou**](iinkanalyzer.md) o traço.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar uma perda de memória, chame [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodeStrkeAddedTo* quando você não precisar mais usar o objeto .

 

Quando *ppContextNodeStrkeAddedTo* é **NULL**, indica que o chamador não está interessado no valor de retorno do método .

O [**IInkAnalyzer**](iinkanalyzer.md) adiciona o traço a [**um IContextNode**](icontextnode.md) do tipo UnclassifiedInk (consulte [Tipos de nó de contexto](context-node-types.md)). Esse nó está na coleção de subnodos do nó raiz (consulte Métodos [**IInkAnalyzer::GetRootNode**](iinkanalyzer-getrootnode.md) e [**IContextNode::GetSubNodes).**](icontextnode-getsubnodes.md)

O [**IInkAnalyzer**](iinkanalyzer.md) atribui o identificador de cultura do thread de entrada ativo ao traço e adiciona o traço ao primeiro nó de contexto UnclassifiedInk sob o nó raiz do analisador de tinta que contém traços com o mesmo identificador de cultura. Se o analisador de tinta não tiver um nó com o mesmo identificador de cultura, ele criará um novo nó de contexto UnclassifiedInk em seu nó raiz e adiciona o traço ao novo nó de contexto UnclassifiedInk.

*plRogkePacketData* contém dados de pacote para todos os pontos no traço. *pRogkePacketDescriptionGuids* contém os GUIDs (identificadores globalmente exclusivos) que descrevem os tipos de dados de pacote incluídos para cada ponto no traço. Para ver uma lista completa das propriedades de pacote disponíveis, consulte [Constantes PacketPropertyGuids](packetpropertyguids-constants.md).

Esse método expande a região suja para a união do valor atual da região e a caixa delimitativa do traço adicionado.

Se [**o IInkAnalyzer**](iinkanalyzer.md) já contiver um traço com o mesmo identificador de traço, **o IInkAnalyzer** retornará um **HRESULT** **de E \_ INVALIDARG.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Inkanalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Método IInkAnalyzer::AddRogkeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Método IInkAnalyzer::AddStrkes**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Método IInkAnalyzer::AddRogkesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Método IInkAnalyzer::RemoveStrke**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**Método IInkAnalyzer::RemoveStrkes**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

