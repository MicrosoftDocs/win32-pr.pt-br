---
description: Suporte a extensões de MTP
ms.assetid: 9e5f3da6-346a-4eca-bc85-2755c569986d
title: Suporte a extensões de MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898df3f1347af2ccc42a796b480156b6603b13ec
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423726"
---
# <a name="supporting-mtp-extensions"></a>Suporte a extensões de MTP

## <a name="media-transfer-protocol"></a>Protocolo de transferência de mídia

O MTP (protocolo de transferência de mídia) é uma extensão do PTP (protocolo de transferência de imagem). Como resultado, todas as semânticas do protocolo PTP são válidas em MTP.

O MTP se comunica usando comandos e respostas entre duas partes, o iniciador e o respondente. As funções dos dispositivos envolvidos são claramente definidas. O PC normalmente é o iniciador, e o dispositivo é sempre o respondente. Um dispositivo que não seja de PC também poderia ser um iniciador (por exemplo, um baralho de carro ou uma caixa de X da Microsoft). Um dispositivo nunca pode assumir ambas as funções ao mesmo tempo.

O iniciador inicia a comunicação enviando um comando para o respondente. O respondente processa o comando e envia de volta uma resposta apropriada. Pode haver uma fase de dados associada ao comando. Se esse for o caso, a direção do fluxo de dados deve ser conhecida com antecedência e aceita pelo iniciador e pelo respondente. Lembre-se de que não há um cabeçalho descritivo que indica fluxos de dados para novos comandos.

O respondente pode iniciar a comunicação independente do iniciador. Por exemplo, o respondente pode enviar eventos para o iniciador. No entanto, nenhum dado pode ser enviado junto com o evento. Se houver dados que precisam ser lidos como parte do evento, o iniciador deverá enviar um comando MTP e o dispositivo poderá enviar dados em resposta ao comando.

Para uma descrição completa do MTP, consulte a [especificação de MTP](https://www.usb.org/sites/default/files/MTPv1_1.zip).

## <a name="sending-mtp-commands"></a>Enviando comandos MTP

Os aplicativos podem enviar comandos MTP para um dispositivo invocando o [**método IPortableDevice::SendCommand.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) O comando enviado depende de se há uma fase de dados e se os dados que acompanham são lidos ou gravados no dispositivo. A tabela a seguir descreve os três comandos de extensão MTP possíveis.

Esteja ciente de que esses comandos são específicos do MTP; e, portanto, são implementados apenas pelo driver de classe WPD MTP.



| Comando  | Descrição  |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**TRANSFERÊNCIA DE DADOS DE EXTREMIDADE EXT DO COMANDO WPD \_ \_ MTP \_ \_ \_ \_**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-end-data-transfer)                                      | Emite um comando MTP que sinaliza a conclusão de uma operação de leitura ou gravação de dados.              |
| [**COMANDO WPD \_ \_ MTP \_ EXT EXECUTE SEM FASE DE \_ \_ \_ \_ \_ DADOS**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-without-data-phase)  | Emite um comando MTP sem uma fase de dados correspondente.                                         |
| [**COMANDO WPD \_ \_ MTP \_ EXT EXECUTE COM DADOS A \_ \_ \_ \_ \_ \_ GRAVAR**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) | Emite um comando MTP que é seguido pelos dados de acompanhamento, que serão gravados no dispositivo. |
| [**COMANDO WPD \_ \_ MTP \_ EXT EXECUTE COM DADOS A \_ \_ \_ \_ \_ \_ LER**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read)   | Emite um comando MTP que é seguido pelos dados de acompanhamento, que são lidos do dispositivo.       |
| [**DADOS DE LEITURA EXT \_ \_ DO MTP \_ DO \_ \_ COMANDO WPD**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-read-data)                                                       | Emite um comando MTP que envia dados do dispositivo para o computador.                                  |
| [**DADOS DE GRAVAÇÃO EXT \_ \_ DO MTP \_ \_ DO \_ COMANDO WPD**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-write-data)                                                     | Emite um comando MTP que envia dados para o dispositivo do pc.                                  |



 

Independentemente da fase, **WPD \_ PROPERTY \_ MTP \_ EXT OPERATION \_ \_ CODE** e **WPD PROPERTY \_ \_ MTP EXT OPERATION \_ \_ \_ PARAMS** devem ser especificados.

Se o driver MTP conseguir enviar o comando para o dispositivo, os valores de retorno sempre conterão **WPD \_ PROPERTY \_ MTP \_ EXT RESPONSE \_ \_ CODE**. Se o código de resposta indicar êxito e se a semântica do comando permitir parâmetros de resposta, o **\_ parâmetro de \_ \_ resposta de \_ \_ extensão MTP da propriedade WPD** também estará disponível.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 
