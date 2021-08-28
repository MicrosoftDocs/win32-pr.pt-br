---
description: Esta seção descreve as considerações para implantar seu aplicativo MUI para uso ideal pela lógica de carregamento do aplicativo e o carregador de recursos.
ms.assetid: 6c10b355-9bdd-4dba-8446-91034d4fe9b8
title: Implantação do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a85f297767c2b22fb8a3096f0df8ed21468ab710
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883517"
---
# <a name="application-deployment"></a>Implantação do aplicativo

Esta seção descreve as considerações para implantar seu aplicativo MUI para uso ideal pela lógica de carregamento do aplicativo e o carregador de recursos.

## <a name="packaging"></a>Empacotamento

o empacotamento do aplicativo depende do tipo de suporte de idioma fornecido, pois Windows instala os pacotes de idiomas com base nas preferências do usuário. Por exemplo, se você tiver decidido o suporte às configurações de idioma do sistema, talvez queira fornecer todo o suporte ao idioma em um único pacote, independentemente do usuário pretendido.

Se o aplicativo e os recursos forem grandes, você deverá usar um pacote por idioma com suporte. Por exemplo, você pode usar esse tipo de empacotamento se seu aplicativo estiver apresentando idiomas selecionáveis pelo usuário e o usuário precisar de adição dinâmica e remoção de recursos de idioma.

## <a name="file-placement-on-windows-vista-and-later"></a>posicionamento de arquivos no Windows Vista e posterior

esta seção descreve o posicionamento de arquivos para um aplicativo MUI direcionado apenas para o Windows Vista e posterior.

### <a name="place-the-ln-file"></a>Coloque o arquivo LN

Um arquivo LN típico para um aplicativo MUI é um arquivo .exe ou um arquivo .dll, por exemplo, BakerDelta.dll. Você deve posicionar esse arquivo na pasta raiz onde seu aplicativo está instalado, por exemplo, X: \\ \\ &lt; somepath &gt; \\BakerDelta.dll.

### <a name="place-language-specific-resource-files"></a>Coloque Language-Specific arquivos de recurso

Seus arquivos de recursos específicos de idioma devem ter nomes previsíveis formados acrescentando ". mui" ao nome completo do arquivo LN, por exemplo, BakerDelta.dll. mui. Esses arquivos devem ser colocados em subpastas nomeadas após os [nomes de idioma](language-names.md)apropriados. O exemplo a seguir mostra o posicionamento de recursos para o arquivo BakerDelta.dll LN, com arquivos de recursos específicos de idioma para inglês (Reino Unido), inglês (Estados Unidos), inglês neutro, espanhol (Espanha), espanhol (México) e espanhol neutro:

-   X: \\ \\ &lt; somepath &gt; \\BakerDelta.dll
-   X: \\ \\ &lt; somepath &gt; \\ en-GB \\BakerDelta.dll. mui
-   X: \\ \\ &lt; somepath &gt; \\ en-US \\BakerDelta.dll. mui
-   X: \\ \\ &lt; somepath &gt; \\ en \\BakerDelta.dll. mui
-   X: \\ \\ &lt; somepath &gt; \\ es-es \\BakerDelta.dll. mui
-   X: \\ \\ &lt; somepath &gt; \\ es-MX \\BakerDelta.dll. mui
-   X: \\ \\ &lt; somepath &gt; \\ es \\BakerDelta.dll. mui

Os arquivos de recursos devem ser colocados em seus locais corretos durante a instalação do aplicativo MUI ou de um pacote de idiomas. É importante posicionar cada arquivo na pasta correta, pois o carregador de recursos não pode operar corretamente de outra forma. Usando o exemplo acima, o carregador de recursos examina X: \\ &lt; somepath &gt; \\ en-US \\BakerDelta.dll. mui para recursos em inglês (Estados Unidos). Se o carregador examinar esse arquivo e encontrar apenas recursos em espanhol, ele falhará.

## <a name="file-placement-on-a-pre-windows-vista-operating-system"></a>posicionamento de arquivos em um sistema operacional Windows Vista anterior

um aplicativo a ser executado em um sistema operacional Windows vista anterior pode usar a convenção Windows vista de colocar arquivos de recursos específicos do idioma em pastas com base em nomes de idiomas. Como alternativa, o aplicativo pode estar em conformidade com uma convenção mais antiga que forma caminhos a partir de [identificadores de idioma](language-identifiers.md). Para aplicativos que oferecem suporte apenas a um único idioma, você pode apenas posicionar o arquivo de recursos específico do idioma no diretório raiz com o arquivo binário.

Por exemplo, considere um arquivo LN chamado BakerDelta.dll, com arquivos de recursos específicos de idioma para inglês (Reino Unido), inglês (Estados Unidos), inglês neutro, espanhol (Espanha), espanhol (México) e espanhol neutro. uma instalação em um sistema operacional Windows Vista anterior pode posicionar esses arquivos da seguinte maneira:

-   X: \\ \\ &lt; somepath &gt; \\BakerDelta.dll
-   X: \\ \\ &lt; somepath &gt; \\BakerDelta.dll. mui (arquivo. mui opcional contendo recursos no idioma do sistema operacional como o fallback final)
-   X: \\ \\ &lt; somepath &gt; \\ MUI \\ 0809 \\BakerDelta.dll. mui
-   X: \\ \\ &lt; somepath &gt; \\ MUI \\ 0409 \\BakerDelta.dll. mui
-   X: \\ \\ &lt; somepath &gt; \\ MUI \\ 0209 \\BakerDelta.dll. mui
-   X: \\ \\ &lt; somepath &gt; \\ MUI \\ 040A \\BakerDelta.dll. mui
-   X: \\ \\ &lt; somepath &gt; \\ MUI \\ 080a \\BakerDelta.dll. mui
-   X: \\ \\ &lt; somepath &gt; \\ MUI \\ 0209 \\BakerDelta.dll. mui

Além desses arquivos, o aplicativo pode configurar um arquivo de recursos específico do idioma de fallback final, para residir na mesma pasta que o próprio aplicativo. Para o exemplo acima, esse arquivo é X: \\ &lt; somepath &gt; \\BakerDelta.dll. mui.

## <a name="installation"></a>Instalação

A lógica de instalação para copiar e configurar arquivos de aplicativo depende dos idiomas com suporte e do local dos arquivos de recursos de idioma nos locais de instalação corretos. Um instalador deve instalar e configurar o aplicativo para que o usuário possa adicionar e remover idiomas facilmente.

Se o seu aplicativo simplesmente instalar o idioma do sistema operacional de destino, o instalador deverá detectar a interface do usuário do sistema operacional para determinar os recursos do aplicativo a serem instalados. Para dar suporte à melhor experiência do usuário, o instalador também deve detectar o idioma da interface do usuário para apresentar uma interface do usuário localizada para a própria instalação.

é recomendável usar Windows Installer (MSI) para criar o software de instalação. Os recursos associados devem ser incluídos no arquivo de recurso de idioma base, conforme descrito em [criando o arquivo de recurso de idioma base](creating-the-base-language-resource-file.md). para obter instruções sobre como usar o MSI para preparar o instalador do aplicativo, consulte [Windows Installer](../msi/windows-installer-portal.md).

## <a name="uninstall-program"></a>Programa de desinstalação

Você também pode querer fornecer um programa de desinstalação com seu aplicativo MUI. O MSI também é recomendado para a criação deste programa. para obter instruções sobre como usar o MSI para preparar o software de desinstalação, consulte [Windows Installer](../msi/windows-installer-portal.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[usando Interface de Usuário Multilíngue](using-multilingual-user-interface.md)
</dt> </dl>

 

 
