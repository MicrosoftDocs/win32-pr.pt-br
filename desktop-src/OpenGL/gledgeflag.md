---
title: função glEdgeFlag (GL. h)
description: Sinaliza bordas como limite ou não associado. | função glEdgeFlag (GL. h)
ms.assetid: cebaa4af-a3bc-4396-9ee0-8cc10bcaf256
keywords:
- função glEdgeFlag OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlag
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 599a0b539e32d0e457f92c256e2cb0b678b05b59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105770465"
---
# <a name="gledgeflag-function"></a>função glEdgeFlag

Sinaliza bordas como limite ou não associado.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glEdgeFlag(
   GLboolean flag
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*flag* 
</dt> <dd>

Especifica o valor do sinalizador de borda atual, **true** ou **false**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Cada vértice de um polígono, um triângulo separado ou um diamante separado especificado entre um par [**glBegin**](/windows/desktop/OpenGL/glbegin) / [**glEnd**](/windows/desktop/OpenGL/glend) é marcado como o início de um limite ou de uma borda não-bound. Se o sinalizador de borda atual for **true** quando o vértice for especificado, o vértice será marcado como o início de uma borda de limite. Se o sinalizador de borda atual for **false**, o vértice será marcado como o início de uma borda não bound. A função **glEdgeFlag** define o sinalizador de borda como **true** se o sinalizador for diferente de zero; caso contrário, **retornará false** .

Os vértices dos triângulos conectados e quadrilaterals conectados sempre são marcados como limite, independentemente do valor do sinalizador de borda.

Os sinalizadores de borda e limites não restritos nos vértices são significativos somente se o \_ \_ modo de polígono GL estiver definido como o \_ ponto GL ou a \_ linha GL. Consulte [**glPolygonMode**](/windows/desktop/OpenGL/glpolygonmode).

Inicialmente, o bit do sinalizador de borda é **true**.

O sinalizador de borda atual pode ser atualizado a qualquer momento. Em particular, **glEdgeFlag** pode ser chamado entre uma chamada para [**glBegin**](/windows/desktop/OpenGL/glbegin) e a chamada correspondente para [**glEnd**](/windows/desktop/OpenGL/glend).

As funções a seguir recuperam informações relacionadas ao **glEdgeFlag**:

sinalizador de borda [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ \_

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



 

