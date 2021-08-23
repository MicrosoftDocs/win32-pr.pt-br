---
description: se nenhum arquivo tiver um número de versão, o Windows Installer usará a lógica ilustrada pelo seguinte diagrama de fluxo para determinar se todos os arquivos instalados pertencentes ao componente devem ser substituídos.
ms.assetid: 82cb0d96-f49f-408e-a8c6-a0d1ee9af8c7
title: Nenhum arquivo tem uma versão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a68a6d74a26a810f2ddb33e1c13b2ed7b372a75d5b262a8b6d8d7ecaca1c99f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065926"
---
# <a name="neither-file-has-a-version"></a>Nenhum arquivo tem uma versão

Se o arquivo de chave de um componente que está sendo instalado (cópia-A) tiver o mesmo nome que um arquivo já instalado no local de destino (cópia-B), o instalador compara o número de versão, a data e o idioma dos dois arquivos.

Se nenhum arquivo tiver um número de versão, o instalador usará a lógica ilustrada pelo seguinte diagrama de fluxo para determinar se todos os arquivos instalados pertencentes ao componente devem ser substituídos. Como o instalador instala apenas componentes inteiros, se o arquivo de chave instalado for substituído, todos os arquivos do componente serão substituídos.

Observe que este diagrama ilustra as [regras de controle de versão de arquivo](file-versioning-rules.md)padrão, que podem ser substituídas definindo a propriedade [**REINSTALLMODE**](reinstallmode.md) . O valor padrão da propriedade **REinstallmode** é "omus".

![regras de controle de versão de arquivo padrão quando nenhum arquivo tem um número de versão](images/waiflow2.png)

Consulte os exemplos de controle de versão de arquivo padrão em [substituindo arquivos existentes](replacing-existing-files.md).

-   [Ambos os arquivos têm uma versão](both-files-have-a-version.md)
-   [Nenhum arquivo tem uma versão com verificação de hash de arquivo](neither-file-has-a-version-with-file-hash-check.md)
-   [Um arquivo tem uma versão](one-file-has-a-version.md)

 

 



