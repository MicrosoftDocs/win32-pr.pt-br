---
description: Ao instalar um codec, você deve registrá-lo no registro. Você também deve verificar se o cache de miniaturas é atualizado caso já existam imagens no seu formato no computador.
ms.assetid: 7aec54cb-40ac-495c-99d9-9c397b740b21
title: Instalação e registro de codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83616071bebdbab14bfdc7dd0f879df3d49789d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797653"
---
# <a name="codec-installation-and-registration"></a>Instalação e registro de codec

Ao instalar um codec, você deve registrá-lo no registro. Você também deve verificar se o cache de miniaturas é atualizado caso já existam imagens no seu formato no computador.

Este tópico contém as seguintes seções:

-   [Registrando um codec](#registering-a-codec)
-   [Atualizando o cache de miniaturas ao instalar o codec](#updating-the-thumbnail-cache-when-installing-your-codec)
-   [Disponibilizando o codec WIC-Enabled para os usuários](#making-your-wic-enabled-codec-available-to-users)
-   [Tópicos relacionados](#related-topics)

## <a name="registering-a-codec"></a>Registrando um codec

Ao registrar um codec, na verdade você está registrando dois componentes: o codificador e o decodificador. Você também precisa fazer entradas do registro para registrar seu formato de contêiner com os manipuladores de metadados para os formatos de metadados aos quais o formato de imagem dá suporte.

Os tópicos a seguir descrevem as entradas de Registro necessárias para registrar seu Codec:

[Entradas gerais do registro](-wic-generalregentries.md)

[Entradas de registro específicas do codificador](-wic-encoderregentries.md)

[Entradas de registro específicas do decodificador](-wic-decoderregentries.md)

[Integração com a Galeria de fotos do Windows e o Windows Explorer](-wic-integrationregentries.md)

## <a name="updating-the-thumbnail-cache-when-installing-your-codec"></a>Atualizando o cache de miniaturas ao instalar o codec

Quando um codec é instalado, o instalador precisa chamar a função a seguir depois de gravar suas entradas de registro.


```C++
SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_IDLIST, NULL, NULL)
```



Essa chamada notifica o Windows de que novas informações de associação de arquivo estão disponíveis. Se as imagens no seu formato de imagem já existirem no computador, o cache de miniaturas conterá miniaturas padrão para elas, pois nenhum decodificador estava disponível para extrair as miniaturas quando as imagens foram adquiridas pela primeira vez. Quando você notifica o Windows de que uma nova associação de arquivo está disponível, o cache em miniatura descarta todas as miniaturas vazias e extrai as miniaturas reais dos arquivos que agora podem ser decodificados.

## <a name="making-your-wic-enabled-codec-available-to-users"></a>Disponibilizando o codec WIC-Enabled para os usuários

Se você for um fabricante de câmera, poderá enviar seus codecs brutos na caixa com suas câmeras. Você também pode postar seus codecs na página de download do seu site da Web. No entanto, se um usuário adquire um arquivo de imagem em seu formato de alguma outra fonte, como um amigo, um associado comercial ou algum outro site, talvez não saiba onde obter o codec para decodificá-lo.

Devido a esse problema, o Windows oferece uma maneira mais fácil para os usuários do seu formato de imagem localizarem seu codec e baixá-lo em seu computador, começando com o Windows Vista. Se a Galeria de fotos do Windows reconhecer uma extensão de nome de arquivo como um formato de imagem e o codec para esse formato não estiver instalado, uma caixa de diálogo informa ao usuário que a foto não pode ser exibida e pergunta se o usuário deseja baixar o software necessário para exibi-lo. Quando o usuário aceita, um site hospedado pela Microsoft é exibido com um link para o site de download do fabricante do codec. (Opcionalmente, você pode solicitar que os usuários sejam levados diretamente ao seu site de download.)

Se desejar que as extensões de nome de arquivo do formato de imagem sejam reconhecidas pela galeria de fotos do Windows para que os usuários possam ser direcionados para o site de download, você deverá fazer o seguinte:

1.  Forneça um site de download para seu codec. (Você pode ter uma página separada para cada codec que fornecer ou uma página que forneça downloads para todos os seus codecs.)

    O site de download deve ser localizado e facilmente pesquisável por modelo de câmera.

2.  Forneça à Microsoft uma lista de extensões para seus formatos de imagem e as URLs para seus sites de download.

Você deve informar à Microsoft sobre as extensões para quaisquer novos codecs desenvolvidas no futuro e de quaisquer alterações nas URLs de seus sites de download, para que as novas informações possam ser adicionadas à galeria de fotos do Windows.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Implementando IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[Conclusão (como escrever um CODEC de WIC-Enabled)](-wic-howtowriteacodec-conclusion.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



