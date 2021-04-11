---
description: Este tópico descreve o conteúdo de vídeo&\# 8211; recursos de proteção que um driver de gráficos pode fornecer.
ms.assetid: 3FDB4908-C75D-4AE0-B32E-93F840E4F30A
title: GPU-Based Proteção de Conteúdo com vídeo D3D11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78097492d375d50688f2472f5d2de99cc21f8594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010306"
---
# <a name="gpu-based-content-protection-with-d3d11-video"></a>GPU-Based Proteção de Conteúdo com vídeo D3D11

Este tópico descreve o conteúdo de vídeo – recursos de proteção que um driver de gráficos pode fornecer.

-   [Introdução](#introduction)
-   [Visão geral do processo de decodificação](#overview-of-the-decoding-process)
-   [Criptografando buffers de vídeo compactados para o decodificador](#encrypting-compressed-video-buffers-for-the-decoder)
    -   [1. consulte os recursos de Proteção de Conteúdo do driver](#1-query-the-content-protection-capabilities-of-the-driver)
    -   [2. configurar o canal autenticado](#2-configure-the-authenticated-channel)
    -   [3. configurar a sessão de criptografia](#3-configure-the-cryptographic-session)
    -   [4. associar o decodificador à sessão de criptografia](#4-associate-the-decoder-with-the-cryptographic-session)
-   [Enviando comandos de canal autenticado](#sending-authenticated-channel-commands)
-   [Enviando consultas de canal autenticado](#sending-authenticated-channel-queries)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

O diagrama a seguir mostra uma exibição simplificada de como o conteúdo de vídeo protegido passa pelo pipeline para ser renderizado.

![um diagrama que mostra o conteúdo de vídeo protegido.](images/d3d9video01.png)

> [!Note]
>
> O [caminho de mídia protegido](protected-media-path.md) (PMP) não está descrito neste diagrama. O fluxo de dados mostrado aqui pode ocorrer em um processo de PMP ou em um processo de aplicativo.

 

O decodificador recebe dados de vídeo criptografados e compactados de uma fonte externa. Presume-se também que o decodificador também receba uma chave de criptografia para descriptografar esses dados. Este tópico não descreve a troca de chaves entre a fonte de vídeo e o decodificador, mas a PMP define um mecanismo possível. A GPU não está envolvida neste estágio.

Para a decodificação acelerada por hardware, o decodificador de software passa o conteúdo de vídeo compactado para a GPU. Para proteger esse conteúdo, o decodificador criptografa novamente os dados, normalmente usando AES-CTR, antes de passá-los para o acelerador de hardware. Um mecanismo de troca de chaves é definido entre o decodificador e o driver de gráficos.

Os quadros de vídeo decodificados são armazenados na memória de vídeo, geralmente em claro. Neste ponto, os quadros são processados e, em seguida, apresentados. Há duas opções principais para apresentação.

-   Ao usar a API D3D9, os quadros podem ser apresentados usando uma sobreposição de hardware. Hardware sem suporte no D3D11. Para obter mais informações, consulte [suporte à sobreposição de hardware](hardware-overlay-support.md).
-   Os quadros podem ser apresentados pelo DWM (gerenciamento de janelas da área de trabalho) usando uma superfície compartilhada.

A última etapa é exibir o quadro no monitor, o que pode exigir proteção de link entre a placa gráfica e o dispositivo de vídeo. Um exemplo de proteção de link é High-Bandwidth Proteção de Conteúdo Digital (HDCP). A proteção de link é configurada usando o [Gerenciador de proteção de saída](output-protection-manager.md) (OPM). Este tópico não descreve OPM; para obter mais informações, consulte [usando o Gerenciador de proteção de saída](using-output-protection-manager.md).

## <a name="overview-of-the-decoding-process"></a>Visão geral do processo de decodificação

Durante a decodificação acelerada por hardware, o decodificador de software deve passar dados de vídeo compactados para a placa gráfica. Para conteúdo premium, esses dados normalmente devem ser criptografados, usando criptografia de chave simétrica, antes de serem enviados para a GPU.

Para criptografar o vídeo para decodificação, o decodificador de software usa as seguintes interfaces:

-   [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder). Representa o dispositivo decodificador, também chamado de acelerador.
-   [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession). Representa uma sessão criptográfica, que fornece a chave de criptografia.
-   [**ID3D11AuthenticatedChannel**](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel). Representa um canal autenticado, que permite que o decodificador de software associe a sessão criptográfica ao decodificador.

![um diagrama que mostra as interfaces de decodificação de Direct3D9.](images/d3d9video02.png)

Todas essas interfaces são obtidas do dispositivo Direct3D11, da seguinte maneira:



| Interface                                                        | Criação                                                                                                                                                |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder)                 | Chame [**ID3D11VideoDevice:: CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview). O tipo de decodificador é identificado por um GUID de perfil. |
| [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession)               | Chame [**ID3D11VideoDevice:: CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession).                                                           |
| [**ID3D11AuthenticatedChannel**](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel) | Chame [**ID3D11VideoDevice:: CreateAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel).                                             |



 

> [!Note]  
> Para obter um ponteiro para a interface [**ID3D11VideoDevice**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice) , chame [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) na interface [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) .

 

O canal autenticado fornece um canal de comunicação confiável entre o decodificador de software e o driver. O canal de comunicação funciona da seguinte maneira:

-   O driver fornece uma cadeia de certificados X. 509 cujo certificado raiz é assinado pela Microsoft.
-   O certificado contém uma chave pública RSA para o driver.
-   O decodificador de software usa a chave pública para enviar o driver a uma chave de sessão AES de 128 bits.
-   O decodificador de software envia consultas e comandos para o canal autenticado.
-   A chave de sessão é usada para computar MACs (códigos de autenticação de mensagem) para as consultas e comandos. O driver usa os MACs para verificar a integridade dos dados de consulta/comando, e o decodificador de software os usa para verificar a integridade dos dados de resposta do driver.

## <a name="encrypting-compressed-video-buffers-for-the-decoder"></a>Criptografando buffers de vídeo compactados para o decodificador

Aqui está uma visão geral de alto nível do processo de criptografia e decodificação:

1.  O decodificador de software recebe um fluxo de dados criptografados da fonte de vídeo. O decodificador descriptografa esse fluxo.
2.  O decodificador de software negocia uma chave de sessão com a sessão criptográfica.
3.  O decodificador de software usa o canal autenticado para associar a sessão criptográfica ao dispositivo decodificador.
4.  O decodificador de software coloca dados compactados em buffers que obtém do dispositivo decodificador (acelerador). Para conteúdo protegido, o codificador de software criptografa os dados que são colocados nos buffers, usando a chave de sessão para a criptografia.
    > [!Note]  
    > Alguns drivers usam uma chave de conteúdo, em vez da chave de sessão, para criptografia. A chave de conteúdo pode mudar de um quadro para o outro.

     

5.  O decodificador envia os buffers compactados criptografados para o acelerador. Para AES-CTR, o decodificador também passa o vetor de inicialização. Se uma chave de conteúdo for usada, o decodificador passará a chave de conteúdo, criptografada usando a chave de sessão.

O Direct3D11 tem suporte padrão para o AES-CTR de 128 bits, mas foi projetado para estender para tipos de criptografia adicionais.

As próximas cinco seções fornecem etapas mais detalhadas.

-   [1. consulte os recursos de Proteção de Conteúdo do driver](#1-query-the-content-protection-capabilities-of-the-driver)
-   [2. configurar o canal autenticado](#2-configure-the-authenticated-channel)
-   [3. configurar a sessão de criptografia](#3-configure-the-cryptographic-session)
-   [4. associar o decodificador à sessão de criptografia](#4-associate-the-decoder-with-the-cryptographic-session)

### <a name="1-query-the-content-protection-capabilities-of-the-driver"></a>1. consulte os recursos de Proteção de Conteúdo do driver

Antes de tentar aplicar a criptografia, obtenha os recursos de proteção de conteúdo do driver.

1.  Obtenha um ponteiro para a interface ID3D11Device.
2.  Chame [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para a interface [**ID3D11VideoDevice**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice) .
3.  Chame [**ID3D11VideoDevice:: GetContentProtectionCaps**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getcontentprotectioncaps). Esse método preenche uma estrutura de [**D3D11_VIDEO_CONTENT_PROTECTION_CAPS**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_content_protection_caps) com os recursos de proteção de conteúdo do driver.

Em particular, procure os seguintes recursos:

-   Se o membro **Caps** contiver o sinalizador **D3D11_CONTENT_PROTECTION_CAPS_SOFTWARE** ou **D3D11_CONTENT_PROTECTION_CAPS_HARDWARE** , o driver poderá executar a criptografia.
-   Se o membro **Caps** contiver o sinalizador **D3D11_CONTENT_PROTECTION_CAPS_CONTENT_KEY** , o driver usará uma chave de conteúdo separada para descriptografia.
-   Chame [**ID3D11VideoDevice:: CheckCryptoKeyExchange**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-checkcryptokeyexchange) para determinar os tipos de trocas de chave que o driver suporta para gerar a chave de sessão.

Recursos adicionais são indicados no membro **Caps** .

### <a name="2-configure-the-authenticated-channel"></a>2. configurar o canal autenticado

A próxima etapa é configurar o canal autenticado.

1.  Chame [**ID3D11VideoDevice:: CreateAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel) para criar o canal autenticado. Para o parâmetro *channelType* , especifique um tipo de canal que corresponda aos recursos do driver.
    -   O tipo de canal **D3D11_AUTHENTICATED_CHANNEL_DRIVER_SOFTWARE** corresponde a **D3D11_CONTENT_PROTECTION_CAPS_SOFTWARE**.
    -   O tipo de canal **D3D11_AUTHENTICATED_CHANNEL_DRIVER_HARDWARE** corresponde a **D3D11_CONTENT_PROTECTION_CAPS_HARDWARE**.

    O método **CreateAuthenticatedChannel** retorna um ponteiro para a interface [**ID3D11AuthenticatedChannel**](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel) .
2.  Chame [**ID3D11AuthenticatedChannel:: Getcertificates**](/windows/desktop/api/d3d11/nf-d3d11-id3d11authenticatedchannel-getcertificatesize) para obter o tamanho do certificado X. 509 do driver. Aloque um buffer do tamanho necessário.
3.  Chame [**ID3D11AuthenticatedChannel:: Getcertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11authenticatedchannel-getcertificate) para obter o certificado. O método copia o certificado no buffer que foi alocado na etapa anterior.
4.  Verifique se o certificado do driver foi assinado pela Microsoft e não foi revogado.
5.  Obtenha a chave pública do certificado.
6.  Gere uma chave de sessão de RSA aleatória. Essa chave de sessão é usada para assinar dados que são enviados para o canal autenticado. Criptografe a chave de sessão usando a chave pública do driver.
7.  Chame [**ID3D11VideoContext:: NegotiateAuthenticatedChannelKeyExchange**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-negotiateauthenticatedchannelkeyexchange) para enviar a chave de sessão criptografada para o driver.
8.  Inicialize o canal seguro da seguinte maneira:
    1.  Preencha uma estrutura de [**D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input) , conforme descrito na documentação.
    2.  Envie o comando [**D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input) chamando [**ID3D11VideoContext:: ConfigureAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel) conforme descrito na seção [enviando comandos de canal autenticados](#sending-authenticated-channel-commands). Esse comando contém os números de sequência iniciais para os comandos e consultas que são enviados para o canal autenticado.
9.  Verifique o tipo de canal enviando uma consulta [**D3D11_AUTHENTICATED_QUERY_CHANNEL_TYPE**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_channel_type_output) para o canal autenticado, conforme descrito na seção [enviando consultas de canal autenticado](#sending-authenticated-channel-queries). Verifique se o tipo de canal corresponde ao que você especificou no método [**CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) .

### <a name="3-configure-the-cryptographic-session"></a>3. configurar a sessão de criptografia

Em seguida, configure a sessão de criptografia e estabeleça a chave de sessão.

1.  Chame [**ID3D11VideoDevice:: CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) para criar a sessão criptográfica. Esse método retorna um ponteiro para a interface [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) .
2.  Chame [**ID3D11CryptoSession:: Getcertificates**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize) para obter o tamanho do certificado X. 509 do driver. Aloque um buffer do tamanho necessário.
3.  Chame [**ID3D11CryptoSession:: Getcertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate) para obter o certificado. O método copia o certificado no buffer que foi alocado na etapa anterior.
4.  Verifique se o certificado do driver foi assinado pela Microsoft e não foi revogado.
5.  Obtenha a chave pública do certificado.
6.  Gere uma chave de sessão de RSA aleatória. Essa é uma chave de sessão separada da chave de sessão de canal autenticado. Criptografe a chave de sessão usando a chave pública do driver.
7.  Chame [**ID3D11VideoContext:: NegotiateCryptoSessionKeyExchange**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-negotiatecryptosessionkeyexchange) para enviar a chave de sessão criptografada para o driver.
8.  Se os recursos de proteção de conteúdo incluírem **3D11_CONTENT_PROTECTION_CAPS_CONTENT_KEY**, crie uma chave de conteúdo de RSA aleatória. Isso será usado posteriormente no processo de decodificação.

### <a name="4-associate-the-decoder-with-the-cryptographic-session"></a>4. associar o decodificador à sessão de criptografia

Em seguida, associe o dispositivo decodificador ao dispositivo Direct3D11 e a sessão criptográfica, da seguinte maneira:

1.  Obtenha um identificador para o dispositivo Direct3D11, enviando uma consulta de [**D3D11_AUTHENTICATED_QUERY_DEVICE_HANDLE**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_device_handle_output) para o canal autenticado.
2.  Preencha uma estrutura de [**D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_crypto_session_input) com as seguintes informações:
    -   Defina o membro **DecodeHandle** para o identificador retornado de [**ID3D11VideoDecoder:: GetDriverHandle**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodecoder-getdriverhandle).
    -   Defina o membro **CryptoSessionHandle** para o identificador retornado de [**ID3D11CryptoSession:: GetCryptoSessionHandle**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcryptosessionhandle).
    -   Defina o membro **DeviceHandle** para o identificador do dispositivo Direct3D11.
3.  Chame [**ID3D11VideoContext:: ConfigureAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel) para enviar um comando [**D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_crypto_session_input) para o canal autenticado.

O diagrama a seguir ilustra a troca de identificadores:

![um diagrama que mostra como o decodificador DXVA está associado à sessão criptográfica.](images/d3d9video03.png)

O decodificador de software agora pode usar a chave de sessão de criptografia para criptografar os buffers de vídeo compactados. Cada buffer compactado terá seu próprio vetor de inicialização (IV) especificado no membro **pIV** da estrutura de [**D3D11_VIDEO_DECODER_BUFFER_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_buffer_desc) .

## <a name="sending-authenticated-channel-commands"></a>Enviando comandos de canal autenticado

Um conjunto de comandos é definido para configurar o canal autenticado e definir várias proteções de conteúdo. Para obter uma lista de comandos, consulte [proteção de conteúdo comandos](content-protection-commands.md).

Para enviar um comando para o canal autenticado, execute as etapas a seguir.

1.  Preencha a estrutura de dados de entrada. Essa estrutura de dados é sempre uma estrutura de [**D3D11_AUTHENTICATED_CONFIGURE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_input) seguida por campos adicionais. Preencha a estrutura de **D3D11_AUTHENTICATED_CONFIGURE_INPUT** , conforme mostrado na tabela a seguir.

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Membro</th>
    <th>DESCRIÇÃO</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><strong>omac</strong></td>
    <td>Ignore este campo por enquanto.</td>
    </tr>
    <tr class="even">
    <td><strong>Configuratype</strong></td>
    <td>GUID que identifica o comando. Para obter uma lista de comandos, consulte <a href="content-protection-commands.md">proteção de conteúdo comandos</a>.</td>
    </tr>
    <tr class="odd">
    <td><strong>hChannel</strong></td>
    <td>O identificador para o canal autenticado.</td>
    </tr>
    <tr class="even">
    <td><strong>SequenceNumber</strong></td>
    <td>O número de sequência. O primeiro número de sequência é especificado com o envio de um comando <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input"><strong>D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE</strong></a> . Cada vez que você enviar outro comando, aumente esse número em 1. O número de sequência protege contra ataques de repetição.
    <blockquote>
    [!Note]<br />
Dois números de sequência separados são usados, um para comandos e outro para consultas.
    </blockquote>
    <br/> <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Calcule a marca OMAC para o bloco de dados que aparece após o membro **OMAC** da estrutura de entrada. Em seguida, copie esse valor de marca para o membro **OMAC** .
3.  Chame [**ID3D11VideoContext:: ConfigureAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel).
4.  O driver coloca a saída do comando na estrutura de [**D3D11_AUTHENTICATED_CONFIGURE_OUTPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_output) .
5.  Calcule a marca OMAC para o bloco de dados que aparece após o membro **OMAC** da estrutura de saída. Compare isso com o valor do membro **OMAC** . Falha se eles não corresponderem.
6.  Compare os valores dos membros **configuratype**, **hChannel** e **SequenceNumber** na estrutura de saída com seus valores para esses membros. Falha se eles não corresponderem.
7.  Incrementar o número de sequência para o próximo comando.

## <a name="sending-authenticated-channel-queries"></a>Enviando consultas de canal autenticado

Um conjunto de consultas é definido para recuperar informações sobre o canal autenticado. Para obter uma lista de consultas, consulte [proteção de conteúdo consultas](content-protection-queries.md).

Para enviar um comando para o canal autenticado, execute as etapas a seguir.

1.  Preencha a estrutura de dados de entrada. Essa estrutura de dados é sempre uma estrutura de [**D3D11_AUTHENTICATED_QUERY_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_input) , possivelmente seguida por campos adicionais. Preencha a estrutura de **D3D11_AUTHENTICATED_QUERY_INPUT** , conforme mostrado na tabela a seguir.

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Membro</th>
    <th>DESCRIÇÃO</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><strong>QueryType</strong></td>
    <td>GUID que identifica a consulta. Para obter uma lista de consultas, consulte <a href="content-protection-queries.md">proteção de conteúdo consultas</a>.</td>
    </tr>
    <tr class="even">
    <td><strong>hChannel</strong></td>
    <td>O identificador para o canal autenticado.</td>
    </tr>
    <tr class="odd">
    <td><strong>SequenceNumber</strong></td>
    <td>O número de sequência. O primeiro número de sequência é especificado com o envio de um comando <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input"><strong>D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE</strong></a> . Cada vez que você enviar outra consulta, aumente esse número em 1. O número de sequência protege contra ataques de repetição.
    <blockquote>
    [!Note]<br />
Dois números de sequência separados são usados, um para comandos e outro para consultas.
    </blockquote>
    <br/> <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Chame [**ID3D11VideoContext:: QueryAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-queryauthenticatedchannel).
3.  O driver coloca a saída da consulta em uma estrutura de [**D3D11_AUTHENTICATED_QUERY_OUTPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_output) . Essa estrutura é seguida por campos adicionais, dependendo do tipo de consulta.
4.  Calcule a marca OMAC para o bloco de dados que aparece após o membro **OMAC** da estrutura de saída. Compare isso com o valor do membro **OMAC** . Falha se eles não corresponderem.
5.  Compare os valores dos membros **configuratype**, **hChannel** e **SequenceNumber** na estrutura de saída com seus valores para esses membros. Falha se eles não corresponderem.
6.  Incrementar o número de sequência para a próxima consulta.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[APIs de vídeo do Direct3D 11](direct3d-11-video-apis.md)
</dt> </dl>

 

 
