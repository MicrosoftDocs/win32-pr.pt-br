---
description: Cria um novo objeto IContextNode filho.
ms.assetid: 35d2b641-fada-418b-9374-0303c7d318e5
title: Método IContextNode::CreateSubNode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreateSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c7b4bc39431d6b4608586e60bdeffb7cd6c79bf95f944e436c16a683e24e634d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092307"
---
# <a name="icontextnodecreatesubnode-method"></a>Método IContextNode::CreateSubNode

Cria um novo objeto [**IContextNode**](icontextnode.md) filho.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateSubNode(
  [in]  const GUID         *pNodeType,
  [out]       IContextNode **ppContextNodeCreated
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pNodeType* \[ Em\]
</dt> <dd>

Um **GUID** que representa o tipo [**de IContextNode a**](icontextnode.md) ser criado.

</dd> <dt>

*ppContextNodeCreated* \[ out\]
</dt> <dd>

Um ponteiro para o [**novo IContextNode.**](icontextnode.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar uma perda de memória, chame [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppContextNodeCreated* quando você não precisar mais usar o nó de contexto.

 

O novo [**IContextNode**](icontextnode.md) é adicionado à coleção de nós filho desse nó de contexto (consulte [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)). Quando há nós filho existentes, o **IContextNode** recém-criado é adicionado como o último nó filho.

Para ver uma lista de tipos de nó de contexto, consulte [Tipos de nó de contexto.](context-node-types.md)

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

[**IContextNode::D eleteSubNode**](icontextnode-deletesubnode.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

