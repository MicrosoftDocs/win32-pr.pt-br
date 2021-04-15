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
# <a name="opportunistic-lock-operations"></a>Operações de bloqueio oportunista

Se um aplicativo solicita bloqueios oportunistas, todos os arquivos para os quais ele solicita bloqueios devem ser abertos para entrada e saída sobrepostas (assíncronas) usando a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) com o sinalizador **\_ \_ sobreposto do sinalizador de arquivo** . Depois que os arquivos são abertos para a operação sobreposta, você pode usar a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com um dos seguintes códigos de controle para trabalhar com os bloqueios oportunistas dos arquivos:

<dl>

[**FSCTL \_ OPBATCH \_ ACK \_ fechamento \_ pendente**](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)  
[**\_ACK de quebra de oplock fsctl \_ \_ \_ não \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)  
[**\_confirmação de \_ quebra de oplock fsctl \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)  
[**\_notificação de \_ quebra de oplock fsctl \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)  
[**OPLOCK FSCTL de \_ solicitação de \_ lote \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)  
[**\_oplock de \_ filtro de solicitação fsctl \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)  
[**\_oplock de solicitação de fsctl \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)  
[**\_Nível de bloqueio de solicitação fsctl \_ \_ \_ 1**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)  
[**\_Nível de bloqueio de solicitação fsctl \_ \_ \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)  
</dl>

 

 
