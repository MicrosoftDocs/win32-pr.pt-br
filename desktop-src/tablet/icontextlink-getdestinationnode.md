---
description: Recupera o objeto IContextNode que é o destino para este IContextLink.
ms.assetid: 7e185e69-821b-409b-bc58-d89a4aefeb23
title: 'Método IContextLink:: GetDestinationNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetDestinationNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 86d34bfcca39f7df9d9010e8dae32747ca8f1d27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296394"
---
# <a name="icontextlinkgetdestinationnode-method"></a>Método IContextLink:: GetDestinationNode

Recupera o objeto [**IContextNode**](icontextnode.md) que é o destino para este [**IContextLink**](icontextlink.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDestinationNode(
  [out] IContextNode **ppDstContextNodeId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppDstContextNodeId* \[ fora\]
</dt> <dd>

Um ponteiro para o objeto [**IContextNode**](icontextnode.md) que é o destino para esse [**IContextLink**](icontextlink.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppDstContextNodeId* quando você não precisar mais usar o nó de destino.

 

Se o objeto [**IContextLink**](icontextlink.md) vincular-se entre um nó que contém a gravação e um nó que contém o desenho, o nó de destino será geralmente o nó que contém a gravação.

Se o objeto [**IContextLink**](icontextlink.md) tiver um tipo de link de delimitados (consulte [**IContextLink:: GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), o nó de destino será o objeto [**IContextNode**](icontextnode.md) que está incluído.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

