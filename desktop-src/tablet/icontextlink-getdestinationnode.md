---
description: Recupera o objeto IContextNode que é o destino deste IContextLink.
ms.assetid: 7e185e69-821b-409b-bc58-d89a4aefeb23
title: Método IContextLink::GetDestinationNode (IACom.h)
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
ms.openlocfilehash: 1a11d9021d4299a1823fee57ed9a80237b4896459b0396a8ba4b140bd377bb80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967446"
---
# <a name="icontextlinkgetdestinationnode-method"></a>Método IContextLink::GetDestinationNode

Recupera o [**objeto IContextNode**](icontextnode.md) que é o destino deste [**IContextLink.**](icontextlink.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDestinationNode(
  [out] IContextNode **ppDstContextNodeId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppDstContextNodeId* \[ out\]
</dt> <dd>

Um ponteiro para o [**objeto IContextNode**](icontextnode.md) que é o destino deste [**IContextLink.**](icontextlink.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar uma perda de memória, chame [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppDstContextNodeId* quando você não precisar mais usar o nó de destino.

 

Se o [**objeto IContextLink**](icontextlink.md) estiver links entre um nó que contém a escrita e um nó que contém desenho, o nó de destino geralmente será o nó que contém a escrita.

Se o objeto [**IContextLink**](icontextlink.md) tiver um tipo de link de Encloses (consulte [**IContextLink::GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), o nó de destino será [**o objeto IContextNode**](icontextnode.md) incluído.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
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

 

