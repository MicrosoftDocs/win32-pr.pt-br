---
description: se ambos os arquivos tiverem um número de versão, o Windows Installer usará a lógica ilustrada pelo seguinte diagrama de fluxo para determinar se todos os arquivos instalados pertencentes ao componente devem ser substituídos.
ms.assetid: c4c8a23b-e1c2-4c96-b708-7cbcbcab4cd4
title: Ambos os arquivos têm uma versão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1338a93b4a45094a9a5951c3c59def15affde96dbbe74f3b134ba9dd7532092
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380741"
---
# <a name="both-files-have-a-version"></a>Ambos os arquivos têm uma versão

Se o arquivo de chave de um componente que está sendo instalado (cópia-A) tiver o mesmo nome que um arquivo já instalado no local de destino (cópia-B), o instalador compara o número de versão e o idioma dos dois arquivos.

Se ambos os arquivos tiverem um número de versão, o instalador usará a lógica ilustrada pelo seguinte diagrama de fluxo para determinar se todos os arquivos instalados pertencentes ao componente devem ser substituídos. Como o instalador instala apenas componentes inteiros, se o arquivo de chave instalado for substituído, todos os arquivos do componente serão substituídos.

Observe que este diagrama ilustra as [regras de controle de versão de arquivo](file-versioning-rules.md)padrão, que podem ser substituídas definindo a propriedade [**REINSTALLMODE**](reinstallmode.md) . O valor padrão da propriedade **REinstallmode** é "omus".

![regras de controle de versão de arquivo padrão quando ambos os arquivos têm o mesmo nome ou número de versão](images/waiflow1.png)

O diagrama anterior também pode ser usado com arquivos sem nenhum idioma especificado. Se Copy-A tiver um idioma especificado e Copy-B não tiver um idioma especificado, Copy-B será substituído por Copy-A. Se Copy-A e Copy-B não tiverem nenhum idioma especificado, Copy-B não será substituído.

Consulte exemplos de controle de versão de arquivo padrão ao [substituir arquivos existentes](replacing-existing-files.md).

-   [Nenhum arquivo tem uma versão](neither-file-has-a-version.md)
-   [Nenhum arquivo tem uma versão com verificação de hash de arquivo](neither-file-has-a-version-with-file-hash-check.md)
-   [Um arquivo tem uma versão](one-file-has-a-version.md)

 

 



