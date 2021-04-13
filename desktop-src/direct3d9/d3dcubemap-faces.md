---
description: Define as faces de um cubemap.
ms.assetid: 6d18b410-6f22-4202-86ae-6b3ef85e6f69
title: Enumeração de D3DCUBEMAP_FACES (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCUBEMAP_FACES
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: eaf482f6f98d695f3aea3198948616c05ed01f72
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298530"
---
# <a name="d3dcubemap_faces-enumeration"></a><span data-ttu-id="93981-103">Enumeração de rostos de D3DCUBEMAP \_</span><span class="sxs-lookup"><span data-stu-id="93981-103">D3DCUBEMAP\_FACES enumeration</span></span>

<span data-ttu-id="93981-104">Define as faces de um cubemap.</span><span class="sxs-lookup"><span data-stu-id="93981-104">Defines the faces of a cubemap.</span></span>

## <a name="syntax"></a><span data-ttu-id="93981-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="93981-105">Syntax</span></span>


```C++
typedef enum D3DCUBEMAP_FACES { 
  D3DCUBEMAP_FACE_POSITIVE_X   = 0,
  D3DCUBEMAP_FACE_NEGATIVE_X   = 1,
  D3DCUBEMAP_FACE_POSITIVE_Y   = 2,
  D3DCUBEMAP_FACE_NEGATIVE_Y   = 3,
  D3DCUBEMAP_FACE_POSITIVE_Z   = 4,
  D3DCUBEMAP_FACE_NEGATIVE_Z   = 5,
  D3DCUBEMAP_FACE_FORCE_DWORD  = 0xffffffff
} D3DCUBEMAP_FACES, *LPD3DCUBEMAP_FACES;
```



## <a name="constants"></a><span data-ttu-id="93981-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="93981-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="93981-107"><span id="D3DCUBEMAP_FACE_POSITIVE_X"></span><span id="d3dcubemap_face_positive_x"></span>**\_ \_ X positivo de face D3DCUBEMAP \_**</span><span class="sxs-lookup"><span data-stu-id="93981-107"><span id="D3DCUBEMAP_FACE_POSITIVE_X"></span><span id="d3dcubemap_face_positive_x"></span>**D3DCUBEMAP\_FACE\_POSITIVE\_X**</span></span>
</dt> <dd>

<span data-ttu-id="93981-108">X-face positiva do cubemap.</span><span class="sxs-lookup"><span data-stu-id="93981-108">Positive x-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="93981-109"><span id="D3DCUBEMAP_FACE_NEGATIVE_X"></span><span id="d3dcubemap_face_negative_x"></span>**\_ \_ X negativo de face D3DCUBEMAP \_**</span><span class="sxs-lookup"><span data-stu-id="93981-109"><span id="D3DCUBEMAP_FACE_NEGATIVE_X"></span><span id="d3dcubemap_face_negative_x"></span>**D3DCUBEMAP\_FACE\_NEGATIVE\_X**</span></span>
</dt> <dd>

<span data-ttu-id="93981-110">X-face negativa de cubemap.</span><span class="sxs-lookup"><span data-stu-id="93981-110">Negative x-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="93981-111"><span id="D3DCUBEMAP_FACE_POSITIVE_Y"></span><span id="d3dcubemap_face_positive_y"></span>**D3DCUBEMAP \_ \_ positivo \_ Y**</span><span class="sxs-lookup"><span data-stu-id="93981-111"><span id="D3DCUBEMAP_FACE_POSITIVE_Y"></span><span id="d3dcubemap_face_positive_y"></span>**D3DCUBEMAP\_FACE\_POSITIVE\_Y**</span></span>
</dt> <dd>

<span data-ttu-id="93981-112">Face y positiva do cubemap.</span><span class="sxs-lookup"><span data-stu-id="93981-112">Positive y-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="93981-113"><span id="D3DCUBEMAP_FACE_NEGATIVE_Y"></span><span id="d3dcubemap_face_negative_y"></span>**Y D3DCUBEMAP de \_ rosto \_ negativo \_**</span><span class="sxs-lookup"><span data-stu-id="93981-113"><span id="D3DCUBEMAP_FACE_NEGATIVE_Y"></span><span id="d3dcubemap_face_negative_y"></span>**D3DCUBEMAP\_FACE\_NEGATIVE\_Y**</span></span>
</dt> <dd>

<span data-ttu-id="93981-114">A face y negativa do cubemap.</span><span class="sxs-lookup"><span data-stu-id="93981-114">Negative y-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="93981-115"><span id="D3DCUBEMAP_FACE_POSITIVE_Z"></span><span id="d3dcubemap_face_positive_z"></span>**D3DCUBEMAP de \_ rosto \_ positivo \_ Z**</span><span class="sxs-lookup"><span data-stu-id="93981-115"><span id="D3DCUBEMAP_FACE_POSITIVE_Z"></span><span id="d3dcubemap_face_positive_z"></span>**D3DCUBEMAP\_FACE\_POSITIVE\_Z**</span></span>
</dt> <dd>

<span data-ttu-id="93981-116">Uma face z positiva do cubemap.</span><span class="sxs-lookup"><span data-stu-id="93981-116">Positive z-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="93981-117"><span id="D3DCUBEMAP_FACE_NEGATIVE_Z"></span><span id="d3dcubemap_face_negative_z"></span>**D3DCUBEMAP de \_ rosto \_ negativo \_ Z**</span><span class="sxs-lookup"><span data-stu-id="93981-117"><span id="D3DCUBEMAP_FACE_NEGATIVE_Z"></span><span id="d3dcubemap_face_negative_z"></span>**D3DCUBEMAP\_FACE\_NEGATIVE\_Z**</span></span>
</dt> <dd>

<span data-ttu-id="93981-118">Z-face negativa de cubemap.</span><span class="sxs-lookup"><span data-stu-id="93981-118">Negative z-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="93981-119"><span id="D3DCUBEMAP_FACE_FORCE_DWORD"></span><span id="d3dcubemap_face_force_dword"></span>**\_DWORD de \_ força \_ facial do D3DCUBEMAP**</span><span class="sxs-lookup"><span data-stu-id="93981-119"><span id="D3DCUBEMAP_FACE_FORCE_DWORD"></span><span id="d3dcubemap_face_force_dword"></span>**D3DCUBEMAP\_FACE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="93981-120">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="93981-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="93981-121">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="93981-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="93981-122">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="93981-122">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93981-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93981-123">Requirements</span></span>



| <span data-ttu-id="93981-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="93981-124">Requirement</span></span> | <span data-ttu-id="93981-125">Valor</span><span class="sxs-lookup"><span data-stu-id="93981-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="93981-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="93981-126">Header</span></span><br/> | <dl> <span data-ttu-id="93981-127"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="93981-127"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93981-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="93981-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93981-129">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="93981-129">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="93981-130">**IDirect3DCubeTexture9::AddDirtyRect**</span><span class="sxs-lookup"><span data-stu-id="93981-130">**IDirect3DCubeTexture9::AddDirtyRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-adddirtyrect)
</dt> <dt>

[<span data-ttu-id="93981-131">**IDirect3DCubeTexture9::GetCubeMapSurface**</span><span class="sxs-lookup"><span data-stu-id="93981-131">**IDirect3DCubeTexture9::GetCubeMapSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)
</dt> <dt>

[<span data-ttu-id="93981-132">**IDirect3DCubeTexture9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="93981-132">**IDirect3DCubeTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="93981-133">**IDirect3DCubeTexture9::UnlockRect**</span><span class="sxs-lookup"><span data-stu-id="93981-133">**IDirect3DCubeTexture9::UnlockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-unlockrect)
</dt> </dl>

 

 
