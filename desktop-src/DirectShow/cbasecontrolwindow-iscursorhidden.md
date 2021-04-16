---
description: O método IsCursorHidden recupera o estado atual do membro de \_ dados m bCursorHidden.
ms.assetid: 4b97b89d-876a-470c-ac41-a88fecb52b2d
title: Método CBaseControlWindow. IsCursorHidden (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsCursorHidden
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 90f02c6cac5fb3ef1edeaa8e03f7bc54a03acb49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752307"
---
# <a name="cbasecontrolwindowiscursorhidden-method"></a><span data-ttu-id="bac91-103">Método CBaseControlWindow. IsCursorHidden</span><span class="sxs-lookup"><span data-stu-id="bac91-103">CBaseControlWindow.IsCursorHidden method</span></span>

<span data-ttu-id="bac91-104">O `IsCursorHidden` método recupera o estado atual do membro de dados **m \_ bCursorHidden** .</span><span class="sxs-lookup"><span data-stu-id="bac91-104">The `IsCursorHidden` method retrieves the current state of the **m\_bCursorHidden** data member.</span></span>

## <a name="syntax"></a><span data-ttu-id="bac91-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bac91-105">Syntax</span></span>


```C++
HRESULT IsCursorHidden(
   long *CursorHidden
);
```



## <a name="parameters"></a><span data-ttu-id="bac91-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bac91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bac91-107">*CursorHidden*</span><span class="sxs-lookup"><span data-stu-id="bac91-107">*CursorHidden*</span></span> 
</dt> <dd>

<span data-ttu-id="bac91-108">Ponteiro para o valor de **m \_ bCursorHidden**.</span><span class="sxs-lookup"><span data-stu-id="bac91-108">Pointer to the value of **m\_bCursorHidden**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bac91-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bac91-109">Return value</span></span>

<span data-ttu-id="bac91-110">Quando chamado sem um parâmetro, retorna OATRUE se o cursor estiver oculto ou OAFALSE se o cursor estiver visível.</span><span class="sxs-lookup"><span data-stu-id="bac91-110">When called without a parameter, returns OATRUE if the cursor is hidden, or OAFALSE if the cursor is visible.</span></span>

## <a name="remarks"></a><span data-ttu-id="bac91-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="bac91-111">Remarks</span></span>

<span data-ttu-id="bac91-112">Os objetos internos devem chamar essa função de membro sem o parâmetro *CursorHidden* para evitar o bloqueio da seção crítica.</span><span class="sxs-lookup"><span data-stu-id="bac91-112">Internal objects should call this member function without the *CursorHidden* parameter to avoid locking the critical section.</span></span> <span data-ttu-id="bac91-113">Os objetos externos acessam essa função de membro com o parâmetro *CursorHidden* por meio do método [**IVideoWindow:: IsCursorHidden**](/windows/desktop/api/Control/nf-control-ivideowindow-iscursorhidden) .</span><span class="sxs-lookup"><span data-stu-id="bac91-113">External objects access this member function with the *CursorHidden* parameter through the [**IVideoWindow::IsCursorHidden**](/windows/desktop/api/Control/nf-control-ivideowindow-iscursorhidden) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bac91-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bac91-114">Requirements</span></span>



| <span data-ttu-id="bac91-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bac91-115">Requirement</span></span> | <span data-ttu-id="bac91-116">Valor</span><span class="sxs-lookup"><span data-stu-id="bac91-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bac91-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bac91-117">Header</span></span><br/>  | <dl> <span data-ttu-id="bac91-118"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bac91-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bac91-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bac91-119">Library</span></span><br/> | <dl> <span data-ttu-id="bac91-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="bac91-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bac91-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="bac91-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bac91-122">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="bac91-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




