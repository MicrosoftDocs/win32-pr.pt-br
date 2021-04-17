---
description: Seu aplicativo globalizado deve definir uma variedade de elementos de interface do usuário, como menus, caixas de diálogo, cadeias de caracteres de ajuda e outros itens, representados como recursos localizados.
ms.assetid: 4d8b769d-0830-4e4e-b284-ce0b21dfe5d4
title: Gerenciamento de recursos do MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeed59c4b835e2c93e5f4cfc9988509349d8b0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757139"
---
# <a name="mui-resource-management"></a>Gerenciamento de recursos do MUI

Seu aplicativo globalizado deve definir uma variedade de elementos de interface do usuário, como menus, caixas de diálogo, cadeias de caracteres de ajuda e outros itens, representados como recursos localizados. O idioma da interface do usuário se torna uma das configurações para o aplicativo. Esta seção descreve a tecnologia de recursos do MUI, que recomendamos que você use para criar os recursos do aplicativo.

## <a name="features-of-the-mui-resource-technology"></a>Recursos da tecnologia de recursos do MUI

A tecnologia de recursos do MUI, exposta no Windows Vista e posterior, tem as seguintes características:

-   Os arquivos de recursos específicos do idioma são armazenados separadamente do binário do código do aplicativo, para que uma alteração de código não afete os recursos.
-   Os recursos para vários idiomas podem ser implantados em uma única instalação ou em instalações separadas para cada idioma.
-   Um recurso é carregado e exibido de acordo com o idioma do aplicativo, conforme definido pelo usuário.

Essa tecnologia associa os recursos definidos em arquivos específicos de idioma a uma versão específica de um arquivo de idioma neutro (LN). O arquivo LN é um arquivo PE do Win32 que representa o binário do código do aplicativo e os recursos neutros à linguagem. A associação de arquivos usa uma soma de verificação refletida nos dados de configuração de recursos contidos em todos os arquivos associados. O carregador de recursos usa a soma de verificação para verificar se os arquivos contêm a mesma versão dos recursos necessários. Ele também valida o idioma no arquivo específico do idioma com seu nome de pasta. O carregador não carregará um arquivo de recurso se a associação apropriada não for estabelecida.

Especificamente, a soma de verificação principal é calculada a partir dos números de versão principal e secundária de um arquivo e do nome do arquivo (diferencia maiúsculas de minúsculas), que são obtidos do recurso de versão. Essa soma de verificação não deve ser alterada entre versões RTM e service pack do mesmo componente. Além disso, uma soma de verificação de serviço é usada para determinar a versão apropriada do arquivo de recursos específico do idioma a ser carregado. Essa soma de verificação é calculada com base nos recursos localizáveis no arquivo.

O MUI fornece dois utilitários de recursos que você pode usar para preparar arquivos de recursos para seu aplicativo. Um utilitário específico do MUI, chamado MUIRCT, permite que você crie um arquivo LN e arquivos de recursos específicos de idioma associados. No Windows Vista e posterior, o compilador do Windows RC também foi modificado para compilar esses arquivos de acordo com a tecnologia de recursos do MUI. Para obter a sintaxe e os detalhes dessas ferramentas, consulte [utilitários de recursos](resource-utilities.md).

## <a name="ln-file"></a>Arquivo LN

O arquivo LN de um aplicativo MUI contém código executável e recursos neutros por idioma que são compartilhados e instalados por todas as versões de idioma do aplicativo.

## <a name="language-specific-resource-file"></a>Language-Specific arquivo de recurso

Um arquivo de recurso específico de idioma normalmente contém cadeias de caracteres de interface do usuário e outros elementos que exigem localização para um idioma específico. Seu aplicativo MUI usa um arquivo de recurso específico de idioma por idioma com suporte. O arquivo LN para o aplicativo é o mesmo para cada arquivo de recurso específico do idioma.

Quando criado usando a tecnologia de recursos do MUI, os arquivos específicos do idioma têm uma extensão ". mui" e são tratados da seguinte maneira:

-   Os arquivos específicos de idioma associados a um determinado arquivo LN compartilham o mesmo nome de arquivo, que é formado pela adição da extensão ". mui" ao nome de arquivo completo (com extensão) do arquivo LN correspondente. Por exemplo, um arquivo LN chamado "Myfile.dll" tem arquivos específicos de idioma denominados "Myfile.dll. mui".
-   Os arquivos específicos do idioma residem em subpastas da pasta que contém o arquivo LN. Cada nome de pasta reflete o idioma.

## <a name="resource-configuration-data"></a>Dados de configuração de recurso

Para associar um arquivo LN a seus arquivos específicos de idioma, a tecnologia de recursos de MUI usa dados de configuração de recursos, incluindo a soma de verificação. O procedimento de compilação de recurso coloca essas informações em uma seção de configuração RC de cada arquivo específico do LN e do idioma. Uma forma legível dessas informações está disponível por meio do utilitário MUIRCT. Para obter mais informações, consulte [utilitários de recursos](resource-utilities.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a interface do usuário multilíngue](about-multilingual-user-interface.md)
</dt> <dt>

[Utilitários de recursos](resource-utilities.md)
</dt> </dl>

 

 



