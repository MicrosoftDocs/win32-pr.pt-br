---
description: A comunicação geralmente envolve quantidades potencialmente grandes de dados ou dados de comprimento desconhecido.
ms.assetid: e7b12b9e-8caa-4dad-b81f-b609ccb92c9f
title: Usando SecBufferDesc e SecBuffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ad12120414a1e0acb7a6b1cfe211b0ed1787d9e676e8329df1e16ecfef17cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785906"
---
# <a name="using-secbufferdesc-and-secbuffer"></a>Usando SecBufferDesc e SecBuffer

A comunicação geralmente envolve quantidades potencialmente grandes de dados ou dados de comprimento desconhecido. O envio e o recebimento de dados são feitos de maneira semelhante ou idêntica em ambos os casos. Para lidar com tamanho desconhecido e quantidades potencialmente grandes de dados, a comunicação SSPI é feita usando duas estruturas, [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) e [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer).

Uma [**estrutura SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) é um contêiner para uma matriz de [**estruturas SecBuffer.**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) Uma **estrutura SecBufferDesc** tem os seguintes membros:

-   Número de versão
-   Número de [**elementos SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)
-   Endereço da matriz de [**estruturas SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)

Uma [**estrutura SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) contém os três membros a seguir:

-   Número de bytes no buffer
-   Tipo de informações contidas no item de dados
-   Os bytes em si

Uma mensagem SSPI inteira geralmente consiste em uma matriz de [**estruturas SecBuffer.**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)

Os seguintes tipos de dados de buffer são definidos da seguinte forma.



| Tipo de buffer                | Significado                                                                                                                                |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| SECBUFFER \_ VAZIO           | Indefinido, substituído pela função [*de pacote de*](../secgloss/s-gly.md) segurança |
| DADOS \_ SECBUFFER            | Dados de pacote                                                                                                                            |
| SECBUFFER \_ TOKEN           | Token de segurança                                                                                                                         |
| SECBUFFER \_ PKG \_ PARAMS     | Parâmetros específicos do pacote                                                                                                            |
| SECBUFFER \_ AUSENTE         | Indicador de dados ausente                                                                                                                 |
| SECBUFFER \_ EXTRA           | Dados extras                                                                                                                             |
| SECBUFFER \_ STREAM          | Dados de fluxo de segurança                                                                                                                   |
| SECBUFFER \_ STREAM \_ TRAILER | Trailer do fluxo de segurança                                                                                                                |
| SECBUFFER \_ STREAM \_ HEADER  | Título do fluxo de segurança                                                                                                                 |



 

Os tipos de buffer acima podem ser combinados usando uma operação **OR** bit a bit com qualquer um dos tipos de buffer a seguir.



| Tipo de buffer         | Significado                                                                          |
|---------------------|----------------------------------------------------------------------------------|
| SECBUFFER \_ ATTRMASK | Mascarar atributos de segurança separando os sinalizadores de atributo do tipo de buffer. |
| SECBUFFER \_ READONLY | O buffer é somente leitura                                                              |



 

Antes de cada chamada para uma API SSPI que requer um parâmetro [**SecBufferDesc,**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) um ou mais elementos de matriz [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) são declarados e inicializados. Por exemplo, pode haver dois buffers de segurança: um que contém dados de mensagem de entrada e outro para o token de segurança opaco de saída retornado pelo pacote de segurança. A ordem dos buffers de segurança no descritor de buffer de segurança não é importante, mas cada buffer deve ser marcado com seu tipo apropriado. Uma marca somente leitura pode ser usada com qualquer buffer de entrada que não deve ser modificado pelo [*pacote de segurança*](../secgloss/s-gly.md).

O tamanho do buffer de saída que deve conter o token de segurança é importante. Um aplicativo pode encontrar o tamanho máximo do token para um pacote de segurança durante a configuração inicial. A chamada para [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) retorna uma matriz de ponteiros para informações do pacote de segurança. A estrutura de informações do pacote de segurança contém o tamanho máximo do token para cada pacote. No exemplo, as informações estão no membro **cbMaxToken** da [**estrutura SecPkgInfo.**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) As mesmas informações podem ser obtidas posteriormente [**usando QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa).

O aplicativo inicializa os ponteiros e tamanhos do buffer na descrição do buffer para indicar onde os dados da mensagem e outras informações podem ser encontrados.

Para obter detalhes, consulte [SecBuffer e SecBufferDesc Example Code](secbuffer-and-secbufferdesc-example-code.md).

 

 
