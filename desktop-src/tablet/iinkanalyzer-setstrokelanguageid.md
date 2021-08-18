---
description: Altera o identificador de localidade para o traço especificado.
ms.assetid: 3714462d-0391-481f-968a-3c121b7dd538
title: Método IInkAnalyzer::SetMissionkeLanguageId (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc91d7d8a710d2640c31e639146bd6a2fd1deac854420d7ceac1bbfdd778022c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091476"
---
# <a name="iinkanalyzersetstrokelanguageid-method"></a>Método IInkAnalyzer::SetRogkeLanguageId

Altera o identificador de localidade para o traço especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetStrokeLanguageId(
  [in] LONG lStrokeId,
  [in] LONG lStrokeLCID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lStrkeId* \[ Em\]
</dt> <dd>

O identificador do traço ao qual atribuir o identificador de localidade.

</dd> <dt>

*lRogkeLCID* \[ Em\]
</dt> <dd>

O identificador de localidade a ser atribuído ao traço.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

A localidade de um traço é definida quando você adiciona o traço chamando o método [**IInkAnalyzer::AddStrke**](iinkanalyzer-addstroke.md), [**Método IInkAnalyzer::AddRogkeForLanguage**](iinkanalyzer-addstrokeforlanguage.md), [**Método IInkAnalyzer::AddEntrokes**](iinkanalyzer-addstrokes.md)ou Método [**IInkAnalyzer::Add IssokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md). Para obter a localidade atualmente atribuída a um traço, chame o método [**IInkAnalyzer::GetRogkeLanguageId**](iinkanalyzer-getstrokelanguageid.md).

O traço especificado é movido para um nó de tinta não classificado (consulte [**IContextNode::GetType**](icontextnode-gettype.md)) que contém traços da mesma linguagem. Se não existir [**nenhum IContextNode,**](icontextnode.md) esse método criará um novo nó de tinta não classificado e moverá o traço para ele. Um nó de tinta não classificado é **um IContextNode** que tem um tipo unclassifiedInk.

Se esse método mover um traço de [**um IContextNode**](icontextnode.md) que não é um nó de tinta não classificado, esse método também adiciona a caixa delimitador do traço à região suja do analisador de tinta (consulte [**Método IInkAnalyzer::GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Esse método não move um traço se o *parâmetro lStrkeLCID* corresponde ao identificador de idioma atual do traço.

Se o traço especificado não estiver associado ao [**IInkAnalyzer,**](iinkanalyzer.md)esse método retornará sem atualizar **o IInkAnalyzer.**

Para obter mais informações sobre identificadores de idioma, consulte Constantes e cadeias de caracteres do [identificador de idioma.](/windows/desktop/Intl/language-identifier-constants-and-strings)

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

[**Método IInkAnalyzer::GetEntrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[**Método IInkAnalyzer::SetRogkesLanguageId**](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

