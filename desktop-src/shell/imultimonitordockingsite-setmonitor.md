---
description: Altera qual monitor é usado para barras de ferramentas encaixadas em um sistema de vários monitores.
title: 'Método IMultiMonitorDockingSite:: setmonitor'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.SetMonitor
api_type:
- COM
api_location: ''
ms.assetid: ba4ace13-7096-4f05-bcb0-ab37f1632406
ms.openlocfilehash: cc177316a850bbf5059cabf48362ab8d5cbe2466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989113"
---
# <a name="imultimonitordockingsitesetmonitor-method"></a><span data-ttu-id="4e366-103">Método IMultiMonitorDockingSite:: setmonitor</span><span class="sxs-lookup"><span data-stu-id="4e366-103">IMultiMonitorDockingSite::SetMonitor method</span></span>

<span data-ttu-id="4e366-104">Altera qual monitor é usado para barras de ferramentas encaixadas em um sistema de vários monitores.</span><span class="sxs-lookup"><span data-stu-id="4e366-104">Changes which monitor is used for docked toolbars on a multiple monitor system.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e366-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e366-105">Syntax</span></span>


```C++
HRESULT SetMonitor(
  [in]  IUnknown *punkSrc,
  [in]  HMONITOR hMonNew,
  [out] HMONITOR *phMonOld
);
```



## <a name="parameters"></a><span data-ttu-id="4e366-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e366-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e366-107">*punkSrc* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4e366-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e366-108">Tipo: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="4e366-108">Type: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="4e366-109">Um ponteiro para o objeto que implementa a interface [_ *IDockingWindow* \*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) para a qual o monitor está sendo alterado.</span><span class="sxs-lookup"><span data-stu-id="4e366-109">A pointer to the object implementing the [_ *IDockingWindow*\*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being altered.</span></span>

</dd> <dt>

<span data-ttu-id="4e366-110">*hMonNew* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4e366-110">*hMonNew* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e366-111">Tipo: **HMONITOR**</span><span class="sxs-lookup"><span data-stu-id="4e366-111">Type: **HMONITOR**</span></span>

<span data-ttu-id="4e366-112">Um identificador para o monitor que substitui o monitor padrão existente.</span><span class="sxs-lookup"><span data-stu-id="4e366-112">A handle to the monitor that replaces the existing default monitor.</span></span>

</dd> <dt>

<span data-ttu-id="4e366-113">*phMonOld* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4e366-113">*phMonOld* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e366-114">Tipo: \**HMONITOR \** _</span><span class="sxs-lookup"><span data-stu-id="4e366-114">Type: \**HMONITOR\** _</span></span>

<span data-ttu-id="4e366-115">Quando essa função retorna, contém um ponteiro para a alça do monitor padrão anterior.</span><span class="sxs-lookup"><span data-stu-id="4e366-115">When this function returns, contains a pointer to the previous default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e366-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4e366-116">Return value</span></span>

<span data-ttu-id="4e366-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="4e366-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="4e366-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4e366-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4e366-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4e366-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e366-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e366-120">Requirements</span></span>



| <span data-ttu-id="4e366-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e366-121">Requirement</span></span> | <span data-ttu-id="4e366-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4e366-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="4e366-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e366-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4e366-124">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4e366-124">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4e366-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e366-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4e366-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4e366-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
