---
title: Método ID3DX11ThreadPump ProcessDeviceWorkItems (D3DX11core. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Define itens de trabalho para o dispositivo depois que eles terminarem de carregar e processar.
ms.assetid: 154e6ea5-0a88-4c8a-9c20-e7fbf95f1946
keywords:
- Método ProcessDeviceWorkItems Direct3D 11
- Método ProcessDeviceWorkItems Direct3D 11, interface ID3DX11ThreadPump
- Interface ID3DX11ThreadPump Direct3D 11, método ProcessDeviceWorkItems
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.ProcessDeviceWorkItems
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ad570785ac7dc36fb5dd9d464e97ef46f52ca93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968590"
---
# <a name="id3dx11threadpumpprocessdeviceworkitems-method"></a><span data-ttu-id="54ce6-107">ID3DX11ThreadPump: método rocessDeviceWorkItems de:P</span><span class="sxs-lookup"><span data-stu-id="54ce6-107">ID3DX11ThreadPump::ProcessDeviceWorkItems method</span></span>

> [!Note]  
> <span data-ttu-id="54ce6-108">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="54ce6-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="54ce6-109">Define itens de trabalho para o dispositivo depois que eles terminarem de carregar e processar.</span><span class="sxs-lookup"><span data-stu-id="54ce6-109">Sets work items to the device after they have finished loading and processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="54ce6-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="54ce6-110">Syntax</span></span>


```C++
HRESULT ProcessDeviceWorkItems(
  [in] UINT iWorkItemCount
);
```



## <a name="parameters"></a><span data-ttu-id="54ce6-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54ce6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54ce6-112">*iWorkItemCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="54ce6-112">*iWorkItemCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54ce6-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="54ce6-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="54ce6-114">O número de itens de trabalho a serem definidos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="54ce6-114">The number of work items to set to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54ce6-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="54ce6-115">Return value</span></span>

<span data-ttu-id="54ce6-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="54ce6-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="54ce6-117">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="54ce6-117">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="54ce6-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="54ce6-118">Remarks</span></span>

<span data-ttu-id="54ce6-119">Quando a bomba do thread terminar de carregar e processar um recurso ou sombreador, ele a manterá em uma fila até que essa API seja chamada, ponto em que os itens processados serão definidos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="54ce6-119">When the thread pump has finished loading and processing a resource or shader, it will hold it in a queue until this API is called, at which point the processed items will be set to the device.</span></span> <span data-ttu-id="54ce6-120">Isso é útil para controlar a quantidade de processamento que é gasto na associação de recursos ao dispositivo para cada quadro.</span><span class="sxs-lookup"><span data-stu-id="54ce6-120">This is useful for controlling the amount of processing that is spent on binding resources to the device for each frame.</span></span>

<span data-ttu-id="54ce6-121">Como um exemplo de como é possível usar essa API, digamos que você esteja se aproximando do final de um nível em seu jogo e queira começar a carregar as texturas, os sombreadores e outros recursos para o próximo nível.</span><span class="sxs-lookup"><span data-stu-id="54ce6-121">As an example of how one might use this API, say you are nearing the end of one level in your game and you want to begin preloading the textures, shaders, and other resources for the next level.</span></span> <span data-ttu-id="54ce6-122">A bomba de thread começará a carregar, descompactar e processar os recursos e os sombreadores em um thread separado até que eles estejam prontos para serem definidos para o dispositivo; nesse ponto, eles serão deixados em uma fila.</span><span class="sxs-lookup"><span data-stu-id="54ce6-122">The thread pump will begin loading, decompressing, and processing the resources and shaders on a separate thread until they are ready to be set to the device, at which point it will leave them in a queue.</span></span> <span data-ttu-id="54ce6-123">Talvez você não queira definir todos os recursos e sombreadores para o dispositivo de uma vez, pois isso pode causar uma lentidão temporária perceptível no desempenho do jogo.</span><span class="sxs-lookup"><span data-stu-id="54ce6-123">One may not want to set all the resources and shaders to the device at once because this may cause a noticeable temporary slow down in the game's performance.</span></span> <span data-ttu-id="54ce6-124">Portanto, essa API pode ser chamada uma vez por quadro para que apenas um pequeno número de itens de trabalho fosse definido para o dispositivo em cada quadro, distribuindo assim a carga de trabalho dos recursos de ligação para o dispositivo em vários quadros.</span><span class="sxs-lookup"><span data-stu-id="54ce6-124">So, this API could be called once per frame so that only a small number work items would be set to the device on each frame, thereby spreading the work load of binding resources to the device over several frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="54ce6-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54ce6-125">Requirements</span></span>



| <span data-ttu-id="54ce6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="54ce6-126">Requirement</span></span> | <span data-ttu-id="54ce6-127">Valor</span><span class="sxs-lookup"><span data-stu-id="54ce6-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54ce6-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="54ce6-128">Header</span></span><br/>  | <dl> <span data-ttu-id="54ce6-129"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="54ce6-129"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="54ce6-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="54ce6-130">Library</span></span><br/> | <dl> <span data-ttu-id="54ce6-131"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54ce6-131"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="54ce6-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="54ce6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54ce6-133">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="54ce6-133">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="54ce6-134">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="54ce6-134">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

