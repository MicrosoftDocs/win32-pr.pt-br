---
description: Processo de conexão do CBasePin
ms.assetid: 4b3a9023-0267-4caa-9d89-88237009df05
title: Processo de conexão do CBasePin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1441b0daba58857e00da0139d3312fb277287fc2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919872"
---
# <a name="cbasepin-connection-process"></a>Processo de conexão do CBasePin

Esta seção descreve como a classe [**CBasePin**](cbasepin.md) implementa o processo de conexão do PIN.

O Gerenciador de gráfico de filtro inicia todas as conexões de PIN. Ele chama o método [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) do pino de saída, especificando o pino de entrada. O pino de saída conclui a conexão chamando o método [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) do pino de entrada. O PIN de entrada pode aceitar ou rejeitar a conexão.

O Gerenciador do grafo de filtro também pode especificar um tipo de mídia para a conexão. Nesse caso, os Pins tentam se conectar com esse tipo. Caso contrário, os Pins devem negociar o tipo. O Gerenciador do grafo de filtro também pode especificar um tipo de mídia *parcial* , que tem o valor GUID \_ NULL para o tipo principal, subtipo ou tipo de formato. Nesse caso, os Pins tentam corresponder a qualquer parte do tipo de mídia especificada; o valor de GUID \_ NULL funciona como um caractere curinga.

O método [**CBasePin:: Connect**](cbasepin-connect.md) começa verificando se o PIN pode aceitar uma conexão. Por exemplo, ele verifica se o PIN ainda não está conectado. Ele delega o restante do processo de conexão para o método [**CBasePin:: AgreeMediaType**](cbasepin-agreemediatype.md) . Tudo o que segue é executado pelo **AgreeMediaType**.

Se o tipo de mídia for totalmente especificado, o PIN chamará o método [**CBasePin:: AttemptConnection**](cbasepin-attemptconnection.md) para tentar a conexão. Caso contrário, ele tentará os tipos de mídia na seguinte ordem:

1.  Os tipos preferenciais do pino de entrada.
2.  Os tipos preferenciais do pino de saída.

Você pode reverter essa ordem definindo o sinalizador [**CBasePin:: m \_ BTryMyTypesFirst**](cbasepin-m-btrymytypesfirst.md) como **true**.

Em cada caso, o PIN chama [**IPin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) para enumerar os tipos de mídia. Esse método recupera um objeto Enumerator, que é passado para o método [**CBasePin:: TryMediaTypes**](cbasepin-trymediatypes.md) . O método **TryMediaTypes** percorre cada tipo de mídia e chama [**AttemptConnection**](cbasepin-attemptconnection.md) para cada tipo.

Dentro do método [**AttemptConnection**](cbasepin-attemptconnection.md) , o pino de saída chama os seguintes métodos:

-   Ele chama [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) em si mesmo, para verificar se o PIN de entrada é adequado.
-   Ele chama [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) , para validar o tipo de mídia.
-   Ele chama [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) no pino de entrada. O PIN de entrada usa esse método para determinar se ele deve aceitar a conexão.
-   Ele chama [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md) sozinho para concluir a conexão.

Observe o seguinte:

-   [**CheckConnect**](cbasepin-checkconnect.md) é um método virtual. Na classe base, esse método verifica se as direções do PIN são compatíveis. Os Pins de saída devem se conectar aos pins de entrada, e vice-versa. A classe PIN derivada normalmente substituirá esse método para executar outras verificações. Por exemplo, ele pode consultar o outro PIN para uma interface que é necessária para a conexão. Se a classe derivada substituir **CheckConnect**, ela também deverá chamar o método [**CBasePin**](cbasepin.md) .
-   [**CheckMediaType**](cbasepin-checkmediatype.md) é um método virtual puro, que a classe derivada deve implementar.
-   [**CompleteConnect**](cbasepin-completeconnect.md) é um método virtual que não faz nada na classe base. As classes derivadas podem substituir esse método para executar qualquer trabalho adicional necessário para concluir a conexão, como a decisão de um alocador de memória.

Se qualquer uma dessas etapas falhar, o pino de saída chamará o método [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) para desfazer quaisquer etapas executadas pelo [**CheckConnect**](cbasepin-checkconnect.md).

O método [**ReceiveConnection**](cbasepin-receiveconnection.md) do pino de entrada chama os métodos [**CheckConnect**](cbasepin-checkconnect.md), [**CheckMediaType**](cbasepin-checkmediatype.md)e [**CompleteConnect**](cbasepin-completeconnect.md) do pino de entrada. Se qualquer uma delas falhar, a tentativa de conexão também falhará.

O diagrama a seguir mostra o processo de conexão no [**CBasePin**](cbasepin.md):

![processo de conexão do CBasePin](images/cbasepin-connect.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CBasePin**](cbasepin.md)
</dt> </dl>

 

 



