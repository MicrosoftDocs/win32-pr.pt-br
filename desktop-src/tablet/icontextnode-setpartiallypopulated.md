---
description: Modifica o valor que indica se esse IContextNode é parcial ou totalmente populado.
ms.assetid: 4d8e1ec0-757d-4346-a77e-263bd612972b
title: Método IContextNode::SetPartiallyPopulated (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6df87085a82117a694b48d08c3e6e1f8500c8959060052f553a53f1a285d9707
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713456"
---
# <a name="icontextnodesetpartiallypopulated-method"></a>Método IContextNode::SetPartiallyPopulated

Modifica o valor que indica se esse [**IContextNode**](icontextnode.md) é parcial ou totalmente populado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetPartiallyPopulated(
  [in] VARIANT_BOOL fPartiallyPopulated
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fPartiallyPopulated* \[ Em\]
</dt> <dd>

**VARIANT \_ TRUE** se esse [**IContextNode**](icontextnode.md) for parcialmente populado; caso contrário, **VARIANT \_ FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

Use esse método quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer.**](iinkanalyzer.md) Para obter mais informações, consulte [Proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).

Ao virtualizar sua árvore de documentos, certifique-se de definir o valor PropertyGuidsForContextNodes.RotatedBoundingBox (usando ContextNode.AddPropertyValue) em todos os objetos ContextNode. A propriedade RotatedBoundingBox é calculada pelo InkAnalyzer e, por padrão, deve estar em todos os ContextNodes de escrita. No entanto, se o aplicativo virtualizar os resultados da análise definindo a propriedade PartiallyPopulated, ao manipular o evento PopulateContextNode, preencha a propriedade RotatedBoundingBox. A falha ao definir a propriedade RotatedBoundingBox resultará em potencial mais dados de documento sendo usados na operação de análise atual

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

[**\_IAnalysisProxyEvents::P opulateContextNode**](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[**IContextNode::CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




