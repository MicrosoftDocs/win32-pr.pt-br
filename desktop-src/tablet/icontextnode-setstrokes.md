---
description: Associa os traços especificados a este IContextNode.
ms.assetid: 5ce8893a-da59-4cec-a349-d5ffc4f43905
title: Método IContextNode::SetRogkes (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 67834a10e5e08070c991af76fe19b720853789a9f5e2c771f5c1ed0dc4fc9754
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119552596"
---
# <a name="icontextnodesetstrokes-method"></a>Método IContextNode::SetStrkes

Associa os traços especificados a este [**IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetStrokes(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ulStrokeIdsCount* \[ Em\]
</dt> <dd>

O número de identificadores de traço *em plRogkeIds.*

</dd> <dt>

*plRogkeIds* \[ Em\]
</dt> <dd>

Os identificadores dos traços a associar a este [**IContextNode.**](icontextnode.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

Esse método não atualiza a região suja do analisador de tinta (consulte [**Método IInkAnalyzer::GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Use esse método quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer.**](iinkanalyzer.md) Use esse método para atribuir dados de traço a um nó de contexto específico. Para obter mais informações sobre como sincronizar os dados do aplicativo **com o IInkAnalyzer,** consulte Proxy de dados [com análise de tinta.](data-proxy-with-ink-analysis.md)

Se qualquer um dos traços especificados já estiver associado ao [**IInkAnalyzer**](iinkanalyzer.md), esse método retornará **E \_ INVALIDARG.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**Método IInkAnalyzer::AddStrke**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Método IInkAnalyzer::AddRogkeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Método IInkAnalyzer::AddStrkes**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Método IInkAnalyzer::AddRogkesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Método IInkAnalyzer::AddRogkesToCustomRecognizer**](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[**Método IInkAnalyzer::AddRogkeToCustomRecognizer**](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[**Método IInkAnalyzer::RemoveStrke**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**Método IInkAnalyzer::RemoveStrkes**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**IContextNode::GetRogkeId**](icontextnode-getstrokeid.md)
</dt> <dt>

[**IContextNode::GetRogkeIds**](icontextnode-getstrokeids.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




