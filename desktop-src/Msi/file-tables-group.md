---
description: o grupo de arquivos de tabelas contém todas as tabelas de Windows Installer relacionadas aos arquivos.
ms.assetid: 8f56328e-ed58-41a1-94b6-266e9c117246
title: Grupo de tabelas de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f8a73aa46b202d184356c14ff12da9ce9ce9880b009418e922b252cc35bc54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142896"
---
# <a name="file-tables-group"></a>Grupo de tabelas de arquivos

![grupo de tabelas de arquivos](images/filegrp.png)

Para obter mais informações sobre este diagrama, consulte a [legenda do diagrama de relação de entidade](entity-relationship-diagram-legend.md).

Um desenvolvedor de pacote do instalador deve considerar popular o grupo de tabelas de arquivos depois de dividir o aplicativo em [componentes e recursos](components-and-features.md) e depois de preencher o [grupo de tabelas principais](core-tables-group.md). O grupo de tabelas de arquivos contém todos os arquivos que pertencem à instalação e a maioria desses arquivos é listada na [tabela de arquivos](file-table.md). A [tabela de diretórios](directory-table.md) não é mostrada na figura, mas está fortemente relacionada ao grupo de tabelas de arquivos. A tabela de diretórios fornece a estrutura de diretório da instalação do.

O grupo de arquivos de tabelas contém todas as tabelas relacionadas aos arquivos.

-   A [tabela de arquivos](file-table.md) lista os arquivos que pertencem à instalação. Os arquivos que não estão listados na tabela de arquivos incluem arquivos de disco, que são listados na tabela de mídia. Como cada arquivo pertence a um componente, a tabela de arquivos tem uma chave externa na tabela de componentes.
-   A [tabela RemoveFile](removefile-table.md) contém uma lista de arquivos a serem removidos pela [ação](removefiles-action.md)removidas.
-   A [tabela de fontes](font-table.md) lista os arquivos de fonte a serem registrados com o sistema.
-   A [tabela selfreg](selfreg-table.md) lista os arquivos de módulo da instalação autoregistrada.
-   A [tabela de mídia](media-table.md) lista a mídia de origem e os discos que pertencem à instalação.
-   A [tabela BindImage](bindimage-table.md) lista os arquivos que estão associados a DLLs importadas por executáveis.
-   A [tabela MoveFile](movefile-table.md) especifica quais arquivos são movidos durante a instalação.
-   A [tabela replicafile](duplicatefile-table.md) especifica quais arquivos são duplicados durante a instalação.
-   A [tabela inifile](inifile-table.md) lista os arquivos de .ini e as informações que o aplicativo precisa definir no arquivo.
-   A [tabela RemoveIniFile](removeinifile-table.md) contém as informações que um aplicativo precisa excluir de um arquivo .ini.
-   A [tabela de ambiente](environment-table.md) é usada para definir os valores de variáveis de ambiente.
-   A [tabela de ícones](icon-table.md) fornece informações de ícone que são copiadas para um arquivo como parte do anúncio do produto.
-   A [tabela FileSFPCatalog](filesfpcatalog-table.md) associa arquivos especificados a arquivos de catálogo de proteção de arquivo do sistema.

    **Windows Vista, Windows Server 2003 e Windows XP:** Sem suporte.

-   A [tabela SFPCatalog](sfpcatalog-table.md) contém catálogos de proteção de arquivo do sistema.

    **Windows Vista, Windows Server 2003 e Windows XP:** Sem suporte.

-   a [tabela MsiFileHash](msifilehash-table.md) é usada para armazenar um hash de 128 bits de um arquivo de origem fornecido pelo pacote de Windows Installer.

 

 



