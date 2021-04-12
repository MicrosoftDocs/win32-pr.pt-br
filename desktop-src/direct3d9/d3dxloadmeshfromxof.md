---
description: Carrega uma malha de um objeto ID3DXFileData.
ms.assetid: 3fcf6a91-fcd4-46da-8278-13bda8af8274
title: Função D3DXLoadMeshFromXof (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac58e5e0c27fb3daaa4795f3d4c4a8488e6c3571
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298609"
---
# <a name="d3dxloadmeshfromxof-function"></a><span data-ttu-id="9b295-103">Função D3DXLoadMeshFromXof</span><span class="sxs-lookup"><span data-stu-id="9b295-103">D3DXLoadMeshFromXof function</span></span>

<span data-ttu-id="9b295-104">Carrega uma malha de um objeto [**ID3DXFileData**](id3dxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="9b295-104">Loads a mesh from an [**ID3DXFileData**](id3dxfiledata.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b295-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b295-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromXof(
  _In_    LPD3DXFILEDATA    pxofMesh,
  _Out_   DWORD             Options,
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Out_   LPD3DXBUFFER      *ppAdjacency,
  _Inout_ LPD3DXBUFFER      *ppMaterials,
  _Out_   LPD3DXBUFFER      *ppEffectInstances,
  _Inout_ DWORD             *pNumMaterials,
  _Out_   LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="9b295-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b295-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b295-107">*pxofMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9b295-107">*pxofMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b295-108">Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="9b295-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="9b295-109">Ponteiro para uma interface [**ID3DXFileData**](id3dxfiledata.md) , representando o objeto de dados de arquivo a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="9b295-109">Pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the file data object to load.</span></span>

</dd> <dt>

<span data-ttu-id="9b295-110">*Opções* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="9b295-110">*Options* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b295-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9b295-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9b295-112">Combinação de um ou mais sinalizadores da enumeração [**D3DXMESH**](./d3dxmesh.md) , especificando as opções de criação para a malha.</span><span class="sxs-lookup"><span data-stu-id="9b295-112">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="9b295-113">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9b295-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b295-114">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="9b295-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="9b295-115">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , o objeto de dispositivo associado à malha.</span><span class="sxs-lookup"><span data-stu-id="9b295-115">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="9b295-116">*ppAdjacency* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9b295-116">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b295-117">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b295-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9b295-118">Ponteiro para um buffer que contém dados de adjacência.</span><span class="sxs-lookup"><span data-stu-id="9b295-118">Pointer to a buffer that contains adjacency data.</span></span> <span data-ttu-id="9b295-119">Os dados de adjacência contêm uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha.</span><span class="sxs-lookup"><span data-stu-id="9b295-119">The adjacency data contains an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="9b295-120">Para obter mais informações sobre como acessar o buffer, consulte [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="9b295-120">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b295-121">*ppMaterials* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="9b295-121">*ppMaterials* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b295-122">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b295-122">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9b295-123">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="9b295-123">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="9b295-124">Quando o método retorna, esse parâmetro é preenchido com uma matriz de estruturas [**D3DXMATERIAL**](d3dxmaterial.md) .</span><span class="sxs-lookup"><span data-stu-id="9b295-124">When the method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="9b295-125">*ppEffectInstances* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9b295-125">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b295-126">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b295-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9b295-127">Ponteiro para um buffer que contém uma matriz de instâncias de efeito, um por grupo de atributos na malha retornada.</span><span class="sxs-lookup"><span data-stu-id="9b295-127">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="9b295-128">Uma instância de efeito é uma instância específica de informações de estado usada para inicializar um efeito.</span><span class="sxs-lookup"><span data-stu-id="9b295-128">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="9b295-129">Consulte [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="9b295-129">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="9b295-130">Para obter mais informações sobre como acessar o buffer, consulte [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="9b295-130">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b295-131">*pNumMaterials* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="9b295-131">*pNumMaterials* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b295-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b295-132">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9b295-133">Aponta para o número de estruturas [**D3DXMATERIAL**](d3dxmaterial.md) na matriz *ppMaterials* , quando o método retorna.</span><span class="sxs-lookup"><span data-stu-id="9b295-133">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="9b295-134">*ppMesh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9b295-134">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b295-135">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b295-135">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="9b295-136">Endereço de um ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , que representa a malha carregada.</span><span class="sxs-lookup"><span data-stu-id="9b295-136">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b295-137">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9b295-137">Return value</span></span>

<span data-ttu-id="9b295-138">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9b295-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9b295-139">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9b295-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9b295-140">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="9b295-140">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b295-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b295-141">Remarks</span></span>

<span data-ttu-id="9b295-142">Para arquivos de malha que não contêm informações de instância de efeito, as instâncias de efeito padrão serão geradas a partir das informações de material no arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="9b295-142">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="9b295-143">Uma instância de efeito padrão terá valores padrão que correspondem aos membros da estrutura [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="9b295-143">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="9b295-144">O nome de textura padrão também é preenchido, mas é tratado de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="9b295-144">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="9b295-145">O nome será Texture0@Name , que corresponde a uma variável de efeito pelo nome de "Texture0" com uma anotação chamada "Name".</span><span class="sxs-lookup"><span data-stu-id="9b295-145">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="9b295-146">Isso conterá o nome do arquivo de cadeia de caracteres para a textura.</span><span class="sxs-lookup"><span data-stu-id="9b295-146">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b295-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b295-147">Requirements</span></span>



| <span data-ttu-id="9b295-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b295-148">Requirement</span></span> | <span data-ttu-id="9b295-149">Valor</span><span class="sxs-lookup"><span data-stu-id="9b295-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b295-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9b295-150">Header</span></span><br/>  | <dl> <span data-ttu-id="9b295-151"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b295-151"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9b295-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b295-152">Library</span></span><br/> | <dl> <span data-ttu-id="9b295-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b295-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9b295-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b295-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b295-155">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="9b295-155">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="9b295-156">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="9b295-156">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="9b295-157">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="9b295-157">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
