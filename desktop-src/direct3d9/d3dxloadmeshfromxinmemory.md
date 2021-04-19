---
description: Carrega uma malha da memória.
ms.assetid: bbaecc00-97ab-433c-b0c7-ac7837bfc3be
title: Função D3DXLoadMeshFromXInMemory (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 66b07a88a938b09217a2fee2b9eed272233edc75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813744"
---
# <a name="d3dxloadmeshfromxinmemory-function"></a><span data-ttu-id="0daaf-103">Função D3DXLoadMeshFromXInMemory</span><span class="sxs-lookup"><span data-stu-id="0daaf-103">D3DXLoadMeshFromXInMemory function</span></span>

<span data-ttu-id="0daaf-104">Carrega uma malha da memória.</span><span class="sxs-lookup"><span data-stu-id="0daaf-104">Loads a mesh from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="0daaf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0daaf-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromXInMemory(
  _In_  LPCVOID           Memory,
  _In_  DWORD             SizeOfMemory,
  _Out_ DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="0daaf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0daaf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0daaf-107">*Memória* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="0daaf-107">*Memory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0daaf-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0daaf-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0daaf-109">Ponteiro para o buffer de memória que contém os dados de malha.</span><span class="sxs-lookup"><span data-stu-id="0daaf-109">Pointer to the memory buffer which contains the mesh data.</span></span>

</dd> <dt>

<span data-ttu-id="0daaf-110">*SizeOfMemory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0daaf-110">*SizeOfMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0daaf-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0daaf-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0daaf-112">Tamanho do arquivo na memória, em bytes.</span><span class="sxs-lookup"><span data-stu-id="0daaf-112">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0daaf-113">*Opções* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="0daaf-113">*Options* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0daaf-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0daaf-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0daaf-115">Combinação de um ou mais sinalizadores da enumeração [**D3DXMESH**](./d3dxmesh.md) , especificando as opções de criação para a malha.</span><span class="sxs-lookup"><span data-stu-id="0daaf-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="0daaf-116">*pD3DDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0daaf-116">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0daaf-117">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0daaf-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0daaf-118">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , o objeto de dispositivo associado à malha.</span><span class="sxs-lookup"><span data-stu-id="0daaf-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="0daaf-119">*ppAdjacency* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0daaf-119">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0daaf-120">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0daaf-120">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0daaf-121">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="0daaf-121">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="0daaf-122">Quando o método retorna, esse parâmetro é preenchido com uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha.</span><span class="sxs-lookup"><span data-stu-id="0daaf-122">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="0daaf-123">*ppMaterials* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0daaf-123">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0daaf-124">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0daaf-124">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0daaf-125">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="0daaf-125">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="0daaf-126">Quando esse método retorna, esse parâmetro é preenchido com uma matriz de estruturas [**D3DXMATERIAL**](d3dxmaterial.md) , contendo informações salvas no arquivo do DirectX.</span><span class="sxs-lookup"><span data-stu-id="0daaf-126">When this method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing information saved in the DirectX file.</span></span>

</dd> <dt>

<span data-ttu-id="0daaf-127">*ppEffectInstances* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0daaf-127">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0daaf-128">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0daaf-128">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0daaf-129">Ponteiro para um buffer que contém uma matriz de instâncias de efeito, um por grupo de atributos na malha retornada.</span><span class="sxs-lookup"><span data-stu-id="0daaf-129">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="0daaf-130">Uma instância de efeito é uma instância específica de informações de estado usada para inicializar um efeito.</span><span class="sxs-lookup"><span data-stu-id="0daaf-130">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="0daaf-131">Consulte [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="0daaf-131">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="0daaf-132">Para obter mais informações sobre como acessar o buffer, consulte [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="0daaf-132">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="0daaf-133">*pNumMaterials* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0daaf-133">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0daaf-134">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0daaf-134">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0daaf-135">Aponta para o número de estruturas [**D3DXMATERIAL**](d3dxmaterial.md) na matriz *ppMaterials* , quando o método retorna.</span><span class="sxs-lookup"><span data-stu-id="0daaf-135">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="0daaf-136">*ppMesh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0daaf-136">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0daaf-137">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="0daaf-137">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="0daaf-138">Endereço de um ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , que representa a malha carregada.</span><span class="sxs-lookup"><span data-stu-id="0daaf-138">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0daaf-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0daaf-139">Return value</span></span>

<span data-ttu-id="0daaf-140">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0daaf-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0daaf-141">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0daaf-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0daaf-142">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0daaf-142">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0daaf-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="0daaf-143">Remarks</span></span>

<span data-ttu-id="0daaf-144">Todas as malhas no arquivo serão recolhidas em uma malha de saída.</span><span class="sxs-lookup"><span data-stu-id="0daaf-144">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="0daaf-145">Se o arquivo contiver uma hierarquia de quadros, todas as transformações serão aplicadas à malha.</span><span class="sxs-lookup"><span data-stu-id="0daaf-145">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="0daaf-146">Para arquivos de malha que não contêm informações de instância de efeito, as instâncias de efeito padrão serão geradas a partir das informações de material no arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="0daaf-146">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="0daaf-147">Uma instância de efeito padrão terá valores padrão que correspondem aos membros da estrutura [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="0daaf-147">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="0daaf-148">O nome de textura padrão também é preenchido, mas é tratado de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="0daaf-148">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="0daaf-149">O nome será Texture0@Name , que corresponde a uma variável de efeito pelo nome de "Texture0" com uma anotação chamada "Name".</span><span class="sxs-lookup"><span data-stu-id="0daaf-149">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="0daaf-150">Isso conterá o nome do arquivo de cadeia de caracteres para a textura.</span><span class="sxs-lookup"><span data-stu-id="0daaf-150">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="0daaf-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0daaf-151">Requirements</span></span>



| <span data-ttu-id="0daaf-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="0daaf-152">Requirement</span></span> | <span data-ttu-id="0daaf-153">Valor</span><span class="sxs-lookup"><span data-stu-id="0daaf-153">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0daaf-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0daaf-154">Header</span></span><br/>  | <dl> <span data-ttu-id="0daaf-155"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0daaf-155"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0daaf-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0daaf-156">Library</span></span><br/> | <dl> <span data-ttu-id="0daaf-157"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0daaf-157"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0daaf-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="0daaf-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0daaf-159">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="0daaf-159">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="0daaf-160">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="0daaf-160">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="0daaf-161">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="0daaf-161">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
