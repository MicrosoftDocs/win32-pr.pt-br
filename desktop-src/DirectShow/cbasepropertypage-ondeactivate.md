---
description: O método OnActivate é chamado quando a janela da caixa de diálogo é destruída.
ms.assetid: 47320e61-324f-4f64-abe1-38fe70e82787
title: Método CBasePropertyPage. Deactivate (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDeactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27191e4895c911d3d13a795306eee2b0ad6989ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811753"
---
# <a name="cbasepropertypageondeactivate-method"></a><span data-ttu-id="3d2db-103">Método CBasePropertyPage. Deactivate</span><span class="sxs-lookup"><span data-stu-id="3d2db-103">CBasePropertyPage.OnDeactivate method</span></span>

<span data-ttu-id="3d2db-104">O `OnDeactivate` método é chamado quando a janela da caixa de diálogo é destruída.</span><span class="sxs-lookup"><span data-stu-id="3d2db-104">The `OnDeactivate` method is called when the dialog box window is destroyed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d2db-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d2db-105">Syntax</span></span>


```C++
virtual HRESULT OnDeactivate();
```



## <a name="parameters"></a><span data-ttu-id="3d2db-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d2db-106">Parameters</span></span>

<span data-ttu-id="3d2db-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3d2db-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3d2db-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3d2db-108">Return value</span></span>

<span data-ttu-id="3d2db-109">A implementação da classe base retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3d2db-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d2db-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d2db-110">Remarks</span></span>

<span data-ttu-id="3d2db-111">O método [**CBasePropertyPage::D eactivate**](cbasepropertypage-deactivate.md) chama o `OnDeactivate` método.</span><span class="sxs-lookup"><span data-stu-id="3d2db-111">The [**CBasePropertyPage::Deactivate**](cbasepropertypage-deactivate.md) method calls the `OnDeactivate` method.</span></span> <span data-ttu-id="3d2db-112">Substitua `OnDeactivate` para liberar os recursos que a classe derivada obteve no método [**CBasePropertyPage:: onactiva**](cbasepropertypage-onactivate.md) ou para executar outras tarefas, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="3d2db-112">Override `OnDeactivate` to release any resources that the derived class obtained in the [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) method, or to perform other tasks as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d2db-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d2db-113">Requirements</span></span>



| <span data-ttu-id="3d2db-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d2db-114">Requirement</span></span> | <span data-ttu-id="3d2db-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3d2db-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d2db-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3d2db-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3d2db-117"><dt>CProp. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d2db-117"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="3d2db-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3d2db-118">Library</span></span><br/> | <dl> <span data-ttu-id="3d2db-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3d2db-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d2db-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d2db-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d2db-121">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="3d2db-121">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




