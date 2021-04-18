---
description: Ocorre antes de IInkAnalyzer excluir um objeto IContextNode.
ms.assetid: 9c89198e-cc64-4041-b7a3-457f94c4aeaf
title: 'Evento _IAnalysisProxyEvents:: ContextNodeDeleting (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeDeleting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 26488c5657b6d2765534f82b6eacae774adcf561
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105763014"
---
# <a name="_ianalysisproxyeventscontextnodedeleting-event"></a>\_Evento IAnalysisProxyEvents:: ContextNodeDeleting

Ocorre antes de [**IInkAnalyzer**](iinkanalyzer.md) excluir um objeto [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ContextNodeDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToBeDeleted
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInkAnalyzer* \[ no\]
</dt> <dd>

O objeto [**IInkAnalyzer**](iinkanalyzer.md) excluindo o objeto [**IContextNode**](icontextnode.md) .

</dd> <dt>

*pContextNodeToBeDeleted* \[ no\]
</dt> <dd>

O objeto [**IContextNode**](icontextnode.md) a ser excluído.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Use esse evento quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md). Esse evento ocorre durante a fase de reconciliação da análise de tinta ou em resposta a um método do analisador de tinta que exclui um [**IContextNode**](icontextnode.md).

Antes que o [**IInkAnalyzer**](iinkanalyzer.md) exclua um [**IContextNode**](icontextnode.md), o **IInkAnalyzer** remove todos os traços do nó de contexto e remove todos os links para outros nós de contexto. Antes de o nó de contexto ser removido, o **IInkAnalyzer** pode gerar os seguintes eventos.

-   O evento [**\_ IAnalysisProxyEvents:: StrokeReparented**](-ianalysisproxyevents-strokereparented.md) quando move um traço do [**IContextNode**](icontextnode.md).
-   O evento [**\_ IAnalysisProxyEvents:: ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) antes de remover um [**IContextLink**](icontextlink.md) do [**IContextNode**](icontextnode.md).
-   O evento **\_ IAnalysisProxyEvents:: ContextNodeDeleting** antes de remover um nó de contexto pai que não tem mais nós filho.

Para obter mais informações sobre como sincronizar os dados do aplicativo com o [**IInkAnalyzer**](iinkanalyzer.md), consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**Método IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Método IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




