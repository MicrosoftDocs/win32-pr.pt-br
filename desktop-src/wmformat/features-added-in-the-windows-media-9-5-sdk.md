---
title: Recursos adicionados no SDK do Windows Media 9,5
description: Recursos adicionados no SDK do Windows Media 9,5
ms.assetid: 1525132c-8aa1-42bb-9552-41531fb83055
keywords:
- SDK do Windows Media Format, recursos
- SDK do Windows Media Format, novos recursos
- SDK do Windows Media Format, interface para processamento específico de aplicativo
- SDK do Windows Media Format, DXVA (aceleração de vídeo do DirectX)
- SDK do Windows Media Format, interface IWMPlayerHook
- IWMPlayerHook
- SDK do Windows Media Format, versões baseadas em x64 do Windows
- SDK do Windows Media Format, codec de imagem de vídeo do Windows Media
- SDK do Windows Media Format, codecs de áudio
- SDK do Windows Media Format, DRM 10 para dispositivos de rede
- SDK do Windows Media Format, licenças DRM
- SDK do Windows Media Format, codec de perfil avançado
- SDK do Windows Media Format, formato de interconexão digital Sony/Philips (S/PDIF)
- SDK do Windows Media Format, formatos de atraso baixo
- SDK do Windows Media Format, modo de busca aproximado
- SDK do Windows Media Format, gravação da playlist
- SDK do Windows Media Format, suporte a vários idiomas
- SDK do Windows Media Format, SDK do Windows Media Gerenciador de Dispositivos
- SDK do Windows Media Format, interfaces de codec
- codecs, imagem de vídeo do Windows Media
- DRM (gerenciamento de direitos digitais), protocolo de transferência segura de dispositivos de rede
- DRM (gerenciamento de direitos digitais), protocolo de transferência segura de dispositivos de rede
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- codecs, codec de perfil avançado
- Formato de interconexão digital Sony/Philips (S/PDIF), transferindo ou transmitindo usando
- S/PDIF (formato de interconexão digital Sony/Philips), transferindo ou transmitindo usando
- modo de procura aproximado
- metadados, suporte a vários idiomas
- SDK do Windows Media Gerenciador de Dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e58c9816ef80325422ee365b952842727b5004e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104084374"
---
# <a name="features-added-in-the-windows-media-95-sdk"></a>Recursos adicionados no SDK do Windows Media 9,5

O SDK 9,5 do Windows Media Format apresentou novos recursos para fornecer segurança e flexibilidade de conteúdo aprimoradas. As seguintes alterações foram feitas no SDK desde a versão da série 9.

## <a name="new-interface-for-application-specific-processing-during-directx-video-acceleration"></a>Nova interface para processamento específico do aplicativo durante aceleração de vídeo do DirectX

Os aplicativos do Player que dão suporte à aceleração de vídeo do DirectX agora podem implementar a interface [**IWMPlayerHook**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook) para executar o processamento específico do aplicativo durante a decodificação do DirectX VA. O leitor chama o método de retorno de chamada [**IWMPLayerHook::P decodificar**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmplayerhook-predecode) antes de passar amostras de vídeo compactados para o processador de vídeo para decodificação.

> [!Note]  
> Para usar a interface **IWMPlayerHook** e a interface [**IWMReaderAdvanced5**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5) associada, você deve ter a atualização do número 888656 instalada no SDK do Windows Media Format. Você pode baixar a atualização no [site da Microsoft](https://support.microsoft.com/?id=888656).

 

## <a name="windows-media-format-sdk-version-for-x64-based-versions-of-windows"></a>Versão do SDK do Windows Media Format para versões baseadas em x64 do Windows

Uma versão baseada em x64 do Windows Media Format SDK está disponível. Esta documentação se aplica às versões de 32 bits e à versão baseada em x64 do SDK. No entanto, o DRM (gerenciamento de direitos digitais) não tem suporte no SDK do Windows Media Format baseado em x64.

## <a name="new-version-of-the-windows-media-video-image-codec"></a>Nova versão do codec de imagem de vídeo do Windows Media

O codec do Windows Media Video 9 Image v2 simplifica os cálculos de geometria de exemplo para panorâmica e zoom. O novo codec também dá suporte a várias transições complexas entre imagens.

## <a name="new-version-of-the-windows-media-audio-codecs"></a>Nova versão dos codecs de áudio do Windows Media

O SDK 9,5 do Windows Media Format inclui os seguintes codecs de áudio atualizados:

-   Áudio do Windows Media 9,1
-   Windows Media Audio 9,1 Professional
-   Áudio do Windows Media 9,1 sem perdas

## <a name="windows-media-drm-10-for-network-devices-protocol-support"></a>Suporte ao protocolo Windows Media DRM 10 para dispositivos de rede

O SDK 9,5 do Windows Media Format oferece suporte ao novo Windows Media DRM 10 para dispositivos de rede protocolo de transferência segura. Esse protocolo pode ser usado para transmitir conteúdo criptografado por uma rede local para um dispositivo de reprodução, como um receptor de vídeo de conjunto superior.

A maioria dos procedimentos usados para implementar o suporte para Windows Media DRM 10 para dispositivos de rede deve ser executada pelo aplicativo. No entanto, você pode usar métodos do Windows Media Format SDK para fornecer a seguinte funcionalidade:

-   Mantenha um banco de dados de dispositivos, incluindo aqueles habilitados para o Windows Media DRM 10 para dispositivos de rede.
-   Valide dispositivos para garantir que eles sejam "perto" o suficiente para o cliente na rede para transmissão segura.
-   Converta arquivos protegidos por DRM no Windows Media DRM 10 para fluxos de dispositivos de rede.
-   Gravar arquivos usando dados anteriormente criptografados.

## <a name="support-for-new-drm-licenses"></a>Suporte para novas licenças DRM

As novas licenças criadas usando o SDK do Windows Media Rights Manager usam níveis de proteção de saída (OPLs) para especificar direitos e restrições para reproduzir e copiar conteúdo. O Windows Media Format SDK fornece suporte para a leitura do OPLs de uma licença.

## <a name="new-video-codec"></a>Novo codec de vídeo

O codec de perfil avançado do Windows Media Video 9 baseia-se na alta qualidade do codec do Windows Media Video 9 ao adicionar suporte para codificação entrelaçada.

## <a name="spdif-output"></a>Saída de S/PDIF

O conteúdo codificado com um dos codecs do Windows Media Audio Professional agora pode ser transferido ou transmitido usando o S/PDIF (formato de interconexão digital) da Sony/Philips.

## <a name="low-delay-audio"></a>Low-Delay áudio

Os codecs do Windows Media Audio 9,1 e Windows Media Audio 9,1 Professional agora oferecem suporte a vários formatos de atraso baixo. Esses formatos produzem fluxos de áudio que podem ser iniciados mais rapidamente, reduzindo a latência em cenários de alternância de fluxo. A latência geral em transmissões ao vivo também é melhorada com o uso de formatos de atraso baixo.

## <a name="approximate-seeking-mode"></a>Modo de procura aproximado

Agora você pode buscar um tempo aproximado em um arquivo ASF com o leitor. Esse modo melhora o desempenho ao executar uma busca imprecisa, como quando um usuário clica na barra de busca no Windows Media Player. A busca aproximada retorna o exemplo de mídia para o cleanpoint anterior em vez de reconstruir o exemplo para o tempo preciso procurado.

## <a name="playlist-burning"></a>Gravação de playlist

O Windows Media DRM 10 dá suporte a direitos de cópia de arquivos de áudio para um CD de livro vermelho como parte de uma lista de reprodução. O Windows Media Format SDK fornece métodos para verificar se os arquivos em uma playlist têm permissão para serem copiados.

## <a name="improved-multiple-language-support-for-metadata"></a>Suporte de Multiple-Language aprimorado para metadados

No SDK do Windows Media Format 9 Series, todos os metadados adicionados a um arquivo foram atribuídos a uma lista de idiomas que recebeu o identificador de idioma do idioma padrão. Isso causou problemas quando os distribuidores de conteúdo em localidades diferentes adicionavam alguns metadados, porque os usuários na localidade do distribuidor só veem os poucos atributos adicionados para seu idioma. O SDK 9,5 do Windows Media Format resolve esse problema não criando uma lista de idiomas até que haja atributos de dois idiomas presentes no arquivo. Nesse ponto, todos os metadados são associados à localidade do segundo idioma, que, em seguida, torna-se o padrão. Dessa forma, um distribuidor de conteúdo pode manter todos os metadados originais de um arquivo, como título e autor, intactos ao adicionar alguns atributos pertinentes à sua localidade.

## <a name="windows-media-device-manager-sdk-included-in-installation"></a>SDK do Windows Media Gerenciador de Dispositivos incluído na instalação

O pacote de instalação do Windows Media Format 9,5 SDK instala o SDK do Windows Media Gerenciador de Dispositivos. A documentação do SDK do Windows Media Gerenciador de Dispositivos pode ser encontrada na pasta C: \\ WMSDK \\ WMFSDK95 \\ WMDM \\ docs (sua pasta será diferente se você não instalar o SDK do formato de mídia do Windows na pasta padrão.)

## <a name="codec-interface-documentation"></a>Documentação da interface do codec

Esta documentação inclui informações sobre como usar os codecs de áudio e vídeo do Windows Media fora do SDK do Windows Media Format. Esta documentação foi lançada originalmente como parte de um download da Microsoft Developer Network. Os aplicativos de exemplo que demonstram o uso do codec DMOs diretamente estão incluídos na instalação do SDK do Windows Media Format juntamente com os cabeçalhos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o SDK do Windows Media Format**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




