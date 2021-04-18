---
description: ICE64 verifica se os novos diretórios no perfil do usuário são removidos corretamente em cenários de roaming.
ms.assetid: d878bf4a-33c4-4c68-bd74-b7884d6680a5
title: ICE64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d103498a56bea26415f4f841d5ec78b5dfe370f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506038"
---
# <a name="ice64"></a>ICE64

ICE64 verifica se os novos diretórios no perfil do usuário são removidos corretamente em cenários de roaming.

A falha em corrigir um aviso ou erro relatado por ICE64 geralmente leva a problemas na limpeza completa do computador durante uma desinstalação. Quando um usuário móvel que instalou o aplicativo faz logon em um computador pela primeira vez, todo o perfil é copiado para baixo no computador. No anúncio (que ocorre após o download do perfil móvel), o instalador verifica se o diretório já existe e, portanto, não o exclui na desinstalação. Isso deixa o diretório no computador do usuário permanentemente.

## <a name="result"></a>Resultado

O ICE64 posta um aviso ou um erro em uma situação de roaming se um novo diretório no perfil do usuário que deve ser removido não for removido.

## <a name="example"></a>Exemplo

ICE64 relata o seguinte erro para o exemplo mostrado.

``` syntax
The directory 'MyOtherFolder' is in the user profile but is not listed in the RemoveFile table.
```

A pasta ' MyOtherFolder ' é uma pasta de perfil Personalizada. Como não está listado na tabela removerfile, ele não é removido em alguns cenários.

Para corrigir esse erro, crie uma linha para a pasta na tabela RemoveFile.

[Tabela de diretórios](directory-table.md)



| Diretório     | Pai do diretório \_ | DefaultDir  |
|---------------|-------------------|-------------|
| AppDataFolder | TARGETDIR         |             |
| MyFolder      | AppDataFolder     | DataFolder  |
| MyOtherFolder | AppDataFolder     | DataFolder2 |



 

[Remover Tabelafile](removefile-table.md)



| FileKey | Componente\_ | FileName | DirProperty | InstallMode |
|---------|-------------|----------|-------------|-------------|
| Key1    | Component1  |          | MyFolder    | 2           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



