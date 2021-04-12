---
description: Conceitos do aplicativo de serviço COM+
ms.assetid: d6b1cf4a-ca39-4d50-a33d-aa639937ef9e
title: Conceitos do aplicativo de serviço COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b24db7a031ed0520f30891d98688af67e853ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456961"
---
# <a name="com-service-application-concepts"></a>Conceitos do aplicativo de serviço COM+

Você pode usar a ferramenta administrativa serviços de componentes para configurar um aplicativo de servidor do COM+ como um aplicativo de serviço. A execução de um aplicativo de servidor COM+ como um serviço oferece as seguintes vantagens:

-   Se seu aplicativo sempre precisar ser executado, os serviços de componentes podem, opcionalmente, fazer com que o servidor seja iniciado automaticamente e também poderá reiniciar o servidor se ele atingir o tempo limite. Por exemplo, se um computador executando componentes de ouvinte de componentes enfileirados for reinicializado, os ouvintes de componentes em fila poderão ser iniciados automaticamente se estiverem configurados como um serviço.
-   Se seu aplicativo precisar executar operações privilegiadas, o aplicativo poderá ser executado como a conta do sistema local. Somente os serviços NT podem ser executados com esse nível de segurança. O aplicativo será compatível com o Serviço de cluster do Windows, que gerencia os serviços durante o failover do sistema.
-   Se outros serviços precisarem ser marcados como dependentes, os serviços de componentes fornecerão essa opção. Por exemplo, se seu aplicativo utiliza a funcionalidade fornecida por outro serviço, o serviço marcado como dependente será iniciado antes do aplicativo ser iniciado.

## <a name="starting-an-application-automatically"></a>Iniciando um aplicativo automaticamente

Quando o aplicativo do servidor COM+ é iniciado automaticamente, ele atua como um serviço, exigindo que o desenvolvedor gerencie o servidor usando a ferramenta administrativa serviços.

> [!Note]  
> A ferramenta administrativa serviços pode ser acessada iniciando a ferramenta administrativa serviços de componentes e clicando em **Serviços (local)**.

 

## <a name="starting-an-application-manually"></a>Iniciando um aplicativo manualmente

Quando o aplicativo do servidor COM+ é iniciado manualmente, ele atua como um host DLL com as configurações de segurança de um serviço. O serviço será iniciado manualmente quando for ativado e desligado automaticamente quando atingir o tempo limite.

## <a name="service-configurations"></a>Configurações de Serviço

Independentemente do tipo de inicialização, o aplicativo pode ser configurado para ser executado como uma conta do sistema local ou atribuído a uma conta de usuário. O sistema local e a conta de usuário podem ser configurados no momento da criação do serviço. Para definir as configurações de segurança, a ferramenta administrativa serviços precisará ser usada. As dependências também podem ser definidas para o serviço.

O aplicativo também pode ser iniciado em qualquer ordem específica, selecionando dependências de uma lista de outros serviços do sistema. Por exemplo, os serviços do sistema podem ser marcados como dependentes e não iniciarão o aplicativo até que os serviços do sistema tenham sido iniciados na ordem especificada. Isso inicializará corretamente o aplicativo de serviço antes de ser usado.

Para obter instruções passo a passo sobre como configurar um aplicativo COM+ para ser executado como um serviço, consulte [Configurando um aplicativo de servidor com+ como um aplicativo de serviço](configuring-a-com--server-application-as-a-service-application.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas do aplicativo de serviço COM+](com--service-application-tasks.md)
</dt> </dl>

 

 



