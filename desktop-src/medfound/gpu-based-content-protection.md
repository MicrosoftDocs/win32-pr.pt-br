---
description: Descreve o conteúdo de vídeo&\# 8211; recursos de proteção que um driver de gráficos pode fornecer.
ms.assetid: FD0625BB-484A-43E6-8931-DB635D4F017F
title: GPU-Based Proteção de Conteúdo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbc1a0f88cae199b9aab38e5ec429ea5427f44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568237"
---
# <a name="gpu-based-content-protection"></a>GPU-Based Proteção de Conteúdo

Este tópico descreve o conteúdo de vídeo – recursos de proteção que um driver de gráficos pode fornecer.

-   [Introdução](#introduction)
-   [Visão geral do processo de decodificação](#overview-of-the-decoding-process)
-   [Criptografando buffers de vídeo compactados para o decodificador](#encrypting-compressed-video-buffers-for-the-decoder)
    -   [1. consulte os recursos de Proteção de Conteúdo do driver](#1-query-the-content-protection-capabilities-of-the-driver)
    -   [2. configurar o canal autenticado](#2-configure-the-authenticated-channel)
    -   [3. configurar a sessão de criptografia](#3-configure-the-cryptographic-session)
    -   [4. obter um identificador para o dispositivo de decodificador de DXVA](#4-get-a-handle-to-the-dxva-decoder-device)
    -   [5. associar o decodificador de DXVA à sessão criptográfica](#5-associate-the-dxva-decoder-with-the-cryptographic-session)
-   [Enviando comandos de canal autenticado](#sending-authenticated-channel-commands)
-   [Enviando consultas de canal autenticado](#sending-authenticated-channel-queries)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

O diagrama a seguir mostra uma exibição simplificada de como o conteúdo de vídeo protegido passa pelo pipeline para ser renderizado.

![um diagrama que mostra o conteúdo de vídeo protegido.](images/d3d9video01.png)

> [!Note]  
> O [caminho de mídia protegido](protected-media-path.md) (PMP) não está descrito neste diagrama. O fluxo de dados mostrado aqui pode ocorrer em um processo de PMP ou em um processo de aplicativo.

 

O decodificador recebe dados de vídeo criptografados e compactados de uma fonte externa. Presume-se também que o decodificador também receba uma chave de criptografia para descriptografar esses dados. Este tópico não descreve a troca de chaves entre a fonte de vídeo e o decodificador, mas a PMP define um mecanismo possível. A GPU não está envolvida neste estágio.

Para a decodificação acelerada por hardware, o decodificador de software passa o conteúdo de vídeo compactado para a GPU. Para proteger esse conteúdo, o decodificador criptografa novamente os dados, normalmente usando AES-CTR, antes de passá-los para o acelerador de hardware. Um mecanismo de troca de chaves é definido entre o decodificador e o driver de gráficos.

Os quadros de vídeo decodificados são armazenados na memória de vídeo, geralmente em claro. Neste ponto, os quadros são processados e, em seguida, apresentados. Há duas opções principais para apresentação.

-   Quadros podem ser apresentados usando uma sobreposição de hardware. Para obter mais informações, consulte [suporte à sobreposição de hardware](hardware-overlay-support.md).
-   Os quadros podem ser apresentados pelo DWM (gerenciamento de janelas da área de trabalho) usando uma superfície compartilhada.

A última etapa é exibir o quadro no monitor, o que pode exigir proteção de link entre a placa gráfica e o dispositivo de vídeo. Um exemplo de proteção de link é High-Bandwidth Proteção de Conteúdo Digital (HDCP). A proteção de link é configurada usando o [Gerenciador de proteção de saída](output-protection-manager.md) (OPM). Este tópico não descreve OPM; para obter mais informações, consulte [usando o Gerenciador de proteção de saída](using-output-protection-manager.md).

## <a name="overview-of-the-decoding-process"></a>Visão geral do processo de decodificação

Durante a decodificação acelerada por hardware, o decodificador de software deve passar dados de vídeo compactados para a placa gráfica. Para conteúdo premium, esses dados normalmente devem ser criptografados, usando criptografia de chave simétrica, antes de serem enviados para a GPU.

Para criptografar o vídeo para decodificação, o decodificador de software usa as seguintes interfaces:

-   [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder). Representa o dispositivo de decodificador DXVA, também chamado de acelerador.
-   [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9). Representa uma sessão criptográfica, que fornece a chave de criptografia.
-   [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9). Representa um canal autenticado, que permite que o decodificador de software associe a sessão criptográfica ao decodificador DXVA.

![um diagrama que mostra as interfaces de decodificação de Direct3D9.](images/d3d9video02.png)

Todas essas interfaces são obtidas do dispositivo Direct3D, da seguinte maneira:



| Interface                                                                | Criação                                                                                                                                                                      |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder)                     | Chame [**IDirectXVideoDecoderService:: CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder). O dispositivo de decodificador DXVA é identificado por um GUID de perfil de DXVA. |
| [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)               | Chame [**IDirect3DDevice9Video:: CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession).                                                                         |
| [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9) | Chame [**IDirect3DDevice9Video:: CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).                                                           |



 

> [!Note]  
> Para obter um ponteiro para a interface [**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video) , chame [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) em um dispositivo D3D9Ex.

 

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
3.  O decodificador de software usa o canal autenticado para associar a sessão criptográfica ao dispositivo de decodificador DXVA.
4.  O decodificador de software coloca dados compactados em buffers de DXVA que obtém do dispositivo de decodificador de DXVA (acelerador). Para conteúdo protegido, o codificador de software criptografa os dados que são colocados nos buffers de DXVA, usando a chave de sessão para a criptografia.
    > [!Note]  
    > Alguns drivers usam uma chave de conteúdo, em vez da chave de sessão, para criptografia. A chave de conteúdo pode mudar de um quadro para o outro.

     

5.  O decodificador envia os buffers compactados criptografados para o acelerador. Para AES-CTR, o decodificador também passa o vetor de inicialização. Se uma chave de conteúdo for usada, o decodificador passará a chave de conteúdo, criptografada usando a chave de sessão.

O Direct3D tem suporte padrão para o AES-CTR de 128 bits, mas foi projetado para estender para tipos de criptografia adicionais.

As próximas cinco seções fornecem etapas mais detalhadas.

-   [1. consulte os recursos de Proteção de Conteúdo do driver](#1-query-the-content-protection-capabilities-of-the-driver)
-   [2. configurar o canal autenticado](#2-configure-the-authenticated-channel)
-   [3. configurar a sessão de criptografia](#3-configure-the-cryptographic-session)
-   [4. obter um identificador para o dispositivo de decodificador de DXVA](#4-get-a-handle-to-the-dxva-decoder-device)
-   [5. associar o decodificador de DXVA à sessão criptográfica](#5-associate-the-dxva-decoder-with-the-cryptographic-session)

### <a name="1-query-the-content-protection-capabilities-of-the-driver"></a>1. consulte os recursos de Proteção de Conteúdo do driver

Antes de tentar aplicar a criptografia, obtenha os recursos de proteção de conteúdo do driver.

1.  Obtenha um ponteiro para o dispositivo Direct3D 9.
2.  Chame [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para a interface [**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video) .
3.  Chame [**IDirect3DDevice9Video:: GetContentProtectionCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-getcontentprotectioncaps). Esse método preenche uma estrutura [**D3DCONTENTPROTECTIONCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcontentprotectioncaps) com os recursos de proteção de conteúdo do driver.

Em particular, procure os seguintes recursos:

-   Se o membro **Caps** contiver o sinalizador **D3DCPCAPS_SOFTWARE** ou **D3DCPCAPS_HARDWARE** , o driver poderá executar a criptografia.
-   O membro **Keyexchangetype** especifica como executar a troca de chaves para a chave de sessão.
-   Se o membro **Caps** contiver o sinalizador **D3DCPCAPS_CONTENTKEY** , o driver usará uma chave de conteúdo separada para criptografia. Isso é importante quando você gera a chave de sessão.

Recursos adicionais são indicados no membro **Caps** .

### <a name="2-configure-the-authenticated-channel"></a>2. configurar o canal autenticado

A próxima etapa é configurar o canal autenticado.

1.  Chame [**IDirect3DDevice9Video:: CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) para criar o canal autenticado. Para o parâmetro *channelType* , especifique um tipo de canal que corresponda aos recursos do driver.
    -   O tipo de canal **D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE** corresponde a **D3DCPCAPS_SOFTWARE**.
    -   O tipo de canal **D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE** corresponde a **D3DCPCAPS_HARDWARE**.

    O método **CreateAuthenticatedChannel** retorna um ponteiro para a interface [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9) junto com um identificador para o canal. O identificador é usado posteriormente para associar a sessão criptográfica ao canal autenticado.
2.  Chame [**IDirect3DAuthenticatedChannel9:: Getcertificates**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize) para obter o tamanho do certificado X. 509 do driver. Aloque um buffer do tamanho necessário.
3.  Chame [**IDirect3DAuthenticatedChannel9:: Getcertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate) para obter o certificado. O método copia o certificado no buffer que foi alocado na etapa anterior.
4.  Verifique se o certificado do driver foi assinado pela Microsoft e não foi revogado.
5.  Obtenha a chave pública do certificado.
6.  Gere uma chave de sessão de RSA aleatória. Essa chave de sessão é usada para assinar dados que são enviados para o canal autenticado. Criptografe a chave de sessão usando a chave pública do driver.
7.  Chame [**IDirect3DAuthenticatedChannel9:: NegotiateKeyExchange**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-negotiatekeyexchange) para enviar a chave de sessão criptografada para o driver.
8.  Inicialize o canal seguro da seguinte maneira:
    1.  Preencha uma estrutura de [**D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE**](d3dauthenticatedchannel-configureinitialize.md) , conforme descrito na documentação.
    2.  Envie o comando [**D3DAUTHENTICATEDCONFIGURE_INITIALIZE**](d3dauthenticatedconfigure-initialize.md) chamando [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) conforme descrito na seção [enviando comandos de canal autenticados](#sending-authenticated-channel-commands). Esse comando contém os números de sequência iniciais para os comandos e consultas que são enviados para o canal autenticado.
9.  Verifique o tipo de canal enviando uma consulta [**D3DAUTHENTICATEDQUERY_CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) para o canal autenticado, conforme descrito na seção [enviando consultas de canal autenticado](#sending-authenticated-channel-queries). Verifique se o tipo de canal corresponde ao que você especificou no método [**CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) .

### <a name="3-configure-the-cryptographic-session"></a>3. configurar a sessão de criptografia

Em seguida, configure a sessão de criptografia e estabeleça a chave de sessão.

1.  Chame [**IDirect3DDevice9Video:: CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession) para criar a sessão criptográfica. Esse método retorna um ponteiro para a interface [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9) e junto com um identificador para a sessão criptográfica.
2.  Chame [**IDirect3DCryptoSession9:: Getcertificates**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificatesize) para obter o tamanho do certificado X. 509 do driver. Aloque um buffer do tamanho necessário.
3.  Chame [**IDirect3DCryptoSession9:: Getcertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificate) para obter o certificado. O método copia o certificado no buffer que foi alocado na etapa anterior.
4.  Verifique se o certificado do driver foi assinado pela Microsoft e não foi revogado.
5.  Obtenha a chave pública do certificado.
6.  Gere uma chave de sessão de RSA aleatória. Essa é uma chave de sessão separada da chave de sessão de canal autenticado. Criptografe a chave de sessão usando a chave pública do driver.
7.  Chame [**IDirect3DCryptoSession9:: NegotiateKeyExchange**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-negotiatekeyexchange) para enviar a chave de sessão criptografada para o driver.
8.  Se os recursos de proteção de conteúdo incluírem **D3DCPCAPS_CONTENTKEY**, crie uma chave de conteúdo de RSA aleatória. Isso será usado posteriormente no processo de decodificação.

### <a name="4-get-a-handle-to-the-dxva-decoder-device"></a>4. obter um identificador para o dispositivo de decodificador de DXVA

Para a próxima etapa, você precisará de um identificador para o dispositivo de decodificador DXVA. Para obter esse identificador, preencha uma estrutura de DXVA2_DecodeExecuteParams da seguinte maneira:


```C++
HANDLE hDecodeDeviceHandle;

DXVA2_DecodeExecuteParams execParams = {0};
DXVA2_DecodeExtensionData ExtensionExecute = {0};
    
execParams.NumCompBuffers = 0;
execParams.pCompressedBuffers = NULL;
execParams.pExtensionData = &ExtensionExecute;

ExtensionExecute.Function = DXVA2_DECODE_GET_DRIVER_HANDLE;
ExtensionExecute.pPrivateInputData = NULL;
ExtensionExecute.PrivateInputDataSize = 0;
ExtensionExecute.pPrivateOutputData = &hDecodeDeviceHandle;
ExtensionExecute.PrivateOutputDataSize = sizeof(HANDLE);
```



Defina o membro **pExtensionData** da estrutura de [**DXVA2_DecodeExecuteParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeexecuteparams) como o endereço de uma estrutura de [**DXVA2_DecodeExtensionData**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeextensiondata) .

Na estrutura [**DXVA2_DecodeExtensionData**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeextensiondata) , defina o membro da **função** como **DXVA2_DECODE_GET_DRIVER_HANDLE**. Defina **pPrivateOutputData** como o endereço de um buffer que é grande o suficiente para armazenar um valor de **identificador** . (No exemplo anterior, esse buffer é a variável *hDecodeDeviceHandle* ).

Em seguida, chame [**IDirectXVideoDecoder:: execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) e passe o endereço da estrutura de [**DXVA2_DecodeExecuteParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeexecuteparams) . O identificador para o decodificador DXVA é retornado em **pPrivateOutputData**.

### <a name="5-associate-the-dxva-decoder-with-the-cryptographic-session"></a>5. associar o decodificador de DXVA à sessão criptográfica

Em seguida, associe o dispositivo de decodificador DXVA ao dispositivo Direct3D e à sessão criptográfica, da seguinte maneira:

1.  Obtenha um identificador para o dispositivo de decodificador DXVA, conforme descrito na seção anterior.
2.  Obtenha um identificador para o dispositivo Direct3D, enviando uma consulta [**D3DAUTHENTICATEDQUERY_DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) para o canal autenticado.
3.  Preencha uma estrutura de [**D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION**](d3dauthenticatedchannel-configurecryptosession.md) com as seguintes informações:
    -   Defina o membro **DXVA2DecodeHandle** para o identificador para o dispositivo de decodificador DXVA.
    -   Defina o membro **CryptoSessionHandle** para o identificador para a sessão de criptografia. Esse identificador é retornado pelo método [**IDirect3DDevice9Video:: CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession) .
    -   Defina o membro **DeviceHandle** para o identificador do dispositivo Direct3D.
4.  Chame [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) para enviar um comando [**D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) para o canal autenticado.

O diagrama a seguir ilustra a troca de identificadores:

![um diagrama que mostra como o decodificador DXVA está associado à sessão criptográfica.](images/d3d9video03.png)

O decodificador de software agora pode usar a chave de sessão de criptografia para criptografar os buffers de vídeo compactados. Cada buffer compactado terá seu próprio vetor de inicialização (IV) especificado no membro **pvPVPState** da estrutura de [**DXVA2_DecodeBufferDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodebufferdesc) .

## <a name="sending-authenticated-channel-commands"></a>Enviando comandos de canal autenticado

Um conjunto de comandos é definido para configurar o canal autenticado e definir várias proteções de conteúdo. Para obter uma lista de comandos, consulte [proteção de conteúdo comandos](content-protection-commands.md).

Para enviar um comando para o canal autenticado, execute as etapas a seguir.

1.  Preencha a estrutura de dados de entrada. Essa estrutura de dados é sempre uma estrutura de [**D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT**](d3dauthenticatedchannel-configure-input.md) seguida por campos adicionais. Preencha a estrutura de **D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT** , conforme mostrado na tabela a seguir.

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
    <td>O número de sequência. O primeiro número de sequência é especificado com o envio de um comando <a href="d3dauthenticatedconfigure-initialize.md"><strong>D3DAUTHENTICATEDCONFIGURE_INITIALIZE</strong></a> . Cada vez que você enviar outro comando, aumente esse número em 1. O número de sequência protege contra ataques de repetição.
    <blockquote>
    [!Note]<br />
Dois números de sequência separados são usados, um para comandos e outro para consultas.
    </blockquote>
    <br/> <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Calcule a marca OMAC para o bloco de dados que aparece após o membro **OMAC** da estrutura de entrada. Em seguida, copie esse valor de marca para o membro **OMAC** .
3.  Chame [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).
4.  O driver coloca a saída do comando na estrutura de [**D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT**](d3dauthenticatedchannel-configure-output.md) .
5.  Calcule a marca OMAC para o bloco de dados que aparece após o membro **OMAC** da estrutura de saída. Compare isso com o valor do membro **OMAC** . Falha se eles não corresponderem.
6.  Compare os valores dos membros **configuratype**, **hChannel** e **SequenceNumber** na estrutura de saída com seus valores para esses membros. Falha se eles não corresponderem.
7.  Incrementar o número de sequência para o próximo comando.

## <a name="sending-authenticated-channel-queries"></a>Enviando consultas de canal autenticado

Um conjunto de consultas é definido para recuperar informações sobre o canal autenticado. Para obter uma lista de consultas, consulte [proteção de conteúdo consultas](content-protection-queries.md).

Para enviar um comando para o canal autenticado, execute as etapas a seguir.

1.  Preencha a estrutura de dados de entrada. Essa estrutura de dados é sempre uma estrutura de [**D3DAUTHENTICATEDCHANNEL_QUERY_INPUT**](d3dauthenticatedchannel-query-input.md) , possivelmente seguida por campos adicionais. Preencha a estrutura de **D3DAUTHENTICATEDCHANNEL_QUERY_INPUT** , conforme mostrado na tabela a seguir.

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
    <td>O número de sequência. O primeiro número de sequência é especificado com o envio de um comando <a href="d3dauthenticatedconfigure-initialize.md"><strong>D3DAUTHENTICATEDCONFIGURE_INITIALIZE</strong></a> . Cada vez que você enviar outra consulta, aumente esse número em 1. O número de sequência protege contra ataques de repetição.
    <blockquote>
    [!Note]<br />
Dois números de sequência separados são usados, um para comandos e outro para consultas.
    </blockquote>
    <br/> <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Chame [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).
3.  O driver coloca a saída da consulta em uma estrutura de [**D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT**](d3dauthenticatedchannel-query-output.md) . Essa estrutura é seguida por campos adicionais, dependendo do tipo de consulta.
4.  Calcule a marca OMAC para o bloco de dados que aparece após o membro **OMAC** da estrutura de saída. Compare isso com o valor do membro **OMAC** . Falha se eles não corresponderem.
5.  Compare os valores dos membros **configuratype**, **hChannel** e **SequenceNumber** na estrutura de saída com seus valores para esses membros. Falha se eles não corresponderem.
6.  Incrementar o número de sequência para a próxima consulta.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[APIs de vídeo do Direct3D 9](direct3d-video-apis.md)
</dt> </dl>

 

 
