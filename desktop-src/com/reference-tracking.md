---
title: Acompanhamento de referência
description: Acompanhamento de referência
ms.assetid: 1e2cf555-3b96-42d5-a0bb-abb720c93520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45607a495e973ec33acde6d97cb1f83259a27c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454363"
---
# <a name="reference-tracking"></a>Acompanhamento de referência

O controle de referência pode impedir a liberação antecipada involuntária ou mal-intencionada de objetos.

Quando você habilita o acompanhamento de referência, está solicitando que as chamadas distribuídas do [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e do [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sejam autenticadas pelo com. Quando o controle de referência está habilitado, o COM controla as contagens de referência por usuário para que um usuário possa chamar **Release** somente em objetos que o usuário chamou anteriormente no **AddRef** . Embora o controle de referência possa diminuir o desempenho, ele garante que, independentemente de quantas vezes um determinado usuário chamar a **versão**, os objetos e stubs ainda existirão se outra pessoa tiver uma referência a eles.

O cliente pode definir o acompanhamento de referência para um processo passando o \_ sinalizador de capacidade de REFS EOAC seguro \_ em uma chamada para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Você também pode habilitar ou desabilitar o controle de referência para todos os aplicativos em um computador usando Dcomcnfg.exe.

Se o acompanhamento de referência estiver habilitado, [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) sempre usará as configurações de segurança padrão. Nesse caso, as chamadas para [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) em **IUnknown** falharão.

 

 