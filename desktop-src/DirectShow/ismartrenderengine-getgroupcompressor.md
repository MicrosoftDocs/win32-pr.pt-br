---
description: O método GetGroupCompressor recupera o filtro de compactação para o grupo especificado.
ms.assetid: 9d71e659-7abb-48c6-b9bd-5239560dc150
title: 'Método ISmartRenderEngine:: GetGroupCompressor (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine.GetGroupCompressor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd866daa225ab398e1a578aa8d21e73bad15e96d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754757"
---
# <a name="ismartrenderenginegetgroupcompressor-method"></a><span data-ttu-id="6698d-103">Método ISmartRenderEngine:: GetGroupCompressor</span><span class="sxs-lookup"><span data-stu-id="6698d-103">ISmartRenderEngine::GetGroupCompressor method</span></span>

> [!Note]  
> <span data-ttu-id="6698d-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="6698d-104">\[Deprecated.</span></span> <span data-ttu-id="6698d-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6698d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6698d-106">O `GetGroupCompressor` método recupera o filtro de compactação para o grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="6698d-106">The `GetGroupCompressor` method retrieves the compression filter for the specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="6698d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6698d-107">Syntax</span></span>


```C++
HRESULT GetGroupCompressor(
   long        Group,
   IBaseFilter **pCompressor
);
```



## <a name="parameters"></a><span data-ttu-id="6698d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6698d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6698d-109">*Grupo*</span><span class="sxs-lookup"><span data-stu-id="6698d-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="6698d-110">Índice de base zero do grupo.</span><span class="sxs-lookup"><span data-stu-id="6698d-110">Zero-based index of the group.</span></span>

</dd> <dt>

<span data-ttu-id="6698d-111">*pCompressor*</span><span class="sxs-lookup"><span data-stu-id="6698d-111">*pCompressor*</span></span> 
</dt> <dd>

<span data-ttu-id="6698d-112">Recebe um ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do filtro de compactação.</span><span class="sxs-lookup"><span data-stu-id="6698d-112">Receives a pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the compression filter.</span></span> <span data-ttu-id="6698d-113">Ele receberá o valor **NULL** se não houver nenhum filtro de compactação.</span><span class="sxs-lookup"><span data-stu-id="6698d-113">It receives the value **NULL** if there is no compression filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6698d-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6698d-114">Return value</span></span>

<span data-ttu-id="6698d-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6698d-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6698d-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6698d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6698d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6698d-117">Remarks</span></span>

<span data-ttu-id="6698d-118">Use esse método para definir propriedades no filtro de compactação, como a taxa de quadros-chave.</span><span class="sxs-lookup"><span data-stu-id="6698d-118">Use this method to set properties on the compression filter, such as the key-frame rate.</span></span> <span data-ttu-id="6698d-119">Chame esse método depois de chamar [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md), mas antes de renderizar o projeto.</span><span class="sxs-lookup"><span data-stu-id="6698d-119">Call this method after calling [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md), but before rendering the project.</span></span> <span data-ttu-id="6698d-120">Em seguida, consulte o pino de saída do filtro de compactação para a interface [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) , que contém métodos para definir parâmetros de compactação.</span><span class="sxs-lookup"><span data-stu-id="6698d-120">Then query the compression filter's output pin for the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface, which contains methods for setting compression parameters.</span></span> <span data-ttu-id="6698d-121">Libere a interface quando terminar.</span><span class="sxs-lookup"><span data-stu-id="6698d-121">Release the interface when you are done.</span></span> <span data-ttu-id="6698d-122">Se você fizer alterações subsequentes na linha do tempo, chame **ConnectFrontEnd** e chame **GetGroupCompressor** novamente para redefinir os parâmetros de compactação.</span><span class="sxs-lookup"><span data-stu-id="6698d-122">If you make any subsequent changes to the timeline, call **ConnectFrontEnd**, and then call **GetGroupCompressor** again to reset the compression parameters.</span></span>

<span data-ttu-id="6698d-123">No retorno, se o valor de \* *pCompressor* for não **nulo**, a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="6698d-123">On return, if the value of \**pCompressor* is non-**NULL**, the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface has an outstanding reference count.</span></span> <span data-ttu-id="6698d-124">Certifique-se de liberar a interface quando terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="6698d-124">Be sure to release the interface when you are done using it.</span></span>

> [!Note]  
> <span data-ttu-id="6698d-125">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="6698d-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6698d-126">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6698d-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6698d-127">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6698d-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6698d-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6698d-128">Requirements</span></span>



| <span data-ttu-id="6698d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6698d-129">Requirement</span></span> | <span data-ttu-id="6698d-130">Valor</span><span class="sxs-lookup"><span data-stu-id="6698d-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6698d-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6698d-131">Header</span></span><br/>  | <dl> <span data-ttu-id="6698d-132"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6698d-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6698d-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6698d-133">Library</span></span><br/> | <dl> <span data-ttu-id="6698d-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6698d-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6698d-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="6698d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6698d-136">**Interface ISmartRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="6698d-136">**ISmartRenderEngine Interface**</span></span>](ismartrenderengine.md)
</dt> <dt>

[<span data-ttu-id="6698d-137">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="6698d-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




