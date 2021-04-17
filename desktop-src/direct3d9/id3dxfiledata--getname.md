---
description: Recupera o nome deste objeto de dados de arquivo.
ms.assetid: 182529cb-144c-4ed8-94bf-6688598e9ea7
title: 'Método ID3DXFileData:: GetName (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e27fc3e95280f29a33d4ececffc7c229563462a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105780373"
---
# <a name="id3dxfiledatagetname-method"></a><span data-ttu-id="63f4b-103">Método ID3DXFileData:: GetName</span><span class="sxs-lookup"><span data-stu-id="63f4b-103">ID3DXFileData::GetName method</span></span>

<span data-ttu-id="63f4b-104">Recupera o nome deste objeto de dados de arquivo.</span><span class="sxs-lookup"><span data-stu-id="63f4b-104">Retrieves the name of this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="63f4b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63f4b-105">Syntax</span></span>


```C++
HRESULT GetName(
  [in]      LPSTR  szName,
  [in, out] SIZE_T *puiSize
);
```



## <a name="parameters"></a><span data-ttu-id="63f4b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63f4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63f4b-107">*szName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63f4b-107">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63f4b-108">Tipo: **[ **LPSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63f4b-108">Type: **[**LPSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63f4b-109">Endereço de um ponteiro para receber o nome deste objeto de dados de arquivo.</span><span class="sxs-lookup"><span data-stu-id="63f4b-109">Address of a pointer to receive the name of this file data object.</span></span> <span data-ttu-id="63f4b-110">Se esse parâmetro for **NULL**, puiSize retornará o tamanho da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="63f4b-110">If this parameter is **NULL**, then puiSize will return the size of the string.</span></span> <span data-ttu-id="63f4b-111">Se szName apontar para uma memória válida, o nome desse objeto de dados de arquivo será copiado para szName até o número de caracteres fornecidos por puiSize.</span><span class="sxs-lookup"><span data-stu-id="63f4b-111">If szName points to valid memory, the name of this file data object will be copied into szName up to the number of characters given by puiSize.</span></span>

</dd> <dt>

<span data-ttu-id="63f4b-112">*puiSize* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="63f4b-112">*puiSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="63f4b-113">Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="63f4b-113">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="63f4b-114">Ponteiro para o tamanho da cadeia de caracteres que representa o nome desse objeto de dados de arquivo.</span><span class="sxs-lookup"><span data-stu-id="63f4b-114">Pointer to the size of the string that represents the name of this file data object.</span></span> <span data-ttu-id="63f4b-115">Esse parâmetro poderá ser **nulo** se szName fornecer uma referência ao nome.</span><span class="sxs-lookup"><span data-stu-id="63f4b-115">This parameter can be **NULL** if szName provides a reference to the name.</span></span> <span data-ttu-id="63f4b-116">Esse parâmetro retornará o tamanho da cadeia de caracteres se szName for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="63f4b-116">This parameter will return the size of the string if szName is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63f4b-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="63f4b-117">Return value</span></span>

<span data-ttu-id="63f4b-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="63f4b-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="63f4b-119">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="63f4b-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="63f4b-120">Se o método falhar, o seguinte valor será retornado: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="63f4b-120">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="63f4b-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="63f4b-121">Remarks</span></span>

<span data-ttu-id="63f4b-122">Para que esse método tenha sucesso, szName ou *puiSize* deve ser não **nulo**.</span><span class="sxs-lookup"><span data-stu-id="63f4b-122">For this method to succeed, either szName or *puiSize* must be non-**NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="63f4b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63f4b-123">Requirements</span></span>



| <span data-ttu-id="63f4b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="63f4b-124">Requirement</span></span> | <span data-ttu-id="63f4b-125">Valor</span><span class="sxs-lookup"><span data-stu-id="63f4b-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63f4b-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="63f4b-126">Header</span></span><br/>  | <dl> <span data-ttu-id="63f4b-127"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="63f4b-127"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="63f4b-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="63f4b-128">Library</span></span><br/> | <dl> <span data-ttu-id="63f4b-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63f4b-129"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="63f4b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="63f4b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63f4b-131">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="63f4b-131">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
