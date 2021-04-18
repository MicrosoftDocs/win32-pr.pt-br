---
description: Registra modelos personalizados.
ms.assetid: e142a0f2-d0ef-4479-82cd-ba8d5059d1d2
title: 'Método ID3DXFile:: RegisterTemplates (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.RegisterTemplates
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b7864b63d55ba219c5076920acc809f824bc1820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764199"
---
# <a name="id3dxfileregistertemplates-method"></a><span data-ttu-id="8a893-103">Método ID3DXFile:: RegisterTemplates</span><span class="sxs-lookup"><span data-stu-id="8a893-103">ID3DXFile::RegisterTemplates method</span></span>

<span data-ttu-id="8a893-104">Registra modelos personalizados.</span><span class="sxs-lookup"><span data-stu-id="8a893-104">Registers custom templates.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a893-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a893-105">Syntax</span></span>


```C++
HRESULT RegisterTemplates(
  [in] LPCVOID pvData,
  [in] SIZE_T  cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="8a893-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a893-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a893-107">*pvData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8a893-107">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a893-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8a893-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8a893-109">Ponteiro para um buffer que consiste em um arquivo. x no formato de texto ou binário que contém modelos.</span><span class="sxs-lookup"><span data-stu-id="8a893-109">Pointer to a buffer consisting of a .x file in text or binary format that contains templates.</span></span>

</dd> <dt>

<span data-ttu-id="8a893-110">*cbSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8a893-110">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a893-111">Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8a893-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8a893-112">Tamanho do buffer apontado por pvData, em bytes.</span><span class="sxs-lookup"><span data-stu-id="8a893-112">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a893-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8a893-113">Return value</span></span>

<span data-ttu-id="8a893-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8a893-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8a893-115">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8a893-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8a893-116">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DXFERR \_ BADVALUE, D3DXFERR \_ PARSEERROR.</span><span class="sxs-lookup"><span data-stu-id="8a893-116">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a893-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a893-117">Remarks</span></span>

<span data-ttu-id="8a893-118">O fragmento de código a seguir fornece uma chamada de exemplo para **RegisterTemplates** e conteúdo de exemplo para o buffer para o qual **pvData** aponta.</span><span class="sxs-lookup"><span data-stu-id="8a893-118">The following code fragment provides an example call to **RegisterTemplates** And example contents for the buffer to which **pvData** points.</span></span>


```
#define XSKINEXP_TEMPLATES \
    "xof 0303txt 0032\
    template XSkinMeshHeader \
    { \
        <3CF169CE-FF7C-44ab-93C0-F78F62D172E2> \
        WORD nMaxSkinWeightsPerVertex; \
        WORD nMaxSkinWeightsPerFace; \
        WORD nBones; \
    } \
    template VertexDuplicationIndices \
    { \
        <B8D65549-D7C9-4995-89CF-53A9A8B031E3> \
        DWORD nIndices; \
        DWORD nOriginalVertices; \
        array DWORD indices[nIndices]; \
    } \
    template SkinWeights \
    { \
        <6F0D123B-BAD2-4167-A0D0-80224F25FABB> \
        STRING transformNodeName;\
        DWORD nWeights; \
        array DWORD vertexIndices[nWeights]; \
        array float weights[nWeights]; \
        Matrix4x4 matrixOffset; \
    }"
.
.
.
        
LPD3DXFILE pD3DXFile = NULL;

if ( FAILED 
        (hr = pD3DXFile->RegisterTemplates( 
            (LPVOID)XSKINEXP_TEMPLATES,
            sizeof( XSKINEXP_TEMPLATES ) - 1 ) ) )
goto End;
```



<span data-ttu-id="8a893-119">Todos os modelos devem especificar um nome e um UUID.</span><span class="sxs-lookup"><span data-stu-id="8a893-119">All templates must specify a name and a UUID.</span></span>

<span data-ttu-id="8a893-120">Esse método chama o método [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) , obtendo um ponteiro de interface [**ID3DXFileEnumObject**](id3dxfileenumobject.md) chamando [**createenumobject**](id3dxfile--createenumobject.md) com **pvData** como o primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8a893-120">This method calls the [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) method, obtaining an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) interface pointer by calling [**CreateEnumObject**](id3dxfile--createenumobject.md) with **pvData** as the first parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a893-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a893-121">Requirements</span></span>



| <span data-ttu-id="8a893-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a893-122">Requirement</span></span> | <span data-ttu-id="8a893-123">Valor</span><span class="sxs-lookup"><span data-stu-id="8a893-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a893-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8a893-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8a893-125"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a893-125"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="8a893-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8a893-126">Library</span></span><br/> | <dl> <span data-ttu-id="8a893-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a893-127"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8a893-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a893-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a893-129">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="8a893-129">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="8a893-130">**RegisterEnumTemplates**</span><span class="sxs-lookup"><span data-stu-id="8a893-130">**RegisterEnumTemplates**</span></span>](id3dxfile--registerenumtemplates.md)
</dt> </dl>

 

 
