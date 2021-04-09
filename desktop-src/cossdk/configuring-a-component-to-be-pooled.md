---
description: Você pode configurar um componente a ser colocado em pool somente quando ele for gravado corretamente para dar suporte a pool. Para obter detalhes sobre esses requisitos, consulte requisitos para objetos pooling.
ms.assetid: ffd812cc-811e-4f2a-8736-d1cb22d5abb7
title: Configurando um componente a ser agrupado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780f7e1d9128b213b138e63b9dfa7e0f40642681
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089578"
---
# <a name="configuring-a-component-to-be-pooled"></a>Configurando um componente a ser agrupado

Você pode configurar um componente a ser colocado em pool somente quando ele for gravado corretamente para dar suporte a pool. Para obter detalhes sobre esses requisitos, consulte [requisitos para objetos pooling](requirements-for-poolable-objects.md).

> [!Note]  
> Por padrão, um componente não está configurado para ser colocado em pool.

 

Ao configurar um componente a ser agrupado, você pode especificar as seguintes propriedades para determinar como o COM+ mantém o pool:

-   **Tamanho mínimo do pool.** Representa o número de objetos que são criados quando o aplicativo é iniciado e o número mínimo de objetos que são mantidos no pool enquanto o aplicativo está em execução. Se o número de objetos disponíveis no pool cair abaixo do mínimo especificado, novos objetos serão criados para atender a todas as solicitações de objeto pendentes e reabastecer o pool. Se o número de objetos disponíveis no pool for maior que o número mínimo, esses objetos excedentes serão destruídos durante um ciclo de limpeza.
-   **Tamanho máximo do pool.** Representa o número máximo de objetos em pool que o Gerenciador de Pooling criará, ambos usados ativamente pelos clientes e inativos no pool. Ao criar objetos, o Gerenciador de Pooling verifica se o tamanho máximo do pool não foi atingido e, se não tiver, o Gerenciador de pool cria uma nova instância do objeto para dispensar para o cliente. Se o tamanho máximo do pool tiver sido atingido, as solicitações do cliente serão enfileiradas e receberão o primeiro objeto disponível do pool, de acordo com a primeira chegada. As solicitações de criação de objeto atingirão o tempo limite após um período especificado.
-   **Tempo limite de criação (MS).** Especifica quanto tempo um cliente aguardará, em milissegundos, para que um objeto seja retornado do pool após uma chamada para [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Se a chamada do cliente não for bem-sucedida, o erro E o \_ tempo limite serão retornados.

**Para definir propriedades relacionadas ao pooling**

1.  No painel de detalhes da ferramenta administrativa serviços de componentes, clique com o botão direito do mouse no componente que você deseja configurar e clique em **Propriedades**.

2.  Na caixa de diálogo Propriedades do componente, clique na guia **ativação** .

3.  Para habilitar o pool de objetos para o componente, marque a caixa de seleção **habilitar pool de objetos** .

4.  Na caixa **tamanho mínimo do pool** , insira o número mínimo de objetos desse tipo no pool. O pool será mantido para ter pelo menos esse número de objetos.

5.  Na caixa u, insira o número máximo de objetos desse tipo no pool. O número de objetos, ambos ativados e desativados, nunca excederá esse valor.

6.  Na caixa **tempo limite de criação (MS)** , digite a quantidade de tempo, em milissegundos, que um cliente aguardará por um objeto em pool se um não estiver disponível imediatamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estatísticas de objeto de monitoramento](monitoring-object-statistics.md)
</dt> </dl>

 

 
