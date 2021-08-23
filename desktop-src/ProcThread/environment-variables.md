---
description: 'Cada processo tem um bloco de ambiente que contém um conjunto de variáveis de ambiente e seus valores. Há dois tipos de variáveis de ambiente: variáveis de ambiente do usuário (definidas para cada usuário) e variáveis de ambiente do sistema (definidas para todos).'
ms.assetid: 6732b12f-ced1-4769-b947-79da8fd2237a
title: Variáveis de ambiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647c685aac8ed6df36c0312d7eef49793fd4b2bbfca5576e0377e59da31dd777
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910316"
---
# <a name="environment-variables"></a>Variáveis de ambiente

Cada processo tem um bloco de ambiente que contém um conjunto de variáveis de ambiente e seus valores. Há dois tipos de variáveis de ambiente: variáveis de ambiente do usuário (definidas para cada usuário) e variáveis de ambiente do sistema (definidas para todos).

Por padrão, um processo filho herda as variáveis de ambiente de seu processo pai. Os programas iniciados pelo processador de comandos herdam as variáveis de ambiente do processador de comando. Para especificar um ambiente diferente para um processo filho, crie um novo bloco de ambiente e passe um ponteiro para ele como um parâmetro para a [**função CreateProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)

O processador de comandos fornece o **comando set** para exibir seu bloco de ambiente ou para criar novas variáveis de ambiente. Você também pode exibir ou modificar  as variáveis de ambiente selecionando Sistema no Painel de Controle **,** selecionando Configurações **avançadas** do sistema e clicando em **Variáveis de Ambiente**.

Cada bloco de ambiente contém as variáveis de ambiente no seguinte formato:<dl> *Var1* = *Value1* \\ 0  
*Var2* = *Valor2* \\ 0  
*Var3* = *Valor3* \\ 0  
...  
*VarN* = *ValueN* \\ 0 \\ 0  
</dl>

O nome de uma variável de ambiente não pode incluir um sinal de igual (=).

A [**função GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings) retorna um ponteiro para o bloco de ambiente do processo de chamada. Isso deve ser tratado como um bloco somente leitura; não modifique-o diretamente. Em vez disso, use [**a função SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable) para alterar uma variável de ambiente. Quando você terminar o bloco de ambiente obtido de **GetEnvironmentStrings,** chame a [**função FreeEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-freeenvironmentstringsa) para liberar o bloco.

Chamar [**SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable) não tem efeito sobre as variáveis de ambiente do sistema. Para adicionar ou modificar programaticamente as variáveis de ambiente do sistema, adicione-as à chave do Registro do Ambiente do Ambiente do Gerenciador de Sessão de Controle do Sistema **HKEY \_ \_ \\ \\ LOCALControlSet \\ \\ \\** e, em seguida, broadcast uma mensagem [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) com *lParam definido* como a cadeia de caracteres "Ambiente". Isso permite que aplicativos, como o shell, escolham suas atualizações.

O tamanho máximo de uma variável de ambiente definida pelo usuário é de 32.767 caracteres. Não há nenhuma limitação técnica sobre o tamanho do bloco de ambiente. No entanto, há limites práticos, dependendo do mecanismo usado para acessar o bloco. Por exemplo, um arquivo em lotes não pode definir uma variável que seja maior que o comprimento máximo da linha de comando.

**Windows Server 2003 e Windows XP:** O tamanho máximo do bloco de ambiente para o processo é de 32.767 caracteres. A partir do Windows Vista e Windows Server 2008, não há nenhuma limitação técnica no tamanho do bloco de ambiente.

A [**função GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable) determina se uma variável especificada é definida no ambiente do processo de chamada e, em caso afirmativo, qual é seu valor.

Para recuperar uma cópia do bloco de ambiente para um determinado usuário, use a [**função CreateEnvironmentBlock.**](/windows/win32/api/userenv/nf-userenv-createenvironmentblock)

Para expandir cadeias de caracteres de variável de ambiente, use a [**função ExpandEnvironmentStrings.**](/windows/desktop/api/processenv/nf-processenv-expandenvironmentstringsa)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Alterando variáveis de ambiente](changing-environment-variables.md)
</dt> <dt>

[Variáveis de ambiente do usuário](../shell/user-environment-variables.md)
</dt> </dl>

 

 
