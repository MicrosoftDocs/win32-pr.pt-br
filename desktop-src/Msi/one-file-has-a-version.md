---
description: Se apenas um dos arquivos tiver um número de versão, o Windows Installer usará a lógica ilustrada pelo seguinte diagrama de fluxo para determinar se todos os arquivos instalados pertencentes ao componente devem ser substituídos.
ms.assetid: 1eda5521-6e23-49b8-9870-f5370def487e
title: Um arquivo tem uma versão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417060119f8b13b1545161faa80552c79e8ca9aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090938"
---
# <a name="one-file-has-a-version"></a>Um arquivo tem uma versão

Se o arquivo de chave de um componente que está sendo instalado (cópia-A) tiver o mesmo nome que um arquivo já instalado no local de destino (cópia-B), o instalador compara o número de versão, a data e o idioma dos dois arquivos.

Se apenas um dos arquivos tiver um número de versão, o instalador usará a lógica ilustrada pelo seguinte diagrama de fluxo para determinar se todos os arquivos instalados pertencentes ao componente devem ser substituídos. Como o instalador instala apenas componentes inteiros, se o arquivo de chave instalado for substituído, todos os arquivos do componente serão substituídos.

Observe que este diagrama ilustra as [regras de controle de versão de arquivo](file-versioning-rules.md)padrão, que podem ser substituídas definindo a propriedade [**REINSTALLMODE**](reinstallmode.md) . O valor padrão da propriedade **REinstallmode** é "omus".

![regras de controle de versão de arquivo padrão quando apenas um arquivo tem um número de versão](images/waiflow3.png)

Consulte os exemplos de controle de versão de arquivo padrão em [substituindo arquivos existentes](replacing-existing-files.md).

-   [Ambos os arquivos têm uma versão](both-files-have-a-version.md)
-   [Nenhum arquivo tem uma versão](neither-file-has-a-version.md)
-   [Nenhum arquivo tem uma versão com verificação de hash de arquivo](neither-file-has-a-version-with-file-hash-check.md)

 

 



