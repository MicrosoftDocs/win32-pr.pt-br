---
title: Dispositivos e tipos de dados
description: Dispositivos e tipos de dados
ms.assetid: 46247983-19c3-4c7a-a615-ba6cd8bd3289
keywords:
- áudio de formato de onda, abertura de dispositivos de saída
- Wave-interface de áudio, abrindo dispositivos de saída
- abrindo Wave-dispositivos de saída de áudio
- áudio de onda, consultando dispositivos de saída
- Wave-interface de áudio, consultando dispositivos de saída
- consultando dispositivos de saída de wave-áudio
- áudio de onda, identificadores de dispositivo
- Wave-interface de áudio, identificadores de dispositivo
- áudio de onda, identificadores de dispositivo
- Wave-interface de áudio, identificadores de dispositivo
- áudio de onda, tipos de dados de saída
- Wave-interface de áudio, tipos de dados de saída
- áudio de forma de onda, formatos de dados
- forma de onda-interface de áudio, formatos de dados
- gravando formato de onda-dados de áudio
- áudio de onda, gravação de dados
- Wave-interface de áudio, gravando dados
- PCM Wave-dados de áudio
- áudio de onda, dados de PCM
- formato de onda-interface de áudio, dados do PCM
- áudio de onda, fechando dispositivos de saída
- Wave-interface de áudio, fechando dispositivos de saída
- fechando a onda-dispositivos de saída de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29561a74695fb8bde950e2e75a430803a1a0351b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105751418"
---
# <a name="devices-and-data-types"></a>Dispositivos e tipos de dados

Esta seção descreve como trabalhar com dispositivos Wave-audio e inclui informações sobre como abri-los, fechá-los e consultá-los para seus recursos. Ele também descreve como controlar os dispositivos em um sistema usando identificadores de dispositivo e de dispositivo.

## <a name="opening-waveform-audio-output-devices"></a>Abrindo Waveform-Audio dispositivos de saída

Use a função [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) para abrir um dispositivo de saída de wave-áudio para reprodução. Essa função abre o dispositivo associado ao identificador de dispositivo especificado e retorna um identificador do dispositivo aberto gravando o identificador de um local de memória especificado.

Alguns computadores de multimídia têm vários dispositivos de saída de wave-áudio. A menos que você queira abrir um dispositivo de saída de áudio de onda específico em um sistema, use o \_ sinalizador do mapeador de ondas para o identificador do dispositivo ao abrir um dispositivo. A função **waveOutOpen** escolhe o dispositivo no sistema que é mais capaz de reproduzir o formato de dados especificado.

## <a name="querying-audio-devices"></a>Consultando dispositivos de áudio

O Windows fornece as seguintes funções para determinar quantos dispositivos de um determinado tipo estão disponíveis em um sistema.



| Função                                       | Descrição                                                                  |
|------------------------------------------------|------------------------------------------------------------------------------|
| [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)         | Recupera o número de dispositivos de saída auxiliar presentes no sistema.      |
| [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)   | Recupera o número de dispositivos de entrada de wave-áudio presentes no sistema.  |
| [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs) | Recupera o número de dispositivos de saída de wave-áudio presentes no sistema. |



 

Os dispositivos de áudio são identificados por um identificador de dispositivo. O identificador do dispositivo é determinado implicitamente do número de dispositivos presentes em um sistema. Identificadores de dispositivo variam de zero a um menor que o número de dispositivos presentes. Por exemplo, se houver dois dispositivos de saída de wave-áudio em um sistema, os identificadores de dispositivo válidos serão 0 e 1.

Depois de determinar quantos dispositivos de um determinado tipo estão presentes em um sistema, você pode usar uma das funções a seguir para consultar os recursos de cada dispositivo.



| Função                                       | Descrição                                                             |
|------------------------------------------------|-------------------------------------------------------------------------|
| [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)         | Recupera os recursos de um dispositivo de saída auxiliar especificado.      |
| [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)   | Recupera os recursos de um dispositivo de entrada Wave-Audio especificado.  |
| [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) | Recupera os recursos de um dispositivo de saída de wave-áudio especificado. |



 

Cada uma dessas funções preenche uma estrutura com informações sobre os recursos de um dispositivo especificado. A tabela a seguir lista as estruturas que correspondem a cada uma dessas funções.



|                                                |                                    |
|------------------------------------------------|------------------------------------|
| Função                                       | Estrutura                          |
| [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)         | [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)         |
| [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)   | [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)   |
| [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) | [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) |



 

Os formatos padrão são listados no membro **dwFormats** da estrutura **WAVEOUTCAPS** . Forma de onda-os dispositivos de áudio podem dar suporte a formatos não padrão. Para determinar se um determinado formato (padrão ou não padrão) é suportado por um dispositivo, você pode chamar a função [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) com o \_ sinalizador de consulta de formato Wave \_ . Esse sinalizador não abre o dispositivo. Você especifica o formato em questão na estrutura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) apontada pelo parâmetro *pwfx* passado para **waveOutOpen**.

Wave-os dispositivos de saída de áudio variam nos recursos aos quais dão suporte. O membro **dwSupport** da estrutura [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) indica se um dispositivo dá suporte a tais recursos como alterações de volume e de timbre.

## <a name="device-handles-and-device-identifiers"></a>Manipuladores de dispositivo e identificadores de dispositivo

Cada função que abre um dispositivo de áudio especifica um identificador de dispositivo, um ponteiro para um local de memória e alguns parâmetros que são exclusivos para cada tipo de dispositivo. O local da memória é preenchido com um identificador de dispositivo. Use este identificador de dispositivo para identificar o dispositivo de áudio aberto ao chamar outras funções de áudio.

A diferença entre identificadores e manipuladores para dispositivos de áudio é sutil, mas importante:

-   Os identificadores de dispositivo são determinados implicitamente do número de dispositivos presentes em um sistema. Esse número é obtido usando a função [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs), [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)ou [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs) .
-   Os identificadores de dispositivo são retornados quando os drivers de dispositivo são abertos usando a função [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) ou [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .

Não há funções que abram ou fechem dispositivos de áudio auxiliares. Os dispositivos de áudio auxiliares não precisam ser abertos e fechados como dispositivos de som de onda, pois não há nenhuma transferência de dados contínua associada a eles. Todas as funções de áudio auxiliares usam identificadores de dispositivo para identificar dispositivos.

## <a name="waveform-audio-output-data-types"></a>Waveform-Audio tipos de dados de saída

Os tipos de dados a seguir são definidos para as funções de saída de wave-áudio.



| Tipo                                 | Descrição                                                                                                                                                   |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HWAVEOUT**                         | Identificador para um dispositivo de saída de wave-áudio aberto.                                                                                                               |
| [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | Estrutura que especifica os formatos de dados com suporte por um dispositivo de entrada de wave-áudio específico. Essa estrutura também é usedfor dispositivos de entrada de wave-áudio. |
| [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | Estrutura usada como um cabeçalho para um bloco de dados de entrada de forma de onda-áudio. Essa estrutura também é usada para dispositivos de entrada de wave-áudio.                            |
| [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)   | Estrutura usada para consultar os recursos de um dispositivo de saída de áudio de onda específico.                                                                        |



 

## <a name="specifying-waveform-audio-data-formats"></a>Especificando Waveform-Audio formatos de dados

Quando você chama a função [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) para abrir um driver de dispositivo para reprodução ou para consultar se o driver dá suporte a um formato de dados específico, use o parâmetro *pwfx* para especificar um ponteiro para uma estrutura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) que contém o formato de dados Wave-Audio solicitado. **WAVEFORMATEX** substitui as estruturas [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) e [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) .

Para dados de áudio separados em mais de dois canais ou tem um tamanho de amostra que não é um múltiplo de 8, você deve usar [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible). Essa estrutura simplesmente configura os bytes extras apontados pelo membro **cbSize** de **WAVEFORMATEX** para fornecer informações extras sobre o formato. **WAVEFORMATEXTENSIBLE** pode ser convertido como **WAVEFORMATEX**.

Também há dois formatos de área de transferência que você pode usar para representar dados de áudio: CF \_ Wave e CF \_ riff. Use o formato de onda do CF \_ para representar dados em um dos formatos padrão, como 11 kHz ou 22 kHz PCM. Use o \_ formato RIFF do CF para representar formatos de dados mais complexos que não podem ser representados como arquivos de áudio de forma de onda padrão.

## <a name="writing-waveform-audio-data"></a>Gravando dados de Waveform-Audio

Depois de abrir com êxito um driver de dispositivo de saída de wave-áudio, você pode começar a tocar um som. O Windows fornece a função [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) para enviar blocos de dados para dispositivos de saída de wave-áudio.

Use a estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) para especificar o bloco de dados de formato de onda-áudio que você está enviando usando **waveOutWrite**. Essa estrutura contém um ponteiro para um bloco de dados bloqueados, o comprimento do bloco de dados e alguns sinalizadores. Este bloco de dados deve ser preparado antes de você usá-lo; para obter informações sobre como preparar um bloco de dados, consulte [blocos de dados de áudio](audio-data-blocks.md).

Depois de enviar um bloco de dados para um dispositivo de saída usando **waveOutWrite**, você deve aguardar até que o driver de dispositivo seja concluído com o bloco de dados antes de liberá-lo. Se você estiver enviando vários blocos de dados, será necessário monitorar a conclusão dos blocos de dados para saber quando enviar blocos adicionais. Para obter mais informações sobre blocos de dados, consulte [blocos de dados de áudio](audio-data-blocks.md).

## <a name="pcm-waveform-audio-data-format"></a>Formato de dados de Waveform-Audio PCM

O membro **lpData** da estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) pointsetts para os exemplos de dados de formato de onda-áudio. Para dados PCM de 8 bits, cada amostra é representada por um único byte de dados não assinado. Para dados PCM de 16 bits, cada amostra é representada por um valor assinado de 16 bits. A tabela a seguir resume os valores máximo, mínimo e intermediário para dados PCM de Wave de onda-áudio.



|             |                 |                  |                |
|-------------|-----------------|------------------|----------------|
| Formato de dados | Valor máximo   | Valor mínimo    | Valor de ponto médio |
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

 

 