---
description: Um aplicativo COM+ é essencialmente um constructo declarativo que permite configurar qualquer número de componentes em comum. Por exemplo, você pode configurar os componentes em um aplicativo com uma política de segurança comum.
ms.assetid: 50039b30-1c91-4e93-9f23-873accb651cf
title: Configurando aplicativos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d6c8caa8dc4ca949a71d9a6b56fd6eae95d415
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465993"
---
# <a name="configuring-com-applications"></a>Configurando aplicativos COM+

Um aplicativo COM+ é essencialmente um constructo declarativo que permite configurar qualquer número de componentes em comum. Por exemplo, você pode configurar os componentes em um aplicativo com uma política de segurança comum.

A configuração é uma parte essencial do processo de desenvolvimento para aplicativos COM+. A maneira como você configura um aplicativo determinará como o COM+ fornecerá serviços para ele e como ele se comporta durante a execução.

Você pode configurar aplicativos COM+ usando a ferramenta de administração dos Serviços de Componentes ou os objetos e interfaces de administração que fornecem a funcionalidade subjacente da ferramenta de administração. Para obter detalhes sobre como executar a administração com script, consulte [Automatizando a administração COM+.](automating-com--administration.md)

Você pode configurar elementos nos seguintes níveis em aplicativos COM+:

-   [Nível do aplicativo Configurações](#application-level-settings)
-   [Nível de componente (nível de classe) Configurações](#component-level-class-level-settings)
-   [Configuração no nível da interface](#interface-level-setting)
-   [Configuração de nível de método](#method-level-setting)
-   [Tópicos relacionados](#related-topics)

A maneira como você instala componentes em um aplicativo pode afetar como você pode configurá-los. Você sempre deve instalar componentes em aplicativos COM+ (em vez de importá-los). A instalação de componentes os registrará totalmente, juntamente com interfaces e bibliotecas de tipos, no RegDB (banco de dados de registro de classe COM+) para que você possa configurá-los.

## <a name="application-level-settings"></a>Application-Level Configurações



| Atributo                                                                                        | Descrição                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ativação](context-activation.md)<br/>                                                  | Especifica o tipo de aplicativo: aplicativo de servidor ou aplicativo de biblioteca.<br/>                                                                                                            |
| [Habilitando verificações de acesso](enabling-access-checks-for-an-application.md)<br/>               | Liga e desliga a verificação de segurança.<br/>                                                                                                                                                      |
| [Nível de segurança](setting-a-security-level-for-access-checks.md)<br/>                      | Especifica que as verificações de acesso serão executadas no nível do processo (níveis de verificação de acesso gerados de funções) ou em níveis de processo e de componente (segurança completa baseada em função).<br/> |
| [Nível de autenticação](setting-an-authentication-level-for-a-server-application.md)<br/>  | Define o nível de autenticação usado em chamadas para o aplicativo.<br/>                                                                                                                        |
| [Nível de representação](setting-an-impersonation-level.md)<br/>                             | Define o nível de representação usado em chamadas para outros aplicativos.<br/>                                                                                                                        |
| [Enfileiramento](creating-queuable-components.md)<br/>                                           | Especifica que os componentes do aplicativo usarão serviços de en fila.<br/>                                                                                                                         |
| [Habilitar CRM](configuring-com--crm-components.md)<br/>                                     | Habilita o uso de Compensating Resource Managers.<br/>                                                                                                                                           |
| [Executar aplicativo como serviço](com--applications-running-as-service-applications.md)<br/> | Configura e implementa um aplicativo de servidor COM+ como um serviço NT.<br/>                                                                                                                    |
| [Serviço SOAP COM+](com--soap-service.md)<br/>                                            | Expõe um aplicativo COM+ como um serviço Web XML.<br/>                                                                                                                                        |
| [Pooling de aplicativos](com--application-pooling.md)<br/>                                   | Adiciona escalabilidade para processos de thread único e integra-se ao serviço de Reciclagem de Aplicativos COM+.<br/>                                                                               |
| [Reciclagem de aplicativos](com--application-recycling.md)<br/>                               | Aumenta a estabilidade do aplicativo desligando normalmente um processo associado a um aplicativo e reiniciando-o.<br/>                                                                  |
| [Processo de despejo](what-s-new-in-com--1-5.md)<br/>                                         | Despeja todo o estado de um processo sem finalização, para fins de depuração.<br/>                                                                                                      |
| Desligamento do processo do servidor<br/>                                                               | Desliga um processo após um período ocioso especificado.<br/>                                                                                                                                      |
| Permissões<br/>                                                                           | Desabilita as alterações nas definições de configuração, incluindo a exclusão.<br/>                                                                                                                          |
| Identidade de segurança<br/>                                                                     | Especifica a identidade sob a qual o aplicativo é executado.<br/>                                                                                                                                 |
| Iniciar no depurador<br/>                                                                    | Especifica que o aplicativo será lançado em um depurador, com configurações de linha de comando especificadas pelo usuário.<br/>                                                                                |
| Habilitar suporte a 3 GB<br/>                                                                    | Habilita o uso do espaço de endereço de memória de processo estendido.<br/>                                                                                                                                    |



 

## <a name="component-level-class-level-settings"></a>Component-Level (nível de classe) Configurações




| Atributo | Descrição | 
|-----------|-------------|
| <a href="configuring-transactions.md">Transações</a><br /> | Define os requisitos automáticos de transação desabilitados, sem suporte, com suporte, obrigatórios ou requer novos.<br /> | 
| <a href="setting-the-synchronization-attribute.md">Sincronização</a><br /> | Define os requisitos de sincronização desabilitados, sem suporte, com suporte, obrigatórios ou requer novos.<br /> | 
| <a href="enabling-jit-activation-for-a-component.md">Ativação JIT</a><br /> | Habilita a ativação Just-In-Time.<br /> | 
| <a href="configuring-a-component-to-be-pooled.md">Pool de objetos</a><br /> | Habilita o pool de objetos. O tamanho mínimo e máximo do pool e os valores de tempo limite do objeto são configuráveis.<br /> | 
| <a href="specifying-an-object-constructor-string-for-a-component.md">Construção de objeto</a><br /> | Habilita a construção de objeto parametrizado com uma cadeia de caracteres de construtor especificada administrativamente. <br /><blockquote>[!Note]<br />A cadeia de caracteres do construtor não deve ser usada para armazenar informações confidenciais de segurança.</blockquote><br /> | 
| <a href="enabling-access-checks-at-the-component-level.md">Verificações de acesso no nível do componente</a><br /> | Liga ou desliga a verificação de segurança baseada em função no nível do componente.<br /> | 
| <a href="assigning-roles-to-components--interfaces--or-methods.md">Atribuição de função declarativa</a><br /> | Habilita a atribuição explícita de funções ao componente.<br /> | 
| <a href="persistent-client-side-failures.md">Classe de exceção na fila</a><br /> | Indica uma classe de exceção para lidar com falhas do lado do cliente.<br /> | 
| <a href="com--instrumentation-concepts.md">Eventos e estatísticas de instrumentação</a><br /> | Habilita relatórios detalhados de estatísticas de objeto e evento do sistema.<br /> | 
| <a href="context-activation.md">Contexto de ativação</a><br /> | Habilita a ativação forçada de um objeto no contexto ou contexto padrão do chamador.<br /> | 
| <a href="what-s-new-in-com--1-5.md">Criando componentes privados</a><br /> | Marca o componente como privado para o aplicativo. Um componente privado pode ser visto e ativado somente por outros componentes no mesmo aplicativo.<br /> | 




 

## <a name="interface-level-setting"></a>Interface-Level configuração



| Atributo                                                                                           | Descrição                                                                                                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Em fila](creating-queuable-components.md)<br/>                                               | Indica uma interface que pode ser envelhável, definida em IDL.<br/>                                                                       |
| [Atribuição de função declarativa](assigning-roles-to-components--interfaces--or-methods.md)<br/> | Habilita a atribuição explícita de funções à interface, bem como funções herdadas implicitamente do nível do componente.<br/> |



 

## <a name="method-level-setting"></a>Method-Level configuração



| Atributo                                                                                           | Descrição                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Auto-done](enabling-auto-done-for-a-method.md)<br/>                                         | Desativa automaticamente o objeto no retorno do método e vota na transação.<br/>                                                       |
| [Atribuição de função declarativa](assigning-roles-to-components--interfaces--or-methods.md)<br/> | Habilita a atribuição explícita de funções ao método, bem como funções herdadas implicitamente dos níveis de interface e componente.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Automatizando a administração COM+](automating-com--administration.md)
</dt> <dt>

[Criando aplicativos COM+](creating-com--applications.md)
</dt> <dt>

[Implantando aplicativos COM+](deploying-com--applications.md)
</dt> </dl>

 

 




