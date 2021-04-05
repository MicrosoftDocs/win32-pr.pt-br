---
description: Recupera o GUID deste objeto de dados de arquivo.
ms.assetid: 79bf56b5-5900-4427-8092-3a1df86f8a57
title: 'Método ID3DXFileData:: GetId (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e1dafb296541b1702e9163dcc6d460cf149b4007
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664038"
---
# <a name="id3dxfiledatagetid-method"></a><span data-ttu-id="44635-103">Método ID3DXFileData:: GetId</span><span class="sxs-lookup"><span data-stu-id="44635-103">ID3DXFileData::GetId method</span></span>

<span data-ttu-id="44635-104">Recupera o GUID deste objeto de dados de arquivo.</span><span class="sxs-lookup"><span data-stu-id="44635-104">Retrieves the GUID of this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="44635-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44635-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] 
            LPGUID pId
);
```



## <a name="parameters"></a><span data-ttu-id="44635-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44635-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44635-107">*pid* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="44635-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44635-108">Tipo: **LPGUID**</span><span class="sxs-lookup"><span data-stu-id="44635-108">Type: **LPGUID**</span></span>

<span data-ttu-id="44635-109">Ponteiro para um GUID para receber a ID deste objeto de dados de arquivo.</span><span class="sxs-lookup"><span data-stu-id="44635-109">Pointer to a GUID to receive the ID of this file data object.</span></span> <span data-ttu-id="44635-110">Se o objeto de dados do arquivo não tiver nenhuma ID, o valor do parâmetro retornado será GUID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="44635-110">If the file data object has no ID, the returned parameter value will be GUID\_NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44635-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="44635-111">Return value</span></span>

<span data-ttu-id="44635-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="44635-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="44635-113">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="44635-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="44635-114">Se o método falhar, o seguinte valor será retornado: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="44635-114">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="44635-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44635-115">Requirements</span></span>



| <span data-ttu-id="44635-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="44635-116">Requirement</span></span> | <span data-ttu-id="44635-117">Valor</span><span class="sxs-lookup"><span data-stu-id="44635-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44635-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44635-118">Header</span></span><br/>  | <dl> <span data-ttu-id="44635-119"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="44635-119"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="44635-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="44635-120">Library</span></span><br/> | <dl> <span data-ttu-id="44635-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44635-121"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="44635-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="44635-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44635-123">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="44635-123">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 




