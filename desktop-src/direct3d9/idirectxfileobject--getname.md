---
description: Recupera um ponteiro para o nome de um objeto de arquivo do DirectX. Preterido.
ms.assetid: feb3faa2-22b9-47ed-8a38-33092821d484
title: 'Método IDirectXFileObject:: GetName (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetName
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 134a1ce61ed1dc0d98a4daf3ba80dd4b0976c372
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105788145"
---
# <a name="idirectxfileobjectgetname-method"></a><span data-ttu-id="ed9fd-104">Método IDirectXFileObject:: GetName</span><span class="sxs-lookup"><span data-stu-id="ed9fd-104">IDirectXFileObject::GetName method</span></span>

<span data-ttu-id="ed9fd-105">Recupera um ponteiro para o nome de um objeto de arquivo do DirectX.</span><span class="sxs-lookup"><span data-stu-id="ed9fd-105">Retrieves a pointer to a DirectX file object's name.</span></span> <span data-ttu-id="ed9fd-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="ed9fd-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed9fd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed9fd-107">Syntax</span></span>


```C++
HRESULT GetName(
  [out]     LPSTR   pstrNameBuf,
  [in, out] LPDWORD pdwBufLen
);
```



## <a name="parameters"></a><span data-ttu-id="ed9fd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed9fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed9fd-109">*pstrNameBuf* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ed9fd-109">*pstrNameBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed9fd-110">Tipo: **[ **LPSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed9fd-110">Type: **[**LPSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed9fd-111">Ponteiro para o buffer no qual o nome do objeto do arquivo do DirectX será copiado.</span><span class="sxs-lookup"><span data-stu-id="ed9fd-111">Pointer to the buffer in which the DirectX file object's name will be copied.</span></span> <span data-ttu-id="ed9fd-112">Defina como **NULL** se apenas o tamanho do buffer for necessário.</span><span class="sxs-lookup"><span data-stu-id="ed9fd-112">Set to **NULL** if only the buffer length is needed.</span></span>

</dd> <dt>

<span data-ttu-id="ed9fd-113">*pdwBufLen* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="ed9fd-113">*pdwBufLen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed9fd-114">Tipo: **[ **LPDWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed9fd-114">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed9fd-115">Ponteiro para um DWORD especificando o comprimento do buffer apontado por pstrNameBuf.</span><span class="sxs-lookup"><span data-stu-id="ed9fd-115">Pointer to a DWORD specifying the length of the buffer pointed to by pstrNameBuf.</span></span> <span data-ttu-id="ed9fd-116">O valor do parâmetro pdwBufLen será modificado para o comprimento do buffer necessário para manter o nome do objeto, mesmo se pstrNameBuf for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="ed9fd-116">The pdwBufLen parameter value will be modified to the buffer length needed to hold the object's name even if pstrNameBuf is **NULL**.</span></span> <span data-ttu-id="ed9fd-117">Em ambos os casos, a função retornará DXFILEERR \_ BADVALUE se o valor original de pdwBufLen não for tão grande quanto ou maior que o comprimento necessário para manter o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="ed9fd-117">In either case, the function will return DXFILEERR\_BADVALUE if the original value of pdwBufLen is not as large as or larger than the length needed to hold the object's name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed9fd-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed9fd-118">Return value</span></span>

<span data-ttu-id="ed9fd-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ed9fd-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ed9fd-120">Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ed9fd-120">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="ed9fd-121">Se o método falhar, o valor de retorno poderá ser um dos valores a seguir. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE</span><span class="sxs-lookup"><span data-stu-id="ed9fd-121">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="ed9fd-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed9fd-122">Requirements</span></span>



| <span data-ttu-id="ed9fd-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed9fd-123">Requirement</span></span> | <span data-ttu-id="ed9fd-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ed9fd-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed9fd-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ed9fd-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ed9fd-126"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed9fd-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="ed9fd-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ed9fd-127">Library</span></span><br/> | <dl> <span data-ttu-id="ed9fd-128"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed9fd-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed9fd-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed9fd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed9fd-130">IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="ed9fd-130">IDirectXFileObject</span></span>](idirectxfileobject.md)
</dt> </dl>

 

 
