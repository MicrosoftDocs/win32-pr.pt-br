---
description: Defina itens de trabalho para o dispositivo depois que eles terminarem de carregar e processar.
ms.assetid: 67a9fcb2-3513-413d-ac3d-9988ef7b5a1f
title: 'ID3DX10ThreadPump: método rocessDeviceWorkItems de:P (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.ProcessDeviceWorkItems
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 88b98d68e4e0e47b2c8e7f9a2e095565c53e2561
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104092004"
---
# <a name="id3dx10threadpumpprocessdeviceworkitems-method"></a><span data-ttu-id="e4539-103">ID3DX10ThreadPump: método rocessDeviceWorkItems de:P</span><span class="sxs-lookup"><span data-stu-id="e4539-103">ID3DX10ThreadPump::ProcessDeviceWorkItems method</span></span>

<span data-ttu-id="e4539-104">Defina itens de trabalho para o dispositivo depois que eles terminarem de carregar e processar.</span><span class="sxs-lookup"><span data-stu-id="e4539-104">Set work items to the device after they have finished loading and processing.</span></span> <span data-ttu-id="e4539-105">Quando a bomba do thread terminar de carregar e processar um recurso ou sombreador, ele a manterá em uma fila até que essa API seja chamada, ponto em que os itens processados serão definidos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e4539-105">When the thread pump has finished loading and processing a resource or shader, it will hold it in a queue until this API is called, at which point the processed items will be set to the device.</span></span> <span data-ttu-id="e4539-106">Isso é útil para controlar a quantidade de processamento que é gasto na associação de recursos ao dispositivo para cada quadro.</span><span class="sxs-lookup"><span data-stu-id="e4539-106">This is useful for controlling the amount of processing that is spent on binding resources to the device for each frame.</span></span> <span data-ttu-id="e4539-107">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="e4539-107">See remarks.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4539-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4539-108">Syntax</span></span>


```C++
HRESULT ProcessDeviceWorkItems(
  [in] UINT iWorkItemCount
);
```



## <a name="parameters"></a><span data-ttu-id="e4539-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4539-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4539-110">*iWorkItemCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4539-110">*iWorkItemCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4539-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4539-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4539-112">O número de itens de trabalho a serem definidos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e4539-112">The number of work items to set to the device.</span></span> <span data-ttu-id="e4539-113">ProcessDeviceObjectCreation criará no máximo objetos iWorkItemCount.</span><span class="sxs-lookup"><span data-stu-id="e4539-113">ProcessDeviceObjectCreation will create at most iWorkItemCount objects.</span></span> <span data-ttu-id="e4539-114">Se não houver itens de trabalho suficientes na fila para processar objetos iWorkItemCount, o ProcessDeviceObjectCreation criará tantos objetos de dispositivo quantos houver itens na fila.</span><span class="sxs-lookup"><span data-stu-id="e4539-114">If there are not enough work items in the queue to process iWorkItemCount objects, ProcessDeviceObjectCreation will create as many device objects as there are items in the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4539-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4539-115">Return value</span></span>

<span data-ttu-id="e4539-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e4539-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e4539-117">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e4539-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e4539-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4539-118">Remarks</span></span>

<span data-ttu-id="e4539-119">Como um exemplo de como é possível usar essa API, digamos que você esteja se aproximando do final de um nível em seu jogo e queira começar a carregar as texturas, os sombreadores e outros recursos para o próximo nível.</span><span class="sxs-lookup"><span data-stu-id="e4539-119">As an example of how one might use this API, say you are nearing the end of one level in your game and you want to begin preloading the textures, shaders, and other resources for the next level.</span></span> <span data-ttu-id="e4539-120">A bomba de thread começará a carregar, descompactar e processar os recursos e os sombreadores em um thread separado até que eles estejam prontos para serem definidos para o dispositivo; nesse ponto, eles serão deixados em uma fila.</span><span class="sxs-lookup"><span data-stu-id="e4539-120">The thread pump will begin loading, decompressing, and processing the resources and shaders on a separate thread until they are ready to be set to the device, at which point it will leave them in a queue.</span></span> <span data-ttu-id="e4539-121">Talvez não seja necessário definir todos os recursos e sombreadores para o dispositivo de uma só vez, pois isso pode causar uma lentidão temporária no desempenho do jogo.</span><span class="sxs-lookup"><span data-stu-id="e4539-121">One may not want to set all the resources and shaders to the device at once because this may cause a noticable temporary slow down in the game's performance.</span></span> <span data-ttu-id="e4539-122">Portanto, essa API pode ser chamada uma vez por quadro, de forma que apenas um pequeno número de itens de trabalho seja definido para o dispositivo em cada quadro, distribuindo assim a carga de trabalho dos recursos de associação para o dispositivo em vários quadros e minimizando a possibilidade de um inatividade ser prejudicado no desempenho do jogo.</span><span class="sxs-lookup"><span data-stu-id="e4539-122">So, this API could be called once per frame so that only a small number work items would be set to the device on each frame, thereby spreading the work load of binding resources to the device over several frames and minimizing the possibility of a noticable slow down in the game's performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4539-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4539-123">Requirements</span></span>



| <span data-ttu-id="e4539-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4539-124">Requirement</span></span> | <span data-ttu-id="e4539-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e4539-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4539-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4539-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e4539-127"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4539-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e4539-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e4539-128">Library</span></span><br/> | <dl> <span data-ttu-id="e4539-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4539-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4539-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4539-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4539-131">ID3DX10ThreadPump</span><span class="sxs-lookup"><span data-stu-id="e4539-131">ID3DX10ThreadPump</span></span>](id3dx10threadpump.md)
</dt> <dt>

[<span data-ttu-id="e4539-132">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="e4539-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
