---
description: 'O aplicativo implementa esse método. Esse método é chamado quando ocorre um retorno de chamada para uma animação definida em uma das faixas durante uma chamada para ID3DXAnimationController:: AdvanceTime.'
ms.assetid: eb606fb0-d6b9-456d-97e1-b595306e6463
title: 'Método ID3DXAnimationCallbackHandler:: HandleCallback (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationCallbackHandler.HandleCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49de0adef71435dbcf35afae8cfa555999826a34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105797596"
---
# <a name="id3dxanimationcallbackhandlerhandlecallback-method"></a><span data-ttu-id="253b7-104">Método ID3DXAnimationCallbackHandler:: HandleCallback</span><span class="sxs-lookup"><span data-stu-id="253b7-104">ID3DXAnimationCallbackHandler::HandleCallback method</span></span>

<span data-ttu-id="253b7-105">O aplicativo implementa esse método.</span><span class="sxs-lookup"><span data-stu-id="253b7-105">The application implements this method.</span></span> <span data-ttu-id="253b7-106">Esse método é chamado quando ocorre um retorno de chamada para uma animação definida em uma das faixas durante uma chamada para [**ID3DXAnimationController:: AdvanceTime**](id3dxanimationcontroller--advancetime.md).</span><span class="sxs-lookup"><span data-stu-id="253b7-106">This method is called when a callback occurs for an animation set in one of the tracks during a call to [**ID3DXAnimationController::AdvanceTime**](id3dxanimationcontroller--advancetime.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="253b7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="253b7-107">Syntax</span></span>


```C++
HRESULT HandleCallback(
  [in] UINT   Track,
  [in] LPVOID pCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="253b7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="253b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="253b7-109">*Acompanhar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="253b7-109">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="253b7-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="253b7-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="253b7-111">Identificador do controle no qual o retorno de chamada ocorre.</span><span class="sxs-lookup"><span data-stu-id="253b7-111">Identifier of the track on which the callback occurs.</span></span>

</dd> <dt>

<span data-ttu-id="253b7-112">*pCallbackData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="253b7-112">*pCallbackData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="253b7-113">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="253b7-113">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="253b7-114">Ponteiro para dados de retorno de chamada de Propriedade do usuário.</span><span class="sxs-lookup"><span data-stu-id="253b7-114">Pointer to user-owned callback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="253b7-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="253b7-115">Return value</span></span>

<span data-ttu-id="253b7-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="253b7-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="253b7-117">Os valores de retorno desse método são implementados por um programador de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="253b7-117">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="253b7-118">Em geral, se nenhum erro ocorrer, Programe o método para retornar o D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="253b7-118">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="253b7-119">Caso contrário, Programe o método para retornar uma mensagem de erro apropriada de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="253b7-119">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="253b7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="253b7-120">Requirements</span></span>



| <span data-ttu-id="253b7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="253b7-121">Requirement</span></span> | <span data-ttu-id="253b7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="253b7-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="253b7-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="253b7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="253b7-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="253b7-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="253b7-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="253b7-125">Library</span></span><br/> | <dl> <span data-ttu-id="253b7-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="253b7-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="253b7-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="253b7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="253b7-128">ID3DXAnimationCallbackHandler</span><span class="sxs-lookup"><span data-stu-id="253b7-128">ID3DXAnimationCallbackHandler</span></span>](id3dxanimationcallbackhandler.md)
</dt> </dl>

 

 
