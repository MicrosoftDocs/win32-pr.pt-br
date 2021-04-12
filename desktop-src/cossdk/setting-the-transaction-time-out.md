---
description: Você pode definir manualmente o tempo limite para as transações usando a ferramenta administrativa serviços de componentes ou pode configurar programaticamente o tempo limite usando as interfaces de administração do COM+.
ms.assetid: f7a35bdf-ea6d-40ea-b3c0-c2a3ae2276c4
title: Definindo a transação Time-Out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b002448ca21e97e2e4996679d87a4b6a7680161f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457140"
---
# <a name="setting-the-transaction-time-out"></a>Definindo a transação Time-Out

Você pode definir manualmente o tempo limite para as transações usando a ferramenta administrativa serviços de componentes ou pode configurar programaticamente o tempo limite usando as interfaces de [Administração do com+](com--administration-interfaces.md). O tempo limite pode ser configurado no nível do computador local e também para componentes individuais.

**Para definir o tempo limite da transação para o computador local usando a ferramenta administrativa serviços de componentes**

1.  Na árvore de console, clique com o botão direito do mouse no computador local que você deseja configurar e clique em **Propriedades**.

2.  Na caixa de diálogo Propriedades do computador, clique na guia **Opções** .

3.  Em **tempo limite da transação**, insira o tempo limite da transação em segundos. O tempo limite padrão é de 60 segundos.

4.  Clique em **OK**.

**Para definir o tempo limite da transação para um componente usando a ferramenta administrativa serviços de componentes**

1.  Na árvore de console, clique com o botão direito do mouse no componente que você deseja configurar e clique em **Propriedades**.

2.  Na caixa de diálogo Propriedades do componente, clique na guia **Transações** .

3.  Marque a caixa rotulada **substituir valor de tempo limite de transação global**.

    > [!Note]  
    > Você não poderá marcar a caixa para substituir o valor de tempo limite da transação global se o **suporte à transação** estiver definido como **desabilitado**, **sem suporte** ou **com suporte**.

     

4.  Em **tempo limite da transação**, insira o tempo limite da transação em segundos. O tempo limite padrão é de 0 segundos, o que significa que o componente nunca fará com que a transação expire o tempo limite.

5.  Clique em **OK**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciando transações automáticas no COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



