---
description: Você pode definir manualmente o nível de isolamento de transação de componentes usando a ferramenta administrativa serviços de componentes ou pode configurar programaticamente o nível de isolamento da transação para um componente usando as interfaces de administração COM+.
ms.assetid: 3ef5b805-334d-4803-be67-00c9e35cdcc6
title: Configurar o nível de isolamento da transação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96af7017f8a46f11428bfacf7282a7d4ae61b4dc3c1fd5bb7e82588f8fff6110
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029456"
---
# <a name="setting-the-transaction-isolation-level"></a>Configurar o nível de isolamento da transação

Você pode definir manualmente o nível de isolamento de transações de componentes usando a ferramenta administrativa serviços de componentes ou pode configurar programaticamente o nível de isolamento da transação para um componente usando as interfaces de administração [COM+.](com--administration-interfaces.md)

Para obter mais informações sobre níveis de isolamento de transação, consulte [Configurando níveis de isolamento de transação.](configuring-transaction-isolation-levels.md)

**Para definir o nível de isolamento da transação usando a ferramenta administrativa serviços de componentes**

1.  Na árvore de console, clique com o botão direito do mouse no componente que você deseja configurar e clique em **Propriedades**.

2.  Na caixa de diálogo propriedades do componente, clique na **guia Transações.**

3.  Em **Nível de Isolamento da** Transação , selecione o valor que você deseja na caixa de seleção. O valor padrão para todos os componentes é **Serializado.**

    > [!Note]  
    > Se **Desabilitado ou** **Sem Suporte estiver selecionado em** Suporte à **transação,** não será possível definir o nível de isolamento da transação.

     

4.  Clique em **OK**.

Você deve repetir esse procedimento para cada componente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando níveis de isolamento de transação](configuring-transaction-isolation-levels.md)
</dt> </dl>

 

 



