---
title: Códigos de retorno do Direct3D 12
description: Veja a seguir os códigos de retorno das funções de API.
ms.assetid: 5F6CC962-7DB7-489F-82A4-9388313014D3
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd04c0c7702f00f1338ce884adc745522390c8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105810777"
---
# <a name="direct3d-12-return-codes"></a><span data-ttu-id="e7948-103">Códigos de retorno do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e7948-103">Direct3D 12 Return Codes</span></span>

<span data-ttu-id="e7948-104">Veja a seguir os códigos de retorno das funções de API.</span><span class="sxs-lookup"><span data-stu-id="e7948-104">The following are return codes from API functions.</span></span> <span data-ttu-id="e7948-105">Para obter mais códigos de retorno, consulte [ \_ erro dxgi](/windows/desktop/direct3ddxgi/dxgi-error).</span><span class="sxs-lookup"><span data-stu-id="e7948-105">For more return codes, see [DXGI\_ERROR](/windows/desktop/direct3ddxgi/dxgi-error).</span></span>



| <span data-ttu-id="e7948-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="e7948-106">HRESULT</span></span>                                                                  | <span data-ttu-id="e7948-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e7948-107">Description</span></span>                                                                                                           |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7948-108">\_Adaptador de erro D3D12 \_ \_ não \_ encontrado</span><span class="sxs-lookup"><span data-stu-id="e7948-108">D3D12\_ERROR\_ADAPTER\_NOT\_FOUND</span></span>                                        | <span data-ttu-id="e7948-109">O PSO armazenado em cache especificado foi criado em um adaptador diferente e não pode ser reutilizado no adaptador atual.</span><span class="sxs-lookup"><span data-stu-id="e7948-109">The specified cached PSO was created on a different adapter and cannot be reused on the current adapter.</span></span>          |
| <span data-ttu-id="e7948-110">Incompatibilidade de versão do driver de \_ erro D3D12 \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="e7948-110">D3D12\_ERROR\_DRIVER\_VERSION\_MISMATCH</span></span>                                  | <span data-ttu-id="e7948-111">O PSO armazenado em cache especificado foi criado em uma versão de driver diferente e não pode ser reutilizado no adaptador atual.</span><span class="sxs-lookup"><span data-stu-id="e7948-111">The specified cached PSO was created on a different driver version and cannot be reused on the current adapter.</span></span>  |
| <span data-ttu-id="e7948-112">D3DERR \_ INVALIDCALL (substituído pela \_ chamada de erro dxgi \_ inválido \_ )</span><span class="sxs-lookup"><span data-stu-id="e7948-112">D3DERR\_INVALIDCALL (replaced with DXGI\_ERROR\_INVALID\_CALL)</span></span>           | <span data-ttu-id="e7948-113">A chamada do método é inválida.</span><span class="sxs-lookup"><span data-stu-id="e7948-113">The method call is invalid.</span></span> <span data-ttu-id="e7948-114">Por exemplo, o parâmetro de um método não pode ser um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="e7948-114">For example, a method's parameter may not be a valid pointer.</span></span>                             |
| <span data-ttu-id="e7948-115">D3DERR \_ WASSTILLDRAWING (substituído pelo \_ erro dxgi \_ \_ ainda estava \_ desenhando)</span><span class="sxs-lookup"><span data-stu-id="e7948-115">D3DERR\_WASSTILLDRAWING (replaced with DXGI\_ERROR\_WAS\_STILL\_DRAWING)</span></span> | <span data-ttu-id="e7948-116">A operação blit anterior que está transferindo informações para ou desta superfície está incompleta.</span><span class="sxs-lookup"><span data-stu-id="e7948-116">The previous blit operation that is transferring information to or from this surface is incomplete.</span></span>                   |
| <span data-ttu-id="e7948-117">E \_ falha</span><span class="sxs-lookup"><span data-stu-id="e7948-117">E\_FAIL</span></span>                                                                  | <span data-ttu-id="e7948-118">Tentativa de criar um dispositivo com a camada de depuração habilitada e a camada não está instalada.</span><span class="sxs-lookup"><span data-stu-id="e7948-118">Attempted to create a device with the debug layer enabled and the layer is not installed.</span></span>                             |
| <span data-ttu-id="e7948-119">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e7948-119">E\_INVALIDARG</span></span>                                                            | <span data-ttu-id="e7948-120">Um parâmetro inválido foi passado para a função de retorno.</span><span class="sxs-lookup"><span data-stu-id="e7948-120">An invalid parameter was passed to the returning function.</span></span>                                                             |
| <span data-ttu-id="e7948-121">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="e7948-121">E\_OUTOFMEMORY</span></span>                                                           | <span data-ttu-id="e7948-122">O Direct3D não pôde alocar memória suficiente para concluir a chamada.</span><span class="sxs-lookup"><span data-stu-id="e7948-122">Direct3D could not allocate sufficient memory to complete the call.</span></span>                                                   |
| <span data-ttu-id="e7948-123">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="e7948-123">E\_NOTIMPL</span></span>                                                               | <span data-ttu-id="e7948-124">A chamada de método não é implementada com a combinação de parâmetros passada.</span><span class="sxs-lookup"><span data-stu-id="e7948-124">The method call isn't implemented with the passed parameter combination.</span></span>                                               |
| <span data-ttu-id="e7948-125">\_falso</span><span class="sxs-lookup"><span data-stu-id="e7948-125">S\_FALSE</span></span>                                                                 | <span data-ttu-id="e7948-126">Valor de êxito alternativo, indicando uma conclusão bem-sucedida, mas não padrão (o significado preciso depende do contexto).</span><span class="sxs-lookup"><span data-stu-id="e7948-126">Alternate success value, indicating a successful but nonstandard completion (the precise meaning depends on context).</span></span> |
| <span data-ttu-id="e7948-127">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="e7948-127">S\_OK</span></span>                                                                    | <span data-ttu-id="e7948-128">Não ocorreu nenhum erro.</span><span class="sxs-lookup"><span data-stu-id="e7948-128">No error occurred.</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="e7948-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e7948-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7948-130">Referência do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e7948-130">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 