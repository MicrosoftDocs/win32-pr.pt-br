---
title: Classificações de comandos MCI
description: Classificações de comandos MCI
ms.assetid: e03edfab-06c9-4337-935b-9effd2996c2e
keywords:
- Comandos MCI, classificações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72b532c56d1cdecac50cb24b14bf4f1b51c401dd5bb2501d1c421064659f1ef2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807925"
---
# <a name="classifications-of-mci-commands"></a>Classificações de comandos MCI

O MCI define quatro classificações de comando: sistema, necessário, básico e estendido. A lista a seguir descreve essas classificações de comando:

-   Os *comandos do sistema* são tratados diretamente pelo MCI, e não pelo driver.
-   Os *comandos necessários* são tratados pelo driver. Todos os drivers MCI devem dar suporte aos comandos e sinalizadores necessários.
-   Os *comandos básicos* (ou comandos opcionais) são usados por alguns dispositivos. Se um dispositivo oferecer suporte a um comando básico, ele deverá dar suporte a um conjunto definido de sinalizadores para esse comando.
-   Os *comandos estendidos* são específicos para um driver ou tipo de dispositivo. Os comandos estendidos incluem comandos, como os comandos [**Put**](put.md) ([**MCI \_ Put**](mci-put.md)) e [**Where**](where.md) ([**MCI \_ Where**](mci-where.md)) para os tipos de dispositivo **DigitalVideo** e **Overlay** , e extensões para comandos existentes (como o sinalizador "Stretch" do comando [**status**](status.md) ([**\_ status MCI**](mci-status.md)) para o tipo de dispositivo de sobreposição).

Embora os comandos System e Required sejam o conjunto mínimo de comandos para qualquer driver MCI, os comandos básico e estendido não têm suporte de todos os drivers. Seu aplicativo sempre pode usar os comandos System e Required e seus sinalizadores, mas se precisar usar um comando ou sinalizador básico ou estendido, ele deverá primeiro consultar o driver usando o comando [**Capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)). As seções a seguir resumem os comandos específicos em cada categoria.

## <a name="system-commands"></a>Comandos do sistema

O MCI processa os seguintes comandos do sistema diretamente, em vez de passá-los para dispositivos MCI.



| String                 | Mensagem                             | Descrição                            |
|------------------------|-------------------------------------|----------------------------------------|
| [**interrupção**](break.md) | [**interrupção de MCI \_**](mci-break.md)     | Define uma chave de interrupção para um dispositivo MCI.    |
| [SysInfo](sysinfo.md) | [**SysInfo do MCI \_**](mci-sysinfo.md) | Retorna informações sobre os dispositivos MCI. |



 

## <a name="required-commands"></a>Comandos necessários

Todos os dispositivos MCI dão suporte aos seguintes comandos necessários.



| String                           | Mensagem                                   | Descrição                                                                                                               |
|----------------------------------|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**recursos**](capability.md) | [**\_GETDEVCAPS MCI**](mci-getdevcaps.md) | Obtém os recursos de um dispositivo.                                                                                     |
| [**inclui**](close.md)           | [**fechamento de MCI \_**](mci-close.md)           | Fecha o dispositivo.                                                                                                        |
| [**informações**](info.md)             | [**informações do MCI \_**](mci-info.md)             | Obtém informações textuais de um dispositivo.                                                                                |
| [**abrir**](open.md)             | [**MCI \_ aberto**](mci-open.md)             | Inicializa o dispositivo.                                                                                                   |
| [**Status**](status.md)         | [**STATUS do MCI \_**](mci-status.md)         | Obtém informações de status do dispositivo. Alguns dos sinalizadores deste comando não são necessários, portanto, ele também é um comando básico. |



 

Os dispositivos também devem oferecer suporte a um conjunto padrão de sinalizadores de comando para os comandos necessários.

## <a name="basic-commands"></a>Comandos básicos

A lista a seguir resume os comandos básicos. O uso desses comandos por um dispositivo MCI é opcional.



| String                   | Mensagem                           | Descrição                                                                                                                                                                                                                             |
|--------------------------|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**carrega**](load.md)     | [**\_carga MCI**](mci-load.md)     | Carrega dados de um arquivo.                                                                                                                                                                                                                 |
| [**temporariamente**](pause.md)   | [**pausa de MCI \_**](mci-pause.md)   | Interrompe a reprodução. A reprodução ou a gravação podem ser retomadas na posição atual.                                                                                                                                                            |
| [**reproduzir**](play.md)     | [**\_reprodução MCI**](mci-play.md)     | Inicia a transmissão de dados de saída.                                                                                                                                                                                                        |
| [**gravável**](record.md) | [**\_registro MCI**](mci-record.md) | Inicia a gravação de dados de entrada.                                                                                                                                                                                                            |
| [**Volte**](resume.md) | [**retomar MCI \_**](mci-resume.md) | Retoma a reprodução ou a gravação em um dispositivo em pausa.                                                                                                                                                                                        |
| [**Guarde**](save.md)     | [**\_salvar MCI**](mci-save.md)     | Salva dados em um arquivo de disco.                                                                                                                                                                                                              |
| [**Procure**](seek.md)     | [**busca de MCI \_**](mci-seek.md)     | Procura para frente ou para trás.                                                                                                                                                                                                              |
| [**Definição**](set.md)       | [**conjunto de MCI \_**](mci-set.md)       | Define o estado operacional do dispositivo.                                                                                                                                                                                                 |
| [**Status**](status.md) | [**STATUS DO MCI**](mci-status.md)  | Obtém informações de status sobre o dispositivo. Esse também é um comando necessário; como alguns de seus sinalizadores não são necessários, eles também estão listados aqui. (Os itens opcionais dão suporte a dispositivos que usam mídia linear com posições identificáveis.) |
| [**deixar**](stop.md)     | [**parada do MCI \_**](mci-stop.md)     | Interrompe a reprodução.                                                                                                                                                                                                                          |



 

Se um driver oferecer suporte a um comando básico, ele também deverá oferecer suporte a um conjunto padrão de sinalizadores para o comando.

## <a name="extended-commands"></a>Comandos estendidos

Alguns dispositivos MCI têm comandos adicionais ou adicionam sinalizadores a comandos existentes. Embora alguns comandos estendidos se apliquem apenas a um driver de dispositivo específico, a maioria deles se aplica a todos os drivers de um determinado tipo de dispositivo. Por exemplo, o comando definido para o tipo de dispositivo **Sequencer** estende o comando [**set**](set.md) ([**MCI \_ set**](mci-set.md)) para adicionar formatos de hora que são necessários para os sequenciadores MIDI.

Você não deve assumir que o dispositivo dá suporte aos comandos estendidos ou sinalizadores. Você pode usar o comando de [**capacidade**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) para determinar se há suporte para um recurso específico e seu aplicativo deve estar pronto para lidar com valores de retorno "comando sem suporte" ou "função sem suporte".

Os comandos estendidos a seguir estão disponíveis com os tipos de dispositivo listados.



| String                         | Mensagem                                 | Tipos de dispositivos            | Descrição                                                                                       |
|--------------------------------|-----------------------------------------|-------------------------|---------------------------------------------------------------------------------------------------|
| [**Configurar**](configure.md) | [**MCI \_ CONFIGURE**](mci-configure.md) | digitalvideo            | Exibe uma caixa de diálogo de configuração.                                                              |
| [**Cue**](cue.md)             | [**MCI \_ CUE**](mci-cue.md)             | digitalvideo, waveaudio | Prepara-se para reprodução ou gravação.                                                                |
| [**Excluir**](delete.md)       | [**MCI \_ DELETE**](mci-delete.md)       | Waveaudio               | Exclui um segmento de dados do arquivo de mídia.                                                       |
| [Escapar](escape.md)           | [**ESCAPE \_ da MCI**](mci-escape.md)       | videodisc               | Envia informações personalizadas para um dispositivo.                                                             |
| [**Congelar**](freeze.md)       | [**MCI \_ FREEZE**](mci-freeze.md)       | overlay                 | Desabilita a aquisição de vídeo para o buffer de quadros.                                                   |
| [**Colocar**](put.md)             | [**MCI PUT**](mci-put.md)              | digitalvideo, sobreposição   | Define as janelas de origem, destino e quadro.                                               |
| [**Perceber**](realize.md)     | [**MCI \_ REALIZE**](mci-realize.md)     | digitalvideo            | Informa ao dispositivo para selecionar e realizar sua paleta em um contexto de dispositivo da janela exibida. |
| [**Setaudio**](setaudio.md)   | [**MCI \_ SETAUDIO**](mci-setaudio.md)  | digitalvideo            | Define parâmetros de áudio para vídeo.                                                                  |
| [**setvideo**](setvideo.md)   | [**MCI \_ SETVIDEO**](mci-setvideo.md)  | digitalvideo            | Define parâmetros de vídeo.                                                                            |
| [**Sinal**](signal.md)       | [**MCI \_ SIGNAL**](mci-signal.md)       | digitalvideo            | Identifica uma posição especificada com um sinal.                                                    |
| [**Spin**](spin.md)           | [**ROTAÇÃO da MCI \_**](mci-spin.md)           | videodisc               | Inicia a rotação do disco ou impede a rotação do disco.                                         |
| [**Passo**](step.md)           | [**ETAPA da \_ MCI**](mci-step.md)           | digitalvideo, videodisc | As etapas reproduzem um ou mais quadros para frente ou para trás.                                             |
| [**Descongelar**](unfreeze.md)   | [**MCI \_ UNFREEZE**](mci-unfreeze.md)   | overlay                 | Permite que o buffer de quadros adquira dados de vídeo.                                                   |
| [**Atualização**](update.md)       | [**ATUALIZAÇÃO \_ da MCI**](mci-update.md)       | digitalvideo            | Reintsimos o quadro atual no contexto do dispositivo.                                               |
| [**Onde**](where.md)         | [**MCI WHERE**](mci-where.md)          | digitalvideo, sobreposição   | Obtém o retângulo que especifica a área de origem, destino ou quadro.                          |
| [**Janela**](window.md)       | [**JANELA \_ MCI**](mci-window.md)       | digitalvideo, sobreposição   | Controla a janela de exibição.                                                                      |



 

 

 




