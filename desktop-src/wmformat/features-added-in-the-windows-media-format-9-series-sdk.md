---
title: Recursos adicionados no SDK Windows Media Format 9 Series
description: Recursos adicionados no SDK Windows Media Format 9 Series
ms.assetid: 73c4da27-a456-4845-a35b-edb75aa3f953
keywords:
- Windows SDK de Formato de Mídia, recursos
- Windows SDK de Formato de Mídia, novos recursos
- Windows SDK de Formato de Mídia, leitores síncronos
- Windows SDK de Formato de Mídia, indexação baseada em quadro
- Windows SDK de Formato de Mídia, códigos de tempo SMPTE
- Windows SDK de Formato de Mídia, DirectShow filtros
- Windows SDK de Formato de Mídia, funcionalidade de escrita drm
- Windows SDK de Formato de Mídia, sinks de arquivos
- Windows SDK de Formato de Mídia, Aceleração de Vídeo DirectX (DXVA)
- Windows SDK de Formato de Mídia, áudio multicanal
- Windows SDK de formato de mídia, marca d'água
- Windows SDK de Formato de Mídia, suporte a vários idiomas
- Windows SDK de Formato de Mídia, modelos de conformidade do dispositivo
- Windows SDK de Formato de Mídia, enumerações de codec
- Windows SDK de Formato de Mídia, exclusão mútua
- Windows SDK de Formato de Mídia, taxa de bits múltipla (MBR)
- Windows SDK de Formato de Mídia, transcodificação com recompactação inteligente
- Windows SDK de Formato de Mídia, recompactação inteligente
- Windows SDK de Formato de Mídia, recompactação
- Windows SDK de formato de mídia, metadados
- Windows SDK de Formato de Mídia, taxa de proporção de pixel dinâmico
- Windows SDK de Formato de Mídia, fluxos de vídeo entrelaçados
- Windows SDK de Formato de Mídia, codificação de duas passs
- Windows SDK de Formato de Mídia,WMStub.lib
- leitores síncronos, sobre
- indexação baseada em quadro
- Códigos de hora SMPTE, sobre
- DirectShow filtros
- sinks de arquivo, aprimoramentos
- áudio multicanal, sobre
- marca d'água,sobre
- codecs,enumerações
- exclusão mútua, sobre
- DRM (gerenciamento de direitos digitais), capacidade de escrita
- DRM (gerenciamento de direitos digitais), capacidade de escrita
- DXVA (Aceleração de Vídeo DirectX), sobre
- DXVA (Aceleração de Vídeo DirectX),sobre
- ASF (Advanced Systems Format), suporte a vários idiomas
- ASF (Formato de Sistemas Avançados), suporte a vários idiomas
- MBR (taxa de bits múltipla), sobre
- MBR (taxa de vários bits),sobre
- transcodificação com recompactação inteligente
- recompactação inteligente
- Recompressão
- metadados, Windows SDK de Formato de Mídia
- taxa de proporção de pixel dinâmico
- fluxos de vídeo entrelaçados
- codificação de duas passs, sobre
- Codificação de duas passs, sobre
- WMStub.lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76dc0f4a8c0b23ba33409039ae7f1d46ada1b3299790ef82fb98b8714f616117
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547446"
---
# <a name="features-added-in-the-windows-media-format-9-series-sdk"></a>Recursos adicionados no SDK Windows Media Format 9 Series

O SDK Windows Media Format 9 series introduziu muitas melhorias e recursos. Esta seção fornece uma visão geral desses recursos para o benefício dos usuários que estão migrando de uma versão anterior do SDK.

## <a name="synchronous-reading"></a>Leitura síncrona

Você pode ler arquivos ASF com chamadas síncronas. Ao ler um arquivo de forma síncrona, você pode alterar as configurações do leitor enquanto ele está lendo. As operações de leitura síncrona do SDK não dão suporte à leitura de arquivos pela Internet, mas você pode usar a interface COM padrão, **IStream,** para ler de fontes personalizadas.

## <a name="frame-based-indexing"></a>Indexação baseada em quadro

Você pode indexar arquivos ASF com base em quadros de vídeo. O leitor e o leitor síncrono podem buscar um quadro de um fluxo de vídeo e sincronizar os outros fluxos com esse quadro.

## <a name="indexing-and-seeking-with-smpte-time-code"></a>Indexação e busca com código de tempo SMPTE

O Windows SDK de Formato de Mídia permite que você armazene códigos de hora SMPTE em arquivos ASF. Os arquivos podem ser indexados por código de hora SMPTE e o leitor assíncrono e o leitor síncrono podem buscar entradas de índice de código de hora SMPTE.

## <a name="directshow-filters"></a>DirectShow Filtros

O Windows SDK de Formato de Mídia inclui dois filtros do Microsoft DirectShow® que permitem que DirectShow aplicativos baseados em dados leiam e escrevam arquivos ASF. DirectShow também permite que os aplicativos capturem dados de dispositivos de áudio e vídeo e descompactem dados de uma variedade de formatos antes de codificar-os como Windows conteúdo baseado em mídia.

## <a name="enhanced-profiles"></a>Perfis aprimorados

Os perfis podem conter informações de compartilhamento de largura de banda e informações de priorização de fluxo. O compartilhamento de largura de banda permite que você especifique que dois ou mais fluxos, independentemente de suas taxas de bits individuais, nunca usarão mais de uma quantidade especificada de largura de banda. Os dados de compartilhamento de largura de banda em um perfil são puramente informacionais; ele não é imposto por nenhuma lógica no SDK. A priorização de fluxo permite que você especifique uma ordem de prioridade para os fluxos em um perfil. Se não houver largura de banda suficiente na reprodução para transmitir o arquivo corretamente, os fluxos de prioridade mais baixa poderão ser ignorados para melhorar o desempenho.

## <a name="drm-writing-capability"></a>Capacidade de escrita drm

Além do suporte de leitura drm existente, o SDK do Windows Media Format 9 Series adicionou suporte para escrever arquivos ASF com proteção DRM versão 1 ou DRM versão 7. Essa nova funcionalidade habilita cenários de "DRM ao vivo", como webcast pago por exibição de eventos de shows ao vivo ou shows.

## <a name="enhanced-file-sink"></a>Aprimorado o sink de arquivos

Vários novos recursos de sink de arquivo foram adicionados à versão série 9 do SDK. Você pode configurar o sink de arquivos para desabilitar a indexação automática de arquivos ASF recém-criados. Você também tem a opção de configurá-lo para entrada e saída sem-cofre.

## <a name="directx-video-acceleration"></a>Aceleração de vídeo do DirectX

A DXVA (Aceleração de Vídeo DirectX) é uma tecnologia que permite a reprodução de vídeo de alta taxa de bits (qualidade de DVD ou melhor) em máquinas menos poderosas com placas gráficas habilitadas para DXVA. Você pode usar o objeto de leitor desse SDK para habilitar a Aceleração de Vídeo do DirectX, se o hardware dá suporte a ele, ao tocar arquivos ASF.

## <a name="multichannel-audio"></a>Áudio multicanal

Você pode codificar e reproduzir áudio multicanal. O codec Windows Media Audio 9 Professional dá suporte a formatos com 6 canais e 8 canais, bem como estéreo de alta definição.

## <a name="watermarking"></a>Watermarking

Você pode codificar arquivos ASF com marcas d'água digitais para segurança. Todos os sistemas de marca-d'água são diferentes em sua abordagem, mas todos inserir identificação em conteúdo codificado. A marca d'água é executada usando DMOs (objetos de mídia® DirectX de terceiros especiais).

## <a name="support-for-multiple-languages-in-asf-files"></a>Suporte para vários idiomas em arquivos ASF

Você pode dar suporte a vários idiomas em arquivos ASF, tanto em fluxos quanto em metadados. Por exemplo, você pode criar um arquivo de vídeo com fluxos de áudio em vários idiomas. Na reprodução, o usuário pode selecionar qual idioma usar ou seu aplicativo pode consultar as informações do sistema no computador em reprodução e selecionar um idioma automaticamente. Atributos de metadados também podem ser inseridos várias vezes, com os valores em idiomas diferentes.

## <a name="device-conformance-templates"></a>Modelos de conformidade do dispositivo

Para auxiliar no direcionamento de conteúdo para dispositivos cliente específicos, os codecs Windows Media agora são compatíveis com modelos de conformidade do dispositivo. Cada modelo contém um intervalo definido de configurações e recursos de codec que devem ser usados para mídias destinadas a uma categoria específica de plataformas. Não há mais suporte para perfis do sistema com as versões mais recentes dos codecs Windows Media. Todos os perfis devem ser personalizados para atender às suas necessidades. Você pode usar modelos de conformidade do dispositivo para ajudá-lo a criar seus perfis.

## <a name="expanded-codec-enumeration"></a>Enumeração codec expandida

O objeto do gerenciador de perfil pode consultar os codecs Windows Áudio de Mídia e Vídeo para os formatos com suporte. Você pode definir parâmetros para os formatos recuperados. Por exemplo, você pode recuperar todos os formatos de taxa de bits variáveis baseados em qualidade com suporte pelo codec Windows Media Audio 9.

## <a name="improved-mutual-exclusion"></a>Exclusão mútua aprimorada

Você pode criar registros nomeados contendo vários fluxos dentro de um objeto de exclusão mútua. Você também pode nomear objetos de exclusão mútua para torná-los mais fáceis de identificar. Isso permite que você crie camadas de exclusão mútua. Por exemplo, um arquivo pode conter fluxos mutuamente exclusivos por taxa de bits e por idioma. A exclusão mútua baseada em linguagem envolveria grupos de fluxos, cada grupo que consiste em fluxos na mesma linguagem, mas mutuamente exclusivos por taxa de bits.

## <a name="expanded-multiple-bit-rate-support"></a>Suporte expandido de taxa de bits múltipla

O suporte à exclusão mútua está incluído para áudio MBR (taxa de bits múltipla) e para vídeo com fluxos de tamanhos de imagem variados.

## <a name="attributes-for-streams"></a>Atributos para Fluxos

Você pode atribuir atributos a fluxos individuais em arquivos ASF. Você ainda deve usar atributos de nível de arquivo para arquivos MP3. Esse recurso não adiciona nenhum método ao SDK, mas os métodos existentes agora aceitarão números de fluxo diferentes de zero.

## <a name="transcoding-with-smart-recompression"></a>Transcodificação com recompactação inteligente

A recompactação inteligente permite transcodificar Windows de áudio de mídia de uma taxa de bits alta para uma taxa de bits mais baixa com melhor qualidade do que antes viável.

## <a name="expanded-metadata-support"></a>Suporte a metadados expandidos

O Windows SDK de Formato de Mídia fornece os seguintes novos recursos de metadados:

-   Marcas de metadados baseadas em índice, habilitando várias marcas com o mesmo nome.
-   Capacidade de ler atributos de header drm sem um arquivo WMStubDRM.lib.
-   Atributos com mais de 64 quilobytes de dados associados.
-   Atributos em vários idiomas.
-   Dezenas de novos atributos predefinidos.

## <a name="dynamic-pixel-aspect-ratio"></a>Taxa de proporção de pixel dinâmico

Os fluxos de vídeo compostos por vários tipos de conteúdo podem ser acomodados identificando a taxa de proporção de pixel das amostras diferentes no fluxo. Isso permite que o aplicativo em reprodução forneça melhor reprodução desse conteúdo.

## <a name="interlaced-video-streams"></a>Vídeo entrelaçados Fluxos

As versões anteriores do Windows SDK de Formato de Mídia do Windows forneceu a capacidade de codificar conteúdo [*entrelaçado*](wmformat-glossary.md) em um fluxo de vídeo de verificação progressiva. Começando com o SDK do Windows Media Format 9 Series, você pode codificar o vídeo entrelaçados preservando seu formato entrelaçado. Isso pode resultar em reprodução aprimorada, especialmente em dispositivos entrelaçados, como conjuntos de tv.

## <a name="two-pass-encoding"></a>Two-Pass codificação

Os novos Windows de mídia permitem codificação de duas passs. O conteúdo codificado em duas passagens pode obter uma saída de qualidade mais alta.

## <a name="new-speech-codec"></a>Novo Codec de Fala

Esse SDK inclui o novo codec Windows Media Audio 9 Voice, que é otimizado para codificar a voz humana usando uma taxa de bits baixa. Esse codec também fornece desempenho superior para conteúdo de voz de música misturada.

## <a name="accessible-video-frame-duration"></a>Duração do quadro de vídeo acessível

Você pode fazer com que o objeto de gravação desse SDK forneça a duração dos quadros de vídeo para o leitor.

## <a name="streaming-html"></a>Streaming HTML

Com a versão anterior desse SDK, você conseguiu usar um comando de script para sinalizar seu aplicativo para abrir uma página da Web. Começando com o SDK do Windows Media Format 9 Series, você pode armazenar os componentes de páginas da Web em seus arquivos ASF para garantir que não haja atraso nas apresentações.

## <a name="wmstublib-no-longer-required-for-build-environment"></a>WMStub.lib não é mais necessário para o ambiente de build

As configurações de ambiente de build para o SDK Windows Formato de Mídia foram alteradas a partir do SDK Windows Media Format 9 Series. Você não precisa mais incluir WMStub.lib para aplicativos que usam esse SDK. No entanto, os aplicativos habilitados para DRM ainda devem obter e assinar um contrato de licença separado e obter uma biblioteca estática exclusiva da Microsoft. Entre wmla@microsoft.com em contato para obter mais informações sobre a biblioteca drm e o contrato de licença. Para obter mais informações sobre como criar projetos com esse SDK, consulte Arquivos de biblioteca [e compilador Configurações](library-files-and-compiler-settings.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o SDK Windows Formato de Mídia**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




