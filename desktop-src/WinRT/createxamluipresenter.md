---
description: Uma função de criador estática que pode criar um XamlUIPresenter para uma superfície de renderização em um aplicativo de área de trabalho.
ms.assetid: 3160E4C2-39D3-8FF5-ED37-78E645D1AC2E
title: Função CreateXamlUIPresenter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateXamlUIPresenter
api_type:
- DllExport
api_location:
- Windows.UI.Xaml.dll
ms.openlocfilehash: f9561a179ec4501406e26cb2bbc38ea69b64b979
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761579"
---
# <a name="createxamluipresenter-function"></a><span data-ttu-id="3b4a8-103">Função CreateXamlUIPresenter</span><span class="sxs-lookup"><span data-stu-id="3b4a8-103">CreateXamlUIPresenter function</span></span>

<span data-ttu-id="3b4a8-104">Uma função de criador estática que pode criar um [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) para uma superfície de renderização em um aplicativo de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3b4a8-104">A static creator function that can create a [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) for a render surface in a desktop app.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b4a8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b4a8-105">Syntax</span></span>


```C++
 static HRESULT WINAPI CreateXamlUIPresenter(
  _In_  IViewObjectPresentNotifySite                 *pPresentSite,
  _Out_ Windows::UI::Xaml::Hosting::IXamlUIPresenter **ppPresenter
);
```



## <a name="parameters"></a><span data-ttu-id="3b4a8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b4a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b4a8-107">*pPresentSite* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b4a8-107">*pPresentSite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b4a8-108">Uma interface de hospedagem existente.</span><span class="sxs-lookup"><span data-stu-id="3b4a8-108">An existing hosting interface.</span></span> <span data-ttu-id="3b4a8-109">Consulte **IViewObjectPresentNotifySite** na documentação do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="3b4a8-109">See **IViewObjectPresentNotifySite** in Internet Explorer documentation.</span></span>

</dd> <dt>

<span data-ttu-id="3b4a8-110">*ppPresenter* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3b4a8-110">*ppPresenter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b4a8-111">A interface **\[ \] exclusiveto** para um [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041).</span><span class="sxs-lookup"><span data-stu-id="3b4a8-111">The **\[exclusiveto\]** interface for a [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b4a8-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3b4a8-112">Return value</span></span>

<span data-ttu-id="3b4a8-113">Um **HRESULT** padrão, **S \_ OK** para sucesso.</span><span class="sxs-lookup"><span data-stu-id="3b4a8-113">A standard **HResult**, **S\_OK** for success.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b4a8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b4a8-114">Remarks</span></span>

<span data-ttu-id="3b4a8-115">Chamar esse método requer um **DllImport** de Windows.UI.Xaml.dll.</span><span class="sxs-lookup"><span data-stu-id="3b4a8-115">Calling this method requires a **DllImport** from Windows.UI.Xaml.dll.</span></span>

<span data-ttu-id="3b4a8-116">Você não pode chamar esse método de um aplicativo da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="3b4a8-116">You cannot call this method from a Windows Store app.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b4a8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b4a8-117">Requirements</span></span>



| <span data-ttu-id="3b4a8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b4a8-118">Requirement</span></span> | <span data-ttu-id="3b4a8-119">Valor</span><span class="sxs-lookup"><span data-stu-id="3b4a8-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b4a8-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3b4a8-120">Header</span></span><br/> | <dl> <span data-ttu-id="3b4a8-121"><dt>Windows. UI. XAML-coretypes. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3b4a8-121"><dt>Windows.ui.xaml-coretypes.idl</dt></span></span> </dl> |
| <span data-ttu-id="3b4a8-122">DLL</span><span class="sxs-lookup"><span data-stu-id="3b4a8-122">DLL</span></span><br/>    | <dl> <span data-ttu-id="3b4a8-123"><dt>Windows.UI.Xaml.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b4a8-123"><dt>Windows.UI.Xaml.dll</dt></span></span> </dl>           |



## <a name="see-also"></a><span data-ttu-id="3b4a8-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b4a8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b4a8-125">**XamlUIPresenter**</span><span class="sxs-lookup"><span data-stu-id="3b4a8-125">**XamlUIPresenter**</span></span>](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041)
</dt> </dl>

 

 
