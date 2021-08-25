---
description: O hash de arquivo está disponível com Windows Instalador. Para obter mais informações, consulte MsiGetFileHash e a tabela MsiFileHash. A tabela MsiFileHash só pode ser usada com arquivos sem versão.
ms.assetid: 608859ac-6640-4c28-b4f0-34ab36d804d7
title: Nenhum arquivo tem uma versão com verificação de hash de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb874cdc29c56f34be2d4ec8604c2436892744e44581258ec237f515600f9024
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869187"
---
# <a name="neither-file-has-a-version-with-file-hash-check"></a>Nenhum arquivo tem uma versão com verificação de hash de arquivo

O hash de arquivo está disponível com Windows Instalador. Para obter mais informações, [**consulte MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) e a [tabela MsiFileHash](msifilehash-table.md). A tabela MsiFileHash só pode ser usada com arquivos sem versão.

Se o arquivo de chave de um componente que está sendo instalado (copy-A) tiver o mesmo nome que um arquivo já instalado no local de destino (copy-B), o instalador comparará o número de versão, a data e o idioma dos dois arquivos.

Se nenhum arquivo tiver um número de versão, o instalador usará a lógica ilustrada pelo diagrama de fluxo a seguir para determinar se todos os arquivos instalados pertencem ao componente. Como o instalador instala apenas componentes inteiros, se o arquivo de chave instalado for substituído, todos os arquivos do componente serão substituídos.

Observe que este diagrama ilustra as Regras de Controle de [Versão](file-versioning-rules.md)de Arquivo padrão, que podem ser substituídos definindo a [**propriedade REINSTALLMODE.**](reinstallmode.md) O valor padrão da **propriedade REINSTALLMODE** é "omus".

![regras de controle de versão de arquivo padrão quando substituídos pela configuração de propriedade reinstallmode](images/waiflow2b.png)

Consulte os exemplos de versão de arquivo padrão em [Substituindo arquivos existentes.](replacing-existing-files.md)

-   [Ambos os arquivos têm uma versão](both-files-have-a-version.md)
-   [Nenhum arquivo tem uma versão](neither-file-has-a-version.md)
-   [Um arquivo tem uma versão](one-file-has-a-version.md)

 

 



