---
description: Um patch Windows Installer (arquivo. msp) é um arquivo usado para fornecer atualizações para Windows Installer aplicativos.
ms.assetid: f59736d7-0b5a-466c-ab60-f210ccccb07f
title: Pacotes de patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56b4bb5b7e182c8118f5a40c45be440784b92099
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661909"
---
# <a name="patch-packages"></a>Pacotes de patch

Um patch Windows Installer (arquivo. msp) é um arquivo usado para fornecer atualizações para Windows Installer aplicativos. O patch é um pacote independente que contém todas as informações necessárias para atualizar o aplicativo. Um pacote de patch (arquivo. msp) pode ser muito menor do que o pacote de Windows Installer (arquivo. msi) para todo o aplicativo atualizado. Para obter mais informações sobre como fornecer atualizações menores aos aplicativos, consulte [reduzindo o tamanho do patch](reducing-patch-size.md).

Um pacote de patch contém as atualizações reais para o aplicativo e descreve quais versões do aplicativo podem receber o patch. Os patches contêm no mínimo duas transformações de banco de dados. Uma transformação atualiza as informações no banco de dados de instalação do aplicativo. A outra transformação adiciona informações que o instalador usa para aplicar patches em arquivos. O instalador usa as informações fornecidas pelas transformações para aplicar arquivos de patch que são armazenados no fluxo de arquivos de gabinete do pacote de patch. Um pacote de patch não tem um banco de dados como um pacote de instalação (arquivo. msi).

A partir do Windows Installer versão 3,0, os pacotes de patch podem conter informações que descrevem a sequência de patches para o patch em relação a outras atualizações na tabela [MsiPatchSequence](msipatchsequence-table.md) e informações descritivas adicionais na tabela [MsiPatchMetaData](msipatchmetadata-table.md) .

Os usuários podem instalar aplicativos e atualizações de uma imagem administrativa de rede. Embora os pacotes de patch possam ser aplicados a instalações administrativas, o método recomendado para fornecer atualizações é fazer com que os usuários instalem o aplicativo original e, em seguida, apliquem os patches à instância local do aplicativo em seu computador. Isso mantém os usuários em sincronia com a imagem administrativa. Se um patch for aplicado à instalação administrativa, todos os clientes da instalação administrativa deverão rearmazenar em cache e reinstalar o aplicativo para receber a atualização. Até que um usuário rearmazene novamente em cache e reinstale o, o usuário não poderá instalar o sob demanda e reparar as instalações da instalação administrativa corrigida.

A partir do Windows Installer 3,0, os não administradores podem aplicar patches a aplicativos gerenciados por usuário depois que o patch foi aprovado como confiável por um administrador. Para obter mais informações sobre como fazer isso, consulte [aplicação de patches Per-User aplicativos gerenciados](patching-per-user-managed-applications.md). Outro método é usar a aplicação de patch de conta de usuário com privilégios mínimos.

> [!Note]  
> Se a política [AllowLockdownPatch](allowlockdownpatch.md) tiver sido definida, os usuários não administradores poderão aplicar um patch a um aplicativo existente durante a execução de uma instalação em privilégios elevados. Esse método não é recomendado porque permite que patches não confiáveis sejam aplicados a um aplicativo que pode ser executado com privilégios elevados.

 

Os pacotes de patches são compostos pelas seguintes partes. Para obter mais informações sobre a construção de pacotes de patch, consulte [criando um pacote de patch](creating-a-patch-package.md).

## <a name="summary-information-stream"></a>Fluxo de informações de resumo

O fluxo de informações resumidas do pacote de patch fornece informações sobre a identidade e a finalidade do patch.

O fluxo de informações de resumo mantém um mínimo dos seguintes:

-   Um GUID que identifica exclusivamente o patch. O GUID desse patch é acrescentado com uma lista de GUIDs para patches anteriores que são substituídos por esse patch.
-   Uma lista delimitada por ponto-e-vírgula de códigos de produto para destinos válidos para este patch.
-   Uma lista delimitada por ponto-e-vírgula dos nomes de subarmazenamento de transformação na ordem em que eles devem ser processados.
-   Uma lista delimitada por ponto-e-vírgula de fontes para este patch.

## <a name="transform-substorage"></a>Transformar subarmazenamento

Um pacote de patch contém transformações que podem adicionar ou remover arquivos, entradas de registro, interfaces do usuário e personalizações. As transformações são incluídas como subarmazenamentos no pacote. Um pacote de patch contém duas transformações para cada banco de dados de destino. Uma transformação são as atualizações reais do banco de dados de instalação e são geradas com base nas diferenças entre as imagens originais e atualizadas do pacote de instalação. A outra transformação adiciona entradas às tabelas [patch](patch-table.md), [PatchPackage](patchpackage-table.md), [Media](media-table.md), [InstallExecuteSequence](installexecutesequence-table.md)e [AdminExecuteSequence](adminexecutesequence-table.md) . As informações no subarmazenamento o vincula a um [**UpgradeCode**](upgradecode.md), [**ProductCode**](productcode.md), [**ProductVersion**](productversion.md)e [**ProductLanguage**](productlanguage.md)específicos. Um pacote de patch que pode ser aplicado a vários destinos contém mais de um par dessas transformações.

## <a name="cabinet-file-stream"></a>Fluxo do arquivo de gabinete

O fluxo de arquivo de gabinete incluído em um patch pode conter estes tipos de arquivos:

-   Arquivos de patch que contêm as informações necessárias para alterar a versão antiga do arquivo para a nova versão. Um único arquivo de patch pode ser usado para atualizar uma ou mais versões antigas de um arquivo.
-   Arquivos adicionais sendo adicionados ao aplicativo que não estão presentes na versão antiga.
-   Um arquivo de substituição inteiro. No caso raro em que a nova versão de um arquivo seja menor do que o patch necessário para atualizar a versão antiga desse arquivo, o novo arquivo pode ser incluído em sua totalidade. Esses são arquivos novos que são instalados em suas versões antigas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um pacote de patch](creating-a-patch-package.md)
</dt> </dl>

 

 



