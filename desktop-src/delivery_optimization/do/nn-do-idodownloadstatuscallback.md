---
title: Interface IDODownloadStatusCallback
description: Usado para receber notificações sobre um download.
keywords:
- Interface IDODownloadStatusCallback
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0917b73939535854469a1fe02ea89acc904cf055
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366067"
---
# <a name="idodownloadstatuscallback-interface"></a><span data-ttu-id="84abf-104">Interface IDODownloadStatusCallback</span><span class="sxs-lookup"><span data-stu-id="84abf-104">IDODownloadStatusCallback interface</span></span>

<span data-ttu-id="84abf-105">A interface **IDODownloadStatusCallback** é usada para receber notificações sobre um download.</span><span class="sxs-lookup"><span data-stu-id="84abf-105">The **IDODownloadStatusCallback** interface is used to receive notifications about a download.</span></span>

## <a name="methods"></a><span data-ttu-id="84abf-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="84abf-106">Methods</span></span>

<span data-ttu-id="84abf-107">A interface **IDODownloadStatusCallback** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="84abf-107">The **IDODownloadStatusCallback** interface has these methods.</span></span>

| <span data-ttu-id="84abf-108">Método</span><span class="sxs-lookup"><span data-stu-id="84abf-108">Method</span></span> | <span data-ttu-id="84abf-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="84abf-109">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="84abf-110">IDODownloadStatusCallback:: onstatuschanged</span><span class="sxs-lookup"><span data-stu-id="84abf-110">IDODownloadStatusCallback::OnStatusChanged</span></span>](./nf-do-idodownloadstatuscallback-onstatuschanged.md) | <span data-ttu-id="84abf-111">O chama sua implementação desse método sempre que um status de download for alterado.</span><span class="sxs-lookup"><span data-stu-id="84abf-111">DO calls your implementation of this method any time a download status has changed.</span></span> |

## <a name="requirements"></a><span data-ttu-id="84abf-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84abf-112">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="84abf-113">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="84abf-113">**Minimum supported client**</span></span> | <span data-ttu-id="84abf-114">Somente aplicativos do Windows 10, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="84abf-114">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="84abf-115">**Servidor mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="84abf-115">**Minimum supported server**</span></span> | <span data-ttu-id="84abf-116">Somente aplicativos do Windows Server, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="84abf-116">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="84abf-117">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="84abf-117">**Header**</span></span> | <span data-ttu-id="84abf-118">Do. h</span><span class="sxs-lookup"><span data-stu-id="84abf-118">Do.h</span></span> |