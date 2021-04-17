---
description: O hash de arquivo está disponível com Windows Installer. Para obter mais informações, consulte MsiGetFileHash e a tabela MsiFileHash. A tabela MsiFileHash só pode ser usada com arquivos sem versão.
ms.assetid: 608859ac-6640-4c28-b4f0-34ab36d804d7
title: Nenhum arquivo tem uma versão com verificação de hash de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415019838ac29418b13b513b393a18af2131510f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502362"
---
# <a name="neither-file-has-a-version-with-file-hash-check"></a>Nenhum arquivo tem uma versão com verificação de hash de arquivo

O hash de arquivo está disponível com Windows Installer. Para obter mais informações, consulte [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) e a [tabela MsiFileHash](msifilehash-table.md). A tabela MsiFileHash só pode ser usada com arquivos sem versão.

Se o arquivo de chave de um componente que está sendo instalado (cópia-A) tiver o mesmo nome que um arquivo já instalado no local de destino (cópia-B), o instalador compara o número de versão, a data e o idioma dos dois arquivos.

Se nenhum arquivo tiver um número de versão, o instalador usará a lógica ilustrada pelo seguinte diagrama de fluxo para determinar se todos os arquivos instalados pertencentes ao componente devem ser substituídos. Como o instalador instala apenas componentes inteiros, se o arquivo de chave instalado for substituído, todos os arquivos do componente serão substituídos.

Observe que este diagrama ilustra as [regras de controle de versão de arquivo](file-versioning-rules.md)padrão, que podem ser substituídas definindo a propriedade [**REINSTALLMODE**](reinstallmode.md) . O valor padrão da propriedade **REinstallmode** é "omus".

![regras de controle de versão de arquivo padrão quando substituídas pela configuração da propriedade REINSTALLMODE](images/waiflow2b.png)

Consulte os exemplos de controle de versão de arquivo padrão em [substituindo arquivos existentes](replacing-existing-files.md).

-   [Ambos os arquivos têm uma versão](both-files-have-a-version.md)
-   [Nenhum arquivo tem uma versão](neither-file-has-a-version.md)
-   [Um arquivo tem uma versão](one-file-has-a-version.md)

 

 



