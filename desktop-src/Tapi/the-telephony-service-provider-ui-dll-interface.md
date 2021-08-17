---
description: Na Telefonia da Microsoft, os provedores de serviços de telefonia são executados em um processo separado de aplicativos de telefonia.
ms.assetid: ccc40d3c-6764-469a-baac-fa625d664ea7
title: A interface DLL da interface do usuário do provedor de serviços de telefonia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6aea6dfd68773dcd96602803230bd160552eab1414135b75a3205a0fac88dd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119403936"
---
# <a name="the-telephony-service-provider-ui-dll-interface"></a>A interface DLL da interface do usuário do provedor de serviços de telefonia

Na Telefonia da Microsoft, os provedores de serviços de telefonia são executados em um processo separado de aplicativos de telefonia. Os provedores de serviços se comunicam com TAPISRV por meio da interface do provedor de serviços de telefonia (TSPI) e executam em seu processo; interface de aplicativos para TAPI, que são carregados no contexto do aplicativo.

Os componentes da TAPI usam vários mecanismos de comunicação entre processos para transmitir solicitações de função e mensagens entre aplicativos e provedores de serviços. Os aplicativos e os provedores de serviços podem estar em execução não apenas em processos separados, mas em sistemas completamente separados. Portanto, os provedores de serviços não podem exibir caixas de diálogo no processo ou até mesmo no computador no qual estão executando; A interface do usuário deve ser invocada de dentro do contexto do aplicativo, no computador no qual o aplicativo está sendo executado.

Esta seção define o mecanismo pelo qual as funções de interface do usuário do provedor de serviços são carregadas e invocadas no contexto do aplicativo. Um mecanismo também é definido pelo qual os provedores de serviços podem abrir caixas de diálogo no contexto do aplicativo quando, de outra forma, não seriam esperados pelo aplicativo. Um exemplo desse último caso seria a caixa de diálogo **Talk/Hangup** exibida por um provedor de serviços de modem de dados quando o modem está sendo usado como um discador para chamadas de voz interativas e o usuário deve ser informado para pegar o telefone e informar ao provedor de serviços quando colocar o modem nohook.

 

 



