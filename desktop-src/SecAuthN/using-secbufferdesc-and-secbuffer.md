---
description: A comunicação geralmente envolve quantidades potencialmente grandes de dados ou dados de comprimento desconhecido.
ms.assetid: e7b12b9e-8caa-4dad-b81f-b609ccb92c9f
title: Usando SecBufferDesc e SecBuffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ca7d8155a610263838d2baf2a7d1c8fc96ec874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829448"
---
# <a name="using-secbufferdesc-and-secbuffer"></a>Usando SecBufferDesc e SecBuffer

A comunicação geralmente envolve quantidades potencialmente grandes de dados ou dados de comprimento desconhecido. O envio e o recebimento de dados são feitos de maneira semelhante ou idêntica em ambos os casos. Para lidar com comprimento desconhecido e quantidades potencialmente grandes de dados, a comunicação SSPI é feita usando duas estruturas, [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) e [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer).

Uma estrutura [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) é um contêiner para uma matriz de estruturas [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) . Uma estrutura **SecBufferDesc** tem os seguintes membros:

-   Número de versão
-   Número de elementos [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)
-   Endereço da matriz de estruturas [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)

Uma estrutura [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) contém os três seguintes membros:

-   Número de bytes no buffer
-   Tipo de informações contidas no item de dados
-   Os bytes em si

Uma mensagem SSPI inteira geralmente consiste em uma matriz de estruturas [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) .

Os tipos de dados de buffer a seguir são definidos da seguinte maneira.



| Tipo de buffer                | Significado                                                                                                                                |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| SECBUFFER \_ vazio           | Indefinido, substituído pela função de [*pacote de segurança*](../secgloss/s-gly.md) |
| dados do SECBUFFER \_            | Dados de pacote                                                                                                                            |
| \_token SECBUFFER           | Token de segurança                                                                                                                         |
| \_parâmetros de pacote SECBUFFER \_     | Parâmetros específicos do pacote                                                                                                            |
| SECBUFFER \_ ausente         | Indicador de dados ausentes                                                                                                                 |
| SECBUFFER \_ extra           | Dados extras                                                                                                                             |
| fluxo de SECBUFFER \_          | Dados de fluxo de segurança                                                                                                                   |
| \_trailer de fluxo de SECBUFFER \_ | Trailer de fluxo de segurança                                                                                                                |
| \_cabeçalho de fluxo de SECBUFFER \_  | Cabeçalho do fluxo de segurança                                                                                                                 |



 

Os tipos de buffer acima podem ser combinados usando uma operação bit-a-**or** com qualquer um dos tipos de buffer a seguir.



| Tipo de buffer         | Significado                                                                          |
|---------------------|----------------------------------------------------------------------------------|
| SECBUFFER \_ ATTRMASK | Mascarar atributos de segurança separando os sinalizadores de atributo do tipo de buffer. |
| SECBUFFER \_ ReadOnly | O buffer é somente leitura                                                              |



 

Antes de cada chamada para uma API SSPI que requer um parâmetro [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) , um ou mais elementos da matriz [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) são declarados e inicializados. Por exemplo, pode haver dois buffers de segurança: um que contenha dados de mensagem de entrada e o outro para o token de segurança opaco de saída retornado pelo pacote de segurança. A ordem dos buffers de segurança no descritor de buffer de segurança não é importante, mas cada buffer deve ser marcado com o tipo apropriado. Uma marca somente leitura pode ser usada com qualquer buffer de entrada que não deve ser modificado pelo [*pacote de segurança*](../secgloss/s-gly.md).

O tamanho do buffer de saída que deve conter o token de segurança é importante. Um aplicativo pode encontrar o tamanho máximo de token para um pacote de segurança durante a instalação inicial. A chamada para [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) retorna uma matriz de ponteiros para informações do pacote de segurança. A estrutura de informações do pacote de segurança contém o tamanho máximo de token para cada pacote. No exemplo, as informações estão no membro **cbMaxToken** da estrutura [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) . As mesmas informações podem ser obtidas posteriormente usando [**QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa).

O aplicativo Inicializa os ponteiros e tamanhos do buffer na descrição do buffer para indicar onde os dados da mensagem e outras informações podem ser encontrados.

Para obter detalhes, consulte o [código de exemplo SecBuffer e SecBufferDesc](secbuffer-and-secbufferdesc-example-code.md).

 

 
