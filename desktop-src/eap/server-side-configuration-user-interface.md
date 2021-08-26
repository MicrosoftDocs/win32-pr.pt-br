---
title: Server-Side configuração Interface do Usuário
description: Implemente uma interface do usuário de configuração para o servidor implementando a interface COM, IEAPProviderConfig.
ms.assetid: b205c573-6694-42c0-b4f1-1480932dd644
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92bf6a1f5b5f0e1302e68dd8ca9070771bfbc7714759a384f67782ffdad6e2ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021806"
---
# <a name="server-side-configuration-user-interface"></a>Server-Side configuração Interface do Usuário

Implemente uma interface do usuário de configuração para o servidor implementando a interface COM, [**IEAPProviderConfig.**](/previous-versions/windows/desktop/api/Rrascfg/nn-rrascfg-ieapproviderconfig) Essa interface COM deriva de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e adiciona três métodos: [**IEAPProviderConfig::Initialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-initialize), [**IEAPProviderConfig::ServerInvokeConfigUI**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-serverinvokeconfigui)e [**IEAPProviderConfig::Uninitialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-uninitialize).

A interface do usuário deve dar suporte à administração remota. Em outras palavras, embora a interface do usuário configure o protocolo de autenticação no servidor, a própria interface do usuário pode estar em execução em um computador diferente. Para dar suporte à administração remota, separe o código da interface do usuário do código que realmente executa a configuração. O código de configuração reside no servidor no qual o protocolo de autenticação é executado.

Use o Active Template Library (ATL) para implementar [**IEAPProviderConfig**](/previous-versions/windows/desktop/api/Rrascfg/nn-rrascfg-ieapproviderconfig). Para obter mais informações, consulte a interface do usuário de configuração do lado do servidor de exemplo no diretório de exemplos do SDK. O CLSID (identificador de classe) para o objeto de interface do usuário de configuração deve ser colocado no Registro com um nome de valor [DE \_ RAS EAP \_ VALUENAME \_ \_ CLSID DE CONFIGURAÇÃO](authentication-protocol-registry-values.md). Para obter mais informações, consulte [Valores do Registro do Protocolo de Autenticação](authentication-protocol-registry-values.md).

Quando o usuário clica no botão Configurar para um protocolo de autenticação na caixa de diálogo Propriedades para Roteamento e RAS, o sistema verifica se existe um valor RAS \_ EAP \_ VALUENAME \_ CONFIG CLSID para esse protocolo de autenticação no \_ Registro. Em caso afirmativo, o COM instalita o objeto de interface do usuário de configuração. Se o sistema não conseguir encontrar RAS \_ EAP VALUENAME CONFIG CLSID no Registro e o sistema tiver acesso aos Serviços de Diretório \_ \_ (DS), o sistema tentará inciar o objeto do Armazenamento de \_ Classes.

No caso em que o usuário está conectado a vários máquinas simultaneamente, vários objetos de interface do usuário de configuração são instanados.

 

 