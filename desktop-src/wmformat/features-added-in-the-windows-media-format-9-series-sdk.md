---
title: Recursos adicionados no SDK da série Windows Media Format 9 Series
description: Recursos adicionados no SDK da série Windows Media Format 9 Series
ms.assetid: 73c4da27-a456-4845-a35b-edb75aa3f953
keywords:
- SDK do Windows Media Format, recursos
- SDK do Windows Media Format, novos recursos
- SDK do Windows Media Format, leitores síncronos
- SDK do Windows Media Format, indexação baseada em quadros
- SDK do Windows Media Format, códigos de tempo SMPTE
- SDK do Windows Media Format, filtros do DirectShow
- SDK do Windows Media Format, recurso de gravação de DRM
- SDK do Windows Media Format, coletores de arquivos
- SDK do Windows Media Format, DXVA (aceleração de vídeo do DirectX)
- SDK do Windows Media Format, áudio multicanal
- SDK do Windows Media Format, marca d' água
- SDK do Windows Media Format, suporte a vários idiomas
- SDK do Windows Media Format, modelos de conformidade do dispositivo
- SDK do Windows Media Format, enumerações de codec
- SDK do Windows Media Format, exclusão mútua
- SDK do Windows Media Format, taxa de bits múltipla (MBR)
- SDK do Windows Media Format, transcodificação com recompactação inteligente
- SDK do Windows Media Format, recompactação inteligente
- SDK do Windows Media Format, recompactação
- SDK do Windows Media Format, metadados
- SDK do Windows Media Format, taxa de proporção de pixels dinâmicos
- SDK do Windows Media Format, fluxos de vídeo entrelaçados
- Windows Media Format SDK, codificação em duas passagens
- SDK do Windows Media Format, WMStub. lib
- leitores síncronos, sobre
- indexação baseada em quadros
- Códigos de tempo SMPTE, sobre
- Filtros do DirectShow
- coletores de arquivos, aprimoramentos
- áudio de multicanal, sobre
- marca d' água, sobre
- codecs, enumerações
- exclusão mútua, sobre
- DRM (gerenciamento de direitos digitais), capacidade de gravação
- DRM (gerenciamento de direitos digitais), capacidade de gravação
- DXVA (aceleração de vídeo do DirectX), sobre
- DXVA (aceleração de vídeo DirectX), sobre
- ASF (Advanced Systems Format), suporte a vários idiomas
- ASF (formato de sistemas avançados), suporte a vários idiomas
- taxa de bits múltipla (MBR), sobre
- MBR (taxa de bits múltipla), sobre
- transcodificação com recompactação inteligente
- recompactação inteligente
- recompactação
- metadados, Windows Media Format SDK
- taxa de proporção de pixels dinâmicos
- fluxos de vídeo entrelaçados
- codificação de dois passos, sobre
- 2-passar codificação, sobre
- WMStub. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adca7e39c89220c2c8c4cac6af354eefb77257aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159874"
---
# <a name="features-added-in-the-windows-media-format-9-series-sdk"></a>Recursos adicionados no SDK da série Windows Media Format 9 Series

O SDK do Windows Media Format 9 Series introduziu muitos aprimoramentos e recursos. Esta seção fornece uma visão geral desses recursos para o benefício dos usuários de migrar de uma versão anterior do SDK.

## <a name="synchronous-reading"></a>Leitura síncrona

Você pode ler arquivos ASF com chamadas síncronas. Ao ler um arquivo de forma síncrona, você pode alterar as configurações do leitor enquanto ele está sendo lido. As operações de leitura síncronas do SDK não oferecem suporte para a leitura de arquivos pela Internet, mas você pode usar a interface COM padrão, **IStream**, para ler de fontes personalizadas.

## <a name="frame-based-indexing"></a>Indexação baseada em quadros

Você pode indexar arquivos ASF com base em quadros de vídeo. O leitor e o leitor síncrono podem buscar um quadro de um fluxo de vídeo e sincronizar os outros fluxos para esse quadro.

## <a name="indexing-and-seeking-with-smpte-time-code"></a>Indexação e busca com o código de tempo SMPTE

O SDK do Windows Media Format permite armazenar códigos de tempo SMPTE em arquivos ASF. Os arquivos podem ser indexados pelo código de hora SMPTE, e o leitor assíncrono e o leitor síncrono podem buscar entradas de índice de código de tempo SMPTE.

## <a name="directshow-filters"></a>Filtros do DirectShow

O SDK do Windows Media Format inclui dois filtros de® do Microsoft DirectShow que permitem que aplicativos baseados em DirectShow leiam e gravem arquivos ASF. O DirectShow também permite que os aplicativos capturem dados de dispositivos de vídeo de áudio e descompactem dados de uma variedade de formatos antes de codificá-los novamente como conteúdo baseado no Windows Media.

## <a name="enhanced-profiles"></a>Perfis avançados

Os perfis podem conter informações de compartilhamento de largura de banda e informações de priorização de fluxo. O compartilhamento de largura de banda permite especificar que dois ou mais fluxos, independentemente de suas taxas de bits individuais, nunca usarão mais do que uma quantidade especificada de largura de banda. A largura de banda que compartilha os dados em um perfil é puramente informativa; Ele não é imposto por nenhuma lógica no SDK. A priorização de fluxo permite que você especifique uma ordem de prioridade para os fluxos em um perfil. Se não houver largura de banda suficiente na reprodução para transmitir o arquivo corretamente, os fluxos de prioridade mais baixos poderão ser ignorados para melhorar o desempenho.

## <a name="drm-writing-capability"></a>Funcionalidade de gravação de DRM

Além do suporte a leitura de DRM existente, o SDK do Windows Media Format 9 Series adicionou suporte para gravar arquivos ASF com a proteção DRM versão 1 ou DRM versão 7. Essa nova funcionalidade habilita cenários de "DRM ao vivo", como webcast de pagamento por exibição de eventos esportivos vivos ou concertos.

## <a name="enhanced-file-sink"></a>Coletor de arquivo avançado

Vários novos recursos de coletor de arquivos foram adicionados à versão 9 Series do SDK. Você pode configurar o coletor de arquivos para desabilitar a indexação automática de arquivos ASF criados recentemente. Você também tem a opção de configurá-lo para entrada e saída sem buffer.

## <a name="directx-video-acceleration"></a>Aceleração de vídeo do DirectX

A DXVA (aceleração de vídeo do DirectX) é uma tecnologia que permite a reprodução de vídeo de alta taxa de bits (qualidade de DVD ou melhor) em computadores menos poderosos com placas gráficas habilitadas para DXVA. Você pode usar o objeto leitor deste SDK para habilitar a aceleração de vídeo do DirectX, se o hardware oferecer suporte a ele, ao reproduzir arquivos ASF.

## <a name="multichannel-audio"></a>Áudio de multicanal

Você pode codificar e reproduzir áudio multicanal. O codec Windows Media Audio 9 Professional dá suporte a formatos com 6 canais e 8 canais, bem como estéreo de alta definição.

## <a name="watermarking"></a>Marca d' água

Você pode codificar arquivos ASF com marcas d' água digitais para segurança. Todos os sistemas de marca d' água são diferentes em sua abordagem, mas toda a identificação de inserção no conteúdo codificado. A marca d' água é executada usando DMOs (objetos de mídia) do® DirectX de terceiros especiais.

## <a name="support-for-multiple-languages-in-asf-files"></a>Suporte para vários idiomas em arquivos ASF

Você pode dar suporte a vários idiomas em arquivos ASF, em fluxos e em metadados. Por exemplo, você pode criar um arquivo de vídeo com fluxos de áudio em vários idiomas. Na reprodução, o usuário pode selecionar qual idioma usar ou o aplicativo pode consultar as informações do sistema no computador de jogo e selecionar um idioma automaticamente. Os atributos de metadados também podem ser inseridos várias vezes, com os valores em idiomas diferentes.

## <a name="device-conformance-templates"></a>Modelos de conformidade do dispositivo

Para auxiliar no direcionamento de conteúdo para dispositivos cliente específicos, os codecs de mídia do Windows agora dão suporte a modelos de conformidade de dispositivo. Cada modelo contém um intervalo definido de configurações e recursos de codec que devem ser usados para a mídia destinada a uma determinada categoria de plataformas. Não há mais suporte para perfis de sistema com as versões mais recentes dos codecs de mídia do Windows. Todos os perfis devem ser personalizados para atender às suas necessidades. Você pode usar modelos de conformidade do dispositivo para ajudá-lo a criar seus perfis.

## <a name="expanded-codec-enumeration"></a>Enumeração de codec expandida

O objeto Gerenciador de perfis pode consultar os codecs de vídeo e áudio do Windows Media para obter os formatos com suporte. Você pode definir parâmetros para os formatos recuperados. Por exemplo, você pode recuperar todos os formatos de taxa de bits variáveis com base em qualidade suportados pelo codec do Windows Media Audio 9.

## <a name="improved-mutual-exclusion"></a>Exclusão mútua aprimorada

Você pode criar registros nomeados contendo vários fluxos dentro de um objeto de exclusão mútua. Você também pode nomear objetos de exclusão mútua para torná-los mais fáceis de identificar. Isso permite que você crie camadas de exclusão mútua. Por exemplo, um arquivo pode conter fluxos mutuamente exclusivos por taxa de bits e por idioma. A exclusão mútua baseada em linguagem envolveria grupos de fluxos, cada grupo consistindo em fluxos no mesmo idioma, mas mutuamente exclusivos por taxa de bits.

## <a name="expanded-multiple-bit-rate-support"></a>Suporte à taxa de vários bits expandido

O suporte à exclusão mútua está incluído para áudio de taxa de bits múltipla (MBR) e para vídeo com fluxos de tamanhos de imagem variados.

## <a name="attributes-for-streams"></a>Atributos para fluxos

Você pode atribuir atributos a fluxos individuais em arquivos ASF. Você ainda deve usar atributos de nível de arquivo para arquivos MP3. Esse recurso não adiciona nenhum método ao SDK, mas os métodos existentes agora aceitam números de fluxo diferentes de zero.

## <a name="transcoding-with-smart-recompression"></a>Transcodificação com recompactação inteligente

A recompactação inteligente permite que você transcodifique arquivos de áudio do Windows Media de uma taxa de bits alta para uma taxa de bits inferior com melhor qualidade do que o que era alcançado anteriormente.

## <a name="expanded-metadata-support"></a>Suporte a metadados expandido

O Windows Media Format SDK fornece os seguintes novos recursos de metadados:

-   Marcas de metadados baseadas em índice, habilitando várias marcas com o mesmo nome.
-   Capacidade de ler atributos de cabeçalho DRM sem um arquivo WMStubDRM. lib.
-   Atributos com mais de 64 quilobytes de dados associados.
-   Atributos em vários idiomas.
-   Dezenas de novos atributos predefinidos.

## <a name="dynamic-pixel-aspect-ratio"></a>Taxa de proporção de pixels dinâmicos

Os fluxos de vídeo compostos por vários tipos de conteúdo podem ser acomodados identificando a taxa de proporção de pixel dos exemplos diferentes no fluxo. Isso permite que o aplicativo de reprodução forneça uma reprodução melhor desse tipo de conteúdo.

## <a name="interlaced-video-streams"></a>Fluxos de vídeo entrelaçados

As versões anteriores do Windows Media Format SDK forneceram a capacidade de codificar o conteúdo [*entrelaçado*](wmformat-glossary.md) em um fluxo de vídeo de verificação progressiva. Começando com o SDK do Windows Media Format 9 Series, você pode codificar vídeo entrelaçado enquanto preserva seu formato entrelaçado. Isso pode resultar em uma reprodução aprimorada, especialmente em dispositivos entrelaçados, como conjuntos de televisão.

## <a name="two-pass-encoding"></a>Codificação de Two-Pass

Os novos codecs de mídia do Windows habilitam a codificação de duas passagens. O conteúdo codificado em duas passagens pode atingir uma saída de qualidade mais alta.

## <a name="new-speech-codec"></a>Novo codec de fala

Esse SDK inclui o novo codec de voz do Windows Media Audio 9 que é otimizado para codificar a voz humana enquanto usa uma taxa de bits baixa. Esse codec também fornece um desempenho superior para conteúdo misto de voz musical.

## <a name="accessible-video-frame-duration"></a>Duração do quadro de vídeo acessível

Você pode ter o objeto gravador desse SDK para fornecer a duração dos quadros de vídeo ao leitor.

## <a name="streaming-html"></a>HTML de streaming

Com a versão anterior deste SDK, você pôde usar um comando de script para sinalizar seu aplicativo para abrir uma página da Web. Começando com o SDK do Windows Media Format 9 Series, você pode armazenar os componentes de páginas da Web em seus arquivos ASF, para garantir que não haja nenhum atraso nas apresentações.

## <a name="wmstublib-no-longer-required-for-build-environment"></a>WMStub. lib não é mais necessário para o ambiente de compilação

As configurações de ambiente de compilação para o SDK do Windows Media Format foram alteradas a partir do SDK do Windows Media Format 9 Series. Você não precisa mais incluir WMStub. lib para aplicativos que usam esse SDK. No entanto, os aplicativos habilitados para DRM ainda devem obter e assinar um contrato de licença separado e obter uma biblioteca estática exclusiva da Microsoft. Entre em contato wmla@microsoft.com para obter mais informações sobre a biblioteca DRM e o contrato de licença. Para obter mais informações sobre como criar projetos com esse SDK, consulte [arquivos de biblioteca e configurações do compilador](library-files-and-compiler-settings.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o SDK do Windows Media Format**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




