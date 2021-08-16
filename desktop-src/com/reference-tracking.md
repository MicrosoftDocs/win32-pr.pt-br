---
title: Acompanhamento de referência
description: Acompanhamento de referência
ms.assetid: 1e2cf555-3b96-42d5-a0bb-abb720c93520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1321c922cc0a7493e3e4792f7c0f925618330c2e42665296fb06792635a4ea70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309759"
---
# <a name="reference-tracking"></a>Acompanhamento de referência

O acompanhamento de referência pode impedir a versão inicial não intencional ou mal-intencionada de objetos.

Ao habilitar o acompanhamento de referência, você está solicitando que as chamadas [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) distribuídas sejam autenticadas pelo COM. Quando o controle de referência está habilitado, o COM mantém o  controle das contagens de referência por usuário para que um usuário possa chamar a Versão somente em objetos que o usuário chamou **anteriormente de AddRef** on. Embora o acompanhamento de referência possa diminuir o desempenho, ele garante que, não importa quantas vezes um determinado usuário chama **Release**, os objetos e stubs ainda existirão se outra pessoa tiver uma referência a eles.

O cliente pode definir o acompanhamento de referência para um processo passando o sinalizador de funcionalidade EOAC SECURE REFS em uma chamada \_ \_ para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Você também pode habilitar ou desabilitar o acompanhamento de referência para todos os aplicativos em um computador usando Dcomcnfg.exe.

Se o controle de referência estiver habilitado, [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) sempre usará as configurações de segurança padrão. Nesse caso, as chamadas para [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) **em IUnknown** falharão.

 

 