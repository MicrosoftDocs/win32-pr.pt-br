---
description: Configurando direitos administrativos para uma partição
ms.assetid: d38e4a63-9ff9-4acb-bb7e-d6c96644bd32
title: Configurando direitos administrativos para uma partição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c421b37dd50fa21ee9cf146749ec00b0c91d98c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646344"
---
# <a name="setting-administrative-rights-for-a-partition"></a>Configurando direitos administrativos para uma partição

Os usuários atribuídos à função de administrador do aplicativo do sistema COM+ têm permissão para criar, modificar e excluir partições COM+. Na ferramenta administrativa serviços de componentes, as funções administrativas podem ser atribuídas aos usuários expandindo a pasta **funções** do aplicativo de sistema com+.

A partir do Windows Server 2003, o recurso de autenticação para o aplicativo de sistema COM+ inclui o valor EOAC \_ Disable \_ AAA. Esse valor, que desabilita as ativações de Activate-as-Activator (AAA), é usado na chamada [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ao iniciar o aplicativo do sistema. Definir o recurso de autenticação como EOAC \_ Disable \_ AAA permite que um aplicativo executado em uma conta com privilégios (como LocalSystem) ajude a impedir que sua identidade seja usada para iniciar componentes não confiáveis.

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

 

 
