---
description: A interface do usuário do cartão inteligente (IU) é uma única caixa de diálogo comum que permite que o usuário especifique ou procure um cartão inteligente para abrir (ou seja, conectar-se e usar em um aplicativo).
ms.assetid: a64a617a-b2ae-471f-a88f-a73f0fc3a791
title: Interface do usuário do cartão inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc558446516149529e9a98d28aa9fe94f80b2777
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751086"
---
# <a name="smart-card-user-interface"></a>Interface do usuário do cartão inteligente

A interface do [*usuário*](../secgloss/u-gly.md) do cartão inteligente (IU) é uma única [*caixa de diálogo comum*](../secgloss/s-gly.md) que permite que o usuário especifique ou procure um cartão inteligente para abrir (ou seja, conectar-se e usar em um aplicativo).

A seguir, há duas maneiras de usar a caixa de diálogo comum. Ambos supõem que a interface do usuário da caixa de diálogo será exibida. Para obter mais informações, consulte [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea).

**Para selecionar um cartão inteligente para abrir**

1.  Declare uma variável do tipo **OPENCARDNAME**.
2.  Forneça informações suficientes na caixa de diálogo comum para restringir a pesquisa de um cartão inteligente que o aplicativo de chamada está procurando. Isso inclui a especificação de **lpstrGroupNames**, **lpstrCardNames** e **rgguidInterfaces**. Isso também inclui a especificação de um modo de compartilhamento preferencial e o protocolo a ser usado quando a caixa de diálogo comum se conecta ao cartão usando os membros **dwShareMode** e **DwPreferredProtocols** da estrutura [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea) .
3.  Chame a função [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) para exibir a caixa de diálogo comum para o usuário. Uma linha de informações de ajuda simples será exibida e, se um dos cartões que estão sendo solicitados for encontrado, o cartão será realçado na exibição. Para pesquisas de nome de cartão múltiplo, o primeiro leitor que contém um dos cartões preferenciais será realçado.
4.  Em seguida, o usuário seleciona um cartão, clica em **OK** e se conecta ao cartão inteligente.

**Para procurar um cartão específico**

1.  Declare uma variável do tipo **OPENCARDNAME**.
2.  Forneça informações suficientes na caixa de diálogo comum para restringir a pesquisa de um cartão inteligente que o aplicativo de chamada está procurando. Isso inclui a especificação de **lpstrGroupNames**, **lpstrCardNames** e **rgguidInterfaces**.
3.  Crie as funções de retorno de chamada **conectar**, **verificar** e **Desconectar** e defina os membros de dados **lpfnConnect**, **lpfnCheck** e **lpfnDisconnect** adequadamente.
    > [!Note]  
    > Todas as três funções e membros devem estar disponíveis ao usar a caixa de diálogo comum dessa maneira.

     

4.  Chame a função de caixa de diálogo [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) comum.
5.  A caixa de diálogo comum irá procurar os cartões solicitados. Se uma [*cadeia de caracteres ATR*](../secgloss/a-gly.md) ou nome do cartão de correspondência for encontrada, as funções de retorno de chamada **conectar**, **verificar** e **Desconectar** serão chamadas em sequência. Se um cartão passar a rotina de **verificação** (ou seja, o retorno de chamada de **verificação** retornar **true**), esse cartão será realçado na exibição para o usuário.
    > [!Note]  
    > Se vários nomes de cartão forem fornecidos, o primeiro leitor que contém um dos cartões solicitados e passará a rotina de **verificação** será o cartão selecionado.

     

6.  Se nenhuma correspondência for encontrada, uma caixa de diálogo comum será exibida.

 

 
