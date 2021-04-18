---
title: Gravação
description: Gravação
ms.assetid: 0026eb1d-5be1-4090-801b-f1c65c179f42
keywords:
- MCI_RECORD comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4248b2d4bbdd984ad23a772f0adca04581afca1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105766857"
---
# <a name="recording"></a>Gravação

A especificação de MCI geral dá suporte à gravação com vídeo digital, Sequencer MIDI, gravador de vídeo-fita (VCR) e dispositivos de wave-áudio; no entanto, somente os dispositivos de onda de áudio e VCR atualmente implementam recursos de gravação. Você pode inserir ou substituir informações gravadas em um arquivo ou registro existente em um novo arquivo. Para gravar em um arquivo existente, abra um arquivo e um dispositivo de wave-áudio como faria normalmente. Para registrar em um novo arquivo, ao abrir o dispositivo, especifique "novo" como o nome do dispositivo se você estiver usando a interface de cadeia de caracteres de comando. Se você estiver usando a interface de mensagem de comando, especifique um nome de arquivo de comprimento zero.

Quando o MCI cria um novo arquivo para gravação, o formato de dados é definido como um formato padrão especificado pelo driver de dispositivo. Para usar um formato diferente do formato padrão, você pode usar o comando [**set**](set.md) ([**MCI \_ set**](mci-set.md)).

Para começar a gravar, use o comando de [**registro**](record.md) (ou o [**\_ registro MCI**](mci-record.md) e a estrutura de [**\_ \_ parâmetros do registro MCI**](mci-record-parms.md) ).

Se você gravar no modo de inserção em um arquivo existente, poderá usar os sinalizadores "de" (MCI \_ de) e "para" (MCI \_ para) do comando de **registro** para especificar as posições inicial e final para gravação. Por exemplo, se você gravar em um arquivo com 20 segundos de comprimento e começar a gravar em 5 segundos e terminar a gravação em 10 segundos, o arquivo resultante terá 25 segundos de comprimento. O arquivo terá um segmento de 5 segundos inserido 5 segundo na gravação original.

Se você gravar com o modo de substituição em um arquivo existente, poderá usar os sinalizadores "de" e "para" para especificar os locais inicial e final da seção que é substituída. Por exemplo, se você gravar em um arquivo com 20 segundos de comprimento e começar a gravar em 5 segundos e terminar a gravação em 10 segundos, ainda terá uma gravação de 20 segundos, mas a seção que começa em 5 segundos e termina em 10 segundos terá sido substituída.

Se você não especificar um local final, a gravação continuará até que você envie um comando [**parar**](stop.md) ([**\_ parada do MCI**](mci-stop.md)) ou até que o driver fique sem espaço livre em disco. Se você gravar em um novo arquivo, poderá omitir o sinalizador "de" ou defini-lo como zero para iniciar a gravação no início de um novo arquivo. Você pode especificar um local final para terminar a gravação ao gravar em um novo arquivo.

O comando de [**registro**](record.md) às vezes é preciso em apenas 1 segundo do local inicial, como com os dispositivos VCR. Para registrar com mais precisão, você deve usar o comando [**Cue**](cue.md) ([**\_ indicação MCI**](mci-cue.md)). Esse comando é reconhecido pelos dispositivos Digital-Video, VCR e Wave-Audio. Para obter mais informações sobre a gravação com dispositivos VCR, consulte [serviços de VCR](vcr-services.md).

## <a name="saving-a-recorded-file"></a>Salvando um arquivo gravado

Quando a gravação for concluída, use o comando [**salvar**](save.md) ( [**ou \_ salve o MCI**](mci-save.md) e a estrutura de [**parâmetros de \_ salvamento \_ do MCI**](mci-save-parms.md) ) para salvar a gravação antes de fechar o dispositivo.

> [!Note]  
> Se você fechar o dispositivo sem salvar, os dados gravados serão perdidos.

 

## <a name="checking-input-levels-pcm-only"></a>Verificando os níveis de entrada (somente PCM)

Para obter o nível do sinal de entrada antes da gravação em um dispositivo de entrada PCM (modulação de código de pulso)-áudio, use o comando [**status**](status.md) ([**\_ status do MCI**](mci-status.md)). Especifique o sinalizador de "nível" (ou o \_ sinalizador de item de status do MCI \_ e defina o membro **dwItem** da estrutura de [**parâmetros de \_ status \_ do MCI**](mci-status-parms.md) para o \_ nível de status de onda MCI \_ \_ ). O nível médio de sinal de entrada é retornado. O valor do canal esquerdo está na palavra de ordem superior e o valor de canal à direita ou mono está na palavra de ordem inferior.

O nível de entrada é representado como um valor não assinado. Para exemplos de 8 bits, esse valor está no intervalo de 0 a 127 (0x7F). Para exemplos de 16 bits, ele está no intervalo de 0 a 32.767 (0x7FFF).

 

 




