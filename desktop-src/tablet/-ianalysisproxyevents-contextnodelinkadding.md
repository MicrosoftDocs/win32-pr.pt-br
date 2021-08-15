---
description: Ocorre antes que o analisador de tinta adiciona um objeto IContextLink entre dois objetos IContextNode.
ms.assetid: ec56cb8e-5154-45ee-911d-e2a240d19dc3
title: _IAnalysisProxyEvents::Evento ContextNodeLinkAdding (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeLinkAdding
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1d100d4ecb4caa6fb7230afd3d4ae6572466ae86855ac9bd28155b6b181cdd5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452151"
---
# <a name="_ianalysisproxyeventscontextnodelinkadding-event"></a>\_Evento IAnalysisProxyEvents::ContextNodeLinkAdding

Ocorre antes que o analisador de tinta adiciona um [**objeto IContextLink**](icontextlink.md) entre dois [**objetos IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ContextNodeLinkAdding(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextLink *pContextLinkToBeAdded
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInkAnalyzer* \[ Em\]
</dt> <dd>

O [**IInkAnalyzer adicionando**](iinkanalyzer.md) o link.

</dd> <dt>

*pContextLinkToBeAdded* \[ Em\]
</dt> <dd>

O [**objeto IContextLink**](icontextlink.md) a ser adicionado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

Use esse evento quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer.**](iinkanalyzer.md) Esse evento ocorre durante a fase de reconciliação da análise de tinta ou em resposta a um método de analisador de tinta que adiciona um novo [**IContextLink**](icontextlink.md) a [**um IContextNode.**](icontextnode.md)

Para obter mais informações sobre como sincronizar os dados do aplicativo [**com o IInkAnalyzer,**](iinkanalyzer.md)consulte Proxy de dados [com análise de tinta.](data-proxy-with-ink-analysis.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**Método IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Método IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




