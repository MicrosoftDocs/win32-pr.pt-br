---
description: Verifica se o monitor está ativo e disponível.
title: 'Método IMultiMonitorDockingSite:: RequestMonitor'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.RequestMonitor
api_type:
- COM
api_location: ''
ms.assetid: 9aa6eb20-de39-41f7-a17e-183f4088f972
ms.openlocfilehash: 5389b10af9aaa3da5d3106d82a4fbdcbd614a094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922926"
---
# <a name="imultimonitordockingsiterequestmonitor-method"></a><span data-ttu-id="1ead2-103">Método IMultiMonitorDockingSite:: RequestMonitor</span><span class="sxs-lookup"><span data-stu-id="1ead2-103">IMultiMonitorDockingSite::RequestMonitor method</span></span>

<span data-ttu-id="1ead2-104">Verifica se o monitor está ativo e disponível.</span><span class="sxs-lookup"><span data-stu-id="1ead2-104">Verifies that the monitor is active and available.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ead2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ead2-105">Syntax</span></span>


```C++
HRESULT RequestMonitor(
  [in] IUnknown *punkSrc,
  [in] HMONITOR *phMon
);
```



## <a name="parameters"></a><span data-ttu-id="1ead2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ead2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ead2-107">*punkSrc* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1ead2-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ead2-108">Tipo: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="1ead2-108">Type: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="1ead2-109">Um ponteiro para o objeto que implementa a interface [_ *IDockingWindow* \*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) .</span><span class="sxs-lookup"><span data-stu-id="1ead2-109">A pointer to the object implementing the [_ *IDockingWindow*\*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface.</span></span>

</dd> <dt>

<span data-ttu-id="1ead2-110">*phMon* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1ead2-110">*phMon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ead2-111">Tipo: \**HMONITOR \** _</span><span class="sxs-lookup"><span data-stu-id="1ead2-111">Type: \**HMONITOR\** _</span></span>

<span data-ttu-id="1ead2-112">Um ponteiro para a alça do monitor padrão.</span><span class="sxs-lookup"><span data-stu-id="1ead2-112">A pointer to the default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ead2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ead2-113">Return value</span></span>

<span data-ttu-id="1ead2-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="1ead2-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="1ead2-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1ead2-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1ead2-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1ead2-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ead2-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ead2-117">Requirements</span></span>



| <span data-ttu-id="1ead2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ead2-118">Requirement</span></span> | <span data-ttu-id="1ead2-119">Valor</span><span class="sxs-lookup"><span data-stu-id="1ead2-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="1ead2-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ead2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1ead2-121">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1ead2-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1ead2-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ead2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1ead2-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1ead2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
