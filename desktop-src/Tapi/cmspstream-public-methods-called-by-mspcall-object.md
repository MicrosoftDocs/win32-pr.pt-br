---
description: A lista a seguir contém os métodos CMSPStream chamados pelo objeto MSPCall.
ms.assetid: 7a59ca78-b5e8-45e9-8fdb-89402ffef916
title: Métodos CMSPStream chamados por objeto MSPCall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89744f9e4cf2739fa11f07edc4be7e331beb620a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760167"
---
# <a name="cmspstream-public-methods-called-by-mspcall-object"></a>Métodos públicos CMSPStream chamados por objeto MSPCall



| Métodos públicos CMSPStream                                 | Descrição                                                                             |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**Init**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-init)                           | Chamado pelo **MSPCall** quando o fluxo é criado.                                   |
| [**Desligar**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-shutdown)                   | Chamado pelo **MSPCall** para cancelar a seleção de todos os objetos de terminal e liberar o objeto de chamada. |
| [**GetState**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-getstate)                   | Chamado pelo objeto MSPCall para obter o status atual do fluxo.                   |
| [**HandleTSPData**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-handletspdata)         | O objeto de chamada derivada pode chamar esse método para permitir que o fluxo manipule os comandos do TSP.     |
| [**ProcessGraphEvent**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-processgraphevent) | Chamado pelo objeto MSPCall para permitir que o fluxo manipule eventos de grafo.                     |



 

 

 



