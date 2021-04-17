---
description: Usando uma lista de decisões de edição para codificação de voz
ms.assetid: a3d88483-acc9-47cf-8735-f17bd3b4ad57
title: Usando uma lista de decisões de edição para codificação de voz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970cc40bc5749b9edc1017546020fa3806a9730b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749180"
---
# <a name="using-an-editing-decision-list-for-encoding-voice"></a>Usando uma lista de decisões de edição para codificação de voz

Uma EDL (lista de decisões de edição), são dados fornecidos a um codec que fornece informações sobre como partes específicas de conteúdo devem ser codificadas. O codec de voz do Windows Media Audio 9 dá suporte a uma EDL simples na qual você pode especificar as partes do conteúdo que contêm música. Por padrão, o codec detecta passagens de música em si quando configurado para codificar conteúdo misto. Você deve usar um EDL somente se o codec não estiver detectando os tipos de conteúdo corretamente.

Para usar uma EDL, o codificador de voz deve ser definido para codificar conteúdo misto. Configure o modo do codec de voz para "misto" definindo a propriedade [MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) como 2. Defina o EDL usando a propriedade [MFPKEY \_ WMAVOICE \_ ENC \_ EDL](mfpkey-wmavoice-enc-edlproperty.md) . O valor dessa propriedade é uma cadeia de caracteres que contém uma lista delimitada por vírgulas dos intervalos de tempo no conteúdo que deve ser codificado como música. O primeiro item da lista é a versão do EDL, que é sempre 1. O segundo item é o número de seções de música descritas na lista. Seguir o segundo item são um número de pares de valores iguais ao segundo item; cada par de valores descreve o ponto inicial e final de uma passagem de música no conteúdo, em milissegundos.

Por exemplo, a cadeia de caracteres EDL "1, 4, 1000, 2000, 5000, 6000, 9000, 10000, 13000, 14000" especifica quatro passagens musicais, cada uma delas com um segundo. Se as informações na cadeia de caracteres do EDL forem inválidas, elas serão ignoradas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o codec de voz do Windows Media Audio 9](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[Trabalhando com áudio](workingwithaudio.md)
</dt> </dl>

 

 



