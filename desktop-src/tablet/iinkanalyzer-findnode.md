---
description: Recupera o objeto IContextNode para um GUID (identificador global exclusivo) especificado.
ms.assetid: b8340666-98ab-4d8c-93c7-58ed05ef30d2
title: Método IInkAnalyzer::FindNode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d3d7e6cd4b24b2cb0977284d62b2bad9e26a8d8944ebc653e22d97d0455d883f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967265"
---
# <a name="iinkanalyzerfindnode-method"></a>Método IInkAnalyzer::FindNode

Recupera o [**objeto IContextNode**](icontextnode.md) para um GUID (identificador global exclusivo) especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FindNode(
  [in]  const GUID         *pId,
  [out]       IContextNode **ppContextNodeFound
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pId* \[ Em\]
</dt> <dd>

O identificador do objeto [**IContextNode.**](icontextnode.md)

</dd> <dt>

*ppContextNodeFound* \[ out\]
</dt> <dd>

Um ponteiro para o [**objeto IContextNode**](icontextnode.md) com o *identificador pId.*

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar uma perda de memória, chame [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodeFound* quando você não precisar mais usar o objeto .

 

Se esse objeto [**IContextNode**](icontextnode.md) não existir como um descendente do nó raiz [**IInkAnalyzer,**](iinkanalyzer.md) **NULL** será retornado.

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

[**Método IInkAnalyzer::FindInkLeafNodes**](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[**Método IInkAnalyzer::FindInkLeafNodesForStrkes**](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[**Método IInkAnalyzer::FindLeafNodes**](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[**Método IInkAnalyzer::FindNodesOfType**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**Método IInkAnalyzer::FindNodesOfTypeForRogkes**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**Método IInkAnalyzer::FindNodesOfTypeInSubTree**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**Método IInkAnalyzer::FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**Método IInkAnalyzer::FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

