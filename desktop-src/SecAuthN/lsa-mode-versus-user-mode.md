---
description: Quando um pacote de segurança SSP/AP está funcionando como um pacote de autenticação, ele é carregado no espaço de processo da LSA (Autoridade de Segurança Local) e é dito que está no modo LSA.
ms.assetid: ff4e61be-dbaa-4cfa-8c72-43e99fe1c3cb
title: Modo LSA versus Modo de Usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aa965cd66f43548243c1e62329e6d9d337a2a0123344a8cb9f10915846a765f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922075"
---
# <a name="lsa-mode-vs-user-mode"></a>Modo LSA versus Modo de Usuário

Quando um pacote [](../secgloss/s-gly.md) de segurança SSP/AP está funcionando como um pacote de autenticação [*,*](../secgloss/a-gly.md)ele é carregado no espaço de processo da LSA (Autoridade de Segurança [*Local)*](../secgloss/l-gly.md) e é dito que está no modo LSA. Os aplicativos de logon acessam a funcionalidade do pacote de autenticação usando as Funções de [Logon LSA](authentication-functions.md). Os desenvolvedores podem usar funções de suporte LSA disponíveis somente para pacotes de segurança no modo LSA para implementar pacotes de autenticação mais sofisticados do que os com suporte anteriormente.

Quando um [*pacote de segurança*](../secgloss/s-gly.md) fornece serviços de segurança para um aplicativo cliente/servidor, ele é carregado nos processos de cliente e servidor e é dito que está no modo de usuário. Aplicativos cliente/servidor acessam os serviços de suporte de segurança do pacote de segurança usando o SSPI [*(Interface*](../secgloss/s-gly.md) do Provedor de Suporte de Segurança) da Microsoft.

O suporte de LSA para SSP/APs inclui funções que as instâncias de modo LSA e modo de usuário de um pacote de segurança podem usar para se comunicar. Além disso, a instância de modo de usuário de um pacote de segurança pode delegar solicitações selecionadas para informações para a instância de modo LSA do pacote.

Para obter detalhes sobre como os pacotes de segurança são inicializados para cada modo, consulte Inicialização do modo [LSA](lsa-mode-initialization.md) e [Inicialização do modo de usuário](user-mode-initialization.md).

 

 
