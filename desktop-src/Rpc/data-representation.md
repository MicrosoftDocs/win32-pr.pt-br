---
title: Representação de dados
description: Os ambientes de computação podem diferir significativamente, pois as arquiteturas de rede podem ser diferentes.
ms.assetid: 34ba76ae-644d-4168-886f-0909a65f1abd
keywords:
- RPC de chamada de procedimento remoto, descrito, representação de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4de187f2b646e55cd4f1a269f0504a2d43e951c3
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "103642909"
---
# <a name="data-representation"></a>Representação de dados

Os ambientes de computação podem diferir significativamente, pois as arquiteturas de rede podem ser diferentes. Para acomodar essas diferenças, o MIDL permite que você modifique a maneira como você representa os dados. Às vezes, você pode simplificar o desenvolvimento convertendo dados em um formato que seu aplicativo possa manipular com mais facilidade. Você pode alterar o formato de dados do aplicativo para que ele possa ser transmitido de forma mais eficiente pela rede.

A **\[** [**transmissão \_ como**](/windows/desktop/Midl/transmit-as) **\]** e **\[** [**representa \_ como**](/windows/desktop/Midl/represent-as) **\]** atributos instruem o compilador a associar um tipo Transmissible que o stub passa entre o cliente e o servidor, com um tipo de usuário que os aplicativos cliente e servidor usam. Você deve fornecer as rotinas que executam a conversão entre o tipo de usuário e o tipo Transmissible e as rotinas para liberar a memória que foi usada para manter os dados convertidos. Usar o atributo **\[ transmitir \_ como \]** IDL ou o atributo **\[ represente \_ como \]** ACF instrui o stub a chamar essas rotinas de conversão antes e após a transmissão. O **\[** atributo [**transmitir \_ como**](/windows/desktop/Midl/transmit-as) **\]** permite converter um tipo de dados em outro tipo de dados para transmissão pela rede. O **\[** atributo " [**representar \_ como**](/windows/desktop/Midl/represent-as) " **\]** permite que você controle a maneira como os dados da rede são apresentados ao aplicativo.

Os **\[** atributos de [**\_ marshaling de conexão**](/windows/desktop/Midl/wire-marshal) **\]** e de **\[** [**\_ marshaling do usuário**](/windows/desktop/Midl/user-marshal) **\]** são extensões da Microsoft para o IDL uso-DCE. Sua sintaxe e funcionalidade são semelhantes às da transmissão especificada pelo DCE **\[ \_ como \]** e **\[ representam \_ como \]** atributos, respectivamente. A diferença é que, em vez de converter os dados de um tipo para outro, você faz marshaling dos dados diretamente. Para fazer isso, você deve fornecer as rotinas externas para o dimensionamento do buffer de dados nos lados do cliente e do servidor, o marshaling e o desempacotamento dos dados nos lados do cliente e do servidor e a liberação dos dados no lado do servidor. O compilador MIDL gera códigos de formato que instruem o mecanismo de NDR a chamar essas rotinas externas quando necessário.

Os atributos de **\[ \_ marshaling \]** e **\[ \_ Marshal \] do usuário** tornam possível o marshaling de tipos de dados que, de outra forma, não poderiam ser transmitidos entre limites de processo. Além disso, como há menos sobrecarga associada à conversão de tipo, **\[ o \_ marshaling \] de conexão** e o **\[ \_ marshaling \] do usuário** fornecem um desempenho aprimorado em tempo de execução, quando comparado a **\[ transmitir \_ como \]** e **\[ representar \_ como \]**. Os atributos de **\[ \_ marshaling \]** e **\[ \_ Marshal \] do usuário** são mutuamente exclusivos em relação uns aos outros e **\[ \_ \]** em relação à **\[ transmissão \_ como \]** e representam os atributos de um determinado tipo.

É importante observar que a implementação dos atributos de **\[ \_ marshaling \] de conexão** e de **\[ \_ marshaling \] do usuário** deve seguir as regras de Marshalling ditadas pela especificação uso-DCE. Por esse motivo, o uso desses atributos não será recomendado se você não estiver familiarizado com o protocolo de conexão. Mais informações sobre a transferência de sintaxe de NDR podem ser encontradas em [www.opengroup.org](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm).

Esta seção fornece uma breve visão geral desses atributos de MIDL, nos seguintes tópicos:

-   [**A transmissão \_ como e representa \_ como atributos**](the-transmit-as-and-represent-as-attributes.md)
-   [**Os \_ atributos de marshaling e \_ Marshal do usuário de transmissão**](the-wire-marshal-and-user-marshal-attributes.md)

 

 