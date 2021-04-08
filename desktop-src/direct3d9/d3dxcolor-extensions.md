---
description: Fornece as seguintes sobrecargas de operador e conversões de tipo para estruturas D3DXCOLOR.
ms.assetid: 89780c6f-c78b-4ebe-876a-6dbc37b598ef
title: Extensões D3DXCOLOR (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOLOR
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 7f457332f371b2c452a465c5b831774488301c6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837953"
---
# <a name="d3dxcolor-extensions"></a><span data-ttu-id="ecf29-103">Extensões D3DXCOLOR</span><span class="sxs-lookup"><span data-stu-id="ecf29-103">D3DXCOLOR Extensions</span></span>

<span data-ttu-id="ecf29-104">Fornece as seguintes sobrecargas de operador e conversões de tipo para estruturas [**D3DXCOLOR**](d3dxcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="ecf29-104">Supplies the following operator overloads and type casts for [**D3DXCOLOR**](d3dxcolor.md) structures.</span></span>

``` syntax
typedef struct D3DXCOLOR
{
#ifdef __cplusplus
public:
    D3DXCOLOR() {}
    D3DXCOLOR( DWORD argb );
    D3DXCOLOR( CONST FLOAT * );
    D3DXCOLOR( CONST D3DXFLOAT16 * );
    D3DXCOLOR( CONST D3DCOLORVALUE& );
    D3DXCOLOR( FLOAT r, FLOAT g, FLOAT b, FLOAT a );

    // casting
    operator DWORD () const;

    operator FLOAT* ();
    operator CONST FLOAT* () const;

    operator D3DCOLORVALUE* ();
    operator CONST D3DCOLORVALUE* () const;

    operator D3DCOLORVALUE& ();
    operator CONST D3DCOLORVALUE& () const;

    // assignment operators
    D3DXCOLOR& operator += ( CONST D3DXCOLOR& );
    D3DXCOLOR& operator -= ( CONST D3DXCOLOR& );
    D3DXCOLOR& operator *= ( FLOAT );
    D3DXCOLOR& operator /= ( FLOAT );

    // unary operators
    D3DXCOLOR operator + () const;
    D3DXCOLOR operator - () const;

    // binary operators
    D3DXCOLOR operator + ( CONST D3DXCOLOR& ) const;
    D3DXCOLOR operator - ( CONST D3DXCOLOR& ) const;
    D3DXCOLOR operator * ( FLOAT ) const;
    D3DXCOLOR operator / ( FLOAT ) const;

    friend D3DXCOLOR operator * ( FLOAT, CONST D3DXCOLOR& );

    BOOL operator == ( CONST D3DXCOLOR& ) const;
    BOOL operator != ( CONST D3DXCOLOR& ) const;

#endif //__cplusplus
    FLOAT r, g, b, a;
} D3DXCOLOR, *LPD3DXCOLOR;
```

<span data-ttu-id="ecf29-105">Tipos derivados: \* LPD3DXCOLOR</span><span class="sxs-lookup"><span data-stu-id="ecf29-105">Derived types: \*LPD3DXCOLOR</span></span>

## <a name="members"></a><span data-ttu-id="ecf29-106">Membros</span><span class="sxs-lookup"><span data-stu-id="ecf29-106">Members</span></span>

<span data-ttu-id="ecf29-107">Para obter mais informações sobre membros de estrutura, consulte [**D3DXCOLOR**](d3dxcolor.md).</span><span class="sxs-lookup"><span data-stu-id="ecf29-107">For more information about structure members, refer to [**D3DXCOLOR**](d3dxcolor.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ecf29-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="ecf29-108">Remarks</span></span>

<span data-ttu-id="ecf29-109">As sobrecargas de operador e as conversões de tipo para essa estrutura são implementadas em d3dx9math. inl.</span><span class="sxs-lookup"><span data-stu-id="ecf29-109">Operator overloads and type casts for this structure are implemented in d3dx9math.inl.</span></span>

> [!Note]  
> <span data-ttu-id="ecf29-110">O Construtor D3DXCOLOR () falha em tempo de execução quando você o executa no modo de depuração no Microsoft Visual Studio 2010 com a opção de compilador [/RTCc (verificações de erro em tempo de execução)](/previous-versions/visualstudio/visual-studio-2010/8wtf2dfz(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="ecf29-110">The D3DXCOLOR() constructor crashes at runtime when you run it in debug mode in Microsoft Visual Studio 2010 with the [Run-Time Error Checks (/RTCc)](/previous-versions/visualstudio/visual-studio-2010/8wtf2dfz(v=vs.100)) compiler option.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ecf29-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecf29-111">Requirements</span></span>



| <span data-ttu-id="ecf29-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecf29-112">Requirement</span></span> | <span data-ttu-id="ecf29-113">Valor</span><span class="sxs-lookup"><span data-stu-id="ecf29-113">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecf29-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ecf29-114">Header</span></span><br/> | <dl> <span data-ttu-id="ecf29-115"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecf29-115"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecf29-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="ecf29-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecf29-117">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="ecf29-117">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
