---
description: O \_ método Get Owner recupera o proprietário da janela atual.
ms.assetid: f0eea5e7-4dfa-4973-ae12-487657e6be80
title: Método de CBaseControlWindow.get_Owner (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8f8e3d4a331dbc66397a7b0058fcefcede2cdbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764584"
---
# <a name="cbasecontrolwindowget_owner-method"></a><span data-ttu-id="298ef-103">Método de proprietário CBaseControlWindow. get \_</span><span class="sxs-lookup"><span data-stu-id="298ef-103">CBaseControlWindow.get\_Owner method</span></span>

<span data-ttu-id="298ef-104">O `get_Owner` método recupera o proprietário da janela atual.</span><span class="sxs-lookup"><span data-stu-id="298ef-104">The `get_Owner` method retrieves the current window owner.</span></span>

## <a name="syntax"></a><span data-ttu-id="298ef-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="298ef-105">Syntax</span></span>


```C++
HRESULT get_Owner(
   OAHWND *Owner
);
```



## <a name="parameters"></a><span data-ttu-id="298ef-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="298ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="298ef-107">*Proprietário*</span><span class="sxs-lookup"><span data-stu-id="298ef-107">*Owner*</span></span> 
</dt> <dd>

<span data-ttu-id="298ef-108">Ponteiro para o proprietário da janela.</span><span class="sxs-lookup"><span data-stu-id="298ef-108">Pointer to the window owner.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="298ef-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="298ef-109">Return value</span></span>

<span data-ttu-id="298ef-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="298ef-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="298ef-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="298ef-111">Remarks</span></span>

<span data-ttu-id="298ef-112">A janela de vídeo pode reproduzir em um ambiente de documento.</span><span class="sxs-lookup"><span data-stu-id="298ef-112">The video window can play back within a document environment.</span></span> <span data-ttu-id="298ef-113">Para fazer isso, a janela deve se tornar um filho de outra janela (para que seja recortada e movida adequadamente).</span><span class="sxs-lookup"><span data-stu-id="298ef-113">To do this, the window must be made a child of another window (so that it is clipped and moved appropriately).</span></span> <span data-ttu-id="298ef-114">Essa propriedade permite que o proprietário da janela seja definido e recuperado.</span><span class="sxs-lookup"><span data-stu-id="298ef-114">This property allows the owner of the window to be set and retrieved.</span></span> <span data-ttu-id="298ef-115">Quando a janela pertence a outra janela, ela simplesmente chama a função **setpai** do Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="298ef-115">When the window is owned by another window, it simply calls the Microsoft Win32 **SetParent** function.</span></span> <span data-ttu-id="298ef-116">Um aplicativo que chama essa função alterará os estilos de janela para definir o bit do WS- \_ Child em.</span><span class="sxs-lookup"><span data-stu-id="298ef-116">An application calling this function will change the window styles to set the WS\_CHILD bit on.</span></span>

<span data-ttu-id="298ef-117">Quando a janela pertence a outra janela, ela encaminha automaticamente determinados conjuntos de mensagens (em particular, mensagens do mouse e do teclado).</span><span class="sxs-lookup"><span data-stu-id="298ef-117">When the window is owned by another window, it will automatically forward certain sets of messages (in particular, mouse and keyboard messages).</span></span> <span data-ttu-id="298ef-118">Isso permite que um aplicativo faça uma edição de ponto de acesso simples e outras interações.</span><span class="sxs-lookup"><span data-stu-id="298ef-118">This allows an application to do simple hot-spot editing and other interactions.</span></span>

<span data-ttu-id="298ef-119">Essa função de membro deve ser chamada por objetos externos por meio da interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e, portanto, bloqueia a seção crítica para sincronizar com o filtro associado.</span><span class="sxs-lookup"><span data-stu-id="298ef-119">This member function is meant to be called by external objects through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, and therefore locks the critical section to synchronize with the associated filter.</span></span> <span data-ttu-id="298ef-120">Chame a função de membro [**CBaseControlWindow:: GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md) para recuperar essa propriedade se não estiver chamando de um objeto externo.</span><span class="sxs-lookup"><span data-stu-id="298ef-120">Call the [**CBaseControlWindow::GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md) member function to retrieve this property if not calling from an external object.</span></span>

## <a name="requirements"></a><span data-ttu-id="298ef-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="298ef-121">Requirements</span></span>



| <span data-ttu-id="298ef-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="298ef-122">Requirement</span></span> | <span data-ttu-id="298ef-123">Valor</span><span class="sxs-lookup"><span data-stu-id="298ef-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="298ef-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="298ef-124">Header</span></span><br/>  | <dl> <span data-ttu-id="298ef-125"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="298ef-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="298ef-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="298ef-126">Library</span></span><br/> | <dl> <span data-ttu-id="298ef-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="298ef-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="298ef-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="298ef-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="298ef-129">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="298ef-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




