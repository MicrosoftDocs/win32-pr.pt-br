---
title: Administrando o cache de pares
description: Observação a partir do Windows 7, o modelo de cache de pares de Serviço de Transferência Inteligente em Segundo Plano (BITS) 3,0 é preterido.
ms.assetid: a33a43e5-02f9-4902-ad3a-ec65b0d80520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b3ea1dd19c9aca855ffd73e174dcb3b588a54d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635193"
---
# <a name="administering-the-peer-cache"></a>Administrando o cache de pares

> [!Note]  
> A partir do Windows 7, o modelo de cache de pares Serviço de Transferência Inteligente em Segundo Plano (BITS) 3,0 é preterido. Se o BITS 4,0 estiver instalado, o modelo de cache de pares de BITS 3,0 estará indisponível.

 

Para melhorar o desempenho do download, o BITS permite que você baixe o conteúdo de computadores pares. Para habilitar esse recurso, o administrador deve habilitar a configuração da política de grupo EnablePeerCaching. Se habilitada, o par pode baixar conteúdo de pares e fornecer conteúdo a pares. O administrador também pode usar as configurações de política DisablePeerCachingClient e DisablePeerCachingServer para evitar o download de conteúdo de um par ou o fornecimento de conteúdo a pares, respectivamente.

Se as configurações de política de grupo não estiverem configuradas, um aplicativo poderá chamar o método [**IBitsPeerCacheAdministration:: SetConfigurationFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags) para definir a preferência de cache de sistemas pares para o computador. Observe que essas preferências são substituídas pelas configurações da política de grupo se elas forem definidas mais tarde. Para determinar se o computador habilita o cache de pares, chame o método [**IBitsPeerCacheAdministration:: GetConfigurationFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-getconfigurationflags) .

Se o cache de pares estiver habilitado, o BITS só armazenará em cache o conteúdo de um trabalho se o trabalho permitir explicitamente que seu conteúdo seja armazenado em cache. O BITS também baixará apenas o conteúdo de um par se o trabalho permitir explicitamente. Para habilitar o cache de sistemas pares para um trabalho, chame o método [**IBackgroundCopyJob4:: SetPeerCachingFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags) .

Além de usar Política de Grupo ou a interface [**IBitsPeerCacheAdministration**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) para habilitar o cache de pares, você também pode usar qualquer um dos métodos para alterar o tamanho do cache padrão e o período de tempo que um arquivo não acessado permanece no cache. Para alterar os padrões usando a interface **IBitsPeerCacheAdministration** , chame os métodos [**SetMaximumCacheSize**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setmaximumcachesize) e [**SetMaximumContentAge**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setmaximumcontentage) . Como esses métodos definem as configurações de preferência, eles são substituídos pelas configurações da política de grupo.

Para listar os pares dos quais o BITS tentará baixar o conteúdo, chame o método [**IBitsPeerCacheAdministration:: EnumPeers**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-enumpeers) .

Para listar os arquivos no cache que o BITS vai atender aos pares, chame o método [**IBitsPeerCacheAdministration:: EnumRecords**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-enumrecords) .

Você nunca deve gerenciar o cache de sistemas pares com relação à descoberta de pares ou exclusão de registros de cache. Essa funcionalidade foi incluída na interface [**IBitsPeerCacheAdministration**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) para fins de integridade.

 

 




