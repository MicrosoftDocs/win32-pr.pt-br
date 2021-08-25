---
description: No núcleo de qualquer instalador está a instalação real dos arquivos.
ms.assetid: e6f6d6a5-bdb0-4866-8d2c-56313d92c94c
title: Regras de controle de versão de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8dfda6a909450ba45cc213016a159bbbc8f9a54b958c7d4e37d051fd86935ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828976"
---
# <a name="file-versioning-rules"></a>Regras de controle de versão de arquivo

No núcleo de qualquer instalador está a instalação real dos arquivos. Determinar se um arquivo deve ser instalado é um processo complexo. No nível mais alto, essa determinação depende de se o componente ao qual um arquivo pertence está marcado para instalação. Uma vez determinado que um arquivo deve ser copiado, o processo será complicado se existir outro arquivo com o mesmo nome na pasta de destino. Nessas situações, fazer a determinação requer um conjunto de regras que envolvem as seguintes propriedades:

-   Versão
-   Data
-   Idioma

O instalador usa essas regras apenas ao tentar instalar um arquivo em um local que já contém um arquivo com o mesmo nome. nesse caso, o Windows Installer usa as regras a seguir, todas as outras coisas sendo iguais para determinar se deseja instalar o.

Versão mais alta vence — todas as outras coisas são iguais, o arquivo com a versão mais alta vence, mesmo que o arquivo no computador tenha a versão mais alta.

Arquivos com controle de versão Win – um arquivo com versão é instalado em um arquivo sem versão.

Favorecer a linguagem do produto — se o arquivo que está sendo instalado tiver um idioma diferente do arquivo no computador, favor favorecer o arquivo com o idioma que corresponde ao produto que está sendo instalado. Os arquivos com neutralidade de idioma são tratados como apenas outra linguagem, de modo que o produto que está sendo instalado é favorecedo novamente.

Vários idiomas incompatíveis — depois de fatorar quaisquer linguagens comuns entre o arquivo que está sendo instalado e o arquivo no computador, quaisquer idiomas restantes são favorecedos de acordo com o que é necessário para o produto que está sendo instalado.

Preservar idiomas do superconjunto — preserve o arquivo que dá suporte a vários idiomas, independentemente de ele já estar no computador ou estar sendo instalado.

Os arquivos sem versão são dados do usuário – se a data de modificação for posterior à data de criação do arquivo no computador, não instale o arquivo porque as personalizações do usuário serão excluídas. Se as datas de modificação e de criação forem as mesmas, instale o arquivo. Se a data de criação for posterior à data de modificação, o arquivo será considerado sem modificações, instale o arquivo.

A instalação de um [arquivo complementar](companion-files.md) não depende de suas próprias informações de controle de versão de arquivo, mas no controle de versão de seu pai complementar. No caso de arquivos complementares, a instalação será ignorada somente se o arquivo pai tiver uma versão superior. Observe que um arquivo que é o caminho de chave para seu componente não deve ser um arquivo complementar porque isso resulta na lógica de controle de versão do arquivo de caminho de chave que está sendo determinado pelo arquivo pai complementar.

Arquivos sem versão usando [arquivos complementares](companion-files.md)– um arquivo sem versão associado a um arquivo com versão usando o mecanismo complementar Opera de acordo com as regras para o arquivo com versão. A única exceção é se o arquivo com versão no computador e o arquivo com controle de versão que está sendo instalado têm a mesma versão e idioma, mas o arquivo complementar está ausente no computador. Nesse caso, o arquivo complementar que está sendo instalado é usado, embora o arquivo com versão no computador seja usado. Além disso, um arquivo não versionado usando um arquivo complementar é instalado se a propriedade [**REinstallmode**](reinstallmode.md) inclui as opções substituir versões mais antigas ("o" ou "e") e a versão do arquivo complementar é igual a um arquivo que já está no computador.

As regras são globais — as regras para determinar quando instalar um arquivo residem em um único local dentro do instalador e são globais, o que significa que eles se aplicam a todos os arquivos igualmente.

Para obter exemplos do formato usado para versões de arquivo, consulte o tipo de dados [version](version.md) . Para obter informações mais específicas, consulte [substituindo arquivos existentes](replacing-existing-files.md) ou o [controle de versão de arquivo padrão](default-file-versioning.md).

 

 



