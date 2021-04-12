---
description: Salva um objeto de dados e seus filhos em um arquivo. x no disco.
ms.assetid: a48cd1b2-d1e7-446b-8482-485ccdd59353
title: 'Método ID3DXFileSaveObject:: Save (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.Save
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c97c2ccf6c509aec1d217e3179c927fe2bb5a797
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370953"
---
# <a name="id3dxfilesaveobjectsave-method"></a><span data-ttu-id="12559-103">Método ID3DXFileSaveObject:: Save</span><span class="sxs-lookup"><span data-stu-id="12559-103">ID3DXFileSaveObject::Save method</span></span>

<span data-ttu-id="12559-104">Salva um objeto de dados e seus filhos em um arquivo. x no disco.</span><span class="sxs-lookup"><span data-stu-id="12559-104">Saves a data object and its children to a .x file on disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="12559-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12559-105">Syntax</span></span>


```C++
HRESULT Save();
```



## <a name="parameters"></a><span data-ttu-id="12559-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12559-106">Parameters</span></span>

<span data-ttu-id="12559-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="12559-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="12559-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12559-108">Return value</span></span>

<span data-ttu-id="12559-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="12559-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="12559-110">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="12559-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="12559-111">Se o método falhar, o valor de retorno poderá ser o seguinte: D3DXFERR \_ BADOBJECT.</span><span class="sxs-lookup"><span data-stu-id="12559-111">If the method fails, the return value can be the following: D3DXFERR\_BADOBJECT.</span></span>

## <a name="remarks"></a><span data-ttu-id="12559-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="12559-112">Remarks</span></span>

<span data-ttu-id="12559-113">Depois que esse método for bem sucedido, [**ID3DXFileSaveObject:: Adddataobject**](id3dxfilesaveobject--adddataobject.md), [**ID3DXFileSaveData:: adddataobject**](id3dxfilesavedata--adddataobject.md) e [**ID3DXFileSaveData:: AddDataReference**](id3dxfilesavedata--adddatareference.md) não poderá mais ser chamado até que um novo objeto [**ID3DXFile**](id3dxfile.md) seja criado.</span><span class="sxs-lookup"><span data-stu-id="12559-113">After this method succeeds, [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md), [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) and [**ID3DXFileSaveData::AddDataReference**](id3dxfilesavedata--adddatareference.md) can no longer be called until a new [**ID3DXFile**](id3dxfile.md) object is created.</span></span>

## <a name="requirements"></a><span data-ttu-id="12559-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12559-114">Requirements</span></span>



| <span data-ttu-id="12559-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="12559-115">Requirement</span></span> | <span data-ttu-id="12559-116">Valor</span><span class="sxs-lookup"><span data-stu-id="12559-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12559-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12559-117">Header</span></span><br/>  | <dl> <span data-ttu-id="12559-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="12559-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="12559-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="12559-119">Library</span></span><br/> | <dl> <span data-ttu-id="12559-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12559-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="12559-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="12559-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12559-122">ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="12559-122">ID3DXFileSaveObject</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 




