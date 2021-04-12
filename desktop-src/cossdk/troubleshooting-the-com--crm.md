---
description: Solucionando problemas do CRM do COM+
ms.assetid: 4d2d9372-b540-4e08-9b57-8687802610b6
title: Solucionando problemas do CRM do COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b04e37d183dbf3df8d017e780917f955e14a033
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501003"
---
# <a name="troubleshooting-the-com-crm"></a>Solucionando problemas do CRM do COM+

Veja a seguir os problemas mais comuns encontrados ao desenvolver e usar o CRM do COM+:

-   **Mensagens do log de eventos.** Se o aplicativo do servidor do CRM encontrar um erro interno sério, ele será FailFast (encerrar o processo do aplicativo do servidor do CRM) e gravará uma mensagem no log de eventos do Windows. Consulte o log de eventos se algum problema for encontrado.

-   **Exceções do compensador de CRM.** A infra-estrutura de CRM cria o compensador de CRM e passa as notificações de resultado da transação e os registros de log gravados pelo trabalhador do CRM. Se o compensador de CRM retornar um erro ou lançar uma exceção, ele será capturado pela infraestrutura do CRM e causará um FailFast. Uma mensagem no log de eventos indica que uma exceção foi recebida do compensador de CRM. É possível forçar essas exceções a serem ignoradas. (Consulte [configurações do registro do CRM do com+](com--crm-registry-settings.md).) As exceções do compensador de CRM provavelmente significam um problema no componente compensador de CRM específico e não na própria infraestrutura de CRM.

-   **Rastreamento de recuperação.** O rastreamento de recuperação pode ser muito útil para determinar problemas durante a recuperação. Para obter informações sobre como habilitar o rastreamento de recuperação, consulte [configurações do registro do com+ CRM](com--crm-registry-settings.md).

-   **Tentando executar com o CRM não habilitado.** Não é suficiente simplesmente posicionar os componentes de trabalho de CRM e compensador de CRM no aplicativo do servidor COM+. O suporte para CRMs deve ser habilitado especificamente para o aplicativo de servidor COM+ específico usando a opção **habilitar gerenciadores de recursos de compensação** na guia **avançado** das páginas de propriedades do aplicativo com+. (Consulte [Configurando componentes do com+ CRM](configuring-com--crm-components.md) para obter mais informações.) Se for feita uma tentativa de usar um CRM dentro de um aplicativo de servidor que não tenha o CRM habilitado, um código de erro será retornado para o trabalhador do CRM.

-   **Tentando executar CRMs em processos de cliente.** CRMs não são executados em processos de cliente; Eles devem ser executados em um processo de aplicativo do servidor COM+. Os componentes do CRM podem ser colocados em um pacote de biblioteca para uso por vários aplicativos de servidor COM+, mas não estão disponíveis para uso em processos de cliente. A tentativa de usar as interfaces do CRM dentro de um processo de cliente retorna um código de erro para o trabalhador do CRM.

-   **Recuperação em andamento.** A recuperação é iniciada quando um aplicativo do servidor CRM é iniciado. No entanto, a recuperação ocorre em segundo plano durante o processamento normal do aplicativo do servidor do CRM. O trabalhador do CRM pode ser criado antes da conclusão da recuperação. CRMs não pode ser usado em um processo de aplicativo do servidor CRM até que a recuperação tenha sido concluída com êxito. Nesse caso, o trabalhador do CRM recebe um código de erro "recuperação em andamento" ao tentar registrar o compensador de CRM. O trabalhador do CRM deve sondar ou, de outra forma, atrasar até que a recuperação tenha sido concluída. O tempo de recuperação é específico para um tipo específico de CRM, e isso deve ser considerado durante a criação do CRM. As recuperações de longa duração não são desejáveis.

-   **Segurança no arquivo de log do CRM.** Se o acesso ao arquivo de log do CRM for negado, consulte [considerações de segurança do CRM do com+](com--crm-security-considerations.md) para obter uma descrição de como a segurança é definida no arquivo de log do CRM.

-   **Transações incertas.** Em casos raros, uma transação DTC pode entrar no estado em dúvida; ou seja, o DTC não pode determinar o resultado da transação. Nesses casos, durante a recuperação, o CRM mantém os registros de log para essa transação no arquivo de log do CRM. Quando a transação incerta tiver sido resolvida pelo DTC, a execução de outra recuperação do CRM concluirá a transação.

-   **Criação e lançamento do compensador de CRM.** Na primeira vez que um compensador de CRM é registrado por um trabalhador de CRM, ele é criado pela infraestrutura de CRM e consultado para determinar em quais interfaces de compensador de CRM ele dá suporte. Em seguida, ele é lançado imediatamente. Os compensadores de CRM precisam dar suporte à capacidade de criação e liberação sem ter tido nenhuma chamada de método interveniente. Se o compensador de CRM não puder ser criado corretamente, talvez devido ao registro COM incorreto ou se ele não oferecer suporte a pelo menos uma das interfaces de compensador de CRM corretas, um código de erro será retornado ao trabalhador do CRM.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do Gerenciador de recursos de compensação COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



