---
description: O método OnActivate é chamado quando a página de propriedades é ativada.
ms.assetid: aff843d4-cfb2-4255-a59c-0579f1cd24bd
title: Método CBasePropertyPage. OnActivate (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnActivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5093cb2ac71e8010bc689e4517b3d8bb758c8436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749843"
---
# <a name="cbasepropertypageonactivate-method"></a><span data-ttu-id="62bb8-103">Método CBasePropertyPage. OnActivate</span><span class="sxs-lookup"><span data-stu-id="62bb8-103">CBasePropertyPage.OnActivate method</span></span>

<span data-ttu-id="62bb8-104">O `OnActivate` método é chamado quando a página de propriedades é ativada.</span><span class="sxs-lookup"><span data-stu-id="62bb8-104">The `OnActivate` method is called when the property page is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="62bb8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62bb8-105">Syntax</span></span>


```C++
virtual HRESULT OnActivate();
```



## <a name="parameters"></a><span data-ttu-id="62bb8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62bb8-106">Parameters</span></span>

<span data-ttu-id="62bb8-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="62bb8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="62bb8-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62bb8-108">Return value</span></span>

<span data-ttu-id="62bb8-109">A implementação da classe base retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="62bb8-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="62bb8-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="62bb8-110">Remarks</span></span>

<span data-ttu-id="62bb8-111">O método [**CBasePropertyPage:: Activate**](cbasepropertypage-activate.md) chama o `OnActivate` método.</span><span class="sxs-lookup"><span data-stu-id="62bb8-111">The [**CBasePropertyPage::Activate**](cbasepropertypage-activate.md) method calls the `OnActivate` method.</span></span> <span data-ttu-id="62bb8-112">Em sua classe derivada, substitua `OnActivate` para inicializar a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="62bb8-112">In your derived class, override `OnActivate` to initialize the dialog box.</span></span>

## <a name="examples"></a><span data-ttu-id="62bb8-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="62bb8-113">Examples</span></span>

<span data-ttu-id="62bb8-114">O exemplo a seguir inicializa um controle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="62bb8-114">The following example initializes a trackbar control.</span></span> <span data-ttu-id="62bb8-115">Este exemplo supõe que **m \_ pOwningFilter** seja um ponteiro para uma interface personalizada no filtro associado à página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="62bb8-115">This example assumes that **m\_pOwningFilter** is a pointer to a custom interface on the filter associated with the property page.</span></span> <span data-ttu-id="62bb8-116">(Use o método [**CBasePropertyPage:: OnConnect**](cbasepropertypage-onconnect.md) para inicializar tais ponteiros.)</span><span class="sxs-lookup"><span data-stu-id="62bb8-116">(Use the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method to initialize such pointers.)</span></span>


```C++
HRESULT CMyProp::OnActivate(void)
{
    ASSERT(m_pOwningFilter != NULL);
    m_pOwningFilter->GetSomeProperty(&m_lOldVal);
    
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETRANGE, 0, MAKELONG(0, 100));
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETTICFREQ, 10, 0);
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1, m_lOldVal);
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="62bb8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62bb8-117">Requirements</span></span>



| <span data-ttu-id="62bb8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="62bb8-118">Requirement</span></span> | <span data-ttu-id="62bb8-119">Valor</span><span class="sxs-lookup"><span data-stu-id="62bb8-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62bb8-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="62bb8-120">Header</span></span><br/>  | <dl> <span data-ttu-id="62bb8-121"><dt>CProp. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62bb8-121"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="62bb8-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62bb8-122">Library</span></span><br/> | <dl> <span data-ttu-id="62bb8-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="62bb8-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62bb8-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="62bb8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62bb8-125">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="62bb8-125">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




