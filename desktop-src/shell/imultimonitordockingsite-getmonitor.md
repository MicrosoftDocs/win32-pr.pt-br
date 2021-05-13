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
ms.openlocfilehash: 2cd437fd6c0e842eb314db6c57420af6b54b05ff
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840637"
---
# <a name="imultimonitordockingsitegetmonitor-method"></a><span data-ttu-id="29dc7-103">Método IMultiMonitorDockingSite:: getmonitor</span><span class="sxs-lookup"><span data-stu-id="29dc7-103">IMultiMonitorDockingSite::GetMonitor method</span></span>

<span data-ttu-id="29dc7-104">Obtém o monitor padrão atual.</span><span class="sxs-lookup"><span data-stu-id="29dc7-104">Gets the current default monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="29dc7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29dc7-105">Syntax</span></span>


```C++
HRESULT GetMonitor(
  [in]  IUnknown *punkSrc,
  [out] HMONITOR *phMon
);
```



## <a name="parameters"></a><span data-ttu-id="29dc7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29dc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29dc7-107">*punkSrc* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="29dc7-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29dc7-108">Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="29dc7-108">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="29dc7-109">Um ponteiro para o objeto que implementa a interface [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) para a qual o monitor está sendo solicitado.</span><span class="sxs-lookup"><span data-stu-id="29dc7-109">A pointer to the object implementing the [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="29dc7-110">*phMon* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="29dc7-110">*phMon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29dc7-111">Tipo: **HMONITOR \***</span><span class="sxs-lookup"><span data-stu-id="29dc7-111">Type: **HMONITOR\***</span></span>

<span data-ttu-id="29dc7-112">Quando a função retorna, contém um ponteiro para a alça do monitor padrão.</span><span class="sxs-lookup"><span data-stu-id="29dc7-112">When the function returns, contains a pointer to the default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29dc7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="29dc7-113">Return value</span></span>

<span data-ttu-id="29dc7-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="29dc7-114">Type: **HRESULT**</span></span>

<span data-ttu-id="29dc7-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="29dc7-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="29dc7-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="29dc7-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="29dc7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29dc7-117">Requirements</span></span>



| <span data-ttu-id="29dc7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="29dc7-118">Requirement</span></span> | <span data-ttu-id="29dc7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="29dc7-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="29dc7-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29dc7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="29dc7-121">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="29dc7-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="29dc7-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29dc7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="29dc7-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="29dc7-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
