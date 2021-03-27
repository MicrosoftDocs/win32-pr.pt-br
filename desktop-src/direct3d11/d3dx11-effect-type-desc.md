---
title: Estrutura de D3DX11_EFFECT_TYPE_DESC (D3dx11effect. h)
description: Descreve um tipo de variável de efeito.
ms.assetid: bf2aa5b7-c68c-42bb-ae70-2fe16f8669a4
keywords:
- Estrutura D3DX11_EFFECT_TYPE_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_TYPE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae0f4e8af391fed5717f47bb4b80398129cb98ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837970"
---
# <a name="d3dx11_effect_type_desc-structure"></a><span data-ttu-id="cc23b-104">\_ \_ Estrutura desc de tipo de efeito D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="cc23b-104">D3DX11\_EFFECT\_TYPE\_DESC structure</span></span>

<span data-ttu-id="cc23b-105">Descreve um tipo de variável de efeito.</span><span class="sxs-lookup"><span data-stu-id="cc23b-105">Describes an effect-variable type.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc23b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc23b-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_TYPE_DESC {
  LPCSTR                      TypeName;
  D3D10_SHADER_VARIABLE_CLASS Class;
  D3D10_SHADER_VARIABLE_TYPE  Type;
  UINT                        Elements;
  UINT                        Members;
  UINT                        Rows;
  UINT                        Columns;
  UINT                        PackedSize;
  UINT                        UnpackedSize;
  UINT                        Stride;
} D3DX11_EFFECT_TYPE_DESC;
```



## <a name="members"></a><span data-ttu-id="cc23b-107">Membros</span><span class="sxs-lookup"><span data-stu-id="cc23b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="cc23b-108">**TypeName**</span><span class="sxs-lookup"><span data-stu-id="cc23b-108">**TypeName**</span></span>
</dt> <dd>

<span data-ttu-id="cc23b-109">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cc23b-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="cc23b-110">Nome do tipo, por exemplo, "FLOAT4" ou "MyStruct".</span><span class="sxs-lookup"><span data-stu-id="cc23b-110">Name of the type, for example "float4" or "MyStruct".</span></span>

</dd> <dt>

<span data-ttu-id="cc23b-111">**Classe**</span><span class="sxs-lookup"><span data-stu-id="cc23b-111">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="cc23b-112">Tipo: **[ **\_ classe de \_ variável \_ d3d10 Shader**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)**</span><span class="sxs-lookup"><span data-stu-id="cc23b-112">Type: **[**D3D10\_SHADER\_VARIABLE\_CLASS**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)**</span></span>

</dd> <dd>

<span data-ttu-id="cc23b-113">A classe Variable (consulte [**a \_ \_ \_ classe da variável d3d10 Shader**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)).</span><span class="sxs-lookup"><span data-stu-id="cc23b-113">The variable class (see [**D3D10\_SHADER\_VARIABLE\_CLASS**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)).</span></span>

</dd> <dt>

<span data-ttu-id="cc23b-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cc23b-114">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="cc23b-115">Tipo: **[ **\_ tipo de \_ variável \_ de sombreador d3d10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)**</span><span class="sxs-lookup"><span data-stu-id="cc23b-115">Type: **[**D3D10\_SHADER\_VARIABLE\_TYPE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)**</span></span>

</dd> <dd>

<span data-ttu-id="cc23b-116">O tipo de variável ( [**consulte \_ \_ \_ tipo de variável de sombreador d3d10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)).</span><span class="sxs-lookup"><span data-stu-id="cc23b-116">The variable type (see [**D3D10\_SHADER\_VARIABLE\_TYPE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)).</span></span>

</dd> <dt>

<span data-ttu-id="cc23b-117">**Elementos**</span><span class="sxs-lookup"><span data-stu-id="cc23b-117">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="cc23b-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cc23b-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="cc23b-119">Número de elementos neste tipo (0 se não for uma matriz).</span><span class="sxs-lookup"><span data-stu-id="cc23b-119">Number of elements in this type (0 if not an array).</span></span>

</dd> <dt>

<span data-ttu-id="cc23b-120">**Membros**</span><span class="sxs-lookup"><span data-stu-id="cc23b-120">**Members**</span></span>
</dt> <dd>

<span data-ttu-id="cc23b-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cc23b-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="cc23b-122">Número de Membros (0 se não for uma estrutura).</span><span class="sxs-lookup"><span data-stu-id="cc23b-122">Number of members (0 if not a structure).</span></span>

</dd> <dt>

<span data-ttu-id="cc23b-123">**Linhas**</span><span class="sxs-lookup"><span data-stu-id="cc23b-123">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="cc23b-124">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cc23b-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="cc23b-125">Número de linhas neste tipo (0 se não for um primitivo numérico).</span><span class="sxs-lookup"><span data-stu-id="cc23b-125">Number of rows in this type (0 if not a numeric primitive).</span></span>

</dd> <dt>

<span data-ttu-id="cc23b-126">**Colunas**</span><span class="sxs-lookup"><span data-stu-id="cc23b-126">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="cc23b-127">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cc23b-127">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="cc23b-128">Número de colunas neste tipo (0 se não for um primitivo numérico).</span><span class="sxs-lookup"><span data-stu-id="cc23b-128">Number of columns in this type (0 if not a numeric primitive).</span></span>

</dd> <dt>

<span data-ttu-id="cc23b-129">**PackedSize**</span><span class="sxs-lookup"><span data-stu-id="cc23b-129">**PackedSize**</span></span>
</dt> <dd>

<span data-ttu-id="cc23b-130">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cc23b-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="cc23b-131">Número de bytes necessários para representar esse tipo de dados, quando compactados rigidamente.</span><span class="sxs-lookup"><span data-stu-id="cc23b-131">Number of bytes required to represent this data type, when tightly packed.</span></span>

</dd> <dt>

<span data-ttu-id="cc23b-132">**UnpackedSize**</span><span class="sxs-lookup"><span data-stu-id="cc23b-132">**UnpackedSize**</span></span>
</dt> <dd>

<span data-ttu-id="cc23b-133">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cc23b-133">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="cc23b-134">Número de bytes ocupados por esse tipo de dados, quando dispostos em um buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="cc23b-134">Number of bytes occupied by this data type, when laid out in a constant buffer.</span></span>

</dd> <dt>

<span data-ttu-id="cc23b-135">**Passo**</span><span class="sxs-lookup"><span data-stu-id="cc23b-135">**Stride**</span></span>
</dt> <dd>

<span data-ttu-id="cc23b-136">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cc23b-136">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="cc23b-137">Número de bytes a serem buscados entre os elementos, quando dispostos em um buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="cc23b-137">Number of bytes to seek between elements, when laid out in a constant buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc23b-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc23b-138">Remarks</span></span>

<span data-ttu-id="cc23b-139">O \_ \_ tipo de efeito D3DX11 \_ DESC é usado com [ **ID3DX11EffectType:: GetDesc**](id3dx11effecttype-getdesc.md)</span><span class="sxs-lookup"><span data-stu-id="cc23b-139">D3DX11\_EFFECT\_TYPE\_DESC is used with [**ID3DX11EffectType::GetDesc**](id3dx11effecttype-getdesc.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="cc23b-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc23b-140">Requirements</span></span>



| <span data-ttu-id="cc23b-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc23b-141">Requirement</span></span> | <span data-ttu-id="cc23b-142">Valor</span><span class="sxs-lookup"><span data-stu-id="cc23b-142">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc23b-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc23b-143">Header</span></span><br/> | <dl> <span data-ttu-id="cc23b-144"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc23b-144"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc23b-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc23b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc23b-146">Efeitos 11 estruturas</span><span class="sxs-lookup"><span data-stu-id="cc23b-146">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

