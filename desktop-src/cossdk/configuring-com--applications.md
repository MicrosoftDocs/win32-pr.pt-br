---
description: Um aplicativo COM+ é essencialmente um Construtor declarativo que permite que você configure qualquer número de componentes em comum. Por exemplo, você pode configurar os componentes em um aplicativo com uma política de segurança comum.
ms.assetid: 50039b30-1c91-4e93-9f23-873accb651cf
title: Configurando aplicativos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16319baf7e34348751e9cafd0efcbd99906d0985
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789262"
---
# <a name="configuring-com-applications"></a>Configurando aplicativos COM+

Um aplicativo COM+ é essencialmente um Construtor declarativo que permite que você configure qualquer número de componentes em comum. Por exemplo, você pode configurar os componentes em um aplicativo com uma política de segurança comum.

A configuração é uma parte essencial do processo de desenvolvimento para aplicativos COM+. A maneira como você configura um aplicativo determinará como o COM+ fornecerá serviços para ele e como ele se comporta durante a execução.

Você pode configurar aplicativos COM+ usando a ferramenta de administração de serviços de componentes ou os objetos e as interfaces de administração programáveis que fornecem a funcionalidade subjacente da ferramenta de administração. Para obter detalhes sobre como executar a administração com script, consulte [automatizando a administração do com+](automating-com--administration.md).

Você pode configurar elementos nos seguintes níveis em aplicativos COM+:

-   [Configurações de nível de aplicativo](#application-level-settings)
-   [Configurações de nível de componente (nível de classe)](#component-level-class-level-settings)
-   [Configuração de nível de interface](#interface-level-setting)
-   [Configuração de nível de método](#method-level-setting)
-   [Tópicos relacionados](#related-topics)

A maneira como você instala componentes em um aplicativo pode afetar como você pode configurá-los. Você sempre deve instalar componentes em aplicativos COM+ (em vez de importá-los). A instalação de componentes irá registrá-los totalmente, juntamente com interfaces e bibliotecas de tipos, no banco de dados de registro de classe COM+ (RegDB) para que você possa configurá-los.

## <a name="application-level-settings"></a>Configurações de Application-Level



| Atributo                                                                                        | Descrição                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ativação](context-activation.md)<br/>                                                  | Especifica o tipo de aplicativo: servidor de aplicativos ou aplicativo de biblioteca.<br/>                                                                                                            |
| [Habilitando verificações de acesso](enabling-access-checks-for-an-application.md)<br/>               | Ativa e desativa a verificação de segurança.<br/>                                                                                                                                                      |
| [Nível de segurança](setting-a-security-level-for-access-checks.md)<br/>                      | Especifica que as verificações de acesso serão executadas no nível do processo (níveis de verificação de acesso gerados a partir de funções) ou no processo e em níveis de componente (segurança baseada em função completa).<br/> |
| [Nível de autenticação](setting-an-authentication-level-for-a-server-application.md)<br/>  | Define o nível de autenticação usado em chamadas para o aplicativo.<br/>                                                                                                                        |
| [Nível de representação](setting-an-impersonation-level.md)<br/>                             | Define o nível de representação usado em chamadas para outros aplicativos.<br/>                                                                                                                        |
| [Serviço](creating-queuable-components.md)<br/>                                           | Especifica que os componentes de aplicativo usarão serviços de enfileiramento.<br/>                                                                                                                         |
| [Habilitar CRM](configuring-com--crm-components.md)<br/>                                     | Habilita o uso de gerenciadores de recursos de compensação.<br/>                                                                                                                                           |
| [Executar aplicativo como serviço](com--applications-running-as-service-applications.md)<br/> | Configura e implementa um aplicativo de servidor COM+ como um serviço NT.<br/>                                                                                                                    |
| [Serviço SOAP COM+](com--soap-service.md)<br/>                                            | Expõe um aplicativo COM+ como um serviço Web XML.<br/>                                                                                                                                        |
| [Pool de aplicativos](com--application-pooling.md)<br/>                                   | Adiciona escalabilidade para processos de thread único e integra-se com o serviço de reciclagem de aplicativo COM+.<br/>                                                                               |
| [Reciclagem de aplicativos](com--application-recycling.md)<br/>                               | Aumenta a estabilidade do aplicativo, desligando um processo associado a um aplicativo e reiniciando-o.<br/>                                                                  |
| [Despejo de processo](what-s-new-in-com--1-5.md)<br/>                                         | Despeja o estado inteiro de um processo sem encerrá-lo, para fins de depuração.<br/>                                                                                                      |
| Desligamento de processo do servidor<br/>                                                               | Desliga um processo após um período ocioso especificado.<br/>                                                                                                                                      |
| Permissões<br/>                                                                           | Desabilita as alterações nas definições de configuração, incluindo a exclusão.<br/>                                                                                                                          |
| Identidade de segurança<br/>                                                                     | Especifica a identidade sob a qual o aplicativo é executado.<br/>                                                                                                                                 |
| Iniciar no depurador<br/>                                                                    | Especifica que o aplicativo será iniciado em um depurador, com as configurações de linha de comando especificadas pelo usuário.<br/>                                                                                |
| Habilitar suporte a 3GB<br/>                                                                    | Habilita o uso do espaço de endereço de memória de processo estendido.<br/>                                                                                                                                    |



 

## <a name="component-level-class-level-settings"></a>Configurações de Component-Level (nível de classe)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="configuring-transactions.md">Transações</a><br/></td>
<td>Define os requisitos automáticos de transação desabilitados, sem suporte, com suporte, necessários ou requer novos.<br/></td>
</tr>
<tr class="even">
<td><a href="setting-the-synchronization-attribute.md">Sincronização</a><br/></td>
<td>Define os requisitos de sincronização desabilitados, sem suporte, com suporte, obrigatório ou requer novos.<br/></td>
</tr>
<tr class="odd">
<td><a href="enabling-jit-activation-for-a-component.md">Ativação JIT</a><br/></td>
<td>Habilita a ativação Just-in-time.<br/></td>
</tr>
<tr class="even">
<td><a href="configuring-a-component-to-be-pooled.md">Pool de objetos</a><br/></td>
<td>Habilita o pooling de objetos. O tamanho mínimo e máximo do pool e os valores de tempo limite do objeto são configuráveis.<br/></td>
</tr>
<tr class="odd">
<td><a href="specifying-an-object-constructor-string-for-a-component.md">Construção de objeto</a><br/></td>
<td>Habilita a construção de objeto com parâmetros com uma cadeia de caracteres de Construtor especificada administrativamente. <br/>
<blockquote>
[!Note]<br />
A cadeia de caracteres do construtor não deve ser usada para armazenar informações confidenciais de segurança.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="enabling-access-checks-at-the-component-level.md">Verificações de acesso no nível do componente</a><br/></td>
<td>Ativa ou desativa a verificação de segurança baseada em função no nível de componente.<br/></td>
</tr>
<tr class="odd">
<td><a href="assigning-roles-to-components--interfaces--or-methods.md">Atribuição de função declarativa</a><br/></td>
<td>Habilita a atribuição explícita de funções ao componente.<br/></td>
</tr>
<tr class="even">
<td><a href="persistent-client-side-failures.md">Classe de exceção de enfileiramento</a><br/></td>
<td>Indica uma classe de exceção para lidar com falhas do lado do cliente.<br/></td>
</tr>
<tr class="odd">
<td><a href="com--instrumentation-concepts.md">Eventos de instrumentação e estatísticas</a><br/></td>
<td>Habilita o relatório detalhado de eventos do sistema e estatísticas de objeto.<br/></td>
</tr>
<tr class="even">
<td><a href="context-activation.md">Contexto de ativação</a><br/></td>
<td>Habilita a ativação forçada de um objeto no contexto do chamador ou no contexto padrão.<br/></td>
</tr>
<tr class="odd">
<td><a href="what-s-new-in-com--1-5.md">Criando componentes privados</a><br/></td>
<td>Marca o componente como privado para o aplicativo. Um componente privado pode ser visto e ativado somente por outros componentes no mesmo aplicativo.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="interface-level-setting"></a>Interface-Level configuração



| Atributo                                                                                           | Descrição                                                                                                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Em fila](creating-queuable-components.md)<br/>                                               | Indica uma interface queuable, definida em IDL.<br/>                                                                       |
| [Atribuição de função declarativa](assigning-roles-to-components--interfaces--or-methods.md)<br/> | Habilita a atribuição explícita de funções à interface, bem como funções herdadas implicitamente do nível de componente.<br/> |



 

## <a name="method-level-setting"></a>Method-Level configuração



| Atributo                                                                                           | Descrição                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Concluído automaticamente](enabling-auto-done-for-a-method.md)<br/>                                         | Desativa automaticamente o objeto no retorno do método e nos votos na transação.<br/>                                                       |
| [Atribuição de função declarativa](assigning-roles-to-components--interfaces--or-methods.md)<br/> | Habilita a atribuição explícita de funções para o método, bem como funções herdadas implicitamente dos níveis de interface e componente.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Automatizando a administração do COM+](automating-com--administration.md)
</dt> <dt>

[Criando aplicativos COM+](creating-com--applications.md)
</dt> <dt>

[Implantando aplicativos COM+](deploying-com--applications.md)
</dt> </dl>

 

 




