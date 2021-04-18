---
description: Salva uma malha em um arquivo. x.
ms.assetid: 6d9cbca8-3847-4e15-95d4-9df3f8269665
title: Função D3DXSaveMeshToX (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshToX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 504e7ad69b83c67dad52ebbf0f6d1eef8639a9fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813308"
---
# <a name="d3dxsavemeshtox-function"></a><span data-ttu-id="76cc1-103">Função D3DXSaveMeshToX</span><span class="sxs-lookup"><span data-stu-id="76cc1-103">D3DXSaveMeshToX function</span></span>

<span data-ttu-id="76cc1-104">Salva uma malha em um arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="76cc1-104">Saves a mesh to a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="76cc1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76cc1-105">Syntax</span></span>


```C++
HRESULT D3DXSaveMeshToX(
  _In_       LPCTSTR            pFilename,
  _In_       LPD3DXMESH         pMesh,
  _In_ const DWORD              *pAdjacency,
  _In_ const D3DXMATERIAL       *pMaterials,
  _In_ const D3DXEFFECTINSTANCE *pEffectInstances,
  _In_       DWORD              NumMaterials,
  _In_       DWORD              Format
);
```



## <a name="parameters"></a><span data-ttu-id="76cc1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76cc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76cc1-107">*pFilename* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="76cc1-107">*pFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76cc1-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="76cc1-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="76cc1-109">Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="76cc1-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="76cc1-110">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="76cc1-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="76cc1-111">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="76cc1-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="76cc1-112">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="76cc1-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="76cc1-113">*pMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="76cc1-113">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76cc1-114">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="76cc1-114">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="76cc1-115">Ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , representando a malha a ser salva em um arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="76cc1-115">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to save to a .x file.</span></span>

</dd> <dt>

<span data-ttu-id="76cc1-116">*pAdjacency* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="76cc1-116">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76cc1-117">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="76cc1-117">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="76cc1-118">Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha.</span><span class="sxs-lookup"><span data-stu-id="76cc1-118">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="76cc1-119">Esse parâmetro pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="76cc1-119">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="76cc1-120">*pMaterials* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="76cc1-120">*pMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76cc1-121">Tipo: **const [**D3DXMATERIAL**](d3dxmaterial.md) \***</span><span class="sxs-lookup"><span data-stu-id="76cc1-121">Type: **const [**D3DXMATERIAL**](d3dxmaterial.md)\***</span></span>

<span data-ttu-id="76cc1-122">Ponteiro para uma matriz de estruturas [**D3DXMATERIAL**](d3dxmaterial.md) , contendo informações de material a serem salvas no arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="76cc1-122">Pointer to an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing material information to be saved in the .x file.</span></span>

</dd> <dt>

<span data-ttu-id="76cc1-123">*pEffectInstances* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="76cc1-123">*pEffectInstances* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76cc1-124">Tipo: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***</span><span class="sxs-lookup"><span data-stu-id="76cc1-124">Type: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)\***</span></span>

<span data-ttu-id="76cc1-125">Ponteiro para uma matriz de instâncias de efeito, um por grupo de atributos na malha.</span><span class="sxs-lookup"><span data-stu-id="76cc1-125">Pointer to an array of effect instances, one per attribute group in the mesh.</span></span> <span data-ttu-id="76cc1-126">Esse parâmetro pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="76cc1-126">This parameter may be **NULL**.</span></span> <span data-ttu-id="76cc1-127">Uma instância de efeito é uma instância específica de informações de estado usada para inicializar um efeito.</span><span class="sxs-lookup"><span data-stu-id="76cc1-127">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="76cc1-128">Para obter mais informações, consulte [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="76cc1-128">For more information, see [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="76cc1-129">*NumMaterials* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="76cc1-129">*NumMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76cc1-130">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="76cc1-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="76cc1-131">Número de estruturas [**D3DXMATERIAL**](d3dxmaterial.md) na matriz *pMaterials* .</span><span class="sxs-lookup"><span data-stu-id="76cc1-131">Number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *pMaterials* array.</span></span>

</dd> <dt>

<span data-ttu-id="76cc1-132">*Formato* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="76cc1-132">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76cc1-133">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="76cc1-133">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="76cc1-134">Uma combinação de formato de arquivo e opções de salvamento ao salvar um arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="76cc1-134">A combination of file format and save options when saving an .x file.</span></span> <span data-ttu-id="76cc1-135">Consulte [D3DX X File Constants](dx9-graphics-reference-d3dx-x-file-constants.md).</span><span class="sxs-lookup"><span data-stu-id="76cc1-135">See [D3DX X File Constants](dx9-graphics-reference-d3dx-x-file-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76cc1-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="76cc1-136">Return value</span></span>

<span data-ttu-id="76cc1-137">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="76cc1-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="76cc1-138">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="76cc1-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="76cc1-139">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="76cc1-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="76cc1-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="76cc1-140">Remarks</span></span>

<span data-ttu-id="76cc1-141">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="76cc1-141">The compiler setting also determines the function version.</span></span> <span data-ttu-id="76cc1-142">Se o Unicode for definido, a chamada de função será resolvida como D3DXSaveMeshToXW.</span><span class="sxs-lookup"><span data-stu-id="76cc1-142">If Unicode is defined, the function call resolves to D3DXSaveMeshToXW.</span></span> <span data-ttu-id="76cc1-143">Caso contrário, a chamada de função é resolvida como D3DXSaveMeshToXA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="76cc1-143">Otherwise, the function call resolves to D3DXSaveMeshToXA because ANSI strings are being used.</span></span>

<span data-ttu-id="76cc1-144">O formato de arquivo padrão é binary; no entanto, se um arquivo for especificado como um arquivo binário e de texto, ele será salvo como um arquivo de texto.</span><span class="sxs-lookup"><span data-stu-id="76cc1-144">The default file format is binary; however, if a file is specified as both a binary and a text file, it will be saved as a text file.</span></span> <span data-ttu-id="76cc1-145">Independentemente do formato de arquivo, você também pode usar o formato compactado para reduzir o tamanho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="76cc1-145">Regardless of the file format, you may also use the compressed format to reduce the file size.</span></span>

<span data-ttu-id="76cc1-146">Veja a seguir um exemplo de código típico de como usar essa função.</span><span class="sxs-lookup"><span data-stu-id="76cc1-146">The following is a typical code example of how to use this function.</span></span>


```
ID3DXMesh*    m_pMesh;           // Mesh object to be saved to a .x file
D3DXMATERIAL* m_pMaterials;      // Array of material structs in the mesh
DWORD         m_dwNumMaterials;  // Number of material structs in the mesh
    
DWORD dwFormat = D3DXF_FILEFORMAT_BINARY;  // Binary-format .x file (default)
// DWORD dwFormat = D3DXF_FILEFORMAT_TEXT; // Text-format .x file
    
// Load mesh into m_pMesh and determine values of m_pMaterials and 
// m_dwNumMaterials with calls to D3DXLoadMeshxxx or other D3DX functions
    
// ...
        
D3DXSaveMeshToX(
    L"outputxfilename.x",
    m_pMesh,
    NULL,
    m_pMaterials,
    NULL,
    m_dwNumMaterials,
    dwFormat );
```



## <a name="requirements"></a><span data-ttu-id="76cc1-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76cc1-147">Requirements</span></span>



| <span data-ttu-id="76cc1-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="76cc1-148">Requirement</span></span> | <span data-ttu-id="76cc1-149">Valor</span><span class="sxs-lookup"><span data-stu-id="76cc1-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="76cc1-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="76cc1-150">Header</span></span><br/>  | <dl> <span data-ttu-id="76cc1-151"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="76cc1-151"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="76cc1-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="76cc1-152">Library</span></span><br/> | <dl> <span data-ttu-id="76cc1-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76cc1-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="76cc1-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="76cc1-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76cc1-155">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="76cc1-155">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="76cc1-156">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="76cc1-156">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="76cc1-157">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="76cc1-157">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
