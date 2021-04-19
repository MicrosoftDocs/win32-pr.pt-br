---
description: Fornece ao sistema informações sobre um documento antes de uma operação de área de transferência de stash ser iniciada.
title: Função DlpNotifyPreStashClipboard (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreStashClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 72ecabb2bbfb7517b52790c0d3b7c1ab8075dbd0
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495308"
---
# <a name="dlpnotifyprestashclipboard-function"></a><span data-ttu-id="71111-103">Função DlpNotifyPreStashClipboard</span><span class="sxs-lookup"><span data-stu-id="71111-103">DlpNotifyPreStashClipboard function</span></span>

<span data-ttu-id="71111-104">Notifica o sistema antes que uma operação de área de transferência de stash seja iniciada.</span><span class="sxs-lookup"><span data-stu-id="71111-104">Notifies the system before a stash clipboard operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="71111-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71111-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreStashClipboard();
```



## <a name="parameters"></a><span data-ttu-id="71111-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71111-106">Parameters</span></span>




## <a name="return-value"></a><span data-ttu-id="71111-107">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="71111-107">Return value</span></span>

<span data-ttu-id="71111-108">Retornar void.</span><span class="sxs-lookup"><span data-stu-id="71111-108">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="71111-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="71111-109">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="71111-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71111-110">Requirements</span></span>



| <span data-ttu-id="71111-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="71111-111">Requirement</span></span>          |    <span data-ttu-id="71111-112">Valor</span><span class="sxs-lookup"><span data-stu-id="71111-112">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71111-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71111-113">Minimum supported client</span></span><br/> | <span data-ttu-id="71111-114">Windows 10, versão 1809 (10,0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="71111-114">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="71111-115">DLL</span><span class="sxs-lookup"><span data-stu-id="71111-115">DLL</span></span><br/>                      | <span data-ttu-id="71111-116">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="71111-116">EndpointDlp.dll</span></span> |