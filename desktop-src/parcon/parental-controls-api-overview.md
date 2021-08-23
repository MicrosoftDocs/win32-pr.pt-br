---
description: Visão geral da API de controles dos pais
ms.assetid: 647e5df8-7c6d-466a-a3d4-eac13efa797d
title: Visão geral da API de controles dos pais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc2dc1995db834aa206dea1a4f657565ac3e38b35766ca6a83ac495c4f1734af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712576"
---
# <a name="parental-controls-api-overview"></a>Visão geral da API de controles dos pais

As APIs usadas para controles dos pais expõem as configurações de diretiva e restrições integradas e o registro em log da funcionalidade.

## <a name="settings"></a>Configurações

São fornecidas duas APIs públicas:

-   Uma API de conformidade mínima com base em COM baseada em COM (chamada de API de conformidade), principalmente para aplicativos, para determinar se o log deve ser ativado. Além disso, métodos simples são fornecidos para:
    -   Recuperando o estado de restrições para restrições da Web, limites de tempo, restrições de jogos e restrições de aplicativos.
    -   Recuperando a ID do filtro de conteúdo da Web ativo.
    -   Determinar se os elementos da interface do usuário do fornecedor devem ser mostrados, de maneira consistente com a ocultação da caixa quando ingressado em um domínio.
    -   Recuperando a última vez que uma configuração foi alterada para um usuário.
    -   Recuperar se os downloads de arquivos baseados em navegador ou navegadores precisam ser bloqueados para um usuário e a capacidade de solicitar uma URL para ser especificamente permitida pelo filtro de conteúdo da Web para esse usuário.
    -   Determinando se um determinado jogo está bloqueado para um usuário.
-   Windows Acesso de API da instrumentação de gerenciamento (WMI) a um namespace de controles pai para gravação completa e acesso de leitura a todas as configurações expostas. Os controles dos pais implantam um provedor WMI para gerenciar permissões de leitura/gravação no armazenamento de configurações subjacente com a aplicação adequada de privilégios para administradores e usuários controlados.

Os ISVs são solicitados a usar a API de conformidade e a API do WMI, conforme necessário, para controlar as restrições conforme apropriado para a segurança filho com base na funcionalidade do aplicativo ou da solução.

## <a name="logging"></a>Registro em log

-   Windows a publicação de eventos padrão e as APIs de consumo são usadas para o monitoramento de atividades de controles dos pais. o sistema de rastreamento e relatório de eventos do Windows Vista melhorou o desempenho do rastreamento de eventos anteriores para a funcionalidade de Windows (ETW). Os controles dos pais definem um canal exclusivo para seus dados no ETW.
-   Os ISVs são solicitados a usar a API de publicação de eventos para registrar a atividade do usuário, conforme especificado na seção usando APIs de controles pais.

 

 



