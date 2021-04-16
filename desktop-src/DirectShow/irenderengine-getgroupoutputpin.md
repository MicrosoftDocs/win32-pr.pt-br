---
description: O método GetGroupOutputPin recupera o pino de saída para o grupo especificado.
ms.assetid: be4e17b6-15bf-43b1-8d93-d52d08c8bce6
title: 'Método IRenderEngine:: GetGroupOutputPin (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetGroupOutputPin
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 21e603e15f598c6d493e179a147391cb941a6c7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757673"
---
# <a name="irenderenginegetgroupoutputpin-method"></a><span data-ttu-id="54092-103">Método IRenderEngine:: GetGroupOutputPin</span><span class="sxs-lookup"><span data-stu-id="54092-103">IRenderEngine::GetGroupOutputPin method</span></span>

> [!Note]  
> <span data-ttu-id="54092-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="54092-104">\[Deprecated.</span></span> <span data-ttu-id="54092-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="54092-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="54092-106">O `GetGroupOutputPin` método recupera o pino de saída para o grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="54092-106">The `GetGroupOutputPin` method retrieves the output pin for the specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="54092-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="54092-107">Syntax</span></span>


```C++
HRESULT GetGroupOutputPin(
        long Group,
  [out] IPin **ppRenderPin
);
```



## <a name="parameters"></a><span data-ttu-id="54092-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54092-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54092-109">*Grupo*</span><span class="sxs-lookup"><span data-stu-id="54092-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="54092-110">Índice de base zero que especifica o grupo.</span><span class="sxs-lookup"><span data-stu-id="54092-110">Zero-based index that specifies the group.</span></span>

</dd> <dt>

<span data-ttu-id="54092-111">*ppRenderPin* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="54092-111">*ppRenderPin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54092-112">Recebe um ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de saída.</span><span class="sxs-lookup"><span data-stu-id="54092-112">Receives a pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54092-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="54092-113">Return value</span></span>

<span data-ttu-id="54092-114">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="54092-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="54092-115">Os possíveis valores incluem os seguintes:</span><span class="sxs-lookup"><span data-stu-id="54092-115">Possible values include the following:</span></span>



| <span data-ttu-id="54092-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="54092-116">Return code</span></span>                                                                                                  | <span data-ttu-id="54092-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="54092-117">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="54092-118"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="54092-118"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="54092-119">O grupo não tem um pino de saída.</span><span class="sxs-lookup"><span data-stu-id="54092-119">Group does not have an output pin.</span></span><br/>                              |
| <dl> <span data-ttu-id="54092-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="54092-120"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="54092-121">Êxito.</span><span class="sxs-lookup"><span data-stu-id="54092-121">Success.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="54092-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="54092-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                 | <span data-ttu-id="54092-123">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="54092-123">Invalid argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="54092-124"><dt>**E \_ deve \_ iniciar o \_ renderizador**</dt></span><span class="sxs-lookup"><span data-stu-id="54092-124"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl>       | <span data-ttu-id="54092-125">Falha ao inicializar o mecanismo de renderização.</span><span class="sxs-lookup"><span data-stu-id="54092-125">Render engine failed to initialize.</span></span><br/>                             |
| <dl> <span data-ttu-id="54092-126"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="54092-126"><dt>**E\_POINTER**</dt></span></span> </dl>                    | <span data-ttu-id="54092-127">Ponteiro inválido.</span><span class="sxs-lookup"><span data-stu-id="54092-127">Invalid pointer.</span></span><br/>                                                |
| <dl> <span data-ttu-id="54092-128"><dt>**o \_ mecanismo de renderização E \_ \_ está \_ desfeito**</dt></span><span class="sxs-lookup"><span data-stu-id="54092-128"><dt>**E\_RENDER\_ENGINE\_IS\_BROKEN**</dt></span></span> </dl> | <span data-ttu-id="54092-129">Falha na operação porque o projeto não foi renderizado com êxito.</span><span class="sxs-lookup"><span data-stu-id="54092-129">Operation failed because project was not rendered successfully.</span></span><br/> |
| <dl> <span data-ttu-id="54092-130"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="54092-130"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>                 | <span data-ttu-id="54092-131">Erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="54092-131">Unexpected error.</span></span><br/>                                               |



 

## <a name="remarks"></a><span data-ttu-id="54092-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="54092-132">Remarks</span></span>

<span data-ttu-id="54092-133">Antes de chamar esse método, chame [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) para criar o front-end do grafo.</span><span class="sxs-lookup"><span data-stu-id="54092-133">Before calling this method, call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) to build the front end of the graph.</span></span> <span data-ttu-id="54092-134">Cada grupo representa um único fluxo de mídia e o front-end tem um pino de saída correspondente.</span><span class="sxs-lookup"><span data-stu-id="54092-134">Each group represents a single media stream, and the front end has a corresponding output pin.</span></span>

<span data-ttu-id="54092-135">Você pode usar esse método para criar a parte de renderização de um grafo de gravação de arquivos.</span><span class="sxs-lookup"><span data-stu-id="54092-135">You can use this method to create the rendering portion of a file-writing graph.</span></span> <span data-ttu-id="54092-136">Conecte os Pins de saída aos filtros do Multiplexador e aos filtros do gravador de arquivo.</span><span class="sxs-lookup"><span data-stu-id="54092-136">Connect the output pins to multiplexer filters and file writer filters.</span></span> <span data-ttu-id="54092-137">Para obter mais informações, consulte [renderizando um projeto](rendering-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="54092-137">For more information, see [Rendering a Project](rendering-a-project.md).</span></span>

<span data-ttu-id="54092-138">Para visualização, você não precisa chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="54092-138">For preview, you don't need to call this method.</span></span> <span data-ttu-id="54092-139">Basta chamar **ConnectFrontEnd** seguido de [**IRenderEngine:: RenderOutputPins**](irenderengine-renderoutputpins.md).</span><span class="sxs-lookup"><span data-stu-id="54092-139">Just call **ConnectFrontEnd** followed by [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md).</span></span>

<span data-ttu-id="54092-140">Se o método retornar S \_ OK, a interface **IPin** que ele retornar terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="54092-140">If the method returns S\_OK, the **IPin** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="54092-141">Certifique-se de liberar a interface quando terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="54092-141">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="54092-142">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="54092-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="54092-143">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="54092-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="54092-144">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="54092-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="54092-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54092-145">Requirements</span></span>



| <span data-ttu-id="54092-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="54092-146">Requirement</span></span> | <span data-ttu-id="54092-147">Valor</span><span class="sxs-lookup"><span data-stu-id="54092-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54092-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="54092-148">Header</span></span><br/>  | <dl> <span data-ttu-id="54092-149"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="54092-149"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="54092-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="54092-150">Library</span></span><br/> | <dl> <span data-ttu-id="54092-151"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54092-151"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54092-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="54092-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54092-153">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="54092-153">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="54092-154">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="54092-154">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




