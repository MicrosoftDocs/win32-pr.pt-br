---
description: Obtenha uma descrição do objeto de fonte atual.
ms.assetid: f08beb35-351f-4087-a2db-097843463291
title: 'Método ID3DX10Font:: GetDesc (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDesc
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 59a7e361ebb6254fcc49eab30ff44ab39c38fd76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105756841"
---
# <a name="id3dx10fontgetdesc-method"></a><span data-ttu-id="9e68a-103">Método ID3DX10Font:: GetDesc</span><span class="sxs-lookup"><span data-stu-id="9e68a-103">ID3DX10Font::GetDesc method</span></span>

<span data-ttu-id="9e68a-104">Obtenha uma descrição do objeto de fonte atual.</span><span class="sxs-lookup"><span data-stu-id="9e68a-104">Get a description of the current font object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e68a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e68a-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [in] D3DX10_FONT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="9e68a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e68a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e68a-107">*pDesc* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e68a-107">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e68a-108">Tipo: **[ **\_ fonte D3DX10 \_ desc**](d3dx10-font-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="9e68a-108">Type: **[**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md)\***</span></span>

<span data-ttu-id="9e68a-109">Ponteiro para uma [**estrutura \_ \_ desc de fonte D3DX10**](d3dx10-font-desc.md) que descreve o objeto Font.</span><span class="sxs-lookup"><span data-stu-id="9e68a-109">Pointer to a [**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md) structure that describes the font object.</span></span> <span data-ttu-id="9e68a-110">Se o UNICODE estiver definido, um ponteiro para um D3DX10FONT \_ DESCW será retornado; caso contrário, um ponteiro para um D3DX10FONT \_ desca será retornado.</span><span class="sxs-lookup"><span data-stu-id="9e68a-110">If UNICODE is defined, a pointer to a D3DX10FONT\_DESCW is returned; otherwise a pointer to a D3DX10FONT\_DESCA is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e68a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e68a-111">Return value</span></span>

<span data-ttu-id="9e68a-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9e68a-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9e68a-113">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9e68a-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9e68a-114">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="9e68a-114">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e68a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e68a-115">Remarks</span></span>

<span data-ttu-id="9e68a-116">Esse método descreverá os objetos de fonte Unicode se o UNICODE estiver definido.</span><span class="sxs-lookup"><span data-stu-id="9e68a-116">This method describes Unicode font objects if UNICODE is defined.</span></span> <span data-ttu-id="9e68a-117">Caso contrário, getdesca é chamado, que retorna um ponteiro para a \_ estrutura desca D3DX10FONT.</span><span class="sxs-lookup"><span data-stu-id="9e68a-117">Otherwise GetDescA is called, which returns a pointer to the D3DX10FONT\_DESCA structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e68a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e68a-118">Requirements</span></span>



| <span data-ttu-id="9e68a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e68a-119">Requirement</span></span> | <span data-ttu-id="9e68a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9e68a-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e68a-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9e68a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9e68a-122"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e68a-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="9e68a-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9e68a-123">Library</span></span><br/> | <dl> <span data-ttu-id="9e68a-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e68a-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e68a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e68a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e68a-126">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="9e68a-126">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="9e68a-127">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="9e68a-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




