---
description: Recupera o tipo do traço especificado.
ms.assetid: bbd0bc23-89f9-4033-bc32-f9bd737c960c
title: 'Método IInkAnalyzer:: getstroketype (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d9358b2583f31fd26310ea880470f36404021fec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164536"
---
# <a name="iinkanalyzergetstroketype-method"></a>Método IInkAnalyzer:: getstroketype

Recupera o tipo do traço especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStrokeType(
  [in]  LONG       lStrokeId,
  [out] StrokeType *pStrokeType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lStrokeId* \[ no\]
</dt> <dd>

O identificador de traço.

</dd> <dt>

*pStrokeType* \[ fora\]
</dt> <dd>

A classificação do traço especificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Se o tipo do traço for o [**valor de StrokeType**](stroketype.md) como não \_ classificado, o [**IInkAnalyzer**](iinkanalyzer.md) classificará o traço durante a análise de tinta. Caso contrário, o **IInkAnalyzer** usará o tipo definido no traço.

O [**IInkAnalyzer**](iinkanalyzer.md) não define o valor do tipo Stroke como parte da análise de tinta. Para especificar ou alterar o tipo de traço, use o método [**IInkAnalyzer:: Setstroketype**](iinkanalyzer-setstroketype.md) ou [**IInkAnalyzer:: setstrokestype**](iinkanalyzer-setstrokestype.md).

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

[**Método IInkAnalyzer:: setstroketype**](iinkanalyzer-setstroketype.md)
</dt> <dt>

[**Método IInkAnalyzer:: setstrokestype**](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




