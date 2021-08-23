---
title: recursos adicionados no SDK do Windows Media 9,5
description: recursos adicionados no SDK do Windows Media 9,5
ms.assetid: 1525132c-8aa1-42bb-9552-41531fb83055
keywords:
- Windows SDK do formato de mídia, recursos
- Windows SDK do formato de mídia, novos recursos
- Windows SDK de formato de mídia, interface para processamento específico de aplicativo
- Windows SDK do formato de mídia, DXVA (aceleração de vídeo do DirectX)
- Windows SDK do formato de mídia, interface IWMPlayerHook
- IWMPlayerHook
- Windows SDK do formato de mídia, versões baseadas em x64 do Windows
- Windows SDK de formato de mídia, codec de imagem de vídeo de mídia Windows
- Windows SDK do formato de mídia, codecs de áudio
- Windows SDK do formato de mídia, DRM 10 para dispositivos de rede
- Windows SDK do formato de mídia, licenças DRM
- Windows SDK de formato de mídia, codec de perfil avançado
- Windows SDK do formato de mídia, formato de interconexão digital Sony/Philips (S/PDIF)
- Windows SDK de formato de mídia, formatos de atraso baixo
- Windows SDK do formato de mídia, modo de busca aproximado
- Windows SDK de formato de mídia, gravação de playlist
- Windows SDK de formato de mídia, suporte a vários idiomas
- Windows sdk do formato de mídia, Windows media Gerenciador de Dispositivos sdk
- Windows SDK de formato de mídia, interfaces de codec
- codecs, Windows imagem de vídeo de mídia
- DRM (gerenciamento de direitos digitais), protocolo de transferência segura de dispositivos de rede
- DRM (gerenciamento de direitos digitais), protocolo de transferência segura de dispositivos de rede
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- codecs, codec de perfil avançado
- Formato de interconexão digital Sony/Philips (S/PDIF), transferindo ou transmitindo usando
- S/PDIF (formato de interconexão digital Sony/Philips), transferindo ou transmitindo usando
- modo de procura aproximado
- metadados, suporte a vários idiomas
- Windows SDK de Gerenciador de Dispositivos de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbcabd2fd3ae1b1030b04c0be342bcb64678e98eef601c83570ad68a13567820
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119591396"
---
# <a name="features-added-in-the-windows-media-95-sdk"></a>recursos adicionados no SDK do Windows Media 9,5

o SDK 9,5 do formato de mídia do Windows introduziu novos recursos para fornecer segurança e flexibilidade de conteúdo aprimoradas. As seguintes alterações foram feitas no SDK desde a versão da série 9.

## <a name="new-interface-for-application-specific-processing-during-directx-video-acceleration"></a>Nova interface para processamento específico do aplicativo durante aceleração de vídeo do DirectX

Os aplicativos do Player que dão suporte à aceleração de vídeo do DirectX agora podem implementar a interface [**IWMPlayerHook**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook) para executar o processamento específico do aplicativo durante a decodificação do DirectX VA. O leitor chama o método de retorno de chamada [**IWMPLayerHook::P decodificar**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmplayerhook-predecode) antes de passar amostras de vídeo compactados para o processador de vídeo para decodificação.

> [!Note]  
> para usar a interface **IWMPlayerHook** e a interface [**IWMReaderAdvanced5**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5) associada, você deve ter a atualização do número 888656 instalada no SDK do formato de mídia Windows. Você pode baixar a atualização no [site da Microsoft](https://support.microsoft.com/?id=888656).

 

## <a name="windows-media-format-sdk-version-for-x64-based-versions-of-windows"></a>Windows Versão do SDK do formato de mídia para versões baseadas em x64 do Windows

uma versão baseada em x64 do SDK do formato de mídia do Windows está disponível. Esta documentação se aplica às versões de 32 bits e à versão baseada em x64 do SDK. no entanto, o DRM (gerenciamento de direitos digitais) não tem suporte no SDK do formato de mídia Windows baseado em x64.

## <a name="new-version-of-the-windows-media-video-image-codec"></a>nova versão do Codec de imagem de vídeo de mídia Windows

o codec Windows Media Video 9 Image v2 simplifica os cálculos de geometria de exemplo para panorâmica e zoom. O novo codec também dá suporte a várias transições complexas entre imagens.

## <a name="new-version-of-the-windows-media-audio-codecs"></a>nova versão dos codecs de áudio de mídia Windows

o SDK 9,5 do formato de mídia do Windows inclui os seguintes codecs de áudio atualizados:

-   Windows Áudio de mídia 9,1
-   Windows Áudio de mídia 9,1 Professional
-   Windows Áudio de mídia 9,1 sem perdas

## <a name="windows-media-drm-10-for-network-devices-protocol-support"></a>Windows Media DRM 10 para suporte de protocolo de dispositivos de rede

o SDK 9,5 do formato de mídia do Windows dá suporte ao novo Windows Media DRM 10 para dispositivos de rede protocolo de transferência segura. Esse protocolo pode ser usado para transmitir conteúdo criptografado por uma rede local para um dispositivo de reprodução, como um receptor de vídeo de conjunto superior.

a maioria dos procedimentos usados para implementar o suporte para Windows mídia DRM 10 para dispositivos de rede deve ser executada pelo aplicativo. no entanto, você pode usar métodos do SDK do formato de mídia Windows para fornecer a seguinte funcionalidade:

-   mantenha um banco de dados de dispositivos, incluindo aqueles habilitados para Windows mídia DRM 10 para dispositivos de rede.
-   Valide dispositivos para garantir que eles sejam "perto" o suficiente para o cliente na rede para transmissão segura.
-   converta arquivos protegidos por DRM em Windows mídia DRM 10 para fluxos de dispositivos de rede.
-   Gravar arquivos usando dados anteriormente criptografados.

## <a name="support-for-new-drm-licenses"></a>Suporte para novas licenças DRM

novas licenças criadas usando o Windows SDK do gerenciador de direitos de mídia usam níveis de proteção de saída (OPLs) para especificar direitos e restrições para reproduzir e copiar conteúdo. o SDK do formato de mídia Windows dá suporte para a leitura do OPLs de uma licença.

## <a name="new-video-codec"></a>Novo codec de vídeo

o codec de perfil avançado do Windows media video 9 baseia-se na alta qualidade do codec do Windows media video 9 ao adicionar suporte para codificação entrelaçada.

## <a name="spdif-output"></a>Saída de S/PDIF

o conteúdo codificado com um dos codecs de Professional de áudio de mídia Windows agora pode ser transferido ou transmitido usando o S/PDIF (formato de interconexão Digital) da Sony/Philips.

## <a name="low-delay-audio"></a>Low-Delay áudio

o Windows media audio 9,1 e Windows áudio de mídia 9,1 Professional codecs agora são compatíveis com vários formatos de atraso baixo. Esses formatos produzem fluxos de áudio que podem ser iniciados mais rapidamente, reduzindo a latência em cenários de alternância de fluxo. A latência geral em transmissões ao vivo também é melhorada com o uso de formatos de atraso baixo.

## <a name="approximate-seeking-mode"></a>Modo de procura aproximado

Agora você pode buscar um tempo aproximado em um arquivo ASF com o leitor. Esse modo melhora o desempenho ao executar uma busca imprecisa, como quando um usuário clica na barra de busca em Windows Media Player. A busca aproximada retorna o exemplo de mídia para o cleanpoint anterior em vez de reconstruir o exemplo para o tempo preciso procurado.

## <a name="playlist-burning"></a>Gravação de playlist

Windows O Media DRM 10 dá suporte a direitos de cópia de arquivos de áudio para um CD de livro vermelho como parte de uma lista de reprodução. o SDK do formato de mídia Windows fornece métodos para verificar se os arquivos em uma playlist têm permissão para serem copiados.

## <a name="improved-multiple-language-support-for-metadata"></a>Suporte de Multiple-Language aprimorado para metadados

no SDK do Windows Media Format 9 Series, todos os metadados adicionados a um arquivo foram atribuídos a uma lista de idiomas que recebeu o identificador de idioma do idioma padrão. Isso causou problemas quando os distribuidores de conteúdo em localidades diferentes adicionavam alguns metadados, porque os usuários na localidade do distribuidor só veem os poucos atributos adicionados para seu idioma. o SDK 9,5 do formato de mídia do Windows resolve esse problema não criando uma lista de idiomas até que haja atributos de dois idiomas presentes no arquivo. Nesse ponto, todos os metadados são associados à localidade do segundo idioma, que, em seguida, torna-se o padrão. Dessa forma, um distribuidor de conteúdo pode manter todos os metadados originais de um arquivo, como título e autor, intactos ao adicionar alguns atributos pertinentes à sua localidade.

## <a name="windows-media-device-manager-sdk-included-in-installation"></a>Windows SDK de Gerenciador de Dispositivos de mídia incluído na instalação

o pacote de instalação do sdk 9,5 do formato de mídia do Windows instala o sdk de Gerenciador de Dispositivos de mídia do Windows. a documentação do SDK do Windows Media Gerenciador de Dispositivos pode ser encontrada na pasta C: \\ WMSDK \\ WMFSDK95 \\ WMDM \\ docs (sua pasta será diferente se você não instalar o SDK do formato de mídia do Windows na pasta padrão.)

## <a name="codec-interface-documentation"></a>Documentação da interface do codec

esta documentação inclui informações sobre como usar os codecs de áudio e vídeo de mídia Windows fora do SDK do formato de mídia do Windows. Esta documentação foi lançada originalmente como parte de um download da Microsoft Developer Network. os aplicativos de exemplo que demonstram o uso do codec DMOs diretamente estão incluídos na instalação do SDK do formato de mídia Windows juntamente com os cabeçalhos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**sobre o SDK do formato de mídia Windows**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




