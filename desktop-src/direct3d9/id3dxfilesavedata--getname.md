---
description: Recupera o nome deste nó de dados do arquivo ID3DXFileSaveData.
ms.assetid: ea697d23-42e7-4661-b605-3654f6a31055
title: 'Método ID3DXFileSaveData:: GetName (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 00fa8c60f423343d3d4c594d31141a2f192802d3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012124"
---
# <a name="id3dxfilesavedatagetname-method"></a><span data-ttu-id="f4f8e-103">Método ID3DXFileSaveData:: GetName</span><span class="sxs-lookup"><span data-stu-id="f4f8e-103">ID3DXFileSaveData::GetName method</span></span>

<span data-ttu-id="f4f8e-104">Recupera o nome deste nó de dados do arquivo [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="f4f8e-104">Retrieves the name of this [**ID3DXFileSaveData**](id3dxfilesavedata.md) file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4f8e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4f8e-105">Syntax</span></span>


```C++
HRESULT GetName(
  [in]      LPSTR  szName,
  [in, out] SIZE_T *puiSize
);
```



## <a name="parameters"></a><span data-ttu-id="f4f8e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4f8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4f8e-107">*szName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f4f8e-107">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4f8e-108">Tipo: **[ **LPSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4f8e-108">Type: **[**LPSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f4f8e-109">Endereço de um ponteiro para receber o nome deste nó de dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f4f8e-109">Address of a pointer to receive the name of this file data node.</span></span> <span data-ttu-id="f4f8e-110">Se esse parâmetro for **NULL**, *puiSize* retornará o tamanho da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f4f8e-110">If this parameter is **NULL**, then *puiSize* will return the size of the string.</span></span> <span data-ttu-id="f4f8e-111">Se szName apontar para uma memória válida, o nome desse nó de dados do arquivo será copiado para o szName até o número de caracteres fornecidos pelo *puiSize* .</span><span class="sxs-lookup"><span data-stu-id="f4f8e-111">If szName points to valid memory, the name of this file data node will be copied into szName up to the number of characters given by *puiSize* .</span></span>

</dd> <dt>

<span data-ttu-id="f4f8e-112">*puiSize* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f4f8e-112">*puiSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4f8e-113">Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f4f8e-113">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f4f8e-114">Ponteiro para o tamanho da cadeia de caracteres que representa o nome desse nó de dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f4f8e-114">Pointer to the size of the string that represents the name of this file data node.</span></span> <span data-ttu-id="f4f8e-115">Esse parâmetro poderá ser **nulo** se szName fornecer uma referência ao nome.</span><span class="sxs-lookup"><span data-stu-id="f4f8e-115">This parameter can be **NULL** if szName provides a reference to the name.</span></span> <span data-ttu-id="f4f8e-116">Esse parâmetro retornará o tamanho da cadeia de caracteres se szName for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="f4f8e-116">This parameter will return the size of the string if szName is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4f8e-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f4f8e-117">Return value</span></span>

<span data-ttu-id="f4f8e-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f4f8e-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f4f8e-119">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f4f8e-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f4f8e-120">Se o método falhar, o seguinte valor será retornado: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="f4f8e-120">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4f8e-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4f8e-121">Remarks</span></span>

<span data-ttu-id="f4f8e-122">Para que esse método tenha sucesso, *szName* ou *puiSize* deve ser não **nulo**.</span><span class="sxs-lookup"><span data-stu-id="f4f8e-122">For this method to succeed, either *szName* or *puiSize* must be non-**NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4f8e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4f8e-123">Requirements</span></span>



| <span data-ttu-id="f4f8e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4f8e-124">Requirement</span></span> | <span data-ttu-id="f4f8e-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f4f8e-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f8e-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4f8e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f4f8e-127"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4f8e-127"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="f4f8e-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f4f8e-128">Library</span></span><br/> | <dl> <span data-ttu-id="f4f8e-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4f8e-129"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f4f8e-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4f8e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4f8e-131">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="f4f8e-131">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 
