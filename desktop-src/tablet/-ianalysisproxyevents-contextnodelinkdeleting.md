---
description: Ocorre antes de IInkAnalyzer excluir um objeto IContextLink entre dois objetos IContextNode.
ms.assetid: bc9716b8-8793-4886-aff4-d880024129a6
title: 'Evento _IAnalysisProxyEvents:: ContextNodeLinkDeleting (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeLinkDeleting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2bf45b8ae900d574bc50151e1bd17f0a124211272d4a83ccb43216ebbf82e2f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452074"
---
# <a name="_ianalysisproxyeventscontextnodelinkdeleting-event"></a>\_Evento IAnalysisProxyEvents:: ContextNodeLinkDeleting

Ocorre antes de [**IInkAnalyzer**](iinkanalyzer.md) excluir um objeto [**IContextLink**](icontextlink.md) entre dois objetos [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ContextNodeLinkDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextLink *pContextLinkToBeDeleted
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInkAnalyzer* \[ no\]
</dt> <dd>

O [**IInkAnalyzer**](iinkanalyzer.md) excluindo o link.

</dd> <dt>

*pContextLinkToBeDeleted* \[ no\]
</dt> <dd>

O objeto [**IContextLink**](icontextlink.md) a ser excluído.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Use esse evento quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md). Esse evento ocorre durante a fase de reconciliação da análise de tinta ou em resposta a um método **IInkAnalyzer** que remove um [**IContextLink**](icontextlink.md) de um [**IContextNode**](icontextnode.md).

Para obter mais informações sobre como sincronizar os dados do aplicativo com o [**IInkAnalyzer**](iinkanalyzer.md), consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**Método IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Método IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




