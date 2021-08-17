---
description: Ao instalar um codec, você deve registrá-lo no Registro. Você também deve garantir que o cache em miniatura seja atualizado caso alguma imagem no formato já exista no computador.
ms.assetid: 7aec54cb-40ac-495c-99d9-9c397b740b21
title: Instalação e registro do Codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc13a2d937e82eae3517b9b20440f4acbb10b16af3fa0b872eb0ddd6c2a8d6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965175"
---
# <a name="codec-installation-and-registration"></a>Instalação e registro do Codec

Ao instalar um codec, você deve registrá-lo no Registro. Você também deve garantir que o cache em miniatura seja atualizado caso alguma imagem no formato já exista no computador.

Este tópico contém as seguintes seções:

-   [Registrando um Codec](#registering-a-codec)
-   [Atualizando o cache em miniatura ao instalar o codec](#updating-the-thumbnail-cache-when-installing-your-codec)
-   [Disponibilizando seu WIC-Enabled codec para os usuários](#making-your-wic-enabled-codec-available-to-users)
-   [Tópicos relacionados](#related-topics)

## <a name="registering-a-codec"></a>Registrando um Codec

Ao registrar um codec, na verdade, você está registrando dois componentes: o codificador e o decodificador. Você também precisa fazer entradas do Registro para registrar seu formato de contêiner com os manipuladores de metadados para os formatos de metadados que o formato de imagem dá suporte.

Os tópicos a seguir descrevem as entradas do Registro que você precisa para registrar seu codec:

[Entradas gerais do Registro](-wic-generalregentries.md)

[Entradas do Registro específicas do codificador](-wic-encoderregentries.md)

[Entradas do Registro específicas do decodificador](-wic-decoderregentries.md)

[Integração com Windows Galeria de Fotos e Windows Explorer](-wic-integrationregentries.md)

## <a name="updating-the-thumbnail-cache-when-installing-your-codec"></a>Atualizando o cache em miniatura ao instalar o codec

Quando um codec é instalado, o instalador precisa chamar a função a seguir depois de escrever suas entradas do Registro.


```C++
SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_IDLIST, NULL, NULL)
```



Essa chamada notifica Windows novas informações de associação de arquivo estão disponíveis. Se as imagens no formato de imagem já existirem no computador, o cache em miniatura conterá miniaturas padrão para elas porque nenhum decodificador estava disponível para extrair as miniaturas quando as imagens foram adquiridas pela primeira vez. Quando você notifica Windows que uma nova associação de arquivo está disponível, o cache em miniatura descarta todas as miniaturas vazias e extrai as miniaturas reais dos arquivos que agora podem ser decodificados.

## <a name="making-your-wic-enabled-codec-available-to-users"></a>Disponibilizando seu WIC-Enabled codec para os usuários

Se você for um fabricante de câmeras, poderá enviar seus codecs brutos na caixa com suas câmeras. Você também pode postar seus codecs na página Baixar do seu site. No entanto, se um usuário adquirir um arquivo de imagem em seu formato de alguma outra fonte, como um amigo, associado comercial ou algum outro site da Web, talvez ele não saiba com onde obter o codec com o qual decodificá-lo.

Devido a esse problema, o Windows oferece uma maneira mais fácil para os usuários do formato de imagem encontrarem seu codec e baixá-lo no computador, começando com o Windows Vista. Se o Windows Galeria de Fotos reconhecer uma extensão de nome de arquivo como um formato de imagem e o codec desse formato não estiver instalado, uma caixa de diálogo informa ao usuário que a foto não pode ser exibida e pergunta se o usuário deseja baixar o software necessário para exibi-la. Quando o usuário aceita, um site hospedado pela Microsoft é exibido com um link para o site de download do fabricante do codec. (Opcionalmente, você pode solicitar que os usuários sejam levados diretamente para seu site de download.)

Se você quiser que as extensões de nome de arquivo do formato de imagem sejam reconhecidas pelo Windows Galeria de Fotos para que os usuários possam ser direcionados para o site de download, faça o seguinte:

1.  Forneça um site de download para seu codec. (Você pode ter uma página separada para cada codec que fornecer ou uma página que forneça downloads para todos os seus codecs.)

    O site de download deve ser localizado e facilmente pesquisável pelo modelo de câmera.

2.  Forneça à Microsoft uma lista de extensões para seus formatos de imagem e as URLs para seus sites de download.

Você deve informar a Microsoft sobre as extensões para quaisquer novos codecs que você desenvolver no futuro e sobre as alterações nas URLs de seus sites de download, para que as novas informações possam ser adicionadas ao Windows Galeria de Fotos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Implementando IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[Conclusão (Como escrever uma WIC-Enabled CODEC)](-wic-howtowriteacodec-conclusion.md)
</dt> <dt>

[Como escrever um codec WIC-Enabled código](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Visão geral do componente de imagens](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



