---
description: Quando um pacote de segurança SSP/AP está funcionando como um pacote de autenticação, ele é carregado no espaço de processo da autoridade de segurança local (LSA) e é considerado no modo LSA.
ms.assetid: ff4e61be-dbaa-4cfa-8c72-43e99fe1c3cb
title: Modo LSA versus modo de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd8fadde30fe60c38a2b8ccb1f158d94ec7d5603
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011524"
---
# <a name="lsa-mode-vs-user-mode"></a>Modo LSA versus modo de usuário

Quando um [*pacote de segurança*](../secgloss/s-gly.md) SSP/AP está funcionando como um [*pacote de autenticação*](../secgloss/a-gly.md), ele é carregado no espaço de processo da [*autoridade de segurança local*](../secgloss/l-gly.md) (LSA) e é considerado no modo LSA. Os aplicativos de logon acessam a funcionalidade do pacote de autenticação usando as [funções de logon LSA](authentication-functions.md). Os desenvolvedores podem usar as funções de suporte do LSA disponíveis somente para os pacotes de segurança do modo LSA para implementar pacotes de autenticação mais sofisticados do que o suportado anteriormente.

Quando um [*pacote de segurança*](../secgloss/s-gly.md) fornece serviços de segurança para um aplicativo cliente/servidor, ele é carregado nos processos de cliente e servidor e é considerado no modo de usuário. Os aplicativos cliente/servidor acessam os serviços de suporte de segurança do pacote de segurança usando o SSPI (Microsoft [*Security Support Provider interface*](../secgloss/s-gly.md) ).

O suporte de LSA para SSP/APs inclui funções que as instâncias de modo LSA e de modo de usuário de um pacote de segurança podem usar para se comunicar. Além disso, a instância do modo de usuário de um pacote de segurança pode delegar solicitações selecionadas para informações para a instância do modo LSA do pacote.

Para obter detalhes sobre como os pacotes de segurança são inicializados para cada modo, consulte [inicialização do modo LSA](lsa-mode-initialization.md) e [inicialização do modo de usuário](user-mode-initialization.md).

 

 
