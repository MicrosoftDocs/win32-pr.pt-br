---
description: As operações de conclusão permitem que um aplicativo especifique como ele deseja tratar uma sessão quando fatores como um destino ocupado impedem uma conexão normal.
ms.assetid: 71e61376-7913-42a9-a8e2-2ea6e4918f30
title: Concluir uma sessão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5736b6be452413811f3530f44db280fe4e2a682f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788071"
---
# <a name="complete-a-session"></a>Concluir uma sessão

As operações de conclusão permitem que um aplicativo especifique como ele deseja tratar uma sessão quando fatores como um destino ocupado impedem uma conexão normal.

As [ \_ constantes LINECALLCOMPLMODE](./linecallcomplmode--constants.md) definem as possíveis opções que um aplicativo pode ter, dependendo dos recursos do provedor de serviços.

Várias solicitações de conclusão de chamada podem estar pendentes para um determinado endereço a qualquer momento. Para identificar solicitações individuais, a implementação retorna um [identificador de conclusão](completion-id-ovr.md). Cancelar uma solicitação de conclusão de chamada em andamento também usa esse identificador de conclusão de chamada.

**TAPI 2. x:** Consulte [**lineCompleteCall**](/windows/win32/api/tapi/nf-tapi-linecompletecall), [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall).

**TAPI 3. x:** Consulte [**ITBasicCallControl:: Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), [**ITBasicCallControl::D isconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).

 

 
