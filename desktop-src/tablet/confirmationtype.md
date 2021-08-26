---
description: Especifica o tipo de confirmação que pode ocorrer em um objeto IContextNode.
ms.assetid: 5c906548-dbf5-4448-b248-070bd43b054e
title: Enumeração confirmtype (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfirmationType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 9f89d5457e3d75bcf781a100449e4da9f8b45624af38760ca0cdda358fbf47ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936946"
---
# <a name="confirmationtype-enumeration"></a>Enumeração confirmtype

Especifica o tipo de confirmação que pode ocorrer em um objeto [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Syntax


```C++
typedef enum ConfirmationType { 
  ConfirmationType_None                   = 0,
  ConfirmationType_NodeTypeAndProperties  = 1,
  ConfirmationType_TopBoundary            = 4
} ConfirmationType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="ConfirmationType_None"></span><span id="confirmationtype_none"></span><span id="CONFIRMATIONTYPE_NONE"></span>**Confirmation \_ nenhum**
</dt> <dd>

Nenhuma confirmação é aplicada. O [**IInkAnalyzer**](iinkanalyzer.md) é livre para alterar um nó de contexto ou qualquer um de seus descendentes, conforme necessário.

</dd> <dt>

<span id="ConfirmationType_NodeTypeAndProperties"></span><span id="confirmationtype_nodetypeandproperties"></span><span id="CONFIRMATIONTYPE_NODETYPEANDPROPERTIES"></span>**NodeTypeAndProperties de confirmações \_**
</dt> <dd>

O [**IInkAnalyzer**](iinkanalyzer.md) não pode alterar o tipo ou qualquer Propriedade do nó de contexto especificado.

</dd> <dt>

<span id="ConfirmationType_TopBoundary"></span><span id="confirmationtype_topboundary"></span><span id="CONFIRMATIONTYPE_TOPBOUNDARY"></span>**TopBoundary de confirmações \_**
</dt> <dd>

O [**IInkAnalyzer**](iinkanalyzer.md) não executará operações, incluindo a adição de tinta ou a mesclagem com outras [**ContextNodes**](icontextnodes.md), que fazem com que o TopBoundary se mova para além do limite superior atual. Por exemplo:

-   Um aplicativo analisa um conjunto de tinta e um ParagraphNode é identificado.
-   O aplicativo confirma a TopBoundary deste parágrafo.
-   O usuário do aplicativo grava a nova tinta acima do parágrafo atual. Quando Analyze for chamado novamente, a nova tinta não será incorporada ao nó de parágrafo confirmado.
-   Como apenas o limite superior é confirmado, o ContextNode pode continuar crescendo em outras direções. A exclusão de traços pode fazer com que o limite superior se mova para baixo. A tradução do ContextNode pode fazer com que o local seja alterado, mas não permitirá que a tinta adicional seja mesclada no novo local.

Este confirmtype é aplicável somente a nós de parágrafo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode usar o valor **NodeTypeAndProperties** somente para os nós de desenho de tinta e palavra de tinta (consulte [**IContextNode:: GetType**](icontextnode-gettype.md)). Caso contrário, um **E \_ INVALIDARG** será retornado de [**IContextNode:: Confirm**](icontextnode-confirm.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextNode:: confirmar**](icontextnode-confirm.md)
</dt> <dt>

[**IContextNode:: IsDeleted**](icontextnode-isconfirmed.md)
</dt> </dl>

 

 




