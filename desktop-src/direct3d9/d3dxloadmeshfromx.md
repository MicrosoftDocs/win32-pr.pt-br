---
description: Carrega uma malha a partir de um arquivo DirectX. x.
ms.assetid: cc43d2c4-3547-4431-b506-010cced26754
title: Função D3DXLoadMeshFromX (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 35622bc62804f012b4ac858f56b336dc60fbbac5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298610"
---
# <a name="d3dxloadmeshfromx-function"></a><span data-ttu-id="ee2a3-103">Função D3DXLoadMeshFromX</span><span class="sxs-lookup"><span data-stu-id="ee2a3-103">D3DXLoadMeshFromX function</span></span>

<span data-ttu-id="ee2a3-104">Carrega uma malha a partir de um arquivo DirectX. x.</span><span class="sxs-lookup"><span data-stu-id="ee2a3-104">Loads a mesh from a DirectX .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee2a3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee2a3-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromX(
  _In_  LPCTSTR           pFilename,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="ee2a3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee2a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee2a3-107">*pFilename* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee2a3-107">*pFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee2a3-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee2a3-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee2a3-109">Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="ee2a3-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="ee2a3-110">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="ee2a3-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="ee2a3-111">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="ee2a3-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="ee2a3-112">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="ee2a3-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ee2a3-113">*Opções* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="ee2a3-113">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee2a3-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee2a3-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee2a3-115">Combinação de um ou mais sinalizadores da enumeração [**D3DXMESH**](./d3dxmesh.md) , que especifica as opções de criação para a malha.</span><span class="sxs-lookup"><span data-stu-id="ee2a3-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, which specifies creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="ee2a3-116">*pD3DDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee2a3-116">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee2a3-117">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ee2a3-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ee2a3-118">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , o objeto de dispositivo associado à malha.</span><span class="sxs-lookup"><span data-stu-id="ee2a3-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="ee2a3-119">*ppAdjacency* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ee2a3-119">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee2a3-120">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee2a3-120">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="ee2a3-121">Ponteiro para um buffer que contém dados de adjacência.</span><span class="sxs-lookup"><span data-stu-id="ee2a3-121">Pointer to a buffer that contains adjacency data.</span></span> <span data-ttu-id="ee2a3-122">Os dados de adjacência contêm uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha.</span><span class="sxs-lookup"><span data-stu-id="ee2a3-122">The adjacency data contains an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="ee2a3-123">Para obter mais informações sobre como acessar o buffer, consulte [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="ee2a3-123">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee2a3-124">*ppMaterials* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ee2a3-124">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee2a3-125">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee2a3-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="ee2a3-126">Ponteiro para um buffer que contém dados de materiais.</span><span class="sxs-lookup"><span data-stu-id="ee2a3-126">Pointer to a buffer containing materials data.</span></span> <span data-ttu-id="ee2a3-127">O buffer contém uma matriz de estruturas [**D3DXMATERIAL**](d3dxmaterial.md) , contendo informações do arquivo do DirectX.</span><span class="sxs-lookup"><span data-stu-id="ee2a3-127">The buffer contains an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing information from the DirectX file.</span></span> <span data-ttu-id="ee2a3-128">Para obter mais informações sobre como acessar o buffer, consulte [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="ee2a3-128">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee2a3-129">*ppEffectInstances* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ee2a3-129">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee2a3-130">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee2a3-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="ee2a3-131">Ponteiro para um buffer que contém uma matriz de instâncias de efeito, um por grupo de atributos na malha retornada.</span><span class="sxs-lookup"><span data-stu-id="ee2a3-131">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="ee2a3-132">Uma instância de efeito é uma instância específica de informações de estado usada para inicializar um efeito.</span><span class="sxs-lookup"><span data-stu-id="ee2a3-132">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="ee2a3-133">Consulte [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="ee2a3-133">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="ee2a3-134">Para obter mais informações sobre como acessar o buffer, consulte [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="ee2a3-134">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee2a3-135">*pNumMaterials* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ee2a3-135">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee2a3-136">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee2a3-136">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ee2a3-137">Aponta para o número de estruturas [**D3DXMATERIAL**](d3dxmaterial.md) na matriz *ppMaterials* , quando o método retorna.</span><span class="sxs-lookup"><span data-stu-id="ee2a3-137">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="ee2a3-138">*ppMesh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ee2a3-138">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee2a3-139">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee2a3-139">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="ee2a3-140">Endereço de um ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , que representa a malha carregada.</span><span class="sxs-lookup"><span data-stu-id="ee2a3-140">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee2a3-141">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ee2a3-141">Return value</span></span>

<span data-ttu-id="ee2a3-142">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ee2a3-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ee2a3-143">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ee2a3-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ee2a3-144">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ee2a3-144">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee2a3-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee2a3-145">Remarks</span></span>

<span data-ttu-id="ee2a3-146">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="ee2a3-146">The compiler setting also determines the function version.</span></span> <span data-ttu-id="ee2a3-147">Se o Unicode for definido, a chamada de função será resolvida como D3DXLoadMeshFromXW.</span><span class="sxs-lookup"><span data-stu-id="ee2a3-147">If Unicode is defined, the function call resolves to D3DXLoadMeshFromXW.</span></span> <span data-ttu-id="ee2a3-148">Caso contrário, a chamada de função é resolvida como D3DXLoadMeshFromXA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="ee2a3-148">Otherwise, the function call resolves to D3DXLoadMeshFromXA because ANSI strings are being used.</span></span>

<span data-ttu-id="ee2a3-149">Todas as malhas no arquivo serão recolhidas em uma malha de saída.</span><span class="sxs-lookup"><span data-stu-id="ee2a3-149">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="ee2a3-150">Se o arquivo contiver uma hierarquia de quadros, todas as transformações serão aplicadas à malha.</span><span class="sxs-lookup"><span data-stu-id="ee2a3-150">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="ee2a3-151">Para arquivos de malha que não contêm informações de instância de efeito, as instâncias de efeito padrão serão geradas a partir das informações de material no arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="ee2a3-151">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="ee2a3-152">Uma instância de efeito padrão terá valores padrão que correspondem aos membros da estrutura [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="ee2a3-152">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="ee2a3-153">O nome de textura padrão também é preenchido, mas é tratado de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="ee2a3-153">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="ee2a3-154">O nome será Texture0@Name , que corresponde a uma variável de efeito pelo nome de "Texture0" com uma anotação chamada "Name".</span><span class="sxs-lookup"><span data-stu-id="ee2a3-154">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="ee2a3-155">Isso conterá o nome do arquivo de cadeia de caracteres para a textura.</span><span class="sxs-lookup"><span data-stu-id="ee2a3-155">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee2a3-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee2a3-156">Requirements</span></span>



| <span data-ttu-id="ee2a3-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee2a3-157">Requirement</span></span> | <span data-ttu-id="ee2a3-158">Valor</span><span class="sxs-lookup"><span data-stu-id="ee2a3-158">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee2a3-159">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ee2a3-159">Header</span></span><br/>  | <dl> <span data-ttu-id="ee2a3-160"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee2a3-160"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ee2a3-161">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee2a3-161">Library</span></span><br/> | <dl> <span data-ttu-id="ee2a3-162"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee2a3-162"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ee2a3-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee2a3-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee2a3-164">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="ee2a3-164">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="ee2a3-165">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="ee2a3-165">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="ee2a3-166">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="ee2a3-166">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
