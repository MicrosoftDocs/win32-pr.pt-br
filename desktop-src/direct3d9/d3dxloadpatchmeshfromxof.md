---
description: Carrega uma malha de patch de um objeto ID3DXFileData.
ms.assetid: 8054e33e-6bf8-4a56-9f66-30600732c84f
title: Função D3DXLoadPatchMeshFromXof (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPatchMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aa2e75e34927d0bb3c68445b994ee0911adb08f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798429"
---
# <a name="d3dxloadpatchmeshfromxof-function"></a><span data-ttu-id="8d194-103">Função D3DXLoadPatchMeshFromXof</span><span class="sxs-lookup"><span data-stu-id="8d194-103">D3DXLoadPatchMeshFromXof function</span></span>

<span data-ttu-id="8d194-104">Carrega uma malha de patch de um objeto [**ID3DXFileData**](id3dxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="8d194-104">Loads a patch mesh from an [**ID3DXFileData**](id3dxfiledata.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d194-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d194-105">Syntax</span></span>


```C++
HRESULT D3DXLoadPatchMeshFromXof(
  _In_  LPD3DXFILEDATA    pxofMesh,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ PDWORD            pNumMaterials,
  _Out_ LPD3DXPATCHMESH   *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="8d194-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d194-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d194-107">*pxofMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8d194-107">*pxofMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d194-108">Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="8d194-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="8d194-109">Ponteiro para uma interface [**ID3DXFileData**](id3dxfiledata.md) , representando o objeto de dados de arquivo a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="8d194-109">Pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the file data object to load.</span></span>

</dd> <dt>

<span data-ttu-id="8d194-110">*Opções* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="8d194-110">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d194-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d194-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d194-112">Combinação de um ou mais sinalizadores [**D3DXMESH**](./d3dxmesh.md) , especificando as opções de criação para a malha.</span><span class="sxs-lookup"><span data-stu-id="8d194-112">Combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="8d194-113">*pD3DDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8d194-113">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d194-114">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="8d194-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="8d194-115">Ponteiro para o dispositivo do qual a malha é criada.</span><span class="sxs-lookup"><span data-stu-id="8d194-115">Pointer to the device that the mesh is created from.</span></span>

</dd> <dt>

<span data-ttu-id="8d194-116">*ppMaterials* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8d194-116">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d194-117">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="8d194-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="8d194-118">Matriz de materiais contida na malha.</span><span class="sxs-lookup"><span data-stu-id="8d194-118">Array of materials contained in the mesh.</span></span> <span data-ttu-id="8d194-119">Cada material é indexado por uma interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="8d194-119">Each material is indexed by an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="8d194-120">*ppEffectInstances* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8d194-120">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d194-121">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="8d194-121">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="8d194-122">Ponteiro para um buffer que contém uma matriz de instâncias de efeito, um por grupo de atributos na malha retornada.</span><span class="sxs-lookup"><span data-stu-id="8d194-122">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="8d194-123">Uma instância de efeito é uma instância específica de informações de estado usada para inicializar um efeito.</span><span class="sxs-lookup"><span data-stu-id="8d194-123">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="8d194-124">Consulte [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="8d194-124">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="8d194-125">Para obter mais informações sobre como acessar o buffer, consulte [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="8d194-125">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d194-126">*pNumMaterials* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8d194-126">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d194-127">Tipo: **PDWORD**</span><span class="sxs-lookup"><span data-stu-id="8d194-127">Type: **PDWORD**</span></span>

<span data-ttu-id="8d194-128">Ponteiro que contém o número de materiais na malha.</span><span class="sxs-lookup"><span data-stu-id="8d194-128">Pointer that contains the number of materials in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="8d194-129">*ppMesh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8d194-129">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d194-130">Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="8d194-130">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="8d194-131">Endereço de um ponteiro para uma interface [**ID3DXPatchMesh**](id3dxpatchmesh.md) , que representa a malha carregada.</span><span class="sxs-lookup"><span data-stu-id="8d194-131">Address of a pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d194-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8d194-132">Return value</span></span>

<span data-ttu-id="8d194-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8d194-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8d194-134">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8d194-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8d194-135">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="8d194-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d194-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d194-136">Remarks</span></span>

<span data-ttu-id="8d194-137">Para arquivos de malha que não contêm informações de instância de efeito, as instâncias de efeito padrão serão geradas a partir das informações de material no arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="8d194-137">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="8d194-138">Uma instância de efeito padrão terá valores padrão que correspondem aos membros da estrutura [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="8d194-138">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="8d194-139">O nome de textura padrão também é preenchido, mas é tratado de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="8d194-139">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="8d194-140">O nome será Texture0@Name , que corresponde a uma variável de efeito pelo nome de "Texture0" com uma anotação chamada "Name".</span><span class="sxs-lookup"><span data-stu-id="8d194-140">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="8d194-141">Isso conterá o nome do arquivo de cadeia de caracteres para a textura.</span><span class="sxs-lookup"><span data-stu-id="8d194-141">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d194-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d194-142">Requirements</span></span>



| <span data-ttu-id="8d194-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d194-143">Requirement</span></span> | <span data-ttu-id="8d194-144">Valor</span><span class="sxs-lookup"><span data-stu-id="8d194-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d194-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8d194-145">Header</span></span><br/>  | <dl> <span data-ttu-id="8d194-146"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d194-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8d194-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8d194-147">Library</span></span><br/> | <dl> <span data-ttu-id="8d194-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d194-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8d194-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d194-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d194-150">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="8d194-150">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="8d194-151">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="8d194-151">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="8d194-152">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="8d194-152">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
