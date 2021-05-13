---
description: Verifica se o monitor está ativo e disponível.
title: Método IMultiMonitorDockingSite::RequestMonitor
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
ms.openlocfilehash: 7f219e5fd62fb4f85fd206501e6a53ac3927195a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841967"
---
# <a name="imultimonitordockingsiterequestmonitor-method"></a><span data-ttu-id="b6943-103">Método IMultiMonitorDockingSite::RequestMonitor</span><span class="sxs-lookup"><span data-stu-id="b6943-103">IMultiMonitorDockingSite::RequestMonitor method</span></span>

<span data-ttu-id="b6943-104">Verifica se o monitor está ativo e disponível.</span><span class="sxs-lookup"><span data-stu-id="b6943-104">Verifies that the monitor is active and available.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6943-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6943-105">Syntax</span></span>


```C++
HRESULT RequestMonitor(
  [in] IUnknown *punkSrc,
  [in] HMONITOR *phMon
);
```



## <a name="parameters"></a><span data-ttu-id="b6943-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6943-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6943-107">*quedas de dados* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="b6943-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6943-108">Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="b6943-108">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="b6943-109">Um ponteiro para o objeto que implementa a interface [**IDockingWindow.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow)</span><span class="sxs-lookup"><span data-stu-id="b6943-109">A pointer to the object implementing the [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface.</span></span>

</dd> <dt>

<span data-ttu-id="b6943-110">*phMon* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="b6943-110">*phMon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6943-111">Tipo: **HMONITOR \***</span><span class="sxs-lookup"><span data-stu-id="b6943-111">Type: **HMONITOR\***</span></span>

<span data-ttu-id="b6943-112">Um ponteiro para o alça do monitor padrão.</span><span class="sxs-lookup"><span data-stu-id="b6943-112">A pointer to the default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6943-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b6943-113">Return value</span></span>

<span data-ttu-id="b6943-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b6943-114">Type: **HRESULT**</span></span>

<span data-ttu-id="b6943-115">Se esse método for bem-sucedido, ele **retornará S \_ OK.**</span><span class="sxs-lookup"><span data-stu-id="b6943-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b6943-116">Caso contrário, ele retornará um **código de erro HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="b6943-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6943-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6943-117">Requirements</span></span>



| <span data-ttu-id="b6943-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6943-118">Requirement</span></span> | <span data-ttu-id="b6943-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b6943-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="b6943-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6943-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b6943-121">Windows 2000 Professional, somente aplicativos da área de trabalho do Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b6943-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b6943-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6943-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b6943-123">Somente aplicativos da área de trabalho do Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b6943-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
