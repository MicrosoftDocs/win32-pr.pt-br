---
description: Carrega uma malha de capa de um objeto de dados de arquivo DirectX. x.
ms.assetid: db284061-2996-4a5f-972d-24577dd1a6d7
title: Função D3DXLoadSkinMeshFromXof (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSkinMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b87e97e0bde7be37497f68c276a09163ea68ee71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103663972"
---
# <a name="d3dxloadskinmeshfromxof-function"></a><span data-ttu-id="3842d-103">Função D3DXLoadSkinMeshFromXof</span><span class="sxs-lookup"><span data-stu-id="3842d-103">D3DXLoadSkinMeshFromXof function</span></span>

<span data-ttu-id="3842d-104">Carrega uma malha de capa de um objeto de dados de arquivo DirectX. x.</span><span class="sxs-lookup"><span data-stu-id="3842d-104">Loads a skin mesh from a DirectX .x file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3842d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3842d-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSkinMeshFromXof(
  _In_  LPD3DXFILEDATA    pxofMesh,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pMatOut,
  _Out_ LPD3DXSKININFO    *ppSkinInfo,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="3842d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3842d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3842d-107">*pxofMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3842d-107">*pxofMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3842d-108">Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="3842d-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="3842d-109">Ponteiro para uma interface [**ID3DXFileData**](id3dxfiledata.md) , representando o objeto de dados de arquivo a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="3842d-109">Pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the file data object to load.</span></span>

</dd> <dt>

<span data-ttu-id="3842d-110">*Opções* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="3842d-110">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3842d-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3842d-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3842d-112">Combinação de um ou mais sinalizadores, da enumeração [**D3DXMESH**](./d3dxmesh.md) , especificando as opções de criação para a malha.</span><span class="sxs-lookup"><span data-stu-id="3842d-112">Combination of one or more flags, from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="3842d-113">*pD3DDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3842d-113">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3842d-114">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="3842d-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="3842d-115">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , o objeto de dispositivo associado à malha.</span><span class="sxs-lookup"><span data-stu-id="3842d-115">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="3842d-116">*ppAdjacency* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3842d-116">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3842d-117">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3842d-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="3842d-118">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="3842d-118">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="3842d-119">Quando esse método retorna, esse parâmetro é preenchido com uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha.</span><span class="sxs-lookup"><span data-stu-id="3842d-119">When this method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="3842d-120">*ppMaterials* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3842d-120">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3842d-121">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3842d-121">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="3842d-122">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="3842d-122">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="3842d-123">Quando o método retorna, esse parâmetro é preenchido com uma matriz de estruturas [**D3DXMATERIAL**](d3dxmaterial.md) .</span><span class="sxs-lookup"><span data-stu-id="3842d-123">When the method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="3842d-124">*ppEffectInstances* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3842d-124">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3842d-125">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3842d-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="3842d-126">Ponteiro para um buffer que contém uma matriz de instâncias de efeito, um por grupo de atributos na malha retornada.</span><span class="sxs-lookup"><span data-stu-id="3842d-126">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="3842d-127">Uma instância de efeito é uma instância específica de informações de estado usada para inicializar um efeito.</span><span class="sxs-lookup"><span data-stu-id="3842d-127">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="3842d-128">Consulte [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="3842d-128">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="3842d-129">Para obter mais informações sobre como acessar o buffer, consulte [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="3842d-129">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="3842d-130">*pMatOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3842d-130">*pMatOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3842d-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3842d-131">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3842d-132">Aponta para o número de estruturas [**D3DXMATERIAL**](d3dxmaterial.md) na matriz *ppMaterials* , quando o método retorna.</span><span class="sxs-lookup"><span data-stu-id="3842d-132">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="3842d-133">*ppSkinInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3842d-133">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3842d-134">Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="3842d-134">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="3842d-135">Endereço de um ponteiro para uma interface [**ID3DXSkinInfo**](id3dxskininfo.md) , que representa as informações de aparência.</span><span class="sxs-lookup"><span data-stu-id="3842d-135">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface, which represents the skinning information.</span></span>

</dd> <dt>

<span data-ttu-id="3842d-136">*ppMesh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3842d-136">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3842d-137">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="3842d-137">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="3842d-138">Endereço de um ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , que representa a malha carregada.</span><span class="sxs-lookup"><span data-stu-id="3842d-138">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, which represents the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3842d-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3842d-139">Return value</span></span>

<span data-ttu-id="3842d-140">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3842d-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3842d-141">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3842d-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3842d-142">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="3842d-142">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY</span></span>

## <a name="remarks"></a><span data-ttu-id="3842d-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="3842d-143">Remarks</span></span>

<span data-ttu-id="3842d-144">Esse método usa um ponteiro para um objeto interno no arquivo. x, permitindo que você carregue a hierarquia de quadros.</span><span class="sxs-lookup"><span data-stu-id="3842d-144">This method takes a pointer to an internal object in the .x file, enabling you to load the frame hierarchy.</span></span>

<span data-ttu-id="3842d-145">Para arquivos de malha que não contêm informações de instância de efeito, as instâncias de efeito padrão serão geradas a partir das informações de material no arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="3842d-145">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="3842d-146">Uma instância de efeito padrão terá valores padrão que correspondem aos membros da estrutura [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="3842d-146">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="3842d-147">O nome de textura padrão também é preenchido, mas é tratado de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="3842d-147">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="3842d-148">O nome será Texture0@Name , que corresponde a uma variável de efeito pelo nome de "Texture0" com uma anotação chamada "Name".</span><span class="sxs-lookup"><span data-stu-id="3842d-148">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="3842d-149">Isso conterá o nome do arquivo de cadeia de caracteres para a textura.</span><span class="sxs-lookup"><span data-stu-id="3842d-149">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="3842d-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3842d-150">Requirements</span></span>



| <span data-ttu-id="3842d-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="3842d-151">Requirement</span></span> | <span data-ttu-id="3842d-152">Valor</span><span class="sxs-lookup"><span data-stu-id="3842d-152">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3842d-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3842d-153">Header</span></span><br/>  | <dl> <span data-ttu-id="3842d-154"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3842d-154"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3842d-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3842d-155">Library</span></span><br/> | <dl> <span data-ttu-id="3842d-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3842d-156"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3842d-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="3842d-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3842d-158">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="3842d-158">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="3842d-159">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="3842d-159">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="3842d-160">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="3842d-160">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
