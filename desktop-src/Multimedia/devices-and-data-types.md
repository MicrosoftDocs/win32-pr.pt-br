---
title: Dispositivos e tipos de dados
description: Dispositivos e tipos de dados
ms.assetid: 46247983-19c3-4c7a-a615-ba6cd8bd3289
keywords:
- waveform audio, abrindo dispositivos de saída
- interface waveform-audio, abrindo dispositivos de saída
- abrindo dispositivos de saída waveform-audio
- waveform audio,consultando dispositivos de saída
- interface waveform-audio, consultando dispositivos de saída
- consultando dispositivos de saída de áudio de forma de onda
- waveform audio,device handles
- interface waveform-audio, alças de dispositivo
- áudio waveform, identificadores de dispositivo
- interface waveform-audio, identificadores de dispositivo
- áudio waveform, tipos de dados de saída
- interface waveform-audio, tipos de dados de saída
- waveform audio, formatos de dados
- interface waveform-audio, formatos de dados
- escrevendo dados waveform-audio
- waveform audio, escrevendo dados
- interface waveform-audio, escrevendo dados
- Dados de áudio de forma de onda do PCM
- áudio waveform, dados do PCM
- interface waveform-audio, dados do PCM
- áudio waveform, fechando dispositivos de saída
- interface waveform-audio, fechando dispositivos de saída
- fechando dispositivos de saída waveform-audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 165f740e260c4e1a25fbd40cac9b8efd66ccd401c3e166dd1119b92c7b9999f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941264"
---
# <a name="devices-and-data-types"></a>Dispositivos e tipos de dados

Esta seção descreve como trabalhar com dispositivos waveform-audio e inclui informações sobre como abri-los, fechar e consultar seus recursos. Ele também descreve como controlar os dispositivos em um sistema usando identificadores de dispositivo e identificadores de dispositivo.

## <a name="opening-waveform-audio-output-devices"></a>Abrindo Waveform-Audio de saída

Use a [**função waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) para abrir um dispositivo de saída waveform-audio para reprodução. Essa função abre o dispositivo associado ao identificador de dispositivo especificado e retorna um identificador do dispositivo aberto escrevendo o identificador de um local de memória especificado.

Alguns computadores multimídia têm vários dispositivos de saída de áudio de forma de onda. A menos que você queira abrir um dispositivo de saída de áudio de forma de onda específico em um sistema, use o sinalizador WAVE MAPPER para o identificador do dispositivo ao \_ abrir um dispositivo. A **função waveOutOpen** escolhe o dispositivo no sistema que é mais bem capaz de reproduzir o formato de dados especificado.

## <a name="querying-audio-devices"></a>Consultando dispositivos de áudio

Windows fornece as funções a seguir para determinar quantos dispositivos de um determinado tipo estão disponíveis em um sistema.



| Função                                       | Descrição                                                                  |
|------------------------------------------------|------------------------------------------------------------------------------|
| [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)         | Recupera o número de dispositivos de saída auxiliares presentes no sistema.      |
| [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)   | Recupera o número de dispositivos de entrada waveform-audio presentes no sistema.  |
| [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs) | Recupera o número de dispositivos de saída de áudio de forma de onda presentes no sistema. |



 

Os dispositivos de áudio são identificados por um identificador de dispositivo. O identificador do dispositivo é determinado implicitamente do número de dispositivos presentes em um sistema. Os identificadores de dispositivo variam de zero a um a menos do que o número de dispositivos presentes. Por exemplo, se houver dois dispositivos de saída waveform-audio em um sistema, os identificadores de dispositivo válidos serão 0 e 1.

Depois de determinar quantos dispositivos de um determinado tipo estão presentes em um sistema, você pode usar uma das funções a seguir para consultar os recursos de cada dispositivo.



| Função                                       | Descrição                                                             |
|------------------------------------------------|-------------------------------------------------------------------------|
| [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)         | Recupera os recursos de um dispositivo de saída auxiliar especificado.      |
| [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)   | Recupera os recursos de um dispositivo de entrada de áudio de forma de onda especificado.  |
| [**Waveoutgetdevcaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) | Recupera os recursos de um dispositivo de saída de áudio de forma de onda especificado. |



 

Cada uma dessas funções preenche uma estrutura com informações sobre os recursos de um dispositivo especificado. A tabela a seguir lista as estruturas que correspondem a cada uma dessas funções.



|  Função                                              |  Estrutura                                  |
|------------------------------------------------|------------------------------------|
| [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)         | [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)         |
| [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)   | [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)   |
| [**Waveoutgetdevcaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) | [**Waveoutcaps**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) |



 

Os formatos padrão são listados no **membro dwFormats** da **estrutura WAVEOUTCAPS.** Dispositivos waveform-audio podem dar suporte a formatos não padrão. Para determinar se um formato específico (padrão ou não padrão) é suportado por um dispositivo, você pode chamar a função [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) com o sinalizador WAVE \_ FORMAT \_ QUERY. Esse sinalizador não abre o dispositivo. Especifique o formato em questão na estrutura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) apontada pelo parâmetro *pwfx* passado para **waveOutOpen.**

Os dispositivos de saída waveform-audio variam de acordo com os recursos que eles suportam. O **membro dwSupport** da estrutura [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) indica se um dispositivo dá suporte a recursos como alterações de volume e de tom.

## <a name="device-handles-and-device-identifiers"></a>Identificadores de dispositivo e identificadores de dispositivo

Cada função que abre um dispositivo de áudio especifica um identificador de dispositivo, um ponteiro para um local de memória e alguns parâmetros exclusivos para cada tipo de dispositivo. O local de memória é preenchido com um alça de dispositivo. Use esse identificador de dispositivo para identificar o dispositivo de áudio aberto ao chamar outras funções de áudio.

A diferença entre identificadores e identificadores para dispositivos de áudio é sutil, mas importante:

-   Os identificadores de dispositivo são determinados implicitamente do número de dispositivos presentes em um sistema. Esse número é obtido usando [**a função auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs), [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)ou [**waveOutGetNumDevs.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs)
-   Os alças de dispositivo são retornados quando os drivers de dispositivo são abertos usando a [**função waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) ou [**waveOutOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)

Não há funções que abrem ou fecham dispositivos de áudio auxiliares. Os dispositivos de áudio auxiliares não precisam ser abertos e fechados como dispositivos waveform-audio porque não há transferência contínua de dados associada a eles. Todas as funções auxiliares de áudio usam identificadores de dispositivo para identificar dispositivos.

## <a name="waveform-audio-output-data-types"></a>Waveform-Audio de dados de saída

Os tipos de dados a seguir são definidos para funções de saída waveform-audio.



| Tipo                                 | Descrição                                                                                                                                                   |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HWAVEOUT**                         | Lidar com um dispositivo de saída de áudio de forma de onda aberta.                                                                                                               |
| [**Waveformatex**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | Estrutura que especifica os formatos de dados com suporte por um dispositivo de entrada waveform-audio específico. Essa estrutura também é usada para dispositivos de entrada waveform-audio. |
| [**Wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | Estrutura usada como um header para um bloco de dados de entrada waveform-audio. Essa estrutura também é usada para dispositivos de entrada waveform-audio.                            |
| [**Waveoutcaps**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)   | Estrutura usada para consultar os recursos de um dispositivo de saída de áudio de forma de onda específico.                                                                        |



 

## <a name="specifying-waveform-audio-data-formats"></a>Especificando Waveform-Audio formatos de dados

Quando você chama a função [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) para abrir um driver de dispositivo para reprodução ou para consultar se o driver dá suporte a um formato de dados específico, use o parâmetro *pwfx* para especificar um ponteiro para uma estrutura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) que contém o formato de dados Wave-Audio solicitado. **WAVEFORMATEX** substitui as estruturas [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) e [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) .

Para dados de áudio separados em mais de dois canais ou tem um tamanho de amostra que não é um múltiplo de 8, você deve usar [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible). Essa estrutura simplesmente configura os bytes extras apontados pelo membro **cbSize** de **WAVEFORMATEX** para fornecer informações extras sobre o formato. **WAVEFORMATEXTENSIBLE** pode ser convertido como **WAVEFORMATEX**.

Também há dois formatos de área de transferência que você pode usar para representar dados de áudio: CF \_ Wave e CF \_ riff. Use o formato de onda do CF \_ para representar dados em um dos formatos padrão, como 11 kHz ou 22 kHz PCM. Use o \_ formato RIFF do CF para representar formatos de dados mais complexos que não podem ser representados como arquivos de áudio de forma de onda padrão.

## <a name="writing-waveform-audio-data"></a>Gravando dados de Waveform-Audio

Depois de abrir com êxito um driver de dispositivo de saída de wave-áudio, você pode começar a tocar um som. Windows fornece a função [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) para enviar blocos de dados para dispositivos de saída de wave-áudio.

Use a estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) para especificar o bloco de dados de formato de onda-áudio que você está enviando usando **waveOutWrite**. Essa estrutura contém um ponteiro para um bloco de dados bloqueados, o comprimento do bloco de dados e alguns sinalizadores. Este bloco de dados deve ser preparado antes de você usá-lo; para obter informações sobre como preparar um bloco de dados, consulte [blocos de dados de áudio](audio-data-blocks.md).

Depois de enviar um bloco de dados para um dispositivo de saída usando **waveOutWrite**, você deve aguardar até que o driver de dispositivo seja concluído com o bloco de dados antes de liberá-lo. Se você estiver enviando vários blocos de dados, será necessário monitorar a conclusão dos blocos de dados para saber quando enviar blocos adicionais. Para obter mais informações sobre blocos de dados, consulte [blocos de dados de áudio](audio-data-blocks.md).

## <a name="pcm-waveform-audio-data-format"></a>Formato de dados de Waveform-Audio PCM

O membro **lpData** da estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) pointsetts para os exemplos de dados de formato de onda-áudio. Para dados PCM de 8 bits, cada amostra é representada por um único byte de dados não assinado. Para dados PCM de 16 bits, cada amostra é representada por um valor assinado de 16 bits. A tabela a seguir resume os valores máximo, mínimo e intermediário para dados PCM de Wave de onda-áudio.



| Formato de dados | Valor máximo   | Valor mínimo    | Valor de ponto médio |
|-------------|-----------------|------------------|----------------|
| PCM de 8 bits   | 255 (0xFF)      | 0                | 128 (0x80)     |
| PCM de 16 bits  | 32.767 (0x7FFF) | – 32.768 (0x8000) | 0              |



 

## <a name="pcm-data-packing"></a>Empacotamento de dados PCM

A ordem dos bytes de dados varia entre os formatos de 8 e 16 bits e entre os formatos mono e estéreo. A lista a seguir descreve a compactação de dados para os diferentes formatos de dados PCM Wave-Audio.



| PCM Wave-formato de áudio | Descrição                                                                                                                                                                                                                                                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mono de 8 bits                | Cada exemplo é 1 byte que corresponde a um único canal de áudio. A amostra 1 é seguida pelas amostras 2, 3, 4 e assim por diante.                                                                                                                                                                                                                           |
| estéreo de 8 bits              | Cada exemplo é 2 bytes. A amostra 1 é seguida pelas amostras 2, 3, 4 e assim por diante. Para cada exemplo, o primeiro byte é o canal 0 (o canal esquerdo) e o segundo byte é o canal 1 (o canal correto).                                                                                                                                               |
| mono de 16 bits               | Cada exemplo é 2 bytes. A amostra 1 é seguida pelas amostras 2, 3, 4 e assim por diante. Para cada exemplo, o primeiro byte é o byte de ordem inferior do canal 0 e o segundo byte é o byte de ordem superior do canal 0.                                                                                                                                         |
| estéreo de 16 bits             | Cada exemplo é 4 bytes. A amostra 1 é seguida pelas amostras 2, 3, 4 e assim por diante. Para cada exemplo, o primeiro byte é o byte de ordem inferior do canal 0 (canal esquerdo); o segundo byte é o byte de ordem superior do canal 0; o terceiro byte é o byte de ordem inferior do canal 1 (canal direito); e o quarto byte é o byte de ordem superior do canal 1. |
| Outras pessoas                    | Cada exemplo está contido em um bloco que é um múltiplo de 4 bytes, mas os exemplos podem ser não alinhados em byte. A organização dos canais é especificada por uma máscara. Para obter mais informações, consulte [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible).                                                                                                 |



 

## <a name="closing-waveform-audio-output-devices"></a>Fechando Waveform-Audio dispositivos de saída

Após a execução de Wave-a reprodução de áudio é concluída, chame [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) para fechar o dispositivo de saída. Se **waveOutClose** for chamado enquanto um arquivo de wave-áudio estiver sendo reproduzido, a operação de fechamento falhará e a função retornará um código de erro indicando que o dispositivo não foi fechado. Se você não quiser aguardar a reprodução terminar antes de fechar o dispositivo, chame a função [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) antes de fechar. Isso termina a reprodução e permite que o dispositivo seja fechado. Certifique-se de usar a função [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) para limpar a preparação em todos os blocos de dados antes de fechar o dispositivo.

 

 