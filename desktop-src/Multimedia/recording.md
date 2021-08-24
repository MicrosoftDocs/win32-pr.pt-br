---
title: Gravação
description: Gravação
ms.assetid: 0026eb1d-5be1-4090-801b-f1c65c179f42
keywords:
- MCI_RECORD comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27033dde148a6f99a1168eea4d6c0a97aea82881638ccb6d6f5535632e897148
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805506"
---
# <a name="recording"></a>Gravação

A especificação geral da MCI dá suporte à gravação com vídeo digital, sequenciador MIDI, VCR (gravador de gravação de vídeo) e dispositivos waveform-audio; no entanto, somente dispositivos waveform-audio e VCR atualmente implementam recursos de gravação. Você pode inserir ou substituir informações gravadas em um arquivo ou registro existente em um novo arquivo. Para gravar em um arquivo existente, abra um dispositivo e um arquivo waveform-audio como faria normalmente. Para registrar em um novo arquivo, ao abrir o dispositivo, especifique "novo" como o nome do dispositivo se você estiver usando a interface de cadeia de caracteres de comando. Se você estiver usando a interface de mensagem de comando, especifique um nome de arquivo de comprimento zero.

Quando a MCI cria um novo arquivo para gravação, o formato de dados é definido como um formato padrão especificado pelo driver de dispositivo. Para usar um formato diferente do formato padrão, você pode usar o [**comando set**](set.md) ([**MCI \_ SET**](mci-set.md)).

Para começar a gravação, use o [**comando record**](record.md) (ou [**REGISTRO MCI \_**](mci-record.md) e a estrutura [**\_ \_ PARMS de REGISTRO MCI).**](mci-record-parms.md)

Se você registrar no modo de inserção em um arquivo existente, poderá usar os sinalizadores "from" (MCI FROM) e \_ "to" (MCI TO) do comando de registro para especificar as posições inicial e final para \_  gravação. Por exemplo, se você gravar em um arquivo de 20 segundos e começar a gravar em 5 segundos e terminar a gravação em 10 segundos, o arquivo resultante terá 25 segundos de duração. O arquivo terá um segmento de 5 segundos inserido 5 segundos na gravação original.

Se você registrar com o modo de substituir para um arquivo existente, poderá usar os sinalizadores "from" e "to" para especificar locais de início e término da seção que é substituída. Por exemplo, se você gravar em um arquivo de 20 segundos e começar a gravar em 5 segundos e terminar a gravação em 10 segundos, ainda terá uma gravação de 20 segundos, mas a seção que começa em 5 segundos e termina em 10 segundos terá sido substituída.

Se você não especificar um local final, a gravação continuará até que você envie um comando [**stop**](stop.md) ([**MCI \_ STOP**](mci-stop.md)) ou até que o driver seja executado sem espaço livre em disco. Se você gravar em um novo arquivo, poderá omitir o sinalizador "from" ou defini-lo como zero para iniciar a gravação no início de um novo arquivo. Você pode especificar um local final para encerrar a gravação ao gravar em um novo arquivo.

Às [**vezes,**](record.md) o comando de registro é preciso em apenas 1 segundo do local inicial, como com dispositivos VCR. Para registrar com mais precisão, você deve usar o [**comando cue**](cue.md) ([**MCI \_ CUE**](mci-cue.md)). Esse comando é reconhecido por dispositivos de vídeo digital, VCR e waveform-audio. Para obter mais informações sobre a gravação com dispositivos VCR, consulte [Serviços vcr](vcr-services.md).

## <a name="saving-a-recorded-file"></a>Salvando um arquivo gravado

Quando a gravação for concluída, use o comando [**save**](save.md) (ou [**MCI \_ SAVE**](mci-save.md) e a estrutura [**MCI \_ SAVE \_ PARMS)**](mci-save-parms.md) para salvar a gravação antes de fechar o dispositivo.

> [!Note]  
> Se você fechar o dispositivo sem salvar, os dados gravados serão perdidos.

 

## <a name="checking-input-levels-pcm-only"></a>Verificando níveis de entrada (somente PCM)

Para obter o nível do sinal de entrada antes de gravar em um dispositivo de entrada de áudio waveform-audio do PCM (Pulse Code), use o [**comando status**](status.md) ([**\_ STATUS da MCI**](mci-status.md)). Especifique o sinalizador "level" (ou o sinalizador ITEM DE STATUS da MCI e de definido o membro \_ \_ **dwItem** da estrutura [**\_ \_ PARMS DE STATUS**](mci-status-parms.md) da MCI como NÍVEL DE STATUS DE ONDA da MCI). \_ \_ \_ O nível médio do sinal de entrada é retornado. O valor do canal esquerdo está na palavra de ordem alta e o valor de canal direito ou mono channel está na palavra de ordem baixa.

O nível de entrada é representado como um valor sem sinal. Para exemplos de 8 bits, esse valor está no intervalo de 0 a 127 (0x7F). Para exemplos de 16 bits, ele está no intervalo de 0 a 32.767 (0x7FFF).

 

 




