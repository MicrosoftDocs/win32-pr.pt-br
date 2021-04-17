---
description: Criando pacotes de instalação para aplicativos COM+
ms.assetid: 3ef7b280-b521-4cd2-9906-013c9dfe16ab
title: Criando pacotes de instalação para aplicativos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ec34852ab405d965fa1ad8f8fb5892616d1347
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782643"
---
# <a name="creating-installation-packages-for-com-applications"></a>Criando pacotes de instalação para aplicativos COM+

Você pode usar a ferramenta administrativa serviços de componentes ou a biblioteca de administração COM+ para criar pacotes de instalação para aplicativos COM+ e proxies de aplicativo.

O COM+ gera Windows Installer pacotes de instalação, que em um único arquivo contém todas as partes necessárias para instalar um aplicativo COM+ em outro computador.

Ao exportar um aplicativo COM+, a ferramenta administrativa serviços de componentes determina o conjunto de classes, componentes e seus atributos do aplicativo, bem como atributos de nível de aplicativo. A partir dessas informações, a ferramenta administrativa serviços de componentes gera um único arquivo. msi, que contém o seguinte:

-   Windows Installer tabelas com informações de registro COM (consulte a documentação do Windows Installer para obter detalhes).
-   Um arquivo. gráfica que contém os atributos do aplicativo. (Esse é um arquivo interno; o formato desse arquivo não está documentado.)
-   DLLs e bibliotecas de tipos que descrevem as interfaces implementadas pelas classes do aplicativo COM+.

Além do arquivo. msi, a ferramenta administrativa serviços de componentes gera um arquivo de gabinete (. cab). Esse arquivo encapsula o arquivo. msi, permitindo que o desenvolvedor implante o aplicativo COM+ por meio do Microsoft Internet Explorer.

> [!Note]  
> Ao exportar um aplicativo COM+, a ferramenta administrativa serviços de componentes empacota apenas as partes COM+ padrão do aplicativo. Ele não empacota, por exemplo, quaisquer arquivos de dados ou DLL dependentes. Os arquivos DLL dependentes devem ser instalados primeiro em um computador antes da instalação do aplicativo COM+. Como alternativa, você pode usar a ferramenta de criação de Windows Installer para adicionar esses arquivos dependentes ao arquivo. msi gerado pela ferramenta administrativa serviços de componentes. (Consulte a documentação do Windows Installer para obter detalhes.)

 

## <a name="installing-com-applications-on-other-computers"></a>Instalando aplicativos COM+ em outros computadores

O arquivo de Windows Installer (. msi) gerado pela ferramenta administrativa serviços de componentes pode ser usado para instalar o aplicativo COM+ em outro computador. O arquivo. msi que contém um aplicativo COM+ pode ser instalado somente em computadores que dão suporte a serviços COM+. Para obter procedimentos detalhados sobre a implantação de aplicativos COM+, consulte "Instalando aplicativos COM+" na ajuda da administração de serviços de componentes.

A menos que o arquivo. msi seja modificado usando uma ferramenta de criação de Windows Installer, os aplicativos COM+ instalados usando o Windows Installer aparecem no painel de controle adicionar ou remover programas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Implantando proxies de aplicativo](deploying-application-proxies.md)
</dt> <dt>

[O catálogo COM+](the-com--catalog.md)
</dt> </dl>

 

 



