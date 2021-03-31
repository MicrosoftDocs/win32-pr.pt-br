---
description: Suporte a extensões de MTP
ms.assetid: 9e5f3da6-346a-4eca-bc85-2755c569986d
title: Suporte a extensões de MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f26a6a5a585167984ec944528bb74a6746e42ac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829592"
---
# <a name="supporting-mtp-extensions"></a>Suporte a extensões de MTP

## <a name="media-transfer-protocol"></a>Protocolo de transferência de mídia

O MTP (protocolo de transferência de mídia) é uma extensão do PTP (protocolo de transferência de imagem). Como resultado, todas as semânticas do protocolo PTP são válidas em MTP.

O MTP se comunica usando comandos e respostas entre duas partes, o iniciador e o respondente. As funções dos dispositivos envolvidos são claramente definidas. O PC normalmente é o iniciador, e o dispositivo é sempre o respondente. Um dispositivo que não seja de PC também poderia ser um iniciador (por exemplo, um baralho de carro ou uma caixa de X da Microsoft). Um dispositivo nunca pode assumir ambas as funções ao mesmo tempo.

O iniciador inicia a comunicação enviando um comando para o respondente. O respondente processa o comando e envia de volta uma resposta apropriada. Pode haver uma fase de dados associada ao comando. Se esse for o caso, a direção do fluxo de dados deve ser conhecida com antecedência e aceita pelo iniciador e pelo respondente. Lembre-se de que não há um cabeçalho descritivo que indica fluxos de dados para novos comandos.

O respondente pode iniciar a comunicação independente do iniciador. Por exemplo, o respondente pode enviar eventos para o iniciador. No entanto, nenhum dado pode ser enviado junto com o evento. Se houver dados que precisam ser lidos como parte do evento, o iniciador deverá enviar um comando MTP e o dispositivo poderá enviar dados em resposta ao comando.

Para obter uma descrição completa do MTP, consulte a [especificação do MTP](https://www.usb.org/sites/default/files/MTPv1_1.zip).

## <a name="sending-mtp-commands"></a>Enviando comandos MTP

Os aplicativos podem enviar comandos MTP para um dispositivo invocando o método [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) . O comando que é enviado depende de se há uma fase de dados e se algum dado que o acompanha é lido ou gravado no dispositivo. A tabela a seguir descreve os três comandos de extensão MTP possíveis.

Lembre-se de que esses comandos são específicos para MTP; e, portanto, são implementadas apenas pelo driver de classe MTP WPD.



|                                                                                                                                      |                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| Comando                                                                                                                              | Descrição                                                                                       |
| [**\_transferência de \_ \_ dados de \_ extremidade \_ de \_ MTP de comando WPD**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-end-data-transfer)                                      | Emite um comando MTP que sinaliza a conclusão de uma operação de leitura ou gravação de dados.              |
| [**comando WPD de \_ \_ MTP \_ ext comando \_ \_ \_ sem \_ fase de dados \_**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-without-data-phase)  | Emite um comando MTP sem uma fase de dados correspondente.                                         |
| [**\_comando WPD \_ MTP \_ ext \_ \_ comando \_ com \_ dados \_ a serem \_ gravados**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) | Emite um comando MTP seguido pelo acompanhamento de dados, que serão gravados no dispositivo. |
| [**\_comando WPD \_ MTP \_ ext \_ \_ comando \_ com \_ dados \_ a serem \_ lidos**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read)   | Emite um comando MTP seguido pelo acompanhamento de dados, que é lido do dispositivo.       |
| [**comando WPD de \_ \_ leitura de \_ \_ dados de extensão MTP \_**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-read-data)                                                       | Emite um comando MTP que envia dados do dispositivo para o PC.                                  |
| [**comando WPD de \_ \_ gravação de \_ \_ \_ dados do MTP**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-write-data)                                                     | Emite um comando MTP que envia dados para o dispositivo do PC.                                  |



 

Seja qual for a fase, a **Propriedade WPD do MTP e o \_ \_ \_ \_ \_ código** da operação de especificação do **\_ \_ MTP \_ ext \_ \_ Property** devem ser especificados.

Se o driver MTP puder enviar o comando para o dispositivo, os valores de retorno sempre conterão o **\_ código de \_ \_ \_ resposta \_ MTP ext da propriedade WPD**. Se o código de resposta indicar êxito e se a semântica do comando permitir parâmetros de resposta, o **\_ parâmetro de \_ \_ resposta de \_ \_ extensão MTP da propriedade WPD** também estará disponível.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 
