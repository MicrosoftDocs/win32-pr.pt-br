---
description: O \_ método Put Owner define a janela pai da janela de vídeo; a janela pai, em seguida, encaminha certas mensagens para a janela de vídeo.
ms.assetid: 8ed85cb0-47be-40c1-947a-dd9f7850d867
title: Método de CBaseControlWindow.put_Owner (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16817d1c3f0fbdf756f6c054b875b8507fd1172a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753753"
---
# <a name="cbasecontrolwindowput_owner-method"></a><span data-ttu-id="208e9-103">Método de proprietário CBaseControlWindow. put \_</span><span class="sxs-lookup"><span data-stu-id="208e9-103">CBaseControlWindow.put\_Owner method</span></span>

<span data-ttu-id="208e9-104">O `put_Owner` método define a janela pai da janela de vídeo; a janela pai, em seguida, encaminha certas mensagens para a janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="208e9-104">The `put_Owner` method sets the video window's parent window; the parent window then forwards certain messages to the video window.</span></span>

## <a name="syntax"></a><span data-ttu-id="208e9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="208e9-105">Syntax</span></span>


```C++
HRESULT put_Owner(
   OAHWND Owner
);
```



## <a name="parameters"></a><span data-ttu-id="208e9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="208e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="208e9-107">*Proprietário*</span><span class="sxs-lookup"><span data-stu-id="208e9-107">*Owner*</span></span> 
</dt> <dd>

<span data-ttu-id="208e9-108">Identificador para a janela pai.</span><span class="sxs-lookup"><span data-stu-id="208e9-108">Handle to the parent window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="208e9-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="208e9-109">Return value</span></span>

<span data-ttu-id="208e9-110">Retorna NOERROR.</span><span class="sxs-lookup"><span data-stu-id="208e9-110">Returns NOERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="208e9-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="208e9-111">Remarks</span></span>

<span data-ttu-id="208e9-112">Internamente, esse método chama a função **Setpai** do Microsoft Win32 para definir o novo proprietário e define o estilo da janela pai como WS \_ Child.</span><span class="sxs-lookup"><span data-stu-id="208e9-112">Internally, this method calls the Microsoft Win32 **SetParent** function to set the new owner and sets the parent window's style to WS\_CHILD.</span></span> <span data-ttu-id="208e9-113">A janela pai encaminhará certos conjuntos de mensagens (em particular, mensagens do mouse e do teclado) para a janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="208e9-113">The parent window will then forward certain sets of messages (in particular, mouse and keyboard messages) to the video window.</span></span>

<span data-ttu-id="208e9-114">Depois de definir o proprietário da janela de vídeo, você deve definir o proprietário como **nulo** e o estilo de janela do proprietário como WS \_ Overlapped e WS \_ CLIPCHILDREN antes de liberar o grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="208e9-114">After you set the video window's owner, you must set the owner to **NULL** and the owner's window style to WS\_OVERLAPPED and WS\_CLIPCHILDREN before releasing the filter graph.</span></span> <span data-ttu-id="208e9-115">Quando você define o proprietário como **NULL**, esse método desativa o bit do WS-Child da janela pai \_ .</span><span class="sxs-lookup"><span data-stu-id="208e9-115">When you set the owner to **NULL**, this method turns off the parent window's WS\_CHILD bit.</span></span> <span data-ttu-id="208e9-116">Se você não definir o proprietário como **nulo**, a janela pai continuará a passar mensagens para a janela de vídeo e os erros provavelmente ocorrerão quando o aplicativo for fechado.</span><span class="sxs-lookup"><span data-stu-id="208e9-116">If you don't set the owner to **NULL**, the parent window will continue to pass messages to the video window and errors will likely occur when the application closes.</span></span>

## <a name="requirements"></a><span data-ttu-id="208e9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="208e9-117">Requirements</span></span>



| <span data-ttu-id="208e9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="208e9-118">Requirement</span></span> | <span data-ttu-id="208e9-119">Valor</span><span class="sxs-lookup"><span data-stu-id="208e9-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="208e9-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="208e9-120">Header</span></span><br/>  | <dl> <span data-ttu-id="208e9-121"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="208e9-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="208e9-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="208e9-122">Library</span></span><br/> | <dl> <span data-ttu-id="208e9-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="208e9-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="208e9-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="208e9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="208e9-125">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="208e9-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




