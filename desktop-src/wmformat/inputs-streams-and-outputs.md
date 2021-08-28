---
title: entradas, Fluxos e saídas
description: entradas, Fluxos e saídas
ms.assetid: f9f979c4-a15c-4f2a-b63c-7fe776394fdd
keywords:
- Windows SDK do formato de mídia, entradas
- Windows SDK do formato de mídia, fluxos
- Windows SDK do formato de mídia, saídas
- ASF (Advanced Systems Format), entradas
- ASF (formato de sistemas avançados), entradas
- ASF (Advanced Systems Format), fluxos
- ASF (formato de sistemas avançados), fluxos
- ASF (Advanced Systems Format), saídas
- ASF (formato de sistemas avançados), saídas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4518ed60495aa2318ad27cdade2885aa2660698b5dbf2659290dabf985246da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701814"
---
# <a name="inputs-streams-and-outputs"></a>entradas, Fluxos e saídas

Uma "entrada" nesta documentação é qualquer fluxo de dados de mídia digital (como áudio ou vídeo) que seu aplicativo entrega ao objeto do gravador de uma fonte usando as APIs apropriadas. As entradas devem ser entregues em um formato com suporte. Há suporte para vários formatos padrão RGB e YUV como entrada, e os codecs de áudio dão suporte a PCM. Se um formato de entrada especificado não tiver suporte nativo pelo codec, o objeto do gravador criará uma instância de um objeto auxiliar de áudio ou vídeo capaz de converter uma ampla variedade de formatos em formatos que o codec pode aceitar. Para entradas de áudio, o objeto auxiliar ajustará a profundidade de bits, a taxa de amostragem e o número de canais conforme necessário. Para entradas de vídeo, o objeto auxiliar de vídeo executará conversões de espaço em cores e ajustes de tamanho de retângulo. Em alguns casos, dados compactados de áudio e vídeo podem ser passados em um fluxo de entrada. Uma entrada pode ser de outro tipo de mídia além de áudio e vídeo, como texto, comandos de script, imagens ainda ou dados de arquivo arbitrários.

Uma "saída" nesta documentação refere-se aos dados que o objeto leitor passa para um aplicativo para renderização. Uma saída é igual a um único fluxo no momento da reprodução. Se você estiver usando a exclusão mútua, todos os fluxos mutuamente exclusivos compartilharão uma única saída. Normalmente, os dados de saída estão na forma de dados de áudio ou vídeo não compactados, embora possam conter qualquer tipo de dados. Os formatos de saída de vídeo com suporte são listados em outro lugar nesta documentação.

O termo "fluxo" nesta documentação refere-se aos dados em um arquivo ASF, ao contrário de (1) os dados de origem de entrada antes de serem processados pelo objeto do gravador e (2) os dados de saída após serem descompactados pelo objeto leitor. Um fluxo ASF contém dados provenientes de uma única entrada no objeto Writer, embora mais de um fluxo possa ser criado com base na mesma entrada. Um fluxo tem o mesmo formato e configurações de compactação do início ao fim. Um arquivo ASF simples tem dois fluxos, um para áudio e outro para vídeo. Um arquivo mais complexo pode ter dois fluxos de áudio e vários fluxos de vídeo. Os fluxos de áudio podem ter as mesmas configurações de compactação, mas contêm conteúdo diferente, como uma narração em diferentes idiomas. Os fluxos de vídeo podem conter o mesmo conteúdo, mas têm configurações de compactação diferentes. As configurações de formato de mídia e de compactação que o objeto gravador aplicará a cada fluxo são especificadas no perfil.

A relação entre entradas, fluxos e saídas pode ser de três tipos básicos. Os três diagramas a seguir ilustram as relações.

Na relação mais básica, que é um perfil sem nenhuma exclusão mútua, cada entrada é processada pelo gravador e inserida no arquivo ASF como um único fluxo. Na reprodução, o leitor lê o fluxo e entrega amostras não compactadas como uma única saída, conforme mostrado no diagrama a seguir.

![diagrama que mostra a relação normal entre entradas, fluxos e saídas.](images/formatsdk03.png)

Uma relação mais complexa ocorre quando uma exclusão mútua de taxa de bits múltipla é usada. Nesse caso, uma única entrada é processada pelo gravador e codificada com várias taxas de bits. Cada codificação dos dados é inserida no arquivo ASF como um fluxo separado. Na reprodução, o leitor determina qual fluxo deve ser descompactado com base na largura de banda disponível. Em seguida, o leitor lê o fluxo selecionado e entrega amostras não compactadas como uma única saída, conforme mostrado no diagrama a seguir.

![diagrama mostrando as relações entre entradas, fluxos e saídas ao usar a exclusão mútua de taxa de bits múltipla.](images/formatsdk04.png)

O terceiro tipo de relação pode ocorrer quando uma exclusão mútua personalizada ou baseada em um idioma é usada. Nessa relação, várias entradas são processadas pelo leitor e cada uma é inserida no arquivo ASF como um fluxo individual. Na reprodução, o aplicativo seleciona manualmente qual fluxo deve ser descompactado com base na lógica que você fornecer. Em seguida, o leitor lê o fluxo selecionado e entrega amostras não compactadas como uma única saída. Esse processo pode ser usado para incluir trilhas sonoras em vários idiomas. O diagrama a seguir ilustra esse processo.

![diagrama mostrando as relações entre entradas, fluxos e saídas ao usar a exclusão mútua personalizada.](images/formatsdk02.png)

Há alguma variação nas relações descritas anteriormente. Por exemplo, um arquivo pode conter todas as três relações, ou uma ou duas delas. Também é possível que algumas entradas sejam compactadas, caso em que o gravador não executa nenhuma compactação adicional. O leitor, além disso, pode fornecer amostras compactadas. Mas, quando faz isso, você deve acessá-los por número de fluxo, não pelo número de saída.

> [!Note]  
> as entradas, os fluxo e as saídas são todos os números atribuídos pelos objetos do SDK do formato de mídia Windows. Fluxos tem um número de fluxo, que é baseado em 1, que você define no perfil. Cada fluxo também é atribuído a um índice de fluxo para uso na enumeração de fluxos em um perfil. Nenhum desses números tem a garantia de estar consistente entre si. Ou seja, o número de entrada 1 pode não corresponder ao fluxo número 1, o número de fluxo 1 pode não corresponder ao índice de fluxo 1 e assim por diante.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Conceitos**](concepts.md)
</dt> <dt>

[**Exclusão mútua**](mutual-exclusion.md)
</dt> </dl>

 

 




