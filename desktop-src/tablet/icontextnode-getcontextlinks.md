---
description: Recupera uma coleção de objetos IContextLink que representa relações com outros objetos IContextNode.
ms.assetid: 0fe56e6d-c779-4916-9c80-6f18cf6f1b09
title: Método IContextNode::GetContextLinks (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2c3b63e50cf43f06f6065a61dacfbbbd8a00fe7959bb5133407a6c2a980a1a20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057828"
---
# <a name="icontextnodegetcontextlinks-method"></a>Método IContextNode::GetContextLinks

Recupera uma coleção de [**objetos IContextLink**](icontextlink.md) que representa relações com outros [**objetos IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetContextLinks(
  [out] IContextLinks **ppContextLinks
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppContextLinks* \[ out\]
</dt> <dd>

Um ponteiro para uma coleção de [**objetos IContextLink**](icontextlink.md) que representa relações com outros [**objetos IContextNode.**](icontextnode.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar uma perda de memória, chame [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppContextLinks* quando você não precisar mais usar a coleção de links de contexto.

 

Para obter informações sobre relações de nó pai ou filho, use [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) ou [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md).

Para obter mais informações sobre os tipos de relações descritos por links, consulte [**IContextLink**](icontextlink.md) e [**ContextLinkDirection**](contextlinkdirection.md).

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

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[**IContextNode::AddContextLink**](icontextnode-addcontextlink.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

