---
description: Define constantes que descrevem os modos de endereçamento de textura com suporte.
ms.assetid: 5c03c55f-4a74-4b0e-ba05-e4a6582ff47c
title: Enumeração D3DTEXTUREADDRESS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREADDRESS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2cb1893541f80efb9bf85ea444b27bebba5dea29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012082"
---
# <a name="d3dtextureaddress-enumeration"></a><span data-ttu-id="f1c3a-103">Enumeração D3DTEXTUREADDRESS</span><span class="sxs-lookup"><span data-stu-id="f1c3a-103">D3DTEXTUREADDRESS enumeration</span></span>

<span data-ttu-id="f1c3a-104">Define constantes que descrevem os modos de endereçamento de textura com suporte.</span><span class="sxs-lookup"><span data-stu-id="f1c3a-104">Defines constants that describe the supported texture-addressing modes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1c3a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1c3a-105">Syntax</span></span>


```C++
typedef enum D3DTEXTUREADDRESS { 
  D3DTADDRESS_WRAP         = 1,
  D3DTADDRESS_MIRROR       = 2,
  D3DTADDRESS_CLAMP        = 3,
  D3DTADDRESS_BORDER       = 4,
  D3DTADDRESS_MIRRORONCE   = 5,
  D3DTADDRESS_FORCE_DWORD  = 0x7fffffff
} D3DTEXTUREADDRESS, *LPD3DTEXTUREADDRESS;
```



## <a name="constants"></a><span data-ttu-id="f1c3a-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="f1c3a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f1c3a-107"><span id="D3DTADDRESS_WRAP"></span><span id="d3dtaddress_wrap"></span>**\_Encapsulamento de D3DTADDRESS**</span><span class="sxs-lookup"><span data-stu-id="f1c3a-107"><span id="D3DTADDRESS_WRAP"></span><span id="d3dtaddress_wrap"></span>**D3DTADDRESS\_WRAP**</span></span>
</dt> <dd>

<span data-ttu-id="f1c3a-108">Peça a textura a cada junção de número inteiro.</span><span class="sxs-lookup"><span data-stu-id="f1c3a-108">Tile the texture at every integer junction.</span></span> <span data-ttu-id="f1c3a-109">Por exemplo, para você valores entre 0 e 3, a textura é repetida três vezes; Nenhum espelhamento é executado.</span><span class="sxs-lookup"><span data-stu-id="f1c3a-109">For example, for u values between 0 and 3, the texture is repeated three times; no mirroring is performed.</span></span>

</dd> <dt>

<span data-ttu-id="f1c3a-110"><span id="D3DTADDRESS_MIRROR"></span><span id="d3dtaddress_mirror"></span>**D3DTADDRESS \_ Mirror**</span><span class="sxs-lookup"><span data-stu-id="f1c3a-110"><span id="D3DTADDRESS_MIRROR"></span><span id="d3dtaddress_mirror"></span>**D3DTADDRESS\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="f1c3a-111">Semelhante ao D3DTADDRESS \_ Wrap, exceto que a textura é invertida a cada junção de inteiro.</span><span class="sxs-lookup"><span data-stu-id="f1c3a-111">Similar to D3DTADDRESS\_WRAP, except that the texture is flipped at every integer junction.</span></span> <span data-ttu-id="f1c3a-112">para você valores entre 0 e 1, por exemplo, a textura é resolvida normalmente; entre 1 e 2, a textura é invertida (espelhada); entre 2 e 3, a textura é normal novamente; e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="f1c3a-112">For u values between 0 and 1, for example, the texture is addressed normally; between 1 and 2, the texture is flipped (mirrored); between 2 and 3, the texture is normal again; and so on.</span></span>

</dd> <dt>

<span data-ttu-id="f1c3a-113"><span id="D3DTADDRESS_CLAMP"></span><span id="d3dtaddress_clamp"></span>**D3DTADDRESS \_ fixe**</span><span class="sxs-lookup"><span data-stu-id="f1c3a-113"><span id="D3DTADDRESS_CLAMP"></span><span id="d3dtaddress_clamp"></span>**D3DTADDRESS\_CLAMP**</span></span>
</dt> <dd>

<span data-ttu-id="f1c3a-114">As coordenadas de textura fora do intervalo de \[ 0,0, 1,0 \] são definidas como a cor de textura em 0,0 ou 1,0, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f1c3a-114">Texture coordinates outside the range \[0.0, 1.0\] are set to the texture color at 0.0 or 1.0, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="f1c3a-115"><span id="D3DTADDRESS_BORDER"></span><span id="d3dtaddress_border"></span>**\_Borda D3DTADDRESS**</span><span class="sxs-lookup"><span data-stu-id="f1c3a-115"><span id="D3DTADDRESS_BORDER"></span><span id="d3dtaddress_border"></span>**D3DTADDRESS\_BORDER**</span></span>
</dt> <dd>

<span data-ttu-id="f1c3a-116">As coordenadas de textura fora do intervalo de \[ 0,0, 1,0 \] são definidas como a cor da borda.</span><span class="sxs-lookup"><span data-stu-id="f1c3a-116">Texture coordinates outside the range \[0.0, 1.0\] are set to the border color.</span></span>

</dd> <dt>

<span data-ttu-id="f1c3a-117"><span id="D3DTADDRESS_MIRRORONCE"></span><span id="d3dtaddress_mirroronce"></span>**D3DTADDRESS \_ MIRRORONCE**</span><span class="sxs-lookup"><span data-stu-id="f1c3a-117"><span id="D3DTADDRESS_MIRRORONCE"></span><span id="d3dtaddress_mirroronce"></span>**D3DTADDRESS\_MIRRORONCE**</span></span>
</dt> <dd>

<span data-ttu-id="f1c3a-118">Semelhante a D3DTADDRESS \_ Mirror e D3DTADDRESS \_ fixe.</span><span class="sxs-lookup"><span data-stu-id="f1c3a-118">Similar to D3DTADDRESS\_MIRROR and D3DTADDRESS\_CLAMP.</span></span> <span data-ttu-id="f1c3a-119">Obtém o valor absoluto da coordenada de textura (assim, espelhamento em cerca de 0) e, em seguida, coloca ao valor máximo.</span><span class="sxs-lookup"><span data-stu-id="f1c3a-119">Takes the absolute value of the texture coordinate (thus, mirroring around 0), and then clamps to the maximum value.</span></span> <span data-ttu-id="f1c3a-120">O uso mais comum é para texturas de volume, em que o suporte para o \_ modo de endereçamento de textura D3DTADDRESS MIRRORONCE completo não é necessário, mas os dados são simétricos em relação a um eixo.</span><span class="sxs-lookup"><span data-stu-id="f1c3a-120">The most common usage is for volume textures, where support for the full D3DTADDRESS\_MIRRORONCE texture-addressing mode is not necessary, but the data is symmetric around the one axis.</span></span>

</dd> <dt>

<span data-ttu-id="f1c3a-121"><span id="D3DTADDRESS_FORCE_DWORD"></span><span id="d3dtaddress_force_dword"></span>**D3DTADDRESS \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f1c3a-121"><span id="D3DTADDRESS_FORCE_DWORD"></span><span id="d3dtaddress_force_dword"></span>**D3DTADDRESS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="f1c3a-122">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="f1c3a-122">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="f1c3a-123">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f1c3a-123">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="f1c3a-124">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="f1c3a-124">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f1c3a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1c3a-125">Requirements</span></span>



| <span data-ttu-id="f1c3a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1c3a-126">Requirement</span></span> | <span data-ttu-id="f1c3a-127">Valor</span><span class="sxs-lookup"><span data-stu-id="f1c3a-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1c3a-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f1c3a-128">Header</span></span><br/> | <dl> <span data-ttu-id="f1c3a-129"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1c3a-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1c3a-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1c3a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1c3a-131">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="f1c3a-131">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="f1c3a-132">**D3DSAMPLERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="f1c3a-132">**D3DSAMPLERSTATETYPE**</span></span>](./d3dsamplerstatetype.md)
</dt> </dl>

 

 
