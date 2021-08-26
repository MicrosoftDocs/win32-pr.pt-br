---
description: Você pode monitorar estatísticas de objeto conforme um aplicativo é executado. Ao fazer isso, você pode ajustar as características do pool de objetos para obter o equilíbrio no desempenho e nos recursos que você gostaria de ter.
ms.assetid: 57987cc1-8bb5-4bbd-a425-fda2e5a8b597
title: Monitorando estatísticas de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e58946953ef1688dcb44223522cc58ccd1195f07ec0173a0b75413fe441195f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070456"
---
# <a name="monitoring-object-statistics"></a>Monitorando estatísticas de objeto

Você pode monitorar estatísticas de objeto conforme um aplicativo é executado. Ao fazer isso, você pode ajustar as características do pool de objetos para obter o equilíbrio no desempenho e nos recursos que você gostaria de ter.

Você pode monitorar o status de todos os objetos configurados para dar suporte a estatísticas de objeto e relatórios de eventos. A habilitação de estatísticas de objeto tem uma pequena sobrecarga de desempenho.

**Para habilitar estatísticas de objeto**

1.  No painel de detalhes da ferramenta administrativa serviços de componentes, clique com o botão direito do mouse no componente que você deseja configurar e clique em **Propriedades**.

2.  Na caixa de diálogo propriedades do componente, clique na **guia Ativação.**

3.  Para habilitar estatísticas de objeto para o componente, em Contexto de **Ativação**, marque a caixa de seleção Componente compatível com eventos **e estatísticas.**

**Para monitorar o status do objeto**

1.  Na árvore de console da ferramenta administrativa serviços de componentes, abra a pasta do aplicativo que inclui os componentes que você deseja monitorar.

2.  Clique com o botão direito do mouse na pasta **Componentes,** aponte **para Exibir** e clique em **Exibição de Status**. O painel de detalhes agora exibe a exibição de status de todos os componentes no aplicativo. A tabela a seguir descreve as seis colunas na exibição de status.

    

    | Coluna                        | Descrição                                                                                                                                                                                                                |
    |-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **ProgID**<br/>         | Identifica um componente específico.<br/>                                                                                                                                                                                |
    | **Objetos**<br/>        | Mostra o número de objetos que atualmente são mantidos por referências de cliente.<br/>                                                                                                                                       |
    | **Ativado**<br/>      | Mostra o número de objetos que estão ativados no momento. <br/>                                                                                                                                                      |
    | **Em pool**<br/>         | Mostra o número total de objetos criados pelo pool, incluindo objetos que estão em uso e objetos que são desativados.<br/>                                                                                      |
    | **Em Chamada**<br/>        | Identifica objetos na chamada.<br/>                                                                                                                                                                                     |
    | **Tempo de chamada (ms)**<br/> | Mostra a duração média da chamada (em milissegundos) das chamadas de método feitas nos últimos 20 segundos (até 20 chamadas). O tempo de chamada é medido no objeto e não inclui o tempo usado para percorrer a rede.<br/> |

    

     

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando um componente a ser em pool](configuring-a-component-to-be-pooled.md)
</dt> </dl>

 

 




