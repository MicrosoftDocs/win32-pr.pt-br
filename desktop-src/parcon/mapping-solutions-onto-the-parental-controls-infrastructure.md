---
description: Mapeando soluções para a infraestrutura de controles dos pais
ms.assetid: 09677019-2cf9-43fe-b16c-e802767bef3a
title: Mapeando soluções para a infraestrutura de controles dos pais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea410663af2e3b2363b7026a6997da5c19a1077a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791555"
---
# <a name="mapping-solutions-onto-the-parental-controls-infrastructure"></a>Mapeando soluções para a infraestrutura de controles dos pais

Cinco categorias de ofertas comuns de reconhecimento de provedores de serviços de Internet e de ISV e do portal são prontamente aparentes:

-   Aplicativo cliente autônomo. Os exemplos são clientes de email e media players. Embora os media players tenham um risco para a Internet e alguns tenham serviços específicos, os controles dos pais do Windows promovem principalmente o registro em log e as restrições das atividades de reprodução para minimizar os impactos da biblioteca e o registro de ruídos nos administradores.
-   Soluções de cliente/servidor. Os exemplos mais proeminentes são soluções de mensagens instantâneas.
-   Pacotes de ISP. Essas são coleções de soluções cliente/servidor e aplicativos cliente, geralmente integradas em uma única interface do usuário do cliente. Observe que a maioria deles também fornece a maioria ou todas as funcionalidades usando o acesso ao navegador, atravessando em soluções somente da Web.
-   Soluções somente da Web. Acessado por meio do navegador. Os exemplos são o email baseado na Web e a funcionalidade de mensagens instantâneas. O acesso a eles pode ser bloqueado por categorias de filtro da Web populadas adequadamente.
-   Soluções semelhantes a firewall. Fornece filtragem no nível da pilha de rede e, potencialmente, outras restrições do sistema operacional.

As recomendações para implementar soluções em conformidade para cada categoria são especificadas na tabela a seguir.



| Category                           | Log                                                  | Configurações de restrições                                    | Imposição de restrições                                 | Substituição de filtro de conteúdo da Web                                                        | Uso do link de extensibilidade para acesso de log e configurações               |
|------------------------------------|----------------------------------------------------------|----------------------------------------------------------|----------------------------------------------------------|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| Cliente "autônomo"<br/>    | Necessário no cliente<br/>                            | Necessário no cliente<br/>                            | Necessário no cliente<br/>                            | N/D<br/>                                                                        | Obrigatório, será exe. Pode simplesmente invocar a navegação da interface do usuário do aplicativo<br/>   |
| Solução de cliente/servidor<br/>  | Necessário no cliente se não for executado pelo servidor<br/> | Necessário no cliente se não for executado pelo servidor<br/> | Necessário no cliente se não for executado pelo servidor<br/> | N/D<br/>                                                                        | Obrigatório, será exe<br/>                                        |
| Pacote de ISP<br/>               | Necessário no cliente se não for executado pelo servidor<br/> | Necessário no cliente se não for executado pelo servidor<br/> | Necessário no cliente se não for executado pelo servidor<br/> | Recomendar o uso do filtro WPC, mas permitir substituição se for robusto para vários usuários<br/> | Obrigatório, será exe<br/>                                        |
| Solução somente da Web<br/>       | Recomendar a execução no servidor<br/>                | Recomendar a execução no servidor<br/>                | Recomendar a execução no servidor<br/>                | N/D<br/>                                                                        | Recomendável. Expor configurações e registro em log do servidor usando exe<br/> |
| Soluções semelhantes a firewall<br/> | Necessário no cliente<br/>                            | Necessário no cliente<br/>                            | Necessário no cliente<br/>                            | Recomendar o uso do filtro WPC, mas permitir substituição se for robusto para vários usuários<br/> | Obrigatório, será exe<br/>                                        |



 

 

 




