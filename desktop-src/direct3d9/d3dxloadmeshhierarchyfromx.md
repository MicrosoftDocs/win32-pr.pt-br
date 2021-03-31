---
description: Carrega a primeira hierarquia de quadros de um arquivo. x.
ms.assetid: 1d446b23-9028-4187-b97c-a61edfe68e39
title: Função D3DXLoadMeshHierarchyFromX (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 308ebf127708849bec8ee8a4f2601f029562634a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930545"
---
# <a name="d3dxloadmeshhierarchyfromx-function"></a><span data-ttu-id="abe58-103">Função D3DXLoadMeshHierarchyFromX</span><span class="sxs-lookup"><span data-stu-id="abe58-103">D3DXLoadMeshHierarchyFromX function</span></span>

<span data-ttu-id="abe58-104">Carrega a primeira hierarquia de quadros de um arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="abe58-104">Loads the first frame hierarchy from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="abe58-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="abe58-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshHierarchyFromX(
  _In_  LPCTSTR                   Filename,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHierarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="abe58-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="abe58-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abe58-107">*Nome do arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="abe58-107">*Filename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abe58-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="abe58-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="abe58-109">Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="abe58-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="abe58-110">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="abe58-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="abe58-111">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="abe58-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="abe58-112">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="abe58-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="abe58-113">*Malhas* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="abe58-113">*MeshOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abe58-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="abe58-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="abe58-115">Combinação de um ou mais sinalizadores da enumeração [**D3DXMESH**](./d3dxmesh.md) que especificam as opções de criação para a malha.</span><span class="sxs-lookup"><span data-stu-id="abe58-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="abe58-116">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="abe58-116">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abe58-117">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="abe58-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="abe58-118">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , o objeto de dispositivo associado à malha.</span><span class="sxs-lookup"><span data-stu-id="abe58-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="abe58-119">*pAlloc* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="abe58-119">*pAlloc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abe58-120">Tipo: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span><span class="sxs-lookup"><span data-stu-id="abe58-120">Type: **[**LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span></span>

<span data-ttu-id="abe58-121">Ponteiro para uma interface [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) .</span><span class="sxs-lookup"><span data-stu-id="abe58-121">Pointer to an [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="abe58-122">*pUserDataLoader* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="abe58-122">*pUserDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abe58-123">Tipo: **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span><span class="sxs-lookup"><span data-stu-id="abe58-123">Type: **[**LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span></span>

<span data-ttu-id="abe58-124">Interface fornecida pelo aplicativo que permite o carregamento de dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="abe58-124">Application provided interface that allows loading of user data.</span></span> <span data-ttu-id="abe58-125">Consulte [**ID3DXLoadUserData**](id3dxloaduserdata.md).</span><span class="sxs-lookup"><span data-stu-id="abe58-125">See [**ID3DXLoadUserData**](id3dxloaduserdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="abe58-126">*ppFrameHierarchy* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="abe58-126">*ppFrameHierarchy* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abe58-127">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)\***</span><span class="sxs-lookup"><span data-stu-id="abe58-127">Type: **[**LPD3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="abe58-128">Retorna um ponteiro para a hierarquia de quadro carregada.</span><span class="sxs-lookup"><span data-stu-id="abe58-128">Returns a pointer to the loaded frame hierarchy.</span></span> <span data-ttu-id="abe58-129">Consulte [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="abe58-129">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="abe58-130">*ppAnimController* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="abe58-130">*ppAnimController* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abe58-131">Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="abe58-131">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="abe58-132">Retorna um ponteiro para o controlador de animação correspondente à animação no arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="abe58-132">Returns a pointer to the animation controller corresponding to animation in the .x file.</span></span> <span data-ttu-id="abe58-133">Isso é criado com rastreamentos e eventos padrão.</span><span class="sxs-lookup"><span data-stu-id="abe58-133">This is created with default tracks and events.</span></span> <span data-ttu-id="abe58-134">Consulte [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="abe58-134">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abe58-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="abe58-135">Return value</span></span>

<span data-ttu-id="abe58-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="abe58-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="abe58-137">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="abe58-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="abe58-138">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="abe58-138">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="abe58-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="abe58-139">Remarks</span></span>

<span data-ttu-id="abe58-140">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="abe58-140">The compiler setting also determines the function version.</span></span> <span data-ttu-id="abe58-141">Se o Unicode for definido, a chamada de função será resolvida como D3DXLoadMeshHierarchyFromXW.</span><span class="sxs-lookup"><span data-stu-id="abe58-141">If Unicode is defined, the function call resolves to D3DXLoadMeshHierarchyFromXW.</span></span> <span data-ttu-id="abe58-142">Caso contrário, a chamada de função será resolvida como D3DXLoadMeshHierarchyFromXA.</span><span class="sxs-lookup"><span data-stu-id="abe58-142">Otherwise, the function call resolves to D3DXLoadMeshHierarchyFromXA.</span></span>

<span data-ttu-id="abe58-143">Todas as malhas no arquivo serão recolhidas em uma malha de saída.</span><span class="sxs-lookup"><span data-stu-id="abe58-143">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="abe58-144">Se o arquivo contiver uma hierarquia de quadros, todas as transformações serão aplicadas à malha.</span><span class="sxs-lookup"><span data-stu-id="abe58-144">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="abe58-145">**D3DXLoadMeshHierarchyFromX** carrega os dados de animação e a hierarquia de quadros de um arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="abe58-145">**D3DXLoadMeshHierarchyFromX** loads the animation data and frame hierarchy from a .x file.</span></span> <span data-ttu-id="abe58-146">Ele examina o arquivo. x e cria uma hierarquia de quadros e um controlador de animação de acordo com o objeto derivado de [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)passado para ele por meio de pAlloc.</span><span class="sxs-lookup"><span data-stu-id="abe58-146">It scans the .x file and builds a frame hierarchy and animation controller according to the [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)-derived object passed to it through pAlloc.</span></span> <span data-ttu-id="abe58-147">O carregamento dos dados requer várias etapas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="abe58-147">Loading the data requires several steps as follows:</span></span>

1.  <span data-ttu-id="abe58-148">Derive [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md), implementando cada método.</span><span class="sxs-lookup"><span data-stu-id="abe58-148">Derive [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md), implementing each method.</span></span> <span data-ttu-id="abe58-149">Isso controla como os quadros e as malhas são alocados e liberados.</span><span class="sxs-lookup"><span data-stu-id="abe58-149">This controls how frames and meshes are allocated and freed.</span></span>
2.  <span data-ttu-id="abe58-150">Derive [**ID3DXLoadUserData**](id3dxloaduserdata.md), implementando cada método.</span><span class="sxs-lookup"><span data-stu-id="abe58-150">Derive [**ID3DXLoadUserData**](id3dxloaduserdata.md), implementing each method.</span></span> <span data-ttu-id="abe58-151">Se o arquivo. x não tiver dados inseridos definidos pelo usuário ou se você não precisar dele, poderá ignorar essa parte.</span><span class="sxs-lookup"><span data-stu-id="abe58-151">If your .x file has no embedded user-defined data, or if you do not need it, you can skip this part.</span></span>
3.  <span data-ttu-id="abe58-152">Crie um objeto da classe [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) e, opcionalmente, da classe loaduserdata.</span><span class="sxs-lookup"><span data-stu-id="abe58-152">Create an object of your [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) class, and optionally of your LoadUserData class.</span></span> <span data-ttu-id="abe58-153">Você não precisa chamar nenhum método desses objetos por conta própria.</span><span class="sxs-lookup"><span data-stu-id="abe58-153">You do not need to call any methods of these objects yourself.</span></span>
4.  <span data-ttu-id="abe58-154">Chame **D3DXLoadMeshHierarchyFromX**, passando o objeto [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) e o objeto [**ID3DXLoadUserData**](id3dxloaduserdata.md) (ou **NULL**) para criar a hierarquia de quadros e o controlador de animação.</span><span class="sxs-lookup"><span data-stu-id="abe58-154">Call **D3DXLoadMeshHierarchyFromX**, passing in your [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) object and your [**ID3DXLoadUserData**](id3dxloaduserdata.md) object (or **NULL**) to create the frame hierarchy and animation controller.</span></span> <span data-ttu-id="abe58-155">Todos os conjuntos de animação e quadros são automaticamente registrados no controlador de animação.</span><span class="sxs-lookup"><span data-stu-id="abe58-155">All the animation sets and frames are automatically registered to the animation controller.</span></span>

<span data-ttu-id="abe58-156">Durante a carga, [**CreateFrame**](id3dxallocatehierarchy--createframe.md) e [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) são chamados de volta em cada quadro para controlar o carregamento e a alocação do quadro.</span><span class="sxs-lookup"><span data-stu-id="abe58-156">During the load, [**CreateFrame**](id3dxallocatehierarchy--createframe.md) and [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) are called back on each frame to control loading and allocation of the frame.</span></span> <span data-ttu-id="abe58-157">O aplicativo define esses métodos para controlar como os quadros são armazenados.</span><span class="sxs-lookup"><span data-stu-id="abe58-157">The application defines these methods to control how frames are stored.</span></span> <span data-ttu-id="abe58-158">[**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md) e [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md) são chamados de volta em cada objeto de malha para controlar o carregamento e a alocação de objetos de malha.</span><span class="sxs-lookup"><span data-stu-id="abe58-158">[**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md) and [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md) are called back on each mesh object to control loading and allocation of mesh objects.</span></span> <span data-ttu-id="abe58-159">[**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md) é chamado de volta para cada objeto de nível superior que não é carregado por outros métodos.</span><span class="sxs-lookup"><span data-stu-id="abe58-159">[**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md) is called back for each top level object that doesn't get loaded by the other methods.</span></span>

<span data-ttu-id="abe58-160">Para liberar esses dados, chame ID3DXAnimationController:: Release para liberar os conjuntos de animação e [**D3DXFRAMEDestroy**](d3dxframedestroy.md), passando o nó raiz da hierarquia de quadros e um objeto de sua classe [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) derivada.</span><span class="sxs-lookup"><span data-stu-id="abe58-160">To free this data, call ID3DXAnimationController::Release to free the animation sets, and [**D3DXFRAMEDestroy**](d3dxframedestroy.md), passing in the root node of the frame hierarchy and an object of your derived [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) class.</span></span> <span data-ttu-id="abe58-161">[**DestroyFrame**](id3dxallocatehierarchy--destroyframe.md) e [**DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) serão chamados para cada objeto de quadro e malha na hierarquia de quadros.</span><span class="sxs-lookup"><span data-stu-id="abe58-161">[**DestroyFrame**](id3dxallocatehierarchy--destroyframe.md) and [**DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) will each be called for every frame and mesh object in the frame hierarchy.</span></span> <span data-ttu-id="abe58-162">Sua implementação do **DestroyFrame** deve liberar tudo alocado pelo [**CreateFrame**](id3dxallocatehierarchy--createframe.md)e, da mesma forma, para os métodos de contêiner de malha.</span><span class="sxs-lookup"><span data-stu-id="abe58-162">Your implementation of **DestroyFrame** should release everything allocated by [**CreateFrame**](id3dxallocatehierarchy--createframe.md), and likewise for the mesh container methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="abe58-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abe58-163">Requirements</span></span>



| <span data-ttu-id="abe58-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="abe58-164">Requirement</span></span> | <span data-ttu-id="abe58-165">Valor</span><span class="sxs-lookup"><span data-stu-id="abe58-165">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="abe58-166">parâmetro</span><span class="sxs-lookup"><span data-stu-id="abe58-166">Header</span></span><br/>  | <dl> <span data-ttu-id="abe58-167"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="abe58-167"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="abe58-168">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="abe58-168">Library</span></span><br/> | <dl> <span data-ttu-id="abe58-169"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="abe58-169"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="abe58-170">Confira também</span><span class="sxs-lookup"><span data-stu-id="abe58-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abe58-171">Funções de animação</span><span class="sxs-lookup"><span data-stu-id="abe58-171">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
