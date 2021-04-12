---
description: Descreve os parâmetros de criação para um dispositivo.
ms.assetid: 7db5ef2b-6894-4113-b726-8b238bb4fb2f
title: Estrutura de D3DDEVICE_CREATION_PARAMETERS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVICE_CREATION_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 72b2f35f1666ec2095c6ea8f5d5588dc7fd62f2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298544"
---
# <a name="d3ddevice_creation_parameters-structure"></a><span data-ttu-id="0450b-103">Estrutura de parâmetros de \_ criação de D3DDEVICE \_</span><span class="sxs-lookup"><span data-stu-id="0450b-103">D3DDEVICE\_CREATION\_PARAMETERS structure</span></span>

<span data-ttu-id="0450b-104">Descreve os parâmetros de criação para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0450b-104">Describes the creation parameters for a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="0450b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0450b-105">Syntax</span></span>


```C++
typedef struct D3DDEVICE_CREATION_PARAMETERS {
  UINT       AdapterOrdinal;
  D3DDEVTYPE DeviceType;
  HWND       hFocusWindow;
  DWORD      BehaviorFlags;
} D3DDEVICE_CREATION_PARAMETERS, *LPD3DDEVICE_CREATION_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="0450b-106">Membros</span><span class="sxs-lookup"><span data-stu-id="0450b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0450b-107">**AdapterOrdinal**</span><span class="sxs-lookup"><span data-stu-id="0450b-107">**AdapterOrdinal**</span></span>
</dt> <dd>

<span data-ttu-id="0450b-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0450b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0450b-109">Número ordinal que denota o adaptador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0450b-109">Ordinal number that denotes the display adapter.</span></span> <span data-ttu-id="0450b-110">\_O padrão D3DADAPTER é sempre o adaptador de vídeo primário.</span><span class="sxs-lookup"><span data-stu-id="0450b-110">D3DADAPTER\_DEFAULT is always the primary display adapter.</span></span> <span data-ttu-id="0450b-111">Use esse ordinal como o parâmetro do adaptador para qualquer um dos métodos [**IDirect3D9**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="0450b-111">Use this ordinal as the Adapter parameter for any of the [**IDirect3D9**](/windows/desktop/api) methods.</span></span> <span data-ttu-id="0450b-112">Observe que diferentes instâncias de objetos do Direct3D 9,0 podem usar ordinais diferentes.</span><span class="sxs-lookup"><span data-stu-id="0450b-112">Note that different instances of Direct3D 9.0 objects can use different ordinals.</span></span> <span data-ttu-id="0450b-113">Os adaptadores podem entrar ou sair de um sistema quando os usuários, por exemplo, adicionam ou removem monitores de um sistema de vários monitores ou quando alternam o hot-swap de um laptop.</span><span class="sxs-lookup"><span data-stu-id="0450b-113">Adapters can enter or leave a system when users, for example, add or remove monitors from a multiple-monitor system or when they hot-swap a laptop.</span></span> <span data-ttu-id="0450b-114">Consequentemente, use esse ordinal somente em uma instância do Direct3D 9,0 conhecida como válida, ou seja, o Direct3D 9,0 que criou essa interface [**IDirect3DDevice9**](/windows/desktop/api) ou o Direct3D 9,0 retornado de [**GetDirect3D**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdirect3d), conforme chamado por meio dessa interface **IDirect3DDevice9** .</span><span class="sxs-lookup"><span data-stu-id="0450b-114">Consequently, use this ordinal only in a Direct3D 9.0 instance known to be valid, that is, either the Direct3D 9.0 that created this [**IDirect3DDevice9**](/windows/desktop/api) interface or the Direct3D 9.0 returned from [**GetDirect3D**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdirect3d), as called through this **IDirect3DDevice9** interface.</span></span>

</dd> <dt>

<span data-ttu-id="0450b-115">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="0450b-115">**DeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="0450b-116">Tipo: **[ **D3DDEVTYPE**](./d3ddevtype.md)**</span><span class="sxs-lookup"><span data-stu-id="0450b-116">Type: **[**D3DDEVTYPE**](./d3ddevtype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0450b-117">Membro do tipo enumerado [**D3DDEVTYPE**](./d3ddevtype.md) .</span><span class="sxs-lookup"><span data-stu-id="0450b-117">Member of the [**D3DDEVTYPE**](./d3ddevtype.md) enumerated type.</span></span> <span data-ttu-id="0450b-118">Denota a quantidade de funcionalidade emulada para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0450b-118">Denotes the amount of emulated functionality for this device.</span></span> <span data-ttu-id="0450b-119">O valor desse parâmetro espelha o valor passado para a chamada [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) que criou este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0450b-119">The value of this parameter mirrors the value passed to the [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) call that created this device.</span></span>

</dd> <dt>

<span data-ttu-id="0450b-120">**hFocusWindow**</span><span class="sxs-lookup"><span data-stu-id="0450b-120">**hFocusWindow**</span></span>
</dt> <dd>

<span data-ttu-id="0450b-121">Tipo: **[ **HWND**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0450b-121">Type: **[**HWND**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0450b-122">Identificador de janela ao qual o foco pertence a este dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="0450b-122">Window handle to which focus belongs for this Direct3D device.</span></span> <span data-ttu-id="0450b-123">O valor desse parâmetro espelha o valor passado para a chamada [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) que criou este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0450b-123">The value of this parameter mirrors the value passed to the [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) call that created this device.</span></span>

</dd> <dt>

<span data-ttu-id="0450b-124">**BehaviorFlags**</span><span class="sxs-lookup"><span data-stu-id="0450b-124">**BehaviorFlags**</span></span>
</dt> <dd>

<span data-ttu-id="0450b-125">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0450b-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0450b-126">Uma combinação de uma ou mais constantes [D3DCREATE](d3dcreate.md) que controlam o comportamento global do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0450b-126">A combination of one or more [D3DCREATE](d3dcreate.md) constants that control global behavior of the device.</span></span> <span data-ttu-id="0450b-127">Essas constantes espelham as constantes passadas para [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) quando o dispositivo foi criado.</span><span class="sxs-lookup"><span data-stu-id="0450b-127">These constants mirror the constants passed to [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) when the device was created.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0450b-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0450b-128">Requirements</span></span>



| <span data-ttu-id="0450b-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="0450b-129">Requirement</span></span> | <span data-ttu-id="0450b-130">Valor</span><span class="sxs-lookup"><span data-stu-id="0450b-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0450b-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0450b-131">Header</span></span><br/> | <dl> <span data-ttu-id="0450b-132"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="0450b-132"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0450b-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="0450b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0450b-134">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="0450b-134">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="0450b-135">**GetCreationParameters**</span><span class="sxs-lookup"><span data-stu-id="0450b-135">**GetCreationParameters**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getcreationparameters)
</dt> <dt>

[<span data-ttu-id="0450b-136">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="0450b-136">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> </dl>

 

 
