---
description: ICE90 posta um aviso se descobrir que o diretório de um atalho foi especificado como uma propriedade pública.
ms.assetid: 47565d9b-c3c2-4a5c-8f91-2b3912a63b47
title: ICE90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b4063d06aa5a0a8688e2a411040d4b64f58f75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827942"
---
# <a name="ice90"></a>ICE90

ICE90 posta um aviso se descobrir que o diretório de um atalho foi especificado como uma propriedade pública. Os nomes das [Propriedades públicas](public-properties.md) são gravados em letras maiúsculas. Um atalho especificado por uma propriedade pública pode não funcionar se o valor da propriedade [**AllUsers**](allusers.md) for alterado.

Essa ação personalizada de ICE valida a tabela de atalho e usa a tabela de diretórios. Se a tabela de diretório não estiver presente, ela será retornada sem validar a tabela de atalho e não lançará nenhum erro ou aviso.

## <a name="result"></a>Resultado

ICE90 posta o aviso a seguir.



| Erro de ICE90                                                                                                                                                                                                                    | Description                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| O atalho ' \[ 1 \] ' tem um diretório que é uma propriedade pública (All Caps) e está no diretório de perfil do usuário. Isso resultará em um problema se o valor da propriedade [**AllUsers**](allusers.md) for alterado na sequência da interface do usuário. | O diretório de um atalho foi especificado como uma propriedade pública. |



 

## <a name="example"></a>Exemplo

ICE90 relata o seguinte aviso para o exemplo:

``` syntax
The shortcut 'Shortcut1' has a directory that is a public property (ALL CAPS) 
and is under user profile directory. This results in a problem if the value 
of the ALLUSERS property changes in the UI sequence.
```

Neste exemplo, MYDIR está em um perfil de usuários. ICE90 posta um aviso porque o local do diretório de destino é especificado por uma propriedade pública, MYDIR. Um usuário pode alterar A propriedade MYDIR ou [**AllUsers**](allusers.md) . Se **AllUsers** estiver definido para o [contexto de instalação](installation-context.md)por máquina e MYDIR estiver em um perfil de usuários, o arquivo de atalho em MYDIR será copiado no perfil "todos os usuários" e não em um perfil de usuário específico. Se **AllUsers** estiver definido para o contexto de instalação por usuário, o arquivo de atalho em MYDIR será copiado para um perfil de usuário específico e não estará disponível para outros usuários.

[Tabela de atalho](shortcut-table.md) (parcial)



| Atalho  | Diretório\_ |
|-----------|-------------|
| Shortcut1 | MYDIR       |



 

[Tabela de diretórios](directory-table.md) (parcial)



| Diretório | Pai do diretório \_ |
|-----------|-------------------|
| MYDIR     | ProgramMenuFolder |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



