---
description: Um aplicativo que contém pelo menos um componente queuable pode ser marcado como enfileirado usando a ferramenta administrativa serviços de componentes.
ms.assetid: 7d9fec63-0bb7-45f3-9d40-736a60d69185
title: Criando filas de componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c44f670cea15e1cb1a4549d5c1e847956eb41d400ae01d557803dbd1ce2b439
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793456"
---
# <a name="creating-component-queues"></a>Criando filas de componentes

Um aplicativo que contém pelo menos um componente queuable pode ser marcado como enfileirado usando a ferramenta administrativa serviços de componentes.

Quando um aplicativo é marcado como enfileirado, o COM+ cria automaticamente uma fila de enfileiramento de mensagens para ele. O nome da fila é o nome do aplicativo; Se o nome da fila corresponder ao nome de uma fila existente, o COM+ usará a fila existente.

> [!Note]  
> O parâmetro do nome do *caminho* do serviço de enfileiramento de mensagens é uma combinação do RSN (Remote Server Name) e do nome do aplicativo com+. O RSN refere-se ao destino de uma ativação remota. Você especifica um RSN durante a instalação de um aplicativo exportável do cliente em um computador cliente. O procedimento de instalação usa o RSN para direcionar a ativação para um computador cliente especificado. Para obter mais informações sobre nomes de fila, consulte a tabela de parâmetros na seção "parâmetros do moniker da fila" em [usando o moniker da fila](using-the-queue-moniker.md).

 

## <a name="component-services-administrative-tool"></a>Ferramenta administrativa serviços de componentes

Para especificar um aplicativo COM+ como enfileirado, use as seguintes etapas:

1.  Na árvore de console da ferramenta administrativa serviços de componentes, em **serviços de componentes**, abra a pasta **aplicativos com+** associada ao computador que você deseja gerenciar.

2.  Clique com o botão direito do mouse no aplicativo para o qual você deseja criar uma fila e clique em **Propriedades**.

3.  Selecione a guia **enfileiramento** na caixa de diálogo Propriedades.

4.  Ative a caixa de seleção rotulada **na fila – esse aplicativo pode ser** acessado pelas filas do MSMQ.

    > [!Note]  
    > Se a caixa de seleção **na fila** estiver esmaecida, o aplicativo não conterá nenhum componente queuable.

     

5.  Clique em **OK**.

## <a name="visual-basic"></a>Visual Basic

Não se aplica.

## <a name="cc"></a>C/C++

Não se aplica.

## <a name="remarks"></a>Comentários

As filas criadas pela biblioteca de administração COM+ ou pela ferramenta administrativa serviços de componentes são marcadas com o atributo transacional do enfileiramento de mensagens.

Depois que um aplicativo enfileirado é instalado no servidor, ele pode ser disponibilizado para clientes exportando o aplicativo e, em seguida, importando o aplicativo em cada cliente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando componentes do Queuable](creating-queuable-components.md)
</dt> <dt>

[Arquitetura de componentes na fila](queued-components-architecture.md)
</dt> </dl>

 

 



