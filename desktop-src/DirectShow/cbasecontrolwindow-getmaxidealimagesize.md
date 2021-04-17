---
description: O método GetMaxIdealImageSize recupera o tamanho máximo de imagem ideal.
ms.assetid: 881c1c3d-7505-44a2-964d-3255e2072f6b
title: Método CBaseControlWindow. GetMaxIdealImageSize (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetMaxIdealImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc8ac53dd30c62f3ebb50585677f83f356b593f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748835"
---
# <a name="cbasecontrolwindowgetmaxidealimagesize-method"></a><span data-ttu-id="a0f1e-103">Método CBaseControlWindow. GetMaxIdealImageSize</span><span class="sxs-lookup"><span data-stu-id="a0f1e-103">CBaseControlWindow.GetMaxIdealImageSize method</span></span>

<span data-ttu-id="a0f1e-104">O `GetMaxIdealImageSize` método recupera o tamanho máximo de imagem ideal.</span><span class="sxs-lookup"><span data-stu-id="a0f1e-104">The `GetMaxIdealImageSize` method retrieves the maximum ideal image size.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0f1e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0f1e-105">Syntax</span></span>


```C++
HRESULT GetMaxIdealImageSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="a0f1e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0f1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0f1e-107">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="a0f1e-107">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="a0f1e-108">Ponteiro para a largura máxima ideal, em pixels.</span><span class="sxs-lookup"><span data-stu-id="a0f1e-108">Pointer to the maximum ideal width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="a0f1e-109">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="a0f1e-109">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="a0f1e-110">Ponteiro para a altura ideal máxima, em pixels.</span><span class="sxs-lookup"><span data-stu-id="a0f1e-110">Pointer to the maximum ideal height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0f1e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a0f1e-111">Return value</span></span>

<span data-ttu-id="a0f1e-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a0f1e-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0f1e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0f1e-113">Remarks</span></span>

<span data-ttu-id="a0f1e-114">Vários renderizadores têm restrições de desempenho quanto ao tamanho das imagens que podem ser exibidas.</span><span class="sxs-lookup"><span data-stu-id="a0f1e-114">Various renderers have performance restrictions on the size of images they can display.</span></span> <span data-ttu-id="a0f1e-115">Embora eles ainda devam funcionar corretamente quando solicitados a exibir imagens maiores do que o máximo especificado, os renderizadores podem indicar os tamanhos ideais mínimo e máximo por meio da interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="a0f1e-115">Although they should still function properly when requested to display images larger than the specified maximum, renderers can nominate the minimum and maximum ideal sizes through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="a0f1e-116">Essa interface pode ser chamada somente quando o grafo de filtro é pausado ou está em execução, porque não é até que os recursos sejam alocados e o renderizador possa reconhecer suas restrições.</span><span class="sxs-lookup"><span data-stu-id="a0f1e-116">This interface can be called only when the filter graph is paused or running, because it is not until then that resources are allocated and the renderer can recognize its restrictions.</span></span> <span data-ttu-id="a0f1e-117">Se não houver restrições, o renderizador preencherá os parâmetros *pWidth* e *pHeight* com as dimensões de vídeo nativa e retornará S \_ false.</span><span class="sxs-lookup"><span data-stu-id="a0f1e-117">If no restrictions exist, the renderer fills in the *pWidth* and *pHeight* parameters with the native video dimensions and returns S\_FALSE.</span></span> <span data-ttu-id="a0f1e-118">Se houver restrições, a largura e a altura restritas serão inseridas e a função de membro retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a0f1e-118">If restrictions do exist, the restricted width and height are entered, and the member function returns S\_OK.</span></span>

<span data-ttu-id="a0f1e-119">As dimensões se aplicam ao tamanho do vídeo de destino e não ao tamanho geral da janela.</span><span class="sxs-lookup"><span data-stu-id="a0f1e-119">The dimensions apply to the size of the destination video and not to the overall window size.</span></span> <span data-ttu-id="a0f1e-120">Portanto, ao calcular o tamanho da janela a ser definida, a conta para os estilos de janela atuais (por exemplo, WS \_ Caption e WS \_ Border).</span><span class="sxs-lookup"><span data-stu-id="a0f1e-120">So, when calculating the size of the window to set, account for the current window styles (for example, WS\_CAPTION and WS\_BORDER).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0f1e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0f1e-121">Requirements</span></span>



| <span data-ttu-id="a0f1e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0f1e-122">Requirement</span></span> | <span data-ttu-id="a0f1e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a0f1e-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0f1e-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a0f1e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a0f1e-125"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0f1e-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a0f1e-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a0f1e-126">Library</span></span><br/> | <dl> <span data-ttu-id="a0f1e-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a0f1e-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0f1e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0f1e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0f1e-129">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="a0f1e-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




