---
description: O encerramento da sessão pode ser originado com uma solicitação de usuário, desconexão remota por outra parte ou por motivos específicos do aplicativo.
ms.assetid: 69ed2e2c-f1c7-4f69-86a0-3cfdd80e423d
title: Encerrar uma sessão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b27013159e7c162027835706ab80bcf1f2c7f870006a6250d0ec4efdf1751ae4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118860504"
---
# <a name="terminate-a-session"></a>Encerrar uma sessão

O encerramento da sessão pode ser originado com uma solicitação de usuário, desconexão remota por outra parte ou por motivos específicos do aplicativo. Quando uma sessão é encerrada, o [identificador](session-identifier-ovr.md) de sessão permanece válido até ser liberado especificamente e pode ser usado para coletar dados pós-conexão.

O encerramento da sessão é concluído desalocando e liberando os recursos associados à sessão. Se uma sessão for simplesmente descartado ou desconectado, mas os recursos não são liberados, o resultado será uma perda de memória no aplicativo e, possivelmente, no provedor de serviços também.

**TAPI 2.x:** Consulte [**lineDrop,**](/windows/win32/api/tapi/nf-tapi-linedrop) [**lineDeallocateCall**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall).

**TAPI 3.x:** Consulte [**ITBasicCallControl::D conectar**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect), execute uma versão COM padrão no ponteiro do objeto Call.

 

 
