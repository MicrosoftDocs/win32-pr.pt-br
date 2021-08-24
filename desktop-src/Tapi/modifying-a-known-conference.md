---
description: O fragmento de código a seguir ilustra a modificação de um intervalo de tempo de conferências. O período de tempo padrão é de trinta minutos. Nesse fragmento, o período de tempo é definido como um ano.
ms.assetid: 7f05d62e-2bcc-4d98-8a71-97ed20a12af2
title: Modificando uma conferência conhecida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b139b05f70f801a28b91ecb6c2773fd740f10df7c0fd2b8e86b904b210cc50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575596"
---
# <a name="modifying-a-known-conference"></a>Modificando uma conferência conhecida

\[os controles e as interfaces de conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O fragmento de código a seguir ilustra a modificação do período de tempo de uma conferência. O período de tempo padrão é de trinta minutos. Nesse fragmento, o período de tempo é definido como um ano.

Este fragmento pressupõe que [a conexão com um servidor ILS](connecting-to-an-ils-server.md) já foi executada e que uma [enumeração de diretório de conferência](enumerating-conference-directories.md) foi executada para obter a entrada de diretório que será modificada.

Esse fragmento também pressupõe que essa não é uma conferência multicast. Alterar os horários em uma conferência multicast requer a notificação do servidor de alocação de endereços multicast. Consulte [adquirindo um endereço de multicast](acquiring-a-multicast-address.md) para obter um exemplo de como trabalhar com endereçamento multicast.


```C++
// If ( hr != S_OK ) process the error here. 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> </dl>

 

 



