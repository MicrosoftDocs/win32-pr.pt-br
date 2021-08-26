---
title: Representação de dados
description: Os ambientes de computação podem diferir significativamente, assim como as arquiteturas de rede.
ms.assetid: 34ba76ae-644d-4168-886f-0909a65f1abd
keywords:
- Chamada de procedimento remoto RPC , descrita, representação de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9a0af96249c356f171396eaf52f91c5e33005eda080929cfbd8eecde27ffa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022086"
---
# <a name="data-representation"></a>Representação de dados

Os ambientes de computação podem diferir significativamente, assim como as arquiteturas de rede. Para acomodar essas diferenças, o MIDL permite que você modifique a maneira como representa os dados. Às vezes, você pode simplificar o desenvolvimento convertendo dados em um formato que seu aplicativo possa manipular com mais facilidade. Você pode alterar o formato de dados do aplicativo para que ele possa ser transmitido com mais eficiência pela rede.

Os atributos transmitir como e representar como instruim o compilador a associar um tipo permitido que o stub passa entre o cliente e o servidor, com um tipo de usuário que os aplicativos cliente e **\[** [**\_**](/windows/desktop/Midl/transmit-as) **\]** servidor **\[** [**\_**](/windows/desktop/Midl/represent-as) **\]** usam. Você deve fornecer as rotinas que realizam a conversão entre o tipo de usuário e o tipo permitido e as rotinas para liberar a memória que foi usada para manter os dados convertidos. Usar o **\[ atributo transmit \_ como \]** IDL **\[ \_ \]** ou representar como atributo ACF instrui o stub a chamar essas rotinas de conversão antes e depois da transmissão. O **\[** [**atributo transmit \_ as**](/windows/desktop/Midl/transmit-as) **\]** permite converter um tipo de dados em outro tipo de dados para transmissão pela rede. O atributo representar como permite controlar a maneira como os dados da rede são apresentados ao **\[** [**\_**](/windows/desktop/Midl/represent-as) **\]** aplicativo.

Os **\[** [**atributos de marshal \_ de**](/windows/desktop/Midl/wire-marshal) **\]** transmissão e **\[** [**\_ marshal**](/windows/desktop/Midl/user-marshal) **\]** de usuário são extensões da Microsoft para a IDL do OSF-DCE. Sua sintaxe e funcionalidade são semelhantes à da transmissão especificada por DCE **\[ \_ como \]** e **\[ representam \_ como \]** atributos, respectivamente. A diferença é que, em vez de converter os dados de um tipo para outro, você faz marshaling dos dados diretamente. Para fazer isso, você deve fornecer as rotinas externas para o tamanho do buffer de dados nos lados do cliente e do servidor, marshaling e desmarque os dados nos lados do cliente e do servidor e liberando os dados no lado do servidor. O compilador MIDL gera códigos de formato que instruim o mecanismo NDR a chamar essas rotinas externas quando necessário.

Os **\[ atributos de marshal de \_ transmissão \]** **\[ e \_ marshal \]** de usuário possibilitam realizar marshal de tipos de dados que, de outra forma, não poderiam ser transmitidos entre os limites do processo. Além disso, como há menos sobrecarga associada à conversão de **\[ \_ \] tipo,** o marshal de transmissão e o **\[ marshal \_ de \]** usuário fornecem um desempenho aprimorado em tempo de execução, **\[ \_ \]** quando comparados a transmitir como e representar **\[ \_ como \]**. Os **\[ atributos de marshal \_ de \]** **\[ \_ \]** **\[ transmissão e marshal de usuário são mutuamente exclusivos em relação uns aos outros e em relação à transmissão como e representam como atributos para um determinado tipo. \_ \]** **\[ \_ \]**

É importante observar que a implementação dos **\[ \_ \]** atributos **\[ de \_ \]** marshal de transmissão e marshal de usuário deve seguir as regras de marshaling ditadas pela especificação osF-DCE. Por esse motivo, o uso desses atributos não será recomendado se você não estiver familiarizado com o protocolo de transmissão. Mais informações sobre a Transferência de Sintaxe NDR podem ser encontradas [em www.opengroup.org](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm).

Esta seção fornece uma breve visão geral deles para atributos MIDL, nos tópicos a seguir:

-   [**O transmitir \_ como e representar como \_ Atributos**](the-transmit-as-and-represent-as-attributes.md)
-   [**Os atributos de \_ marshal de transmissão e marshal de \_ usuário**](the-wire-marshal-and-user-marshal-attributes.md)

 

 