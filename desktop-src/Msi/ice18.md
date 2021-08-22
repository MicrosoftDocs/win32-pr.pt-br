---
description: ICE18 valida que todos os diretórios vazios usados como um caminho de chave para um componente são listados na tabela CreateFolder.
ms.assetid: de31b893-831b-4a6d-809a-c4a3056b8a66
title: ICE18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ca102e8fdec5e30283cd879ddb5677a2bba79f90ba5a9a790ea50923e0aeedb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581136"
---
# <a name="ice18"></a>ICE18

ICE18 valida que todos os diretórios vazios usados como um caminho de chave para um componente são listados na [tabela CreateFolder](createfolder-table.md).

Se a coluna KeyPath da [tabela de componentes](component-table.md) for nula, isso significará que o diretório listado na \_ coluna diretório é o caminho de chave para esse componente. Como as pastas criadas pelo instalador são excluídas quando se tornam vazias, essa pasta deve estar listada na [tabela CreateFolder](createfolder-table.md) para impedir que o instalador tente instalar todas as vezes.

Não torne o diretório SystemFolder o caminho de chave de um componente. Como essa pasta está presente em todos os sistemas operacionais, o instalador sempre detecta o caminho da chave se o componente está presente ou não. Nesse caso, o caminho da chave deve ser um arquivo, uma entrada do registro ou uma fonte de dados ODBC.

Ao executar um ICE18 de validação, primeiro verifique se os itens a seguir estão todos verdadeiros:

-   A coluna KeyPath da [tabela de componentes](component-table.md) contém um valor nulo.
-   Que não há arquivos listados para o componente na tabela de [arquivos](file-table.md).
-   Que não há arquivos para o componente listado na [tabela removerfile](removefile-table.md) e que o valor em DirProperty seja o mesmo que a \_ coluna Directory da [tabela Component](component-table.md).
-   Que não há arquivos para o componente listado na [tabela duplicatefile](duplicatefile-table.md) e que o valor em DestFolder seja o mesmo da \_ coluna Directory da [tabela Component](component-table.md).
-   Que não há arquivos para o componente listado na [tabela MoveFile](movefile-table.md) e que o valor em DestFolder é o mesmo que a \_ coluna Directory da [tabela Component](component-table.md).

Se todos forem verdadeiros, o ICE18 validará o seguinte:

-   Se a \_ coluna Component da [tabela CreateFolder](createfolder-table.md) tem o mesmo valor que a coluna Component da [tabela Component](component-table.md).
-   Se a \_ coluna Directory da tabela CreateFolder tem o mesmo valor que a coluna Directory \_ da [tabela Component](component-table.md).

## <a name="result"></a>Resultado

ICE18 posta uma mensagem de erro se o pacote de instalação especifica um diretório como o caminho da chave para o componente que não está listado na [tabela CreateFolder](createfolder-table.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



