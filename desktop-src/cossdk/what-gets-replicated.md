---
description: O que é replicado
ms.assetid: d1f0bc92-37bc-4de2-876a-e6b8b09da58d
title: O que é replicado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60b08151c14d0254bd856fe2ee5b7b83d85714d1b435a32817bf66cc11a1e81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636646"
---
# <a name="what-gets-replicated"></a>O que é replicado

## <a name="applications"></a>Aplicativos

Todos os aplicativos instalados no computador de origem são replicados, exceto pelo seguinte:

<dl> <dt>

<span id="Non-COM__application_elements_and_dependencies"></span><span id="non-com__application_elements_and_dependencies"></span><span id="NON-COM__APPLICATION_ELEMENTS_AND_DEPENDENCIES"></span>Dependências e elementos de aplicativo não COM+
</dt> <dd>

O administrador é responsável por replicar tudo o que um aplicativo COM+ depende, mas que não faz parte adequadamente do próprio aplicativo, como arquivos de dados e DLLs. COMREPL não replicará nada fora dos elementos do aplicativo COM+.

</dd> <dt>

<span id="COM__preinstalled_applications"></span><span id="com__preinstalled_applications"></span><span id="COM__PREINSTALLED_APPLICATIONS"></span>Aplicativos pré-instalados com+
</dt> <dd>

Os aplicativos que são usados internamente pelo COM+ e são instalados por meio do programa de instalação COM+ não são replicados. Entre elas estão as seguintes:

-   Aplicativo do sistema
-   Utilitários COM+
-   Ouvinte da fila de letra morta do QC COM+

</dd> <dt>

<span id="Applications_created_by_IIS"></span><span id="applications_created_by_iis"></span><span id="APPLICATIONS_CREATED_BY_IIS"></span>Aplicativos criados pelo IIS
</dt> <dd>

Esses aplicativos não são replicados e incluem o seguinte:

-   Aplicativos em processo do IIS
-   Utilitários do IIS
-   Todos os aplicativos criados para raízes virtuais isoladas ou em pool

</dd> </dl>

## <a name="computer-list"></a>Lista de computadores

Os computadores remotos nomeados na **pasta Computadores** na ferramenta de administração dos Serviços de Componentes não serão replicados da origem para o computador de destino.

## <a name="properties"></a>Propriedades

As seguintes **propriedades da coleção LocalComputer** são replicadas:

-   TransactionTimeout
-   ResourcePoolingEnabled
-   DCOMEnabled
-   DefaultAuthenticationLevel
-   DefaultImpersonationLevel
-   SecurityTrackingEnabled
-   CISEnabled
-   SecureReferencesEnabled
-   InternetPortsListed
-   DeafultToInternetPorts
-   Portas
-   RpcProxyEnabled

As seguintes **propriedades da coleção LocalComputer** não são replicadas:

-   Descrição
-   ApplicationProxyRSN
-   IsRouter

Para ver descrições das **propriedades da coleção LocalComputer,** consulte [**LocalComputer**](localcomputer.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciamento de Arquivos](file-management.md)
</dt> <dt>

[Registro em log e relatório de erros](logging-and-error-reporting.md)
</dt> <dt>

[Fases de replicação](replication-phases.md)
</dt> <dt>

[Usando COMREPL](using-comrepl.md)
</dt> </dl>

 

 



