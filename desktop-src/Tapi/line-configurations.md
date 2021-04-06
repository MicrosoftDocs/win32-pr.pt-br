---
description: Um dispositivo de linha pode representar um pool de recursos homogêneos (canais) que são usados para estabelecer chamadas. Em um computador cliente, um TSP geralmente fornece acesso a um ou mais dispositivos de linha.
ms.assetid: cb599a4d-80dd-40fe-b448-f9ea58f01124
title: Configurações de linha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8722dab15763822f6535783ecc8bc18e681e13ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827375"
---
# <a name="line-configurations"></a>Configurações de linha

Um dispositivo de linha pode representar um pool de recursos homogêneos (canais) que são usados para estabelecer chamadas. Em um computador cliente, um TSP geralmente fornece acesso a um ou mais dispositivos de linha.

Aqui estão alguns exemplos de como um provedor de serviços pode modelar várias configurações:

**Exemplo 1:** Uma única linha POTS nos modelos de conexão centrados no computador ou no telefone. O modelo mais direto é um dispositivo de linha única com um canal.

**Exemplo 2:** Uma única linha BRI-ISDN nos modelos de conexão centrados no computador ou no telefone. O provedor de serviços tem várias opções sobre como pode querer modelar isso, por exemplo:

-   Modele a linha BRI como um dispositivo de linha única com um pool de dois canais B que permite que ambos os canais sejam combinados para estabelecer chamadas de 128 kbps.
-   Modele cada canal B como um dispositivo de linha separado e não permita que ambos os canais sejam combinados em um único canal de 128 kbps.
-   Modele a conexão BRI como dois dispositivos de linha separados, cada um deles desenhando até dois canais de um pool compartilhado de dois canais B.
-   Modele como três dispositivos de linha, um para cada canal B e outro para a combinação. Claramente nos dois últimos modelos, os recursos podem ser atribuídos a diferentes dispositivos de linha em momentos diferentes.

**Exemplo 3:** Em sistemas cliente/servidor, um pool de portas de telefone anexadas a um servidor pode ser compartilhado entre vários computadores cliente em uma rede local. O pool pode ser administrado para atribuir um número máximo de dispositivos de linha (cota) a cada estação de trabalho cliente. Não é incomum que a soma de todas as cotas exceda o número total de linhas. Além disso, um determinado cliente com uma cota igual a 2 pode ser satisfeito usando as portas 1 e 2 ao mesmo tempo e as portas 7 e 11 em um momento posterior. O provedor de serviços para o pool pode modelar essa disposição fornecendo a cada estação de trabalho cliente acesso a dois dispositivos de linha.

Suponha que a configuração de provedores de serviço para um determinado computador seja de tal forma que esse provedor de serviço específico obtenha um **DeviceIDBase** de 3. Isso implica que os identificadores de dispositivo (fixos) para esse cliente são 3 e 4. Se o aplicativo posteriormente chamar a função TAPI 2 [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) para o dispositivo 3 e novamente para o dispositivo 4, deverá ser capaz de assumir que os recursos do dispositivo para cada um desses dispositivos são constantes, pois esse é o modelo de dispositivo. Desde que a configuração do provedor de serviço do computador fornecido permaneça constante, os identificadores de dispositivo que aparecem no nível de TSPI permanecem constantes, mesmo que o servidor altere as alocações de porta. Para dispositivos baseados em servidor que são agrupados conforme descrito no exemplo 3, isso só contém os dispositivos de linha que têm recursos de dispositivo idênticos. É claro que, se a configuração do provedor de serviço do computador fornecido for alterada, de modo que esse provedor de serviços obtenha um **DeviceIDBase** diferente, identificadores de dispositivo serão alterados de forma correspondente.

**Exemplo 4:** Link de comutador para host:

-   Para fornecer telefonia pessoal a cada área de trabalho, o provedor de serviços pode modelar a linha PBX emparelhada com o computador como um dispositivo de linha única com um canal. Cada computador cliente teria um dispositivo de linha disponível.
-   Cada estação de terceiros pode ser modelada como um dispositivo de linha separado. Isso permite que o aplicativo controle chamadas em outras estações. Essa solução requer que o aplicativo abra cada linha que deseja manipular ou monitorar, o que pode ser bom se apenas um pequeno número de linhas for interessante, mas poderá gerar muita sobrecarga se um grande número de linhas estiver envolvido.
-   O conjunto de todas as estações de terceiros pode ser modelado como um único dispositivo de linha com um endereço (número de telefone) atribuído a ele por estação. Apenas um único dispositivo deve ser aberto, fornecendo monitoramento e controle de todos os endereços na linha (todas as estações). Para originar uma chamada em qualquer uma dessas estações, o aplicativo precisa apenas especificar o endereço da estação para a operação que faz a chamada. Nenhuma operação de abertura extra é necessária. Essa modelagem implica que todas as estações têm os mesmos recursos de dispositivo de linha, embora seus recursos de endereço possam ser diferentes.

> [!Note]  
> Todos esses exemplos são simplesmente maneiras diferentes de um provedor de serviços optar por implementar o mapeamento do comportamento do dispositivo de linha em alguma percepção física.

 

 

 
