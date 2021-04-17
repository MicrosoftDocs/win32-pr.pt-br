---
description: O agente de rede DDE inicia o DDE de rede se detectar atividade DDE de rede local.
ms.assetid: bc1e6a06-be07-4ae8-94da-9603a885b3a5
title: Agente DDE de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a6259b512782102936f54f65646454509c6b37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784184"
---
# <a name="network-dde-agent"></a>Agente DDE de rede

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]

O agente de rede DDE inicia o DDE de rede se detectar atividade DDE de rede local. Ele não detecta um cliente remoto tentando se conectar. Portanto, antes que qualquer cliente possa se conectar com êxito, a rede DDE deve ser iniciada no computador servidor. Observe que o DDE de rede não é iniciado por padrão. Para iniciar o DDE de rede, execute NETDDE.EXE. Esse arquivo está localizado no seu diretório do Windows.

O agente DDE de rede também inicia os aplicativos necessários para o DDE de rede. Depois que o DDE de rede é iniciado, as conversas DDE são controladas por meio de uma janela DDE de rede associada a um dos aplicativos DDE de rede. Esse aplicativo atua como um proxy. Ele se comunica com todos os aplicativos DDE locais e remotos.

 

 



