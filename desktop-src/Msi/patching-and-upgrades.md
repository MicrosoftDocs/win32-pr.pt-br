---
description: Como um pacote de instalação pode conter os arquivos que compõem um aplicativo, bem como as informações necessárias para sua instalação, Windows Installer pode ser usado para atualizar o aplicativo.
ms.assetid: da946739-9efc-4bf0-8a9a-6f6ead3c4a34
title: Aplicação de patch e atualizações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8cee185461ac14c8eac336a5af0c1315eb5e027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921781"
---
# <a name="patching-and-upgrades"></a>Aplicação de patch e atualizações

Como um pacote de instalação pode conter os arquivos que compõem um aplicativo, bem como as informações necessárias para sua instalação, Windows Installer pode ser usado para atualizar o aplicativo. O instalador pode atualizar as informações nas seguintes partes do pacote de instalação:

-   O arquivo. msi.
-   Os arquivos do aplicativo.
-   As informações de registro de Windows Installer.

O tipo de atualização pode ser caracterizado pelas alterações que a atualização faz no código do produto, versão do produto e código do pacote do aplicativo. A versão do produto do aplicativo é armazenada na propriedade [**ProductVersion**](productversion.md) . O código do produto do aplicativo é armazenado na propriedade [**ProductCode**](productcode.md) . O código do [pacote](package-codes.md) do aplicativo é armazenado na propriedade [**Summary do número de revisão**](revision-number-summary.md) .

Uma atualização que altera o aplicativo para outro produto é necessária para alterar o [**ProductCode**](productcode.md) do aplicativo. Para obter mais informações sobre quais atualizações exigem a alteração do **ProductCode** , consulte [alterando o código do produto](changing-the-product-code.md). A atualização pode alterar o [**ProductVersion**](productversion.md) e deixar o **ProductCode** inalterado se versões futuras do aplicativo precisarem diferenciar entre as versões atualizadas e não atualizáveis do produto atual. O [código do pacote](package-codes.md) identifica exclusivamente o pacote de instalação e deve ser sempre alterado sempre que a atualização ou atualização altera qualquer informação no pacote de instalação.

Ao decidir se deseja alterar a versão do produto, você deve considerar se as versões futuras do aplicativo precisarão diferenciar entre as versões atualizadas e não atualizáveis do produto atual. Para garantir a diferenciação no futuro, uma [atualização secundária](minor-upgrades.md) deve ser usada em vez de uma [pequena atualização](small-updates.md).

-   Se uma atualização alterar o arquivo. msi e os arquivos de aplicativo, mas não alterar a propriedade [**ProductCode**](productcode.md) ou a propriedade [**ProductVersion**](productversion.md) , será chamada de uma [pequena atualização](small-updates.md).
-   Se a atualização alterar o [**ProductVersion**](productversion.md), mas não alterar o [**ProductCode**](productcode.md), será chamada de uma [pequena atualização](minor-upgrades.md).
-   Se a atualização alterar a instalação para um produto totalmente diferente, o [**ProductCode**](productcode.md) deverá ser alterado e a atualização será chamada de [atualização principal](major-upgrades.md).

> [!Note]  
> Para garantir a diferenciação das versões do produto atual no futuro, uma [atualização secundária](minor-upgrades.md) deve ser usada em vez de uma [pequena atualização](small-updates.md).

 

A tabela a seguir resume os diferentes tipos de atualizações.



| Tipo de atualização                       | ProductCode | ProductVersion | Descrição                                                                                                                                                                                                                                                                                                           |
|--------------------------------------|-------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Pequena atualização](small-updates.md)    | Nenhuma alteração   | Nenhuma alteração      | Uma atualização para um ou dois arquivos que é muito pequeno para garantir a alteração do [**ProductVersion**](productversion.md). O código do pacote na propriedade [**Resumo do número de revisão**](revision-number-summary.md) é alterado. Pode ser enviado como um pacote de instalação completo ou como um [pacote de patch](patch-packages.md). |
| [Atualização secundária](minor-upgrades.md)  | Nenhuma alteração   | Alterado        | Uma pequena atualização que torna as alterações significativas o suficiente para garantir a alteração da propriedade [**ProductVersion**](productversion.md) . Pode ser enviado como um pacote de instalação completo ou como um [pacote de patch](patch-packages.md).                                                                                                |
| [Principais atualizações](major-upgrades.md) | Alterado     | Alterado        | Uma atualização abrangente do produto que garante uma alteração na propriedade [**ProductCode**](productcode.md) . Fornecido como um [pacote de patch](patch-packages.md) ou como um pacote de instalação de produto completo.                                                                                                             |



 

> [!Note]  
> O Windows Installer pode instalar um aplicativo, ou uma atualização, para todos os usuários de um computador (contexto por computador) ou para um usuário específico (contexto por usuário), dependendo dos privilégios de acesso do usuário, do valor da propriedade [**AllUsers**](allusers.md) e da versão do sistema operacional. Os desenvolvedores de aplicativos devem considerar em quais atualizações de contexto serão instaladas. Se os contextos do aplicativo e da atualização forem diferentes, o aplicativo poderá não ser atualizado conforme o esperado.

 

Os usuários podem atualizar para um aplicativo reinstalando um pacote de Windows Installer para o aplicativo. Observe que as atualizações [secundárias](minor-upgrades.md) podem ser aplicadas da mesma maneira que [as pequenas atualizações](small-updates.md). Para obter mais informações sobre como atualizar um aplicativo reinstalando o aplicativo, consulte estas seções:

-   [Aplicando pequenas atualizações reinstalando o produto](applying-small-updates-by-reinstalling-the-product.md)
-   [Aplicando as principais atualizações instalando o produto](applying-major-upgrades-by-installing-the-product.md)

Uma atualização para um aplicativo pode ser fornecida aos usuários como um pacote de patch Windows Installer. Um patch pode conter um arquivo inteiro ou apenas os bits de arquivo necessários para atualizar parte de um arquivo. Isso significa que o usuário pode baixar um patch de atualização muito menor do que o produto inteiro e que preserva as personalizações do usuário por meio da atualização. Observe que as atualizações [secundárias](minor-upgrades.md) podem ser aplicadas da mesma maneira que [as pequenas atualizações](small-updates.md). Para obter mais informações sobre como atualizar um aplicativo usando um patch, consulte estas seções:

-   [Aplicação de patch](patching.md)
-   [Criando um patch de atualização pequena](creating-a-small-update-patch.md)
-   [Aplicando pequenas atualizações por meio da aplicação de patch na instalação local do produto](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
-   [Aplicando pequenas atualizações por meio da aplicação de patch em uma imagem administrativa](applying-small-updates-by-patching-an-administrative-image.md)
-   [Aplicando as principais atualizações por meio da aplicação de patch na instalação local do produto](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)

 

 



