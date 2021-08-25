---
description: Recupera o objeto IContextNode que é a origem para este IContextLink.
ms.assetid: 2f55ae9c-9f63-4d49-9bf0-9e169b819e79
title: 'Método IContextLink:: GetSourceNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetSourceNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 609f3012608586f7e6c3279cd0dab4232f58ca3e0e31145124622e87684e06f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940406"
---
# <a name="icontextlinkgetsourcenode-method"></a>Método IContextLink:: GetSourceNode

Recupera o objeto [**IContextNode**](icontextnode.md) que é a origem para este [**IContextLink**](icontextlink.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSourceNode(
  [out] IContextNode **ppSrcContextNodeId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppSrcContextNodeId* \[ fora\]
</dt> <dd>

Um ponteiro para o objeto [**IContextNode**](icontextnode.md) que é a origem para esse [**IContextLink**](icontextlink.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppSrcContextNodeId* quando você não precisar mais usar o nó de origem.

 

Se o objeto [**IContextLink**](icontextlink.md) vincular-se entre um nó que contém a gravação e um nó que contém o desenho, o nó de origem será geralmente o nó que contém o desenho.

Se o objeto [**IContextLink**](icontextlink.md) tiver um tipo de link de incloses (consulte [**IContextLink:: GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), o nó de origem será o nó que inclui o nó de destino.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextLink::GetDestinationNode**](icontextlink-getdestinationnode.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

