---
description: As operações de conclusão permitem que um aplicativo especifique como deseja lidar com uma sessão quando fatores como um destino ocupado impedem a conexão normal.
ms.assetid: 71e61376-7913-42a9-a8e2-2ea6e4918f30
title: Concluir uma sessão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20686f89feef5bb73d4ccbb786482f2528d700f42f0c4359fd965418077b8544
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118867974"
---
# <a name="complete-a-session"></a>Concluir uma sessão

As operações de conclusão permitem que um aplicativo especifique como deseja lidar com uma sessão quando fatores como um destino ocupado impedem a conexão normal.

As [ \_ constantes LINECALLCOMPLMODE](./linecallcomplmode--constants.md) definem as possíveis opções que um aplicativo pode ter, dependendo das funcionalidades do provedor de serviços.

Várias solicitações de conclusão de chamada podem estar pendentes para um determinado endereço a qualquer momento. Para identificar solicitações individuais, a implementação retorna um [identificador de conclusão](completion-id-ovr.md). Cancelar uma solicitação de conclusão de chamada em andamento também usa esse identificador de conclusão de chamada.

**TAPI 2.x:** Consulte [**lineCompleteCall,**](/windows/win32/api/tapi/nf-tapi-linecompletecall) [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall).

**TAPI 3.x:** Consulte [**ITBasicCallControl::Conexão**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), [**ITBasicCallControl::D conectar**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).

 

 
