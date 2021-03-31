---
description: Carrega uma malha de um recurso.
ms.assetid: 3cf253dc-4f3f-4949-ab24-8225667f95f2
title: Função D3DXLoadMeshFromXResource (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b3e1d9d14d86296df48e2d27f77e2f79f3ad73c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103663999"
---
# <a name="d3dxloadmeshfromxresource-function"></a><span data-ttu-id="07739-103">Função D3DXLoadMeshFromXResource</span><span class="sxs-lookup"><span data-stu-id="07739-103">D3DXLoadMeshFromXResource function</span></span>

<span data-ttu-id="07739-104">Carrega uma malha de um recurso.</span><span class="sxs-lookup"><span data-stu-id="07739-104">Loads a mesh from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="07739-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07739-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromXResource(
  _In_  HMODULE           Module,
  _In_  LPCSTR            Name,
  _In_  LPCSTR            Type,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="07739-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07739-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07739-107">*Módulo* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="07739-107">*Module* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07739-108">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07739-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="07739-109">Manipule para o módulo em que o recurso está localizado, ou **NULL** para o módulo associado à imagem que o sistema operacional usou para criar o processo atual.</span><span class="sxs-lookup"><span data-stu-id="07739-109">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span> <span data-ttu-id="07739-110">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="07739-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="07739-111">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="07739-111">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07739-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07739-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="07739-113">Ponteiro para uma cadeia de caracteres que especifica o recurso do qual criar a malha.</span><span class="sxs-lookup"><span data-stu-id="07739-113">Pointer to a string that specifies the resource to create the mesh from.</span></span> <span data-ttu-id="07739-114">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="07739-114">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="07739-115">*Tipo* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="07739-115">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07739-116">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07739-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="07739-117">Ponteiro para uma cadeia de caracteres que especifica o tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="07739-117">Pointer to a string that specifies the resource type.</span></span> <span data-ttu-id="07739-118">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="07739-118">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="07739-119">*Opções* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="07739-119">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07739-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07739-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="07739-121">Combinação de um ou mais sinalizadores da enumeração [**D3DXMESH**](./d3dxmesh.md) que especificam as opções de criação para a malha.</span><span class="sxs-lookup"><span data-stu-id="07739-121">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="07739-122">*pD3DDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="07739-122">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07739-123">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="07739-123">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="07739-124">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , o objeto de dispositivo associado à malha.</span><span class="sxs-lookup"><span data-stu-id="07739-124">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="07739-125">*ppAdjacency* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="07739-125">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07739-126">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="07739-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="07739-127">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="07739-127">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="07739-128">Quando o método retorna, esse parâmetro é preenchido com uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha.</span><span class="sxs-lookup"><span data-stu-id="07739-128">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="07739-129">*ppMaterials* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="07739-129">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07739-130">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="07739-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="07739-131">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="07739-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="07739-132">Quando esse método retorna, esse parâmetro é preenchido com uma matriz de estruturas [**D3DXMATERIAL**](d3dxmaterial.md) , contendo informações salvas no arquivo do DirectX.</span><span class="sxs-lookup"><span data-stu-id="07739-132">When this method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing information saved in the DirectX file.</span></span>

</dd> <dt>

<span data-ttu-id="07739-133">*ppEffectInstances* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="07739-133">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07739-134">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="07739-134">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="07739-135">Ponteiro para um buffer que contém uma matriz de instâncias de efeito, um por grupo de atributos na malha retornada.</span><span class="sxs-lookup"><span data-stu-id="07739-135">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="07739-136">Uma instância de efeito é uma instância específica de informações de estado usada para inicializar um efeito.</span><span class="sxs-lookup"><span data-stu-id="07739-136">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="07739-137">Consulte [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="07739-137">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="07739-138">Para obter mais informações sobre como acessar o buffer, consulte [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="07739-138">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="07739-139">*pNumMaterials* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="07739-139">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07739-140">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="07739-140">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="07739-141">Aponta para o número de estruturas [**D3DXMATERIAL**](d3dxmaterial.md) na matriz *ppMaterials* , quando o método retorna.</span><span class="sxs-lookup"><span data-stu-id="07739-141">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="07739-142">*ppMesh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="07739-142">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07739-143">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="07739-143">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="07739-144">Endereço de um ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , que representa a malha carregada.</span><span class="sxs-lookup"><span data-stu-id="07739-144">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07739-145">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="07739-145">Return value</span></span>

<span data-ttu-id="07739-146">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="07739-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="07739-147">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="07739-147">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="07739-148">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="07739-148">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="07739-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="07739-149">Remarks</span></span>

<span data-ttu-id="07739-150">Consulte [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) para saber mais sobre os parâmetros de módulo, nome e tipo.</span><span class="sxs-lookup"><span data-stu-id="07739-150">See [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) to find out more about the Module, Name and Type parameters.</span></span>

<span data-ttu-id="07739-151">Todas as malhas no arquivo serão recolhidas em uma malha de saída.</span><span class="sxs-lookup"><span data-stu-id="07739-151">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="07739-152">Se o arquivo contiver uma hierarquia de quadros, todas as transformações serão aplicadas à malha.</span><span class="sxs-lookup"><span data-stu-id="07739-152">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="07739-153">Para arquivos de malha que não contêm informações de instância de efeito, as instâncias de efeito padrão serão geradas a partir das informações de material no arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="07739-153">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="07739-154">Uma instância de efeito padrão terá valores padrão que correspondem aos membros da estrutura [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="07739-154">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="07739-155">O nome de textura padrão também é preenchido, mas é tratado de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="07739-155">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="07739-156">O nome será Texture0@Name , que corresponde a uma variável de efeito pelo nome de "Texture0" com uma anotação chamada "Name".</span><span class="sxs-lookup"><span data-stu-id="07739-156">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="07739-157">Isso conterá o nome do arquivo de cadeia de caracteres para a textura.</span><span class="sxs-lookup"><span data-stu-id="07739-157">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="07739-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07739-158">Requirements</span></span>



| <span data-ttu-id="07739-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="07739-159">Requirement</span></span> | <span data-ttu-id="07739-160">Valor</span><span class="sxs-lookup"><span data-stu-id="07739-160">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07739-161">parâmetro</span><span class="sxs-lookup"><span data-stu-id="07739-161">Header</span></span><br/>  | <dl> <span data-ttu-id="07739-162"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="07739-162"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="07739-163">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="07739-163">Library</span></span><br/> | <dl> <span data-ttu-id="07739-164"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07739-164"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="07739-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="07739-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07739-166">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="07739-166">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="07739-167">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="07739-167">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="07739-168">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="07739-168">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
