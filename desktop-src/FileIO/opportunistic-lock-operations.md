---
description: Se um aplicativo solicita bloqueios oportunistas, todos os arquivos para os quais ele solicita bloqueios devem ser abertos para entrada e saída sobrepostas (assíncronas) usando a função CreateFile com o \_ sinalizador sobreposto do sinalizador de arquivo \_ .
ms.assetid: 1595c03e-9f6d-456c-8164-fafba06bbd79
title: Operações de bloqueio oportunista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefd9b292747e89f5ebafd94cb8aa0e38833e8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505889"
---
# <a name="opportunistic-lock-operations"></a><span data-ttu-id="60286-103">Operações de bloqueio oportunista</span><span class="sxs-lookup"><span data-stu-id="60286-103">Opportunistic Lock Operations</span></span>

<span data-ttu-id="60286-104">Se um aplicativo solicita bloqueios oportunistas, todos os arquivos para os quais ele solicita bloqueios devem ser abertos para entrada e saída sobrepostas (assíncronas) usando a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) com o sinalizador **\_ \_ sobreposto do sinalizador de arquivo** .</span><span class="sxs-lookup"><span data-stu-id="60286-104">If an application requests opportunistic locks, all files for which it requests locks must be opened for overlapped (asynchronous) input and output by using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function with the **FILE\_FLAG\_OVERLAPPED** flag.</span></span> <span data-ttu-id="60286-105">Depois que os arquivos são abertos para a operação sobreposta, você pode usar a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com um dos seguintes códigos de controle para trabalhar com os bloqueios oportunistas dos arquivos:</span><span class="sxs-lookup"><span data-stu-id="60286-105">After the files are opened for overlapped operation, you can use the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with one of the following control codes to work with those files' opportunistic locks:</span></span>

<dl>

[<span data-ttu-id="60286-106">**FSCTL \_ OPBATCH \_ ACK \_ fechamento \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="60286-106">**FSCTL\_OPBATCH\_ACK\_CLOSE\_PENDING**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)  
[<span data-ttu-id="60286-107">**\_ACK de quebra de oplock fsctl \_ \_ \_ não \_ 2**</span><span class="sxs-lookup"><span data-stu-id="60286-107">**FSCTL\_OPLOCK\_BREAK\_ACK\_NO\_2**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)  
[<span data-ttu-id="60286-108">**\_confirmação de \_ quebra de oplock fsctl \_**</span><span class="sxs-lookup"><span data-stu-id="60286-108">**FSCTL\_OPLOCK\_BREAK\_ACKNOWLEDGE**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)  
[<span data-ttu-id="60286-109">**\_notificação de \_ quebra de oplock fsctl \_**</span><span class="sxs-lookup"><span data-stu-id="60286-109">**FSCTL\_OPLOCK\_BREAK\_NOTIFY**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)  
[<span data-ttu-id="60286-110">**OPLOCK FSCTL de \_ solicitação de \_ lote \_**</span><span class="sxs-lookup"><span data-stu-id="60286-110">**FSCTL\_REQUEST\_BATCH\_OPLOCK**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)  
[<span data-ttu-id="60286-111">**\_oplock de \_ filtro de solicitação fsctl \_**</span><span class="sxs-lookup"><span data-stu-id="60286-111">**FSCTL\_REQUEST\_FILTER\_OPLOCK**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)  
[<span data-ttu-id="60286-112">**\_oplock de solicitação de fsctl \_**</span><span class="sxs-lookup"><span data-stu-id="60286-112">**FSCTL\_REQUEST\_OPLOCK**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)  
[<span data-ttu-id="60286-113">**\_Nível de bloqueio de solicitação fsctl \_ \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="60286-113">**FSCTL\_REQUEST\_OPLOCK\_LEVEL\_1**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)  
[<span data-ttu-id="60286-114">**\_Nível de bloqueio de solicitação fsctl \_ \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="60286-114">**FSCTL\_REQUEST\_OPLOCK\_LEVEL\_2**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)  
</dl>

 

 
