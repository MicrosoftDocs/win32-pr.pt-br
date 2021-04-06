---
description: Net.exe pode ser usado para parar e iniciar o protocolo IPv6.
ms.assetid: faa555d9-eb20-4b7a-94eb-b67a48ee630e
title: Net.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5074696b71ce000ef330f2c88fceef0f60b0222e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827106"
---
# <a name="netexe"></a>Net.exe

Net.exe pode ser usado para parar e iniciar o protocolo IPv6. Reiniciar o IPv6 reinicializa o protocolo como se o computador estivesse reiniciando, o que pode alterar os números de interface. Net.exe tem muitos subcomandos. Os comandos a seguir são relevantes para o IPv6:

<dl> <dt>

<span id="net_stop_tcpip6"></span><span id="NET_STOP_TCPIP6"></span>**tcpip6 net stop**
</dt> <dd>

Interrompe o protocolo IPv6 e o descarrega da memória. Esse comando falhará se algum soquete IPv6 estiver aberto.

</dd> <dt>

<span id="net_start_tcpip6"></span><span id="NET_START_TCPIP6"></span>**net start tcpip6**
</dt> <dd>

Inicia o protocolo IPv6 se ele foi interrompido. Se um novo arquivo de driver de Tcpip6.sys estiver presente no diretório% systemroot% \\ System32 \\ drivers, esse arquivo de driver será carregado.

</dd> </dl>

 

 



