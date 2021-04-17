---
description: Cria um arquivo. x e salva a hierarquia de malha e as animações correspondentes nele.
ms.assetid: 803926fe-8cb7-422a-9920-56f7d0b0d0ea
title: Função D3DXSaveMeshHierarchyToFile (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshHierarchyToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2de65f9bc2f9e40a5bc07c6f0b4d00112f0df21
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105790509"
---
# <a name="d3dxsavemeshhierarchytofile-function"></a><span data-ttu-id="19c1c-103">Função D3DXSaveMeshHierarchyToFile</span><span class="sxs-lookup"><span data-stu-id="19c1c-103">D3DXSaveMeshHierarchyToFile function</span></span>

<span data-ttu-id="19c1c-104">Cria um arquivo. x e salva a hierarquia de malha e as animações correspondentes nele.</span><span class="sxs-lookup"><span data-stu-id="19c1c-104">Creates a .x file and saves the mesh hierarchy and corresponding animations in it.</span></span>

## <a name="syntax"></a><span data-ttu-id="19c1c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19c1c-105">Syntax</span></span>


```C++
HRESULT D3DXSaveMeshHierarchyToFile(
  _In_       LPCSTR                    pFilename,
  _In_       DWORD                     XFormat,
  _In_ const D3DXFRAME                 *pFrameRoot,
  _In_       LPD3DXANIMATIONCONTROLLER pAnimController,
  _In_       LPD3DXSAVEUSERDATA        pUserDataSaver
);
```



## <a name="parameters"></a><span data-ttu-id="19c1c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19c1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19c1c-107">*pFilename* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19c1c-107">*pFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19c1c-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19c1c-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19c1c-109">Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo. x que identifica a malha salva.</span><span class="sxs-lookup"><span data-stu-id="19c1c-109">Pointer to a string that specifies the name of the .x file identifying the saved mesh.</span></span> <span data-ttu-id="19c1c-110">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="19c1c-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="19c1c-111">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="19c1c-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="19c1c-112">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="19c1c-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="19c1c-113">*XFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19c1c-113">*XFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19c1c-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19c1c-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19c1c-115">Formato do arquivo. x (texto ou binário, compactado ou não).</span><span class="sxs-lookup"><span data-stu-id="19c1c-115">Format of the .x file (text or binary, compressed or not).</span></span> <span data-ttu-id="19c1c-116">Consulte D3DXF \_ FILEformat.</span><span class="sxs-lookup"><span data-stu-id="19c1c-116">See D3DXF\_FILEFORMAT.</span></span> <span data-ttu-id="19c1c-117">\_ \_ O formato de arquivo D3DXF compactado pode ser combinado (usando um OR lógico) com os sinalizadores de texto FileFormat binário ou D3DXF FileFormat D3DXF \_ \_ \_ \_ para reduzir o tamanho de arquivos de saída.</span><span class="sxs-lookup"><span data-stu-id="19c1c-117">D3DXF\_FILEFORMAT\_COMPRESSED can be combined (using a logical OR) with either the D3DXF\_FILEFORMAT\_BINARY or D3DXF\_FILEFORMAT\_TEXT flags to reduce the output file size.</span></span>

</dd> <dt>

<span data-ttu-id="19c1c-118">*pFrameRoot* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19c1c-118">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19c1c-119">Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="19c1c-119">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="19c1c-120">Nó raiz da hierarquia a ser salva.</span><span class="sxs-lookup"><span data-stu-id="19c1c-120">Root node of the hierarchy to be saved.</span></span> <span data-ttu-id="19c1c-121">Consulte [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="19c1c-121">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="19c1c-122">*pAnimController* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19c1c-122">*pAnimController* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19c1c-123">Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="19c1c-123">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="19c1c-124">Controlador de animação que tem conjuntos de animação a serem armazenados.</span><span class="sxs-lookup"><span data-stu-id="19c1c-124">Animation controller that has animation sets to be stored.</span></span> <span data-ttu-id="19c1c-125">Consulte [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="19c1c-125">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="19c1c-126">*pUserDataSaver* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19c1c-126">*pUserDataSaver* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19c1c-127">Tipo: **[ **LPD3DXSAVEUSERDATA**](id3dxsaveuserdata.md)**</span><span class="sxs-lookup"><span data-stu-id="19c1c-127">Type: **[**LPD3DXSAVEUSERDATA**](id3dxsaveuserdata.md)**</span></span>

<span data-ttu-id="19c1c-128">Interface fornecida pelo aplicativo que permite salvar os dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="19c1c-128">Application-provided interface that allows saving of user data.</span></span> <span data-ttu-id="19c1c-129">Consulte [**ID3DXSaveUserData**](id3dxsaveuserdata.md).</span><span class="sxs-lookup"><span data-stu-id="19c1c-129">See [**ID3DXSaveUserData**](id3dxsaveuserdata.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19c1c-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="19c1c-130">Return value</span></span>

<span data-ttu-id="19c1c-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="19c1c-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="19c1c-132">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="19c1c-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="19c1c-133">Se a função falhar, o valor de retorno poderá ser: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="19c1c-133">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="19c1c-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="19c1c-134">Remarks</span></span>

<span data-ttu-id="19c1c-135">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="19c1c-135">The compiler setting also determines the function version.</span></span> <span data-ttu-id="19c1c-136">Se o Unicode for definido, a chamada de função será resolvida como D3DXSaveMeshHierarchyToFileW.</span><span class="sxs-lookup"><span data-stu-id="19c1c-136">If Unicode is defined, the function call resolves to D3DXSaveMeshHierarchyToFileW.</span></span> <span data-ttu-id="19c1c-137">Caso contrário, a chamada de função será resolvida como D3DXSaveMeshHierarchyToFileA.</span><span class="sxs-lookup"><span data-stu-id="19c1c-137">Otherwise, the function call resolves to D3DXSaveMeshHierarchyToFileA.</span></span>

<span data-ttu-id="19c1c-138">Essa função não salva conjuntos de animação compactados.</span><span class="sxs-lookup"><span data-stu-id="19c1c-138">This function does not save compressed animation sets.</span></span>

## <a name="requirements"></a><span data-ttu-id="19c1c-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19c1c-139">Requirements</span></span>



| <span data-ttu-id="19c1c-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="19c1c-140">Requirement</span></span> | <span data-ttu-id="19c1c-141">Valor</span><span class="sxs-lookup"><span data-stu-id="19c1c-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19c1c-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="19c1c-142">Header</span></span><br/>  | <dl> <span data-ttu-id="19c1c-143"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="19c1c-143"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="19c1c-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="19c1c-144">Library</span></span><br/> | <dl> <span data-ttu-id="19c1c-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19c1c-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="19c1c-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="19c1c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19c1c-147">Funções de animação</span><span class="sxs-lookup"><span data-stu-id="19c1c-147">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> <dt>

[<span data-ttu-id="19c1c-148">Referência de arquivo X</span><span class="sxs-lookup"><span data-stu-id="19c1c-148">X File Reference</span></span>](dx9-graphics-reference-d3dx-x-file.md)
</dt> </dl>

 

 
