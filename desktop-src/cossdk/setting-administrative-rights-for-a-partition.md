---
description: Definindo direitos administrativos para uma partição
ms.assetid: d38e4a63-9ff9-4acb-bb7e-d6c96644bd32
title: Definindo direitos administrativos para uma partição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33431c5beff76e015d28b6a7e886823620126f2ed9b84db68af9a8f3b8ac1d28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915819"
---
# <a name="setting-administrative-rights-for-a-partition"></a>Definindo direitos administrativos para uma partição

Os usuários atribuídos à função Administrador do Aplicativo do Sistema COM+ têm permissão para criar, modificar e excluir partições COM+. Na ferramenta administrativa Serviços de Componentes, as funções  administrativas podem ser atribuídas aos usuários expandindo a pasta Funções do Aplicativo do Sistema COM+.

A partir Windows Server 2003, a funcionalidade de autenticação para o aplicativo do sistema COM+ inclui o valor EOAC \_ DISABLE \_ AAA. Esse valor, que desabilita ativações como ativador (AAA), é usado na chamada [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ao iniciar o aplicativo do sistema. Definir a funcionalidade de autenticação como EOAC DISABLE AAA permite que um aplicativo executado em uma conta privilegiada \_ (como LocalSystem) ajude a impedir que sua identidade seja usada para iniciar componentes não \_ confidenciais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Coletando métricas de partição](collecting-partition-metrics.md)
</dt> <dt>

[Configurando o cache de partição](configuring-the-partition-cache.md)
</dt> <dt>

[Agrupando aplicativos em partições](grouping-applications-into-partitions.md)
</dt> <dt>

[Gerenciando partições locais](managing-local-partitions.md)
</dt> <dt>

[Gerenciando partições no Active Directory](managing-partitions-within-active-directory.md)
</dt> </dl>

 

 
