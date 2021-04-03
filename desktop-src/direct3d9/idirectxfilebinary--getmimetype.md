---
description: Recupera o tipo MIME (Multipurpose Internet Mail Extensions) para os dados binários. Preterido.
ms.assetid: 57c42ace-4313-40d8-9992-eaf12edf3a30
title: 'Método IDirectXFileBinary:: getMimeType (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.GetMimeType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 965006dc6fbad1176307341a19fd1f186e670104
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930580"
---
# <a name="idirectxfilebinarygetmimetype-method"></a><span data-ttu-id="1ba4f-104">Método IDirectXFileBinary:: getMimeType</span><span class="sxs-lookup"><span data-stu-id="1ba4f-104">IDirectXFileBinary::GetMimeType method</span></span>

<span data-ttu-id="1ba4f-105">Recupera o tipo MIME (Multipurpose Internet Mail Extensions) para os dados binários.</span><span class="sxs-lookup"><span data-stu-id="1ba4f-105">Retrieves the Multipurpose Internet Mail Extensions (MIME) type for the binary data.</span></span> <span data-ttu-id="1ba4f-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="1ba4f-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ba4f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ba4f-107">Syntax</span></span>


```C++
HRESULT GetMimeType(
  [out] LPCSTR *pszMimeType
);
```



## <a name="parameters"></a><span data-ttu-id="1ba4f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ba4f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ba4f-109">*pszMimeType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1ba4f-109">*pszMimeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ba4f-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1ba4f-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1ba4f-111">Endereço de um ponteiro para receber a cadeia de caracteres do tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="1ba4f-111">Address of a pointer to receive the MIME type string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ba4f-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ba4f-112">Return value</span></span>

<span data-ttu-id="1ba4f-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1ba4f-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1ba4f-114">Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1ba4f-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="1ba4f-115">Se o método falhar, o valor de retorno poderá ser DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="1ba4f-115">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ba4f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ba4f-116">Remarks</span></span>

<span data-ttu-id="1ba4f-117">Quando não houver nenhum tipo MIME especificado em um arquivo do DirectX para um objeto binário, a função definirá pszMimeType como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="1ba4f-117">When there is no MIME type specified in a DirectX file for a binary object, the function will set pszMimeType to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ba4f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ba4f-118">Requirements</span></span>



| <span data-ttu-id="1ba4f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ba4f-119">Requirement</span></span> | <span data-ttu-id="1ba4f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1ba4f-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ba4f-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ba4f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1ba4f-122"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ba4f-122"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="1ba4f-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1ba4f-123">Library</span></span><br/> | <dl> <span data-ttu-id="1ba4f-124"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ba4f-124"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ba4f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ba4f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ba4f-126">IDirectXFileBinary</span><span class="sxs-lookup"><span data-stu-id="1ba4f-126">IDirectXFileBinary</span></span>](idirectxfilebinary.md)
</dt> </dl>

 

 
