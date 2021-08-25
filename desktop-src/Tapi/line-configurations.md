---
description: Um dispositivo de linha pode representar um pool de recursos homogêneos (canais) que são usados para estabelecer chamadas. Em um computador cliente, um TSP normalmente fornece acesso a um ou mais dispositivos de linha.
ms.assetid: cb599a4d-80dd-40fe-b448-f9ea58f01124
title: Configurações de linha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d3705854a5bd485dba01452a3885e52c3c2d0baf0d495a65a2db24d75894eeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126246"
---
# <a name="line-configurations"></a>Configurações de linha

Um dispositivo de linha pode representar um pool de recursos homogêneos (canais) que são usados para estabelecer chamadas. Em um computador cliente, um TSP normalmente fornece acesso a um ou mais dispositivos de linha.

Aqui estão alguns exemplos de como um provedor de serviços pode modelar várias configurações:

**Exemplo 1:** Uma única linha DOIS nos modelos de conexão centrados em computador ou centrados em telefone. O modelo mais simples é um dispositivo de linha única com um canal.

**Exemplo 2:** Uma única linha BRI-ISDN nos modelos de conexão centrados em computador ou centrados em telefone. O provedor de serviços tem várias opções sobre como ele pode querer modelar isso, por exemplo:

-   Modele a linha BRI como um dispositivo de linha única com um pool de dois canais B que permite que ambos os canais sejam combinados para estabelecer chamadas de 128 kbps.
-   Modele cada canal B como um dispositivo de linha separado e não permitir que ambos os canais sejam combinados em um único canal de 128 kbps.
-   Modele a conexão BRI como dois dispositivos de linha separados, cada um desenhando até dois canais de um pool compartilhado de dois canais B.
-   Modele como dispositivos de três linhas, um para cada canal B e outro para a combinação. Claramente, nos dois últimos modelos, os recursos podem ser atribuídos a dispositivos de linha diferentes em momentos diferentes.

**Exemplo 3:** Em sistemas cliente/servidor, um pool de portas telefônicas anexadas a um servidor pode ser compartilhado entre vários computadores cliente em uma rede local. O pool pode ser administrado para atribuir um número máximo de dispositivos de linha (cota) a cada estação de trabalho cliente. Não é incomum que a soma de todas as cotas exceda o número total de linhas. Além disso, um determinado cliente com uma cota igual a 2 pode ser atendido usando as portas 1 e 2 ao mesmo tempo e as portas 7 e 11 em um momento posterior. O provedor de serviços para o pool pode modelar essa disposição, dando a cada estação de trabalho cliente acesso a dispositivos de duas linhas.

Suponha que a configuração de provedores de serviço para um determinado computador seja tal que esse provedor de serviços específico obtém um **DeviceIDBase** de 3. Isso significa que os identificadores de dispositivo (fixos) para este cliente são 3 e 4. Se o aplicativo chamar posteriormente a linha de função TAPI [**2GetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) para o dispositivo 3 e novamente para o dispositivo 4, ele deverá ser capaz de assumir que os recursos do dispositivo para cada um desses dispositivos são constantes, porque esse é o modelo de dispositivo. Desde que a configuração do provedor de serviços do computador determinado permaneça constante, os identificadores de dispositivo que aparecem no nível do TSPI permanecerão constantes, mesmo que o servidor mude as alocações de porta. Para dispositivos baseados em servidor que estão em pool, conforme descrito no Exemplo 3, isso se mantém somente para dispositivos de linha que têm funcionalidades de dispositivo idênticas. É claro que, se a configuração do provedor de serviços do computador determinado for alterada, de modo que esse provedor de serviços obtém um **DeviceIDBase** diferente, os identificadores de dispositivo são alterados correspondentemente.

**Exemplo 4:** Link alternar para host:

-   Para fornecer telefonia pessoal para cada área de trabalho, o provedor de serviços pode modelar a linha PBX emparelhada com o computador como um dispositivo de linha única com um canal. Cada computador cliente teria um dispositivo de linha disponível.
-   Cada estação de terceiros pode ser modelada como um dispositivo de linha separado. Isso permite que o aplicativo controle chamadas em outras estações. Essa solução exige que o aplicativo abra cada linha que deseja manipular ou monitorar, o que pode ser bom se apenas um pequeno número de linhas for de interesse, mas poderá gerar muita sobrecarga se um grande número de linhas estiver envolvido.
-   O conjunto de todas as estações de terceiros pode ser modelado como um dispositivo de linha única com um endereço (número de telefone) atribuído a ele por estação. Somente um único dispositivo deve ser aberto, fornecendo monitoramento e controle de todos os endereços na linha (todas as estações). Para originar uma chamada em qualquer uma dessas estações, o aplicativo só precisa especificar o endereço da estação para a operação que faz a chamada. Nenhuma operação aberta extra é necessária. Essa modelagem implica que todas as estações têm as mesmas funcionalidades de dispositivo de linha, embora seus recursos de endereço poderiam ser diferentes.

> [!Note]  
> Todos esses exemplos são simplesmente maneiras diferentes que um provedor de serviços pode optar por implementar o mapeamento do comportamento do dispositivo de linha em alguma realização física.

 

 

 
