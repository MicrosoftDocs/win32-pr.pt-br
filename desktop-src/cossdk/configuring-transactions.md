---
description: O atributo Transaction é uma propriedade declarativa que gerencia automaticamente as transações do desenvolvedor de componentes. Ao definir esse atributo, você elimina a necessidade de usar controles de transação explícitos em seu componente.
ms.assetid: ea0e4d7e-2598-4a42-993c-58815f2fa138
title: Configurando transações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57f27d47836193dc5d23c44e3344cb2a81d5984
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104551699"
---
# <a name="configuring-transactions"></a>Configurando transações

O *atributo Transaction* é uma propriedade declarativa que gerencia automaticamente as transações do desenvolvedor de componentes. Ao definir esse atributo, você elimina a necessidade de usar controles de transação explícitos em seu componente.

O COM+ usa o atributo Transaction do componente para determinar o tipo de proteção de transação necessário para cada objeto que ele ativa. Dependendo de seu requisito, um objeto pode compartilhar a transação do chamador, exigir uma nova transação ou operar sem proteção de transação.

O COM+ fornece os seguintes valores de atributo de transação:

<dl> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>Desabilitado
</dt> <dd>

Em geral, você deve definir esse valor de atributo somente quando tiver certeza de que o componente nunca acessa um Gerenciador de recursos. Quando você desabilita o atributo Transaction, o COM+ ignora os requisitos transacionais do componente na determinação do posicionamento de contexto do objeto. Como resultado, o objeto pode compartilhar o contexto (e a transação) do chamador. Ao migrar um componente COM para COM+, você deve desabilitar o atributo Transaction para manter o mesmo comportamento transacional que o componente COM não configurado.

> [!Note]  
> Um *componente não configurado* é um componente com que não foi instalado em um aplicativo com+.

 

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>Sem suporte
</dt> <dd>

Quando você define esse valor de atributo, o COM+ garante que qualquer objeto criado a partir do componente nunca participe de uma transação, independentemente do status transacional de seu chamador. Ao declarar esse valor, você garante que um objeto não vote na transação de seu chamador nem possa iniciar uma transação por conta própria. Sem suporte é o valor padrão para todos os componentes.

</dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>Porta
</dt> <dd>

Quando você define esse valor de atributo, o COM+ garante que qualquer objeto criado a partir do componente participará de uma transação, se houver. Você declara esse valor quando deseja que um objeto Compartilhe em sua transação do chamador sem exigir uma transação própria.

</dd> <dt>

<span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>Necessário
</dt> <dd>

Quando você define esse valor de atributo, o COM+ garante que qualquer objeto criado a partir do componente seja transacional. Quando o COM+ ativa um objeto com a configuração necessária, ele examina o status transacional de seu chamador. Se o chamador tiver uma transação, o novo objeto será incluído na transação atual. Caso contrário, o COM+ inicia uma transação, tornando o novo objeto a raiz da transação. Essa é a configuração preferida para um componente que executa atividades de recursos, pois ajuda a fornecer proteção de transação para essas atividades.

</dd> <dt>

<span id="Requires_New"></span><span id="requires_new"></span><span id="REQUIRES_NEW"></span>Requer novo
</dt> <dd>

Quando você define esse valor de atributo, o COM+ garante que todos os objetos criados a partir do componente devem participar de uma nova transação como a raiz da transação, independentemente do status transacional do chamador. O COM+ inicia automaticamente uma nova transação que é distinta da transação do chamador.

> [!Note]  
> COM+ não dá suporte a transações aninhadas. Quando um objeto transacional chama outro componente marcado como requer novo, o COM+ cria um limite transacional independente para o objeto que acabou de ser ativado. A segunda transação não pode afetar a primeira transação, a menos que a primeira transação explicitamente anote os resultados da segunda transação e modifique seu voto com base nesses resultados.

 

</dd> </dl>

## <a name="transaction-attribute-dependencies"></a>Dependências de atributo de transação

A tabela a seguir mostra as características de cada valor de atributo de transação COM+, incluindo o efeito do valor em características de transação. O COM+ impõe a [ativação](com--just-in-time-activation.md) e a [sincronização](com--synchronization.md) JIT para todos os componentes de transação.



| Valor do atributo          | Nova transação   | Transação do cliente                 | Raiz da transação                        | Ativação JIT      | Sincronização     |
|--------------------------|-------------------|--------------------------------------|-----------------------------------------|---------------------|---------------------|
| Desabilitado<br/>      | Nunca<br/>  | Talvez<br/>                     | Nunca<br/>                        | Opcional<br/> | Opcional<br/> |
| Sem suporte<br/> | Nunca<br/>  | Nunca<br/>                     | Nunca<br/>                        | Opcional<br/> | Opcional<br/> |
| Com suporte<br/>     | Nunca<br/>  | Se o cliente tiver uma transação<br/> | Nunca<br/>                        | Obrigatório<br/> | Obrigatório<br/> |
| Obrigatório<br/>      | Talvez<br/>  | Se o cliente tiver uma transação<br/> | Se o cliente não tiver nenhuma transação<br/> | Obrigatório<br/> | Obrigatório<br/> |
| Requer novo<br/>  | Sempre<br/> | Nunca<br/>                     | Sempre<br/>                       | Obrigatório<br/> | Obrigatório<br/> |



 

## <a name="transaction-boundaries"></a>Limites da transação

Uma transação tem um início, um fim e ocorre exatamente uma vez. Durante sua execução, uma transação pode chamar em um recurso, como um banco de dados ou fila, para realizar uma ou mais tarefas. Cada recurso cai dentro do *limite da transação*. Todos os recursos dentro de um limite de transação, que podem abranger vários limites de processo e computador, compartilhar uma única transação. É importante gerenciar a consistência entre esse processo e os limites do computador.

O COM+ garante a consistência gerenciando os limites de transação automaticamente, com base no valor do atributo de transação que você define para cada componente. Uma transação COM+ flui automaticamente para objetos instruídos a participar de uma transação e ignora os objetos instruídos a executar fora de uma transação. COM+ não dá suporte a transações aninhadas. Em vez disso, as transações COM+ são distintas e de curta duração.

O primeiro objeto em um limite de transação é especial para a transação e é chamado de *objeto raiz* da transação. Pode haver apenas um objeto raiz em uma transação. Todos os outros objetos na hierarquia transacional sob o objeto raiz são chamados de *objetos interiores*.

## <a name="mapping-transactions"></a>Mapeando transações

Uma maneira de garantir que um objeto seja incluído no limite de transação correto é mapear suas transações antes de começar a gravar seus componentes. Ao mapear transações, você pode determinar a melhor configuração para cada componente que você escreve. Quanto mais certeza você estiver sobre como seus componentes devem ser usados, mais fácil será selecionar o valor correto do atributo de transação.

Em tempo de execução, o COM+ examina o atributo Transaction para determinar se um objeto deve ser a raiz de uma nova transação, ser criado em uma transação existente ou ser criado como um objeto não transacional.

A ilustração a seguir mostra um possível mapeamento de transação. Na ilustração, o cliente cria o objeto 1, que requer uma transação. Como não existe nenhuma transação, o COM+ cria a transação 1 e coloca o objeto 1 nela como o objeto raiz. O objeto 1 cria o objeto 2, que dá suporte a transações e, portanto, é colocado na transação 1. O objeto 2 cria o objeto 3, que não oferece suporte a transações e, portanto, é colocado fora de todas as transações. O objeto 2 também cria o objeto 4, que requer uma transação e, portanto, é colocado na transação 1. O objeto 3 cria o objeto 5, que dá suporte a transações. No entanto, como o objeto 5 é criado por um objeto que não existe em uma transação, ele também é colocado fora de todas as transações. O objeto 4 cria o objeto 6, que requer uma nova transação, portanto, o COM+ cria a transação 2 e coloca o objeto 6 nela como o objeto raiz. O objeto 6 cria o objeto 7, que dá suporte a transações e, portanto, é colocado na transação 2.

![Diagrama que mostra uma interação do cliente com a transação 1 e a transação 2.](images/fc7e2d03-94c2-40d9-a79b-1e05ca31dd80.png)

A ilustração anterior mostra duas áreas problemáticas potenciais. Primeiro, a maior parte do trabalho é dividida entre duas transações distintas. Se a transação 1 falhar depois que o objeto 4 criar o objeto 6, a transação 2 não será afetada pelo resultado da transação 1. Se esse resultado não for intencional, talvez você prefira dobrar as operações de ambas as transações em uma única transação, o que pode ser feito alterando o atributo de transação do objeto 6 para necessário.

A ilustração de mapeamento também mostra que o objeto 3 e o objeto 5 não são transacionais, executando completamente fora do escopo das transações 1 e 2. Se o objeto 5 atualizar dados persistentes, talvez você queira reconsiderar seu status não transacional. O objeto 5 pode ser colocado em uma transação alterando seu atributo de transação para obrigatório.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando o atributo de transação](setting-the-transaction-attribute.md)
</dt> </dl>

 

 




