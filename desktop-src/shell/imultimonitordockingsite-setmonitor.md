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
ms.openlocfilehash: be773ee68c214f6a2fab8da89f1f48b867e71239
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841937"
---
# <a name="imultimonitordockingsitesetmonitor-method"></a><span data-ttu-id="8d80d-103">Método IMultiMonitorDockingSite:: setmonitor</span><span class="sxs-lookup"><span data-stu-id="8d80d-103">IMultiMonitorDockingSite::SetMonitor method</span></span>

<span data-ttu-id="8d80d-104">Altera qual monitor é usado para barras de ferramentas encaixadas em um sistema de vários monitores.</span><span class="sxs-lookup"><span data-stu-id="8d80d-104">Changes which monitor is used for docked toolbars on a multiple monitor system.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d80d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d80d-105">Syntax</span></span>


```C++
HRESULT SetMonitor(
  [in]  IUnknown *punkSrc,
  [in]  HMONITOR hMonNew,
  [out] HMONITOR *phMonOld
);
```



## <a name="parameters"></a><span data-ttu-id="8d80d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d80d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d80d-107">*punkSrc* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8d80d-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d80d-108">Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="8d80d-108">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="8d80d-109">Um ponteiro para o objeto que implementa a interface [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) para a qual o monitor está sendo alterado.</span><span class="sxs-lookup"><span data-stu-id="8d80d-109">A pointer to the object implementing the [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being altered.</span></span>

</dd> <dt>

<span data-ttu-id="8d80d-110">*hMonNew* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8d80d-110">*hMonNew* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d80d-111">Tipo: **HMONITOR**</span><span class="sxs-lookup"><span data-stu-id="8d80d-111">Type: **HMONITOR**</span></span>

<span data-ttu-id="8d80d-112">Um identificador para o monitor que substitui o monitor padrão existente.</span><span class="sxs-lookup"><span data-stu-id="8d80d-112">A handle to the monitor that replaces the existing default monitor.</span></span>

</dd> <dt>

<span data-ttu-id="8d80d-113">*phMonOld* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8d80d-113">*phMonOld* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d80d-114">Tipo: **HMONITOR \***</span><span class="sxs-lookup"><span data-stu-id="8d80d-114">Type: **HMONITOR\***</span></span>

<span data-ttu-id="8d80d-115">Quando essa função retorna, contém um ponteiro para a alça do monitor padrão anterior.</span><span class="sxs-lookup"><span data-stu-id="8d80d-115">When this function returns, contains a pointer to the previous default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d80d-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8d80d-116">Return value</span></span>

<span data-ttu-id="8d80d-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8d80d-117">Type: **HRESULT**</span></span>

<span data-ttu-id="8d80d-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8d80d-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8d80d-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8d80d-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d80d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d80d-120">Requirements</span></span>



| <span data-ttu-id="8d80d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d80d-121">Requirement</span></span> | <span data-ttu-id="8d80d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8d80d-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="8d80d-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d80d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8d80d-124">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8d80d-124">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8d80d-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d80d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8d80d-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8d80d-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
