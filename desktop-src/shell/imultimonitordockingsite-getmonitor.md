---
description: Obtém o monitor padrão atual.
title: 'Método IMultiMonitorDockingSite:: getmonitor'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.GetMonitor
api_type:
- COM
api_location: ''
ms.assetid: 0bae75eb-ebd5-4de4-9249-0e9bb489f61f
ms.openlocfilehash: 1260da5ee4404a7ec4597a57e7e3836d6f133426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989049"
---
# <a name="imultimonitordockingsitegetmonitor-method"></a><span data-ttu-id="bb651-103">Método IMultiMonitorDockingSite:: getmonitor</span><span class="sxs-lookup"><span data-stu-id="bb651-103">IMultiMonitorDockingSite::GetMonitor method</span></span>

<span data-ttu-id="bb651-104">Obtém o monitor padrão atual.</span><span class="sxs-lookup"><span data-stu-id="bb651-104">Gets the current default monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb651-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb651-105">Syntax</span></span>


```C++
HRESULT GetMonitor(
  [in]  IUnknown *punkSrc,
  [out] HMONITOR *phMon
);
```



## <a name="parameters"></a><span data-ttu-id="bb651-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb651-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb651-107">*punkSrc* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bb651-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb651-108">Tipo: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="bb651-108">Type: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="bb651-109">Um ponteiro para o objeto que implementa a interface [_ *IDockingWindow* \*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) para a qual o monitor está sendo solicitado.</span><span class="sxs-lookup"><span data-stu-id="bb651-109">A pointer to the object implementing the [_ *IDockingWindow*\*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="bb651-110">*phMon* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bb651-110">*phMon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb651-111">Tipo: \**HMONITOR \** _</span><span class="sxs-lookup"><span data-stu-id="bb651-111">Type: \**HMONITOR\** _</span></span>

<span data-ttu-id="bb651-112">Quando a função retorna, contém um ponteiro para a alça do monitor padrão.</span><span class="sxs-lookup"><span data-stu-id="bb651-112">When the function returns, contains a pointer to the default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb651-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bb651-113">Return value</span></span>

<span data-ttu-id="bb651-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="bb651-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="bb651-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bb651-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bb651-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bb651-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb651-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb651-117">Requirements</span></span>



| <span data-ttu-id="bb651-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb651-118">Requirement</span></span> | <span data-ttu-id="bb651-119">Valor</span><span class="sxs-lookup"><span data-stu-id="bb651-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="bb651-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb651-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bb651-121">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bb651-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bb651-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb651-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bb651-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bb651-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
