---
description: O comando SIOCGIFCONF fornecido pela maioria das implementações UNIX tem suporte na forma de funções WSAIoctl e WSPIoctl com o comando SIO \_ GET \_ INTERFACE \_ LIST. Esse comando retorna a lista de interfaces configuradas e seus parâmetros.
ms.assetid: c5028dae-052a-444c-837c-cd8d6d901b6c
title: Usando UNIX Ioctls no Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da517adb6480a1bd20100a3d9a6d0896f544c1b541ce547a0f76e5c88aa24210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118558858"
---
# <a name="using-unix-ioctls-in-winsock"></a>Usando UNIX Ioctls no Winsock

O **comando SIOCGIFCONF** fornecido pela maioria das implementações UNIX tem suporte na forma de [**funções WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) e [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) com o comando **SIO GET INTERFACE \_ \_ \_ LIST**. Esse comando retorna a lista de interfaces configuradas e seus parâmetros.

> [!Note]  
> O suporte a esse comando é obrigatório Windows provedores de serviços TCP/IP compatíveis com soquetes 2.

 

O parâmetro *lpvOutBuffer* aponta para o buffer no qual [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) e [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) armazenam as informações sobre interfaces. O número de interfaces (número de estruturas retornadas em *lpvOutBuffer*) pode ser determinado com base no comprimento real do buffer de saída retornado em *lpcbBytesReturned.*

 

 
