---
description: A tabela a seguir contém códigos de retorno de funções de API.
ms.assetid: 7b67d428-d000-4c3e-adc1-b5fc67a15a6a
title: Códigos de retorno do Direct3D 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15a2fcdc4db5bd2d295b7cd3078ed80d401ce52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789422"
---
# <a name="direct3d-10-return-codes"></a><span data-ttu-id="e8dc9-103">Códigos de retorno do Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="e8dc9-103">Direct3D 10 Return Codes</span></span>

<span data-ttu-id="e8dc9-104">A tabela a seguir contém códigos de retorno de funções de API.</span><span class="sxs-lookup"><span data-stu-id="e8dc9-104">The following table contains return codes from API functions.</span></span>



| <span data-ttu-id="e8dc9-105">HRESULT</span><span class="sxs-lookup"><span data-stu-id="e8dc9-105">HRESULT</span></span>                                         | <span data-ttu-id="e8dc9-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="e8dc9-106">Description</span></span>                                                                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8dc9-107">\_Arquivo de erro d3d10 \_ \_ não \_ encontrado</span><span class="sxs-lookup"><span data-stu-id="e8dc9-107">D3D10\_ERROR\_FILE\_NOT\_FOUND</span></span>                  | <span data-ttu-id="e8dc9-108">O arquivo não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="e8dc9-108">The file was not found.</span></span>                                                                                                                               |
| <span data-ttu-id="e8dc9-109">Erro D3D10 em \_ \_ excesso de \_ \_ \_ objetos de estado exclusivos \_</span><span class="sxs-lookup"><span data-stu-id="e8dc9-109">D3D10\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS</span></span> | <span data-ttu-id="e8dc9-110">Há muitas instâncias exclusivas de um tipo específico de [objeto de estado](d3d10-graphics-programming-guide-api-features-state-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e8dc9-110">There are too many unique instances of a particular type of [state object](d3d10-graphics-programming-guide-api-features-state-objects.md).</span></span>          |
| <span data-ttu-id="e8dc9-111">D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="e8dc9-111">D3DERR\_INVALIDCALL</span></span>                             | <span data-ttu-id="e8dc9-112">A chamada do método é inválida.</span><span class="sxs-lookup"><span data-stu-id="e8dc9-112">The method call is invalid.</span></span> <span data-ttu-id="e8dc9-113">Por exemplo, o parâmetro de um método não pode ser um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="e8dc9-113">For example, a method's parameter may not be a valid pointer.</span></span>                                                             |
| <span data-ttu-id="e8dc9-114">D3DERR \_ WASSTILLDRAWING</span><span class="sxs-lookup"><span data-stu-id="e8dc9-114">D3DERR\_WASSTILLDRAWING</span></span>                         | <span data-ttu-id="e8dc9-115">A operação blit anterior que está transferindo informações para ou desta superfície está incompleta.</span><span class="sxs-lookup"><span data-stu-id="e8dc9-115">The previous blit operation that is transferring information to or from this surface is incomplete.</span></span>                                                   |
| <span data-ttu-id="e8dc9-116">E \_ falha</span><span class="sxs-lookup"><span data-stu-id="e8dc9-116">E\_FAIL</span></span>                                         | <span data-ttu-id="e8dc9-117">Tentativa de criar um dispositivo com a [camada de depuração](d3d10-graphics-programming-guide-api-features-layers.md) habilitada e a camada não está instalada.</span><span class="sxs-lookup"><span data-stu-id="e8dc9-117">Attempted to create a device with the [debug layer](d3d10-graphics-programming-guide-api-features-layers.md) enabled and the layer is not installed.</span></span> |
| <span data-ttu-id="e8dc9-118">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e8dc9-118">E\_INVALIDARG</span></span>                                   | <span data-ttu-id="e8dc9-119">Um parâmetro inválido foi passado para a função de retorno.</span><span class="sxs-lookup"><span data-stu-id="e8dc9-119">An invalid parameter was passed to the returning function.</span></span>                                                                                            |
| <span data-ttu-id="e8dc9-120">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="e8dc9-120">E\_OUTOFMEMORY</span></span>                                  | <span data-ttu-id="e8dc9-121">O Direct3D não pôde alocar memória suficiente para concluir a chamada.</span><span class="sxs-lookup"><span data-stu-id="e8dc9-121">Direct3D could not allocate sufficient memory to complete the call.</span></span>                                                                                   |
| <span data-ttu-id="e8dc9-122">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="e8dc9-122">E\_NOTIMPL</span></span>                                      | <span data-ttu-id="e8dc9-123">A chamada de método não é implementada com a combinação de parâmetros passada.</span><span class="sxs-lookup"><span data-stu-id="e8dc9-123">The method call isn't implemented with the passed parameter combination.</span></span>                                                                              |
| <span data-ttu-id="e8dc9-124">\_falso</span><span class="sxs-lookup"><span data-stu-id="e8dc9-124">S\_FALSE</span></span>                                        | <span data-ttu-id="e8dc9-125">Valor de êxito alternativo, indicando uma conclusão bem-sucedida, mas não padrão (o significado preciso depende do contexto).</span><span class="sxs-lookup"><span data-stu-id="e8dc9-125">Alternate success value, indicating a successful but nonstandard completion (the precise meaning depends on context).</span></span>                                 |
| <span data-ttu-id="e8dc9-126">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="e8dc9-126">S\_OK</span></span>                                           | <span data-ttu-id="e8dc9-127">Não ocorreu nenhum erro.</span><span class="sxs-lookup"><span data-stu-id="e8dc9-127">No error occurred.</span></span>                                                                                                                                    |



 

<span data-ttu-id="e8dc9-128">Para escrever código que manipula [valores HRESULT](../winprog/windows-data-types.md) de robustez, use as macros com êxito (HR) e com falha (HR).</span><span class="sxs-lookup"><span data-stu-id="e8dc9-128">To write code that handles [HRESULT values](../winprog/windows-data-types.md) robustly, use the SUCCEEDED(hr) and FAILED(hr) macros.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8dc9-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e8dc9-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8dc9-130">Referência do Direct3D</span><span class="sxs-lookup"><span data-stu-id="e8dc9-130">Direct3D Reference</span></span>](d3d10-graphics-reference-d3d10.md)
</dt> <dt>

[<span data-ttu-id="e8dc9-131">Referência para Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="e8dc9-131">Reference for Direct3D 10</span></span>](d3d10-graphics-reference.md)
</dt> </dl>

 

 
