---
description: Estrutura D3DXMATRIXA16 (D3DX10Math.h) – uma matriz alinhada a 4x4, 16 byte que contém métodos e sobrecargas de operador.
ms.assetid: d9e9c1cc-7555-4011-a4b4-8cce20404841
title: Estrutura D3DXMATRIXA16 (D3DX10Math.h)
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
- D3DX10Math.h
ms.openlocfilehash: 4953b51cdd09cdbcac4855bd423ce37dda5b979e06153589b5b2ded21004b3ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853396"
---
# <a name="d3dxmatrixa16-structure-d3dx10mathh"></a>Estrutura D3DXMATRIXA16 (D3DX10Math.h)

Uma matriz alinhada de 4x4 e 16 byte que contém métodos e sobrecargas de operador.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXMATRIXA16 {
  FLOAT _ij;
} D3DXMATRIXA16, *LPD3DXMATRIXA16;
```



## <a name="members"></a>Membros

<dl> <dt>

**\_Ij**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

O componente (i, j) da matriz, em que i é o número da linha e j é o número da coluna. Por exemplo, \_ 34 significa o mesmo que \[ um , o componente na terceira linha e na quarta \] coluna.

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma matriz alinhada de 16 byte, quando usada por funções matemáticas D3DX, foi otimizada para melhorar o desempenho em processadores Intel Pentium 4. Matrizes são alinhadas independentemente de onde são criadas: na pilha do programa, no heap ou no escopo global. O alinhamento é realizado usando \_ declspec(align(16)), que funciona com o .NET do Visual C++ e com Visual C++ 6.0 somente quando o pacote do processador \_ está instalado. Infelizmente, não há nenhuma maneira de detectar o pacote do processador, portanto, o alinhamento de byte é ligado por padrão apenas com Visual C++ .NET.

Vetores e quatternions não são alinhados por byte em D3DX. Ao usar vetores e quatternions com funções matemáticas D3DX, use declspec(align(16)) para gerar vetores alinhados por byte e quatternions, pois eles terão um desempenho significativamente \_ melhor. A definição \_ de declspec é mostrada aqui.


```
#define D3DX_ALIGN16 __declspec(align(16))
```



Outros compiladores interpretam **D3DXMATRIXA16** [**como D3DXMATRIX.**](d3d10-d3dxmatrix.md) Usar essa estrutura em um compilador que realmente não alinha a matriz pode ser problemático porque não exporá bugs que ignoram o alinhamento. Por exemplo, se um objeto **D3DXMATRIXA16** estiver dentro de uma estrutura ou classe, um [memcpy](https://msdn2.microsoft.com/library/dswaw1wk(vs.71).aspx) poderá ser feito com empacotamento rígido (ignorando limites de 16 byte). Isso causaria quebras de build se o compilador adicionasse algum tempo o alinhamento de matriz.

### <a name="d3dxmatrixa16-extensions"></a>Extensões D3DXMATRIXA16

**D3DXMATRIXA16** tem as seguintes extensões C++.


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
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
