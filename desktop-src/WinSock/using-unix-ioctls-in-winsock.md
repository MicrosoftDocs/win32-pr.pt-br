---
description: O comando SIOCGIFCONF fornecido pela maioria das implementações do UNIX tem suporte na forma de funções WSAIoctl e WSPIoctl com o comando SIO \_ obter a \_ lista de interface \_ . Esse comando retorna a lista de interfaces configuradas e seus parâmetros.
ms.assetid: c5028dae-052a-444c-837c-cd8d6d901b6c
title: Usando os IOCTLs do UNIX no Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0b52c311ea8c5f67dc374503f00c3ca16c5d053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810729"
---
# <a name="using-unix-ioctls-in-winsock"></a>Usando os IOCTLs do UNIX no Winsock

O comando **SIOCGIFCONF** fornecido pela maioria das implementações do UNIX tem suporte na forma de funções [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) e [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) com o comando **sio obter a \_ \_ \_ lista de interface**. Esse comando retorna a lista de interfaces configuradas e seus parâmetros.

> [!Note]  
> O suporte a esse comando é obrigatório para provedores de serviço TCP/IP em conformidade com o Windows Sockets 2.

 

O parâmetro *lpvOutBuffer* aponta para o buffer no qual [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) e [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) armazenam as informações sobre interfaces. O número de interfaces (número de estruturas retornado em *lpvOutBuffer*) pode ser determinado com base no tamanho real do buffer de saída retornado em *lpcbBytesReturned*.

 

 
