---
description: Descreve como o Windows 10 usa conjuntos de API em operações de carregador.
title: Operação de carregador de conjunto de API
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 701409c0d8dac2c275add06d2502c8764d502aba
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "105793761"
---
# <a name="api-set-loader-operation"></a>Operação de carregador de conjunto de API

Os [conjuntos de API](windows-apisets.md) dependem do suporte do so no carregador de biblioteca para introduzir efetivamente um redirecionamento de namespace de módulo para o processo de associação de biblioteca. O [nome do contrato do conjunto de API](windows-apisets.md#api-set-contract-names) é usado pelo carregador de biblioteca para executar um redirecionamento de tempo de execução da referência a um binário de host de destino que hospeda a implementação apropriada do conjunto de API.

Quando o carregador encontra uma dependência em um conjunto de API em tempo de execução, o carregador consulta os dados de configuração na imagem para identificar o binário de host para um conjunto de API. Esses dados de configuração são chamados de **esquema de conjunto de API**. O esquema é montado como uma propriedade do sistema operacional, e o mapeamento entre conjuntos de API e binários pode diferir dependendo de quais binários são incluídos em um determinado dispositivo. O esquema permite que uma função importada em um único binário seja roteada corretamente em diferentes dispositivos, mesmo que os nomes de módulo do host binário tenham sido renomeados ou completamente refatorado em diferentes dispositivos Windows.

O Windows 10 dá suporte a duas técnicas padrão para consumir e usar a interface com conjuntos de API: **encaminhamento direto** e **encaminhamento reverso**.

### <a name="direct-forwarding"></a>Encaminhamento direto

Nessa configuração, o código de consumo importa um nome de módulo de conjunto de API diretamente. Essa importação é resolvida em uma única operação e é o método mais eficiente com a menor sobrecarga. Conceitualmente, essa resolução pode apontar para diferentes binários em dispositivos Windows 10 diferentes, como é mostrado no exemplo a seguir:

Conjunto de API importado: **api-feature1-l1-1-0.dll**
-  PC com Windows > **feature1.dll**
-  > de HoloLens- **feature1_holo.dll**
-  > IoT **feature1_iot.dll**

Como os mapeamentos são mantidos em um repositório de dados de esquema personalizado, isso significa que um nome de conjunto de API que termina com **. dll** não se refere diretamente a um arquivo no disco. A parte **. dll** do nome do conjunto de API é apenas uma convenção exigida pelo carregador. O nome do conjunto de APIs é mais parecido com um alias ou um nome virtual para um arquivo DLL físico. Isso torna o nome portátil em todo o intervalo de dispositivos com Windows 10.

### <a name="reverse-forwarding"></a>Encaminhamento reverso

Embora os nomes de conjunto de API forneçam um namespace estável para módulos entre dispositivos, nem sempre é prático converter cada binário nesse novo sistema. Por exemplo, um aplicativo pode estar em uso comum por muitos anos e a recompilação dos binários do aplicativo pode não ser viável. Além disso, alguns aplicativos podem precisar continuar executando em sistemas criados antes que determinados conjuntos de API sejam introduzidos.

Para acomodar esse nível de compatibilidade, um sistema de *encaminhadores* é fornecido em todos os dispositivos Windows 10 que abrangem um subconjunto da superfície da API do Win32. Esses encaminhadores usam os nomes de módulo que foram introduzidos em computadores Windows e aproveitam o sistema de configuração de API para fornecer compatibilidade em todos os dispositivos Windows 10.

A operação do carregador se comporta desta forma:

1.  Em um dispositivo que não seja um computador Windows, o carregador recebe uma dependência de nome de módulo de computador Windows herdada que não está presente no dispositivo.
2.  O carregador localiza um encaminhador de conjunto de API para este módulo e o carrega na memória.
3.  O encaminhador tem um mapeamento para a API definida para a função fornecida que está sendo chamada.
4.  O carregador localiza o binário de host apropriado para o dispositivo especificado.

Conceitualmente, o mapeamento é semelhante a:

DLL importada: **feature1.dll**
- PC com Windows > **feature1.dll**
- HoloLens-> **feature1.dll** encaminhador-> **api-feature1-l1-1-0.dll**  ->  **feature1_holo.dll**
- IOT-> **feature1.dll** encaminhador > **api-feature1-l1-1-0.dll**  ->  **feature1_iot.dll**

O resultado final é funcionalmente o mesmo que o [encaminhamento direto](#direct-forwarding), mas o realiza de forma a maximizar a compatibilidade de aplicativos.

> [!NOTE]
> O encaminhamento reverso fornece cobertura apenas para um subconjunto da superfície da API do Win32. Ele não permite que aplicativos direcionados a versões da área de trabalho do Windows 10 sejam executados em todos os dispositivos Windows 10.
