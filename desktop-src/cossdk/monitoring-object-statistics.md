---
description: Você pode monitorar as estatísticas de objeto conforme um aplicativo é executado. Ao fazer isso, você pode ajustar as características do pool de objetos para obter o equilíbrio entre o desempenho e os recursos que gostaria de ter.
ms.assetid: 57987cc1-8bb5-4bbd-a425-fda2e5a8b597
title: Estatísticas de objeto de monitoramento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f438bc7081546083f1930fe31f16a2198b09b48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296089"
---
# <a name="monitoring-object-statistics"></a>Estatísticas de objeto de monitoramento

Você pode monitorar as estatísticas de objeto conforme um aplicativo é executado. Ao fazer isso, você pode ajustar as características do pool de objetos para obter o equilíbrio entre o desempenho e os recursos que gostaria de ter.

Você pode monitorar o status de todos os objetos que estão configurados para dar suporte a estatísticas de objetos e relatórios de eventos. A habilitação de estatísticas de objeto tem uma sobrecarga de desempenho muito pequena.

**Para habilitar estatísticas de objeto**

1.  No painel de detalhes da ferramenta administrativa serviços de componentes, clique com o botão direito do mouse no componente que você deseja configurar e clique em **Propriedades**.

2.  Na caixa de diálogo Propriedades do componente, clique na guia **ativação** .

3.  Para habilitar as estatísticas de objeto para o componente, em **contexto de ativação**, marque a caixa de seleção o **componente dá suporte a eventos e estatísticas** .

**Para monitorar o status do objeto**

1.  Na árvore de console da ferramenta administrativa serviços de componentes, abra a pasta do aplicativo que inclui os componentes que você deseja monitorar.

2.  Clique com o botão direito do mouse na pasta **componentes** , aponte para **Exibir** e clique em **modo de exibição de status**. O painel de detalhes agora exibe a exibição de status de todos os componentes no aplicativo. A tabela a seguir descreve as seis colunas no modo de exibição de status.

    

    | Coluna                        | Descrição                                                                                                                                                                                                                |
    |-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **ProgID**<br/>         | Identifica um componente específico.<br/>                                                                                                                                                                                |
    | **Objetos**<br/>        | Mostra o número de objetos que estão sendo mantidos por referências de cliente.<br/>                                                                                                                                       |
    | **Ativado**<br/>      | Mostra o número de objetos que estão ativados no momento. <br/>                                                                                                                                                      |
    | **Em pool**<br/>         | Mostra o número total de objetos criados pelo pool, incluindo objetos que estão em uso e objetos que são desativados.<br/>                                                                                      |
    | **Em chamada**<br/>        | Identifica objetos em chamada.<br/>                                                                                                                                                                                     |
    | **Tempo de chamada (MS)**<br/> | Mostra a duração média da chamada (em milissegundos) das chamadas de método feitas nos últimos 20 segundos (até 20 chamadas). O tempo de chamada é medido no objeto e não inclui o tempo usado para atravessar a rede.<br/> |

    

     

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando um componente a ser agrupado](configuring-a-component-to-be-pooled.md)
</dt> </dl>

 

 




