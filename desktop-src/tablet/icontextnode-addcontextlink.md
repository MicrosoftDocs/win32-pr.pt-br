---
description: Adiciona um novo IContextLink à coleção de links de contexto do objeto IContextNode.
ms.assetid: b7b9da10-3015-4976-bc4e-1a7f69b7c85b
title: 'Método IContextNode:: AddContextLink (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 515ade35baed591060e76818d2b3e00a3654a89a9d42dda21d170ee54b2773ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967435"
---
# <a name="icontextnodeaddcontextlink-method"></a>Método IContextNode:: AddContextLink

Adiciona um novo [**IContextLink**](icontextlink.md) à coleção de links de contexto do objeto [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddContextLink(
  [in]  IContextNode         *pDestinationNode,
  [in]  ContextLinkDirection linkDirection,
  [out] IContextLink         **ppContextLinkToAdd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDestinationNode* \[ no\]
</dt> <dd>

O [**IContextNode**](icontextnode.md) de destino para o novo [**IContextLink**](icontextlink.md).

</dd> <dt>

*linkDirection* \[ no\]
</dt> <dd>

A direção do objeto [**IContextLink**](icontextlink.md) a ser criado.

</dd> <dt>

*ppContextLinkToAdd* \[ fora\]
</dt> <dd>

Um ponteiro para o novo objeto [**IContextLink**](icontextlink.md) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppContextLinkToAdd* quando você não precisar mais usar o nó de contexto.

 

Esse objeto [**IContextNode**](icontextnode.md) é o nó de origem (consulte [**IContextLink:: GetSourceNode**](icontextlink-getsourcenode.md)) para o novo objeto [**IContextLink**](icontextlink.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextLinks**](icontextlinks.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[**IContextNode::D eleteContextLink**](icontextnode-deletecontextlink.md)
</dt> <dt>

[**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

