---
title: função glEdgeFlagv (GL. h)
description: Sinaliza bordas como limite ou não associado. | função glEdgeFlagv (GL. h)
ms.assetid: 69b5ddbd-7c0c-47f0-a358-d8bf81755c88
keywords:
- função glEdgeFlagv OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlagv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe031ab3981e3daa2e6b1aefd51c9eaa62c84483
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298283"
---
# <a name="gledgeflagv-function"></a>função glEdgeFlagv

Sinaliza bordas como limite ou não associado.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glEdgeFlagv(
   const GLboolean *flag
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*flag* 
</dt> <dd>

Especifica um ponteiro para uma matriz que contém um único elemento booliano, que substitui o valor do sinalizador de borda atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Cada vértice de um polígono, um triângulo separado ou um diamante separado especificado entre um par [**glBegin**](/windows/desktop/OpenGL/glbegin) / [**glEnd**](/windows/desktop/OpenGL/glend) é marcado como o início de um limite ou de uma borda não-bound. Se o sinalizador de borda atual for **true** quando o vértice for especificado, o vértice será marcado como o início de uma borda de limite. Se o sinalizador de borda atual for **false**, o vértice será marcado como o início de uma borda não bound. A função **glEdgeFlagv** define o sinalizador de borda como **true** se o sinalizador for diferente de zero; caso contrário, **retornará false** .

Os vértices dos triângulos conectados e quadrilaterals conectados sempre são marcados como limite, independentemente do valor do sinalizador de borda.

Os sinalizadores de borda e limites não restritos nos vértices são significativos somente se o \_ \_ modo de polígono GL estiver definido como o \_ ponto GL ou a \_ linha GL. Consulte [**glPolygonMode**](/windows/desktop/OpenGL/glpolygonmode).

Inicialmente, o bit do sinalizador de borda é **true**.

O sinalizador de borda atual pode ser atualizado a qualquer momento. Em particular, **glEdgeFlagv** pode ser chamado entre uma chamada para [**glBegin**](/windows/desktop/OpenGL/glbegin) e a chamada correspondente para [**glEnd**](/windows/desktop/OpenGL/glend).

As funções a seguir recuperam informações relacionadas ao **glEdgeFlagv**:

sinalizador de borda [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ \_

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



 

