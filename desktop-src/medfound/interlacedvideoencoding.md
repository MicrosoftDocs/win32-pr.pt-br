---
description: Codificação de vídeo entrelaçado
ms.assetid: 7695d4e3-4a75-4972-ab02-bc532d6a4dce
title: Codificação de vídeo entrelaçado (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fafacb56f29964e81b040c59cdb75d8ebb35830b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922571"
---
# <a name="interlaced-video-encoding-microsoft-media-foundation"></a>Codificação de vídeo entrelaçado (Microsoft Media Foundation)

Os dados de vídeo destinados ao uso com computadores normalmente são *progressivos*, o que significa que cada quadro é codificado como uma única imagem. Alguns dispositivos, como televisões, não exibem um quadro de uma só vez, mas como duas imagens. Uma das imagens, ou campos, contém todas as linhas ainda numeradas. O outro campo contém os dados de todas as linhas ímpares numeradas. O vídeo codificado com mais de um campo por quadro é chamado de entrelaçado, pois é renderizado alternando entre o campo par e o campo ímpar.

No passado, o conteúdo de vídeo entrelaçado era sempre desentrelaçado antes da codificação com o codec de vídeo do Windows Media. No entanto, a partir do Windows Media 9 Series, o codificador de vídeo dá suporte à compactação de conteúdo entrelaçado sem primeiro convertê-lo para progressivo. Manter o entrelaçamento em um arquivo codificado é importante se o conteúdo for renderizado em uma exibição entrelaçada, como uma televisão. Esse recurso é de maior importância, como o suporte para o espelhamento de conteúdo baseado no Windows Media para players de DVD, caixas superiores de conjunto e outras eletrônicas domésticas.

A maneira mais fácil de codificar e fornecer vídeo entrelaçado é desenvolver seu aplicativo usando o Windows Media Format SDK e armazenar o conteúdo em arquivos ASF. As informações entrelaçadas sobre quadros são passadas para o codec usando extensões de unidade de dados, que funcionam bem para conteúdo ASF, mas são um pouco mais complicados de dar suporte a outros contêineres. Para obter mais informações sobre extensões de unidade de dados, consulte [usando extensões de unidade de dados](usingdataunitextensions.md).

Para dar suporte à codificação entrelaçada envolve duas etapas principais: obter as informações do quadro para o codificador e fornecer as informações para o aplicativo de renderização. Essas etapas são descritas nos parágrafos a seguir.

## <a name="interlaced-video-and-the-encoder"></a>Vídeo entrelaçado e o codificador

A primeira etapa na codificação de vídeo com entrelaçamento mantido é configurar o codificador para codificar campos entrelaçados. Para fazer isso, defina a propriedade [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) como **true**. Isso prepara o codificador para receber amostras entrelaçadas. Cada amostra de entrada deve conter ambos os campos.

Cada exemplo que você processa com o codificador após a ativação da codificação entrelaçada deve ter uma extensão de unidade de dados anexada. Os exemplos sem a extensão de unidade de dados esperada são considerados progressivos. O GUID que identifica a extensão é D590DC20-07BC-436C-9CF7-F3BBFBF1A4DC. Os valores passados pelos objetos do Windows Media Format SDK são definidos na tabela a seguir.



| Valor      | Descrição                                                                                                                              |
|------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 0x00000020 | Especifica que o exemplo é codificado primeiro com o campo inferior. Esse valor só é significativo quando combinado com o valor entrelaçado. |
| 0x00000040 | Especifica que o exemplo é codificado primeiro com o campo superior. Esse valor só é significativo quando combinado com o valor entrelaçado.    |
| 0x00000080 | Especifica que o exemplo é entrelaçado. Esse é o único valor que é significativo para o codec DMOs.                                    |



 

Um dos dois primeiros valores é sempre combinado com 0x80 usando um OR bit a bit **ou** antes de ser definido no exemplo. No entanto, o codificador verifica apenas 0x80 e ignora o restante da extensão. Se a extensão identificar o exemplo como entrelaçado, o codificador manterá o entrelaçamento de exemplo no fluxo compactado e inserirá um sinalizador de indicação no fluxo para que o decodificador possa identificar quadros entrelaçados. Cada amostra entrelaçada é marcada, de modo que o conteúdo de origem que é uma mistura progressiva e entrelaçada pode ser codificado em um fluxo em conjunto.

O objeto gravador do SDK do Windows Media Format inclui as extensões de unidade de dados do tipo de conteúdo nos exemplos que ele grava na seção de dados do contêiner do ASF para uso no momento da renderização.

## <a name="reading-and-rendering-interlaced-video"></a>Leitura e renderização de vídeo entrelaçado

O decodificador identifica amostras entrelaçadas com base no sinalizador definido no fluxo pelo codificador. Como padrão, o decodificador Desentrelaça os exemplos e entrega saídas progressivas. O aplicativo de player pode configurar o decodificador para processar as saídas com o entrelaçamento mantido, definindo a propriedade de [ \_ \_ desentrelaçamento de deMFPKEY de decodificação](mfpkey-decoder-deinterlacingproperty.md) .

A dificuldade na reprodução de vídeo entrelaçado surge depois que o decodificador entrega os exemplos. O processador (placa de vídeo ou chip em um dispositivo) não pode exibir corretamente o conteúdo do vídeo sem saber qual campo é. Em aplicativos que usam o Windows Media Format SDK, a extensão de unidade de dados de tipo de conteúdo é recuperada de amostras não compactadas e pode ser passada para o dispositivo.

Ao usar os objetos de codec diretamente, nenhuma dessas transferências de dados é automática. Você deve implementar o suporte de extensão de unidade de dados, tanto em seus objetos de buffer quanto no contêiner que você usa para o conteúdo codificado. Os tipos mais comuns de contêineres de mídia (como AVI) não oferecem suporte a metadados de nível de exemplo. Você pode implementar seu próprio sistema para armazenar os dados no arquivo e associá-los a exemplos individuais, mas apenas um leitor personalizado poderá recuperá-lo.

> [!Note]  
> Definir a propriedade [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) como **true** e, em seguida, não enviar quaisquer amostras com a extensão de unidade de dados de tipo de conteúdo anexada pode fazer com que o codificador falhe. Defina o codificador para codificação entrelaçada somente se você tiver amostras entrelaçadas a serem entregues.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com vídeo](workingwithvideo.md)
</dt> </dl>

 

 



