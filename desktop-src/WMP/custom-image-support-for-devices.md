---
title: Suporte a imagens personalizadas para dispositivos
description: Suporte a imagens personalizadas para dispositivos
ms.assetid: 0ccc327c-e953-4348-9802-705331b574ac
keywords:
- Windows Media Player, suporte a imagens personalizadas para dispositivos
- Windows Media Player, suporte a imagens para dispositivos
- suporte a imagens personalizadas do dispositivo
- suporte a imagens personalizadas para dispositivos
- suporte a imagens para dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ffdf318df39935e844cc84919bb4d6e50cc259a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105761473"
---
# <a name="custom-image-support-for-devices"></a>Suporte a imagens personalizadas para dispositivos

> [!Note]  
> Esta seção documenta um recurso do Windows Media Player 10 que está disponível ao usar o sistema operacional Windows XP. Ele pode não estar disponível em versões subsequentes.

 

Os fabricantes de dispositivos podem fornecer dois arquivos de imagem especiais para personalizar a maneira como um dispositivo é representado na interface do usuário do Windows Media Player 10. Esses dois arquivos são:

-   DevIcon. fil. Um arquivo de formato de ícone do Windows que representa o hardware do dispositivo. Essa imagem é exibida no Windows Media Player 10 em qualquer lugar em que um ícone é usado para representar um dispositivo, como a lista de dispositivos no recurso de **sincronização** .
-   Devlog. fil. Um arquivo de formato PNG que representa o logotipo corporativo do fabricante do dispositivo. Essa imagem é exibida no Windows Media Player 10 em qualquer lugar da identidade visual corporativa que é usada, como a caixa de diálogo **configuração do dispositivo** .

## <a name="general-guidelines-for-images"></a>Diretrizes gerais para imagens

As diretrizes a seguir se aplicam ao suporte de imagem personalizada em geral:

-   Esse recurso é opcional. Os dispositivos que não fornecem imagens serão representados por imagens padrão.
-   Esse recurso tem suporte somente para dispositivos habilitados para MTP.
-   Para evitar alterações nos arquivos, é recomendável que os arquivos de imagem sejam armazenados no firmware ou em um meio de armazenamento protegido, não com arquivos criados pelo usuário.
-   Os arquivos não devem ser retornados para os clientes do Windows Media Gerenciador de Dispositivos que enumeram o armazenamento raiz do dispositivo. Além disso, excluir, mover ou renomear os arquivos deve falhar.
-   Se o dispositivo fornecer mais de um meio de armazenamento, o dispositivo deverá retornar os arquivos de imagem em resposta às solicitações de abertura de arquivo de qualquer meio. Ícones de dispositivo diferentes podem ser retornados de cada meio de armazenamento.
-   Para clientes habilitados para Windows Media Gerenciador de Dispositivos 1,2, essas imagens terão precedência sobre as propriedades de ícone fornecidas pelos mecanismos de instalação do Windows, como propriedades do nó do dispositivo.
-   As imagens não devem conter nenhuma informação que exija localização.
-   Para dispositivos com várias funções, somente os recursos de reprodução de música do Windows XP usarão essas imagens.

## <a name="creating-the-device-icon-image"></a>Criando a imagem de ícone do dispositivo

O arquivo de imagem do ícone do dispositivo, DevIcon. Fil, deve conter um arquivo no formato de ícone do Windows. Os ícones de artigo [do MSDN no Win32](/previous-versions/ms997538(v=msdn.10)) descrevem como criar um arquivo desse tipo. O artigo do MSDN [criando ícones do Windows XP](/previous-versions/ms997636(v=msdn.10)) fornece diretrizes de estilo para ícones do Windows XP. O arquivo de imagem do ícone do dispositivo incorpora doze imagens em um único arquivo, fornecendo quatro tamanhos diferentes com três profundidades de cor diferentes cada.

Certifique-se de prestar atenção especial às seguintes diretrizes:

-   Os tamanhos recomendados (em pixels) são 16x16, 32x32, 48x48 e 256x256.
-   As profundidades de cor recomendadas são de 24 bits com canal alfa de 8 bits, 8 bits com transparência de 1 bit e 4 bits com transparência de 1 bit.
-   Use o ângulo de perspectiva e as recomendações de sombra descritas nos artigos do MSDN mencionados anteriormente.

Depois de criar o arquivo de ícone, basta renomeá-lo DevIcon. fil.

## <a name="creating-the-corporate-logo-image"></a>Criando a imagem do logotipo corporativo

O arquivo de imagem de logotipo corporativo, devlogo. Fil, deve conter um arquivo no formato PNG. Use as seguintes diretrizes ao criar a imagem:

-   As dimensões máximas para a imagem são 150x32 pixels.
-   A imagem deve dar suporte à mesclagem alfa para habilitar uma transição suave entre a interface do usuário do Windows Media Player 10 e o logotipo.

Depois de criar o arquivo de logotipo corporativo, basta renomeá-lo como desvlogo. fil.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 