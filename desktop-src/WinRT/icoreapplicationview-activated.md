---
description: Ocorre quando um aplicativo da Windows Store é ativado.
ms.assetid: CA0DB2D4-3417-48F5-8455-D87D0F323A1E
title: 'Evento ICoreApplicationView:: Activated (Windows. ApplicationModel. Core. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612f7110aa149396b18815afe664ee404c70fc52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164483"
---
# <a name="icoreapplicationviewactivated-event"></a><span data-ttu-id="1a774-103">Evento ICoreApplicationView:: Activated</span><span class="sxs-lookup"><span data-stu-id="1a774-103">ICoreApplicationView::Activated event</span></span>

<span data-ttu-id="1a774-104">Ocorre quando um aplicativo da Windows Store é ativado.</span><span class="sxs-lookup"><span data-stu-id="1a774-104">Occurs when a Windows Store app is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a774-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a774-105">Syntax</span></span>


```C++
void Activated(
  [in] ITypedEventHandler<ICoreApplicationView*, IActivatedEventArgs*> handler
);
```



## <a name="parameters"></a><span data-ttu-id="1a774-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a774-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a774-107">*manipulador* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1a774-107">*handler* \[in\]</span></span>
<span data-ttu-id="1a774-108"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1a774-108"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="1a774-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1a774-109">Return value</span></span>

<span data-ttu-id="1a774-110">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1a774-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a774-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a774-111">Remarks</span></span>

<span data-ttu-id="1a774-112">Não chame o método [**Exit**](/previous-versions//hh438368(v=vs.85)) de dentro do *manipulador*.</span><span class="sxs-lookup"><span data-stu-id="1a774-112">Do not call the [**Exit**](/previous-versions//hh438368(v=vs.85)) method from within *handler*.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a774-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a774-113">Requirements</span></span>



| <span data-ttu-id="1a774-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a774-114">Requirement</span></span> | <span data-ttu-id="1a774-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1a774-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a774-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a774-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1a774-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1a774-117">Windows 8</span></span><br/>                                                                                         |
| <span data-ttu-id="1a774-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a774-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1a774-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1a774-119">Windows Server 2012</span></span><br/>                                                                               |
| <span data-ttu-id="1a774-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1a774-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a774-121"><dt>Windows. ApplicationModel. Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a774-121"><dt>Windows.ApplicationModel.Core.h</dt></span></span> </dl>   |
| <span data-ttu-id="1a774-122">INSERI</span><span class="sxs-lookup"><span data-stu-id="1a774-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1a774-123"><dt>Windows. ApplicationModel. Core. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1a774-123"><dt>Windows.ApplicationModel.Core.idl</dt></span></span> </dl> |



 

 
