---
description: O método GetClassWindowStyles recupera estilos de classe e estilos de janela da janela.
ms.assetid: 6eec7912-c654-4e4f-b6f1-ec94c7284575
title: Método CBaseWindow. GetClassWindowStyles (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetClassWindowStyles
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a34332f84a91ee88d61ee5f29f0b6a0b0cc44714
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758700"
---
# <a name="cbasewindowgetclasswindowstyles-method"></a><span data-ttu-id="0e0d8-103">Método CBaseWindow. GetClassWindowStyles</span><span class="sxs-lookup"><span data-stu-id="0e0d8-103">CBaseWindow.GetClassWindowStyles method</span></span>

<span data-ttu-id="0e0d8-104">O `GetClassWindowStyles` método recupera estilos de classe e estilos de janela da janela.</span><span class="sxs-lookup"><span data-stu-id="0e0d8-104">The `GetClassWindowStyles` method retrieves the window's class styles and window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e0d8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e0d8-105">Syntax</span></span>


```C++
virtual LPTSTR GetClassWindowStyles(
   DWORD *pClassStyles,
   DWORD *pWindowStyles,
   DWORD *pWindowStylesEx
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="0e0d8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e0d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e0d8-107">*pClassStyles*</span><span class="sxs-lookup"><span data-stu-id="0e0d8-107">*pClassStyles*</span></span> 
</dt> <dd>

<span data-ttu-id="0e0d8-108">Ponteiro para uma variável que recebe os estilos de classe.</span><span class="sxs-lookup"><span data-stu-id="0e0d8-108">Pointer to a variable that receives the class styles.</span></span>

</dd> <dt>

<span data-ttu-id="0e0d8-109">*pWindowStyles*</span><span class="sxs-lookup"><span data-stu-id="0e0d8-109">*pWindowStyles*</span></span> 
</dt> <dd>

<span data-ttu-id="0e0d8-110">Ponteiro para uma variável que recebe os estilos de janela.</span><span class="sxs-lookup"><span data-stu-id="0e0d8-110">Pointer to a variable that receives the window styles.</span></span>

</dd> <dt>

<span data-ttu-id="0e0d8-111">*pWindowStylesEx*</span><span class="sxs-lookup"><span data-stu-id="0e0d8-111">*pWindowStylesEx*</span></span> 
</dt> <dd>

<span data-ttu-id="0e0d8-112">Ponteiro para uma variável que recebe os estilos de janela estendida.</span><span class="sxs-lookup"><span data-stu-id="0e0d8-112">Pointer to a variable that receives the extended window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e0d8-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0e0d8-113">Return value</span></span>

<span data-ttu-id="0e0d8-114">Retorna uma cadeia de texto estática que contém o nome da classe.</span><span class="sxs-lookup"><span data-stu-id="0e0d8-114">Returns a static text string that contains the class name.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e0d8-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e0d8-115">Remarks</span></span>

<span data-ttu-id="0e0d8-116">O método [**CBaseWindow::P reparewindow**](cbasewindow-preparewindow.md) chama esse método para recuperar os estilos de classe da janela e os estilos de janela.</span><span class="sxs-lookup"><span data-stu-id="0e0d8-116">The [**CBaseWindow::PrepareWindow**](cbasewindow-preparewindow.md) method calls this method to retrieve the window's class styles and window styles.</span></span>

<span data-ttu-id="0e0d8-117">Este método é virtual puro; a classe derivada deve implementá-la.</span><span class="sxs-lookup"><span data-stu-id="0e0d8-117">This method is pure virtual; the derived class must implement it.</span></span> <span data-ttu-id="0e0d8-118">O exemplo a seguir mostra uma possível implementação:</span><span class="sxs-lookup"><span data-stu-id="0e0d8-118">The following example shows a possible implementation:</span></span>


```C++
LPTSTR CMyWindowClass::GetClassWindowStyles(DWORD *pClassStyles,
                                            DWORD *pWindowStyles,
                                            DWORD *pWindowStylesEx)
{
    *pClassStyles = CS_HREDRAW | CS_VREDRAW;
    *pWindowStyles = WS_OVERLAPPEDWINDOW | WS_CLIPCHILDREN;
    *pWindowStylesEx = WS_EX_WINDOWEDGE;
    return TEXT("MyWindowClass");
}
```



<span data-ttu-id="0e0d8-119">O objeto usa o estilo de classe para o membro **lpszClassName** de uma estrutura WNDCLASS, que ele passa para a função **registerClass** .</span><span class="sxs-lookup"><span data-stu-id="0e0d8-119">The object uses the class style for the **lpszClassName** member of a WNDCLASS structure, which it passes to the **RegisterClass** function.</span></span> <span data-ttu-id="0e0d8-120">O objeto usa os estilos de janela para os parâmetros *dwExStyle* e *DwStyle* da função **CreateWindowEx** .</span><span class="sxs-lookup"><span data-stu-id="0e0d8-120">The object uses the window styles for the *dwExStyle* and *dwStyle* parameters of the **CreateWindowEx** function.</span></span> <span data-ttu-id="0e0d8-121">Para obter mais informações, consulte o SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="0e0d8-121">For more information, see the Platform SDK.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e0d8-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e0d8-122">Requirements</span></span>



| <span data-ttu-id="0e0d8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e0d8-123">Requirement</span></span> | <span data-ttu-id="0e0d8-124">Valor</span><span class="sxs-lookup"><span data-stu-id="0e0d8-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e0d8-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0e0d8-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0e0d8-126"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e0d8-126"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0e0d8-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0e0d8-127">Library</span></span><br/> | <dl> <span data-ttu-id="0e0d8-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0e0d8-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e0d8-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e0d8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e0d8-130">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="0e0d8-130">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




