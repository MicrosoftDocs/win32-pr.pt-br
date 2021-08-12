---
description: Conceitos do aplicativo de serviço COM+
ms.assetid: d6b1cf4a-ca39-4d50-a33d-aa639937ef9e
title: Conceitos do aplicativo de serviço COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0d0cedae4af19825e6e48a0e2aded102f96bed0c08b45c48cfb2f7e3bbd52ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548762"
---
# <a name="com-service-application-concepts"></a>Conceitos do aplicativo de serviço COM+

Você pode usar a ferramenta administrativa serviços de componentes para configurar um aplicativo de servidor COM+ como um aplicativo de serviço. A execução de um aplicativo de servidor COM+ como serviço oferece as seguintes vantagens:

-   Se o aplicativo sempre precisar estar em execução, os Serviços de Componentes poderão, opcionalmente, fazer com que o servidor seja iniciado automaticamente e também pode reiniciar o servidor se ele esgotar. Por exemplo, se um computador que executa componentes de ouvinte de Componentes Em Fila for reinicializado, os ouvintes de Componentes En en fila poderão ser iniciados automaticamente se eles estão configurados como um serviço.
-   Se o aplicativo precisar executar operações privilegiadas, o aplicativo poderá ser executado como a conta do sistema local. Somente os serviços NT têm permissão para executar com esse nível de segurança. O aplicativo será compatível com o Windows Serviço de cluster, que gerencia serviços durante o failover do sistema.
-   Se outros serviços precisam ser marcados como dependentes, os Serviços de Componentes fornece essa opção. Por exemplo, se seu aplicativo usar a funcionalidade fornecida por outro serviço, o serviço marcado como dependente será iniciado antes do início do aplicativo.

## <a name="starting-an-application-automatically"></a>Iniciando um aplicativo automaticamente

Quando o aplicativo de servidor COM+ é iniciado automaticamente, ele atua como um serviço, exigindo que o desenvolvedor gerencie o servidor usando a ferramenta administrativa Serviços.

> [!Note]  
> A ferramenta administrativa Serviços pode ser acessada iniciando a ferramenta administrativa serviços de componentes e clicando **em Serviços (Local)**.

 

## <a name="starting-an-application-manually"></a>Iniciando um aplicativo manualmente

Quando o aplicativo de servidor COM+ é iniciado manualmente, ele atua como um host DLL com as configurações de segurança de um serviço. O serviço será iniciado manualmente quando ativado e desligado automaticamente quando o tempo for encerrado.

## <a name="service-configurations"></a>Configurações de Serviço

Independentemente do tipo de inicialização, o aplicativo pode ser configurado para ser executado como uma conta do sistema local ou atribuído a uma conta de usuário. O sistema local e a conta de usuário podem ser configurados no momento da criação do serviço. Para definir as configurações de segurança, a ferramenta administrativa Serviços terá que ser usada. As dependências também podem ser definidas para o serviço.

O aplicativo também pode ser iniciado em qualquer ordem específica selecionando dependências em uma lista de outros serviços do sistema. Por exemplo, os serviços do sistema podem ser marcados como dependentes e não iniciarão o aplicativo até que os serviços do sistema tenham sido iniciados na ordem especificada. Isso inicializa corretamente o aplicativo de serviço antes de ser usado.

Para uma instrução passo a passo sobre como configurar um aplicativo COM+ para ser executado como um serviço, consulte Configurando um aplicativo de servidor [COM+ como um aplicativo de serviço](configuring-a-com--server-application-as-a-service-application.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas do aplicativo de serviço COM+](com--service-application-tasks.md)
</dt> </dl>

 

 



