---
description: Você pode definir manualmente o nível de isolamento da transação de componentes usando a ferramenta administrativa serviços de componentes ou pode configurar programaticamente o nível de isolamento da transação para um componente usando as interfaces de administração do COM+.
ms.assetid: 3ef5b805-334d-4803-be67-00c9e35cdcc6
title: Configurar o nível de isolamento da transação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b0447af2591c4f4b3e8e76c017157c02908367
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646485"
---
# <a name="setting-the-transaction-isolation-level"></a>Configurar o nível de isolamento da transação

Você pode definir manualmente o nível de isolamento da transação de componentes usando a ferramenta administrativa serviços de componentes ou pode configurar programaticamente o nível de isolamento da transação para um componente usando as [interfaces de administração do com+](com--administration-interfaces.md).

Para obter mais informações sobre níveis de isolamento de transação, consulte [Configuring TRANSACTION ISOLATION Levels](configuring-transaction-isolation-levels.md).

**Para definir o nível de isolamento da transação usando a ferramenta administrativa serviços de componentes**

1.  Na árvore de console, clique com o botão direito do mouse no componente que você deseja configurar e clique em **Propriedades**.

2.  Na caixa de diálogo Propriedades do componente, clique na guia **Transações** .

3.  Em **nível de isolamento da transação**, selecione o valor desejado na caixa suspensa. O valor padrão para todos os componentes é **serializado**.

    > [!Note]  
    > Se **desabilitado** ou **sem suporte** for selecionado em **suporte a transações**, você não poderá definir o nível de isolamento da transação.

     

4.  Clique em **OK**.

Você deve repetir este procedimento para cada componente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando níveis de isolamento da transação](configuring-transaction-isolation-levels.md)
</dt> </dl>

 

 



