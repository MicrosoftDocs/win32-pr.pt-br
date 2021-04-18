---
description: O encerramento da sessão pode ser originado com uma solicitação do usuário, desconexão remota por outra parte ou por motivos específicos do aplicativo.
ms.assetid: 69ed2e2c-f1c7-4f69-86a0-3cfdd80e423d
title: Encerrar uma sessão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac433f1c8104ec41a3c42dc44c32a2b110d79469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760325"
---
# <a name="terminate-a-session"></a>Encerrar uma sessão

O encerramento da sessão pode ser originado com uma solicitação do usuário, desconexão remota por outra parte ou por motivos específicos do aplicativo. Quando uma sessão é encerrada, o [identificador de sessão](session-identifier-ovr.md) permanece válido até ser liberado especificamente e pode ser usado para coletar dados de pós-conexão.

O encerramento da sessão é concluído pela desalocação e liberação dos recursos associados à sessão. Se uma sessão for meramente descartada ou desconectada, mas os recursos não forem liberados, o resultado será um vazamento de memória no aplicativo e possivelmente no provedor de serviços também.

**TAPI 2. x:** Consulte [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop), [**lineDeallocateCall**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall).

**TAPI 3. x:** Consulte [**ITBasicCallControl::D isconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect), executar uma versão com padrão no ponteiro de objeto de chamada.

 

 
