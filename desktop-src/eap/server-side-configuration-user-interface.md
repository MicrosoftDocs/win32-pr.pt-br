---
title: Interface do usuário de configuração do Server-Side
description: Implemente uma interface do usuário de configuração para o servidor implementando a interface COM, IEAPProviderConfig.
ms.assetid: b205c573-6694-42c0-b4f1-1480932dd644
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0904c90fea2bef3ccc00c00135be09a711d8454
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294004"
---
# <a name="server-side-configuration-user-interface"></a>Interface do usuário de configuração do Server-Side

Implemente uma interface do usuário de configuração para o servidor implementando a interface COM, [**IEAPProviderConfig**](/previous-versions/windows/desktop/api/Rrascfg/nn-rrascfg-ieapproviderconfig). Essa interface COM deriva de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e adiciona três métodos: [**IEAPProviderConfig:: Initialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-initialize), [**IEAPProviderConfig:: ServerInvokeConfigUI**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-serverinvokeconfigui)e [**IEAPProviderConfig:: Uninitialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-uninitialize).

A interface do usuário deve dar suporte à administração remota. Em outras palavras, embora a interface do usuário configure o protocolo de autenticação no servidor, a própria interface do usuário pode estar em execução em um computador diferente. Para dar suporte à administração remota, separe o código da interface do usuário do código que realmente executa a configuração. O código de configuração reside no servidor no qual o protocolo de autenticação é executado.

Use o Active Template Library (ATL) para implementar [**IEAPProviderConfig**](/previous-versions/windows/desktop/api/Rrascfg/nn-rrascfg-ieapproviderconfig). Para obter mais informações, consulte a interface do usuário de configuração do lado do servidor de exemplo no diretório de exemplos do SDK. O identificador de classe (CLSID) para o objeto de interface do usuário de configuração deve ser colocado no registro com um nome de valor de [RAS \_ EAP \_ valueName \_ config \_ CLSID](authentication-protocol-registry-values.md). Para obter mais informações, consulte [valores do registro do protocolo de autenticação](authentication-protocol-registry-values.md).

Quando o usuário clica no botão configurar para um protocolo de autenticação na caixa de diálogo Propriedades para roteamento e RAS, o sistema verifica se um \_ \_ \_ \_ valor de CLSID de configuração do EAP-valor do RAS para esse protocolo de autenticação existe no registro. Nesse caso, COM instancia o objeto de interface do usuário de configuração. Se o sistema não conseguir encontrar o \_ CLSID de configuração do valor de protocolo RAS EAP \_ \_ \_ no registro e o sistema tiver acesso aos serviços de diretório (DS), o sistema tentará criar uma instância do objeto a partir do armazenamento de classe.

No caso em que o usuário está conectado a várias máquinas simultaneamente, vários objetos de interface do usuário de configuração são instanciados.

 

 