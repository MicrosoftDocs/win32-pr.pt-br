---
description: Um 4x4, matriz alinhada em 16 bytes que contém métodos e sobrecargas de operador.
ms.assetid: c7082fe5-f98b-4ab7-b8c2-7cdbab4848ad
title: Estrutura D3DXMATRIXA16 (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATRIXA16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 57d2e5e796b929c87d4724d298758f26088918c4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103663991"
---
# <a name="d3dxmatrixa16-structure-d3dx9mathh"></a>Estrutura D3DXMATRIXA16 (D3dx9math. h)

Um 4x4, matriz alinhada em 16 bytes que contém métodos e sobrecargas de operador.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXMATRIXA16 {
  FLOAT _ij;
} D3DXMATRIXA16, *LPD3DXMATRIXA16;
```



## <a name="members"></a>Membros

<dl> <dt>

**\_Ligatura**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

O componente (i, j) da matriz, onde é o número da linha e j é o número da coluna. Por exemplo, \_ 34 significa o mesmo que \[ um ₃ ₄ \] , o componente na terceira linha e a quarta coluna.

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma matriz alinhada de 16 bytes, quando usada pelas funções matemáticas do D3DX, foi otimizada para melhorar o desempenho em processadores Intel Pentium 4. As matrizes são alinhadas independentemente de onde são criadas: na pilha de programas, no heap ou no escopo global. O alinhamento é feito usando \_ \_ declspec (align (16)), que funciona com Visual C++ .net e com Visual C++ 6,0 somente quando o pacote de processador é instalado. Infelizmente, não há como detectar o pacote do processador, portanto, o alinhamento de bytes é ativado por padrão somente com o Visual C++ .NET.

Vetores e quaternions não são alinhados em byte em D3DX. Ao usar vetores e quaternions com funções matemáticas de D3DX, use \_ declspec (align (16)) para gerar vetores alinhados em bytes e quaternions, pois eles serão executados significativamente melhor. A definição de \_ declspec é mostrada aqui.


```
#define D3DX_ALIGN16 __declspec(align(16))
```



Outros compiladores interpretam D3DXMATRIXA16 como D3DXMATRIX. Usar essa estrutura em um compilador que não alinha de fato a matriz pode ser problemática porque não expõe bugs que ignoram o alinhamento. Por exemplo, se um objeto D3DXMATRIXA16 estiver dentro de uma estrutura ou classe, um [**memcpy**](https://msdn.microsoft.com/library/dswaw1wk(v=VS.71).aspx) poderá ser feito com uma embalagem justa (ignorando limites de 16 bytes). Isso causaria quebras de compilação se o compilador fosse ao mesmo tempo em que adicionava o alinhamento da matriz.

### <a name="d3dxmatrixa16"></a>D3DXMATRIXA16

O **D3DXMATRIXA16** tem as seguintes extensões C++.


```
typedef struct _D3DXMATRIXA16 : public D3DXMATRIX
{
    _D3DXMATRIXA16();
    _D3DXMATRIXA16( CONST FLOAT * f);
    _D3DXMATRIXA16( CONST D3DMATRIX& m);
    _D3DXMATRIXA16( FLOAT _11, FLOAT _12, FLOAT _13, FLOAT _14,
                    FLOAT _21, FLOAT _22, FLOAT _23, FLOAT _24,
                    FLOAT _31, FLOAT _32, FLOAT _33, FLOAT _34,
                    FLOAT _41, FLOAT _42, FLOAT _43, FLOAT _44 );
    void* operator new(size_t s);
    void* operator new[](size_t s);

    // The two operators below are not virtual operators. If you cast
    //   to D3DXMATRIX, do not delete using them
    void operator delete(void* p);
    void operator delete[](void* p);

    struct _D3DXMATRIXA16& operator=(CONST D3DXMATRIX& rhs);
} _D3DXMATRIXA16;

typedef D3DX_ALIGN16 _D3DXMATRIXA16 D3DXMATRIXA16, *LPD3DXMATRIXA16;
        
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXMATRIX**](d3dxmatrix.md)
</dt> </dl>

 

 
