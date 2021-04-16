---
description: O que é replicado
ms.assetid: d1f0bc92-37bc-4de2-876a-e6b8b09da58d
title: O que é replicado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2739cb0ff615ddc38f30a7aa9b0a572be5e28a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765751"
---
# <a name="what-gets-replicated"></a>O que é replicado

## <a name="applications"></a>Aplicativos

Todos os aplicativos instalados no computador de origem são replicados, exceto os seguintes:

<dl> <dt>

<span id="Non-COM__application_elements_and_dependencies"></span><span id="non-com__application_elements_and_dependencies"></span><span id="NON-COM__APPLICATION_ELEMENTS_AND_DEPENDENCIES"></span>Elementos e dependências não-COM + de aplicativo
</dt> <dd>

O administrador é responsável por replicar qualquer coisa de que um aplicativo COM+ depende, mas que não faz parte apropriada do próprio aplicativo, como arquivos de dados e DLLs. COMREPL não replicará nada fora dos elementos do aplicativo COM+.

</dd> <dt>

<span id="COM__preinstalled_applications"></span><span id="com__preinstalled_applications"></span><span id="COM__PREINSTALLED_APPLICATIONS"></span>Aplicativos pré-instalados COM+
</dt> <dd>

Os aplicativos que são usados internamente pelo COM+ e são instalados por meio do programa de instalação do COM+ não são replicados. Entre elas estão as seguintes:

-   Aplicativo do sistema
-   Utilitários COM+
-   Ouvinte de fila de mensagens mortas do QC COM+

</dd> <dt>

<span id="Applications_created_by_IIS"></span><span id="applications_created_by_iis"></span><span id="APPLICATIONS_CREATED_BY_IIS"></span>Aplicativos criados pelo IIS
</dt> <dd>

Esses aplicativos não são replicados e incluem o seguinte:

-   Aplicativos em processo do IIS
-   Utilitários do IIS
-   Todos os aplicativos criados para raízes virtuais isoladas ou em pool

</dd> </dl>

## <a name="computer-list"></a>Lista de computadores

Os computadores remotos chamados na pasta **computadores** na ferramenta de administração de serviços de componentes não serão replicados da origem para o computador de destino.

## <a name="properties"></a>Propriedades

As seguintes propriedades de coleção **LocalComputer** são replicadas:

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

As seguintes propriedades de coleção **LocalComputer** não são replicadas:

-   Descrição
-   ApplicationProxyRSN
-   Isroteador

Para obter descrições das propriedades da coleção **LocalComputer** , consulte [**LocalComputer**](localcomputer.md).

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

 

 



