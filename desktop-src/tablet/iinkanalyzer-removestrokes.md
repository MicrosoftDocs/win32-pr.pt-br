---
description: Remove os traços especificados do IInkAnalyzer.
ms.assetid: ea7c8a9f-a427-4781-b5ba-97ffd983dbe5
title: Método IInkAnalyzer::RemoveStrkes (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e6d53d21df9734ee43cdda618c5221fd83300598d46b51bd366c50fedf5cec45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092016"
---
# <a name="iinkanalyzerremovestrokes-method"></a>Método IInkAnalyzer::RemoveStrkes

Remove os traços especificados do [**IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RemoveStrokes(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ulRogkeIdCount* \[ Em\]
</dt> <dd>

O número de identificadores de traço *em plStrkes.*

</dd> <dt>

*plRogkes* \[ Em\]
</dt> <dd>

Os identificadores para os traços a remover.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

Esse método remove os dados de pacote para e faz referência aos traços especificados do [**IInkAnalyzer.**](iinkanalyzer.md)

Esse método remove os traços do nó de contexto folha que faz referência aos traços. Se qualquer [**IContextNode**](icontextnode.md) não referenciar mais nenhum traço, esse método excluirá **o IContextNode** e quaisquer objetos **IContextNode** ancestrais que não tenham mais nenhum nós filho.

Depois que esse método remove os traços do [**IContextNode**](icontextnode.md), ele atualiza a região suja do objeto [**IInkAnalyzer**](iinkanalyzer.md) (consulte [**Método IInkAnalyzer::GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) para incluir a caixa delimitador dos traços removidos.

Se um traço identificado *em plStrkes* não estiver associado ao [**IInkAnalyzer,**](iinkanalyzer.md)esse método ignorará o identificador.

Se nenhum dos traços identificados em *plStrkes* estiver associado ao analisador de tinta, esse método retornará sem atualizar [**o IInkAnalyzer.**](iinkanalyzer.md)

Esse método retorna e o código de erro *quando plRogkes* é nulo.

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

[**Método IInkAnalyzer::AddRogkesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Método IInkAnalyzer::RemoveStrke**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**Método IInkAnalyzer::GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




