---
title: Redirecionador de registro
description: O redirecionador de registro isola os aplicativos de 32 bits e 64 bits fornecendo exibições lógicas separadas de determinadas partes do registro no WOW64.
ms.assetid: b3989f79-0439-485a-96c1-4f2227d48653
keywords:
- Guia de programação do Windows de 64 bits-programação do Windows de 64 bits, redirecionador de registro
- Programação do Windows redirecter de 64 bits
- Programação de redirecionamento do Windows de 64 bits
- Programação WOW64 de 64 bits do Windows, redirecionador de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c11e68f307aa014adb7cae8415f1baba155678
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364096"
---
# <a name="registry-redirector"></a>Redirecionador de registro

O redirecionador de registro isola os aplicativos de 32 bits e 64 bits fornecendo exibições lógicas separadas de determinadas partes do registro no WOW64. O redirecionador de registro intercepta as chamadas de registro de 32 bits e 64 bits para suas respectivas exibições de registro lógico e as mapeia para o local de registro físico correspondente. O processo de redirecionamento é transparente para o aplicativo. Portanto, um aplicativo de 32 bits pode acessar os dados do registro como se estivessem em execução em janelas de 32 bits, mesmo que os dados sejam armazenados em um local diferente em janelas de bits 64.

**Windows 10 no ARM:** Além da exibição lógica de 32 bits para aplicativos x86, o Windows 10 no ARM inclui uma exibição lógica separada para aplicativos ARM de 32 bits.

Um subconjunto de chaves em caminhos de registro redirecionados é compartilhado. chamadas de registro de 32 bits para chaves compartilhadas não são redirecionadas. Em vez disso, uma cópia física da chave é mapeada em cada exibição lógica do registro. Para obter uma lista de chaves redirecionadas e chaves compartilhadas, consulte [chaves do registro afetadas pelo WOW64](shared-registry-keys.md).

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Para habilitar a interoperabilidade de aplicativos por meio de COM e outros mecanismos, um subconjunto de chaves de registro redirecionadas também é *refletido*. O processo de reflexão do registro copia chaves e valores do registro entre duas exibições do registro para mantê-las sincronizadas. A reflexão do registro foi removida a partir do Windows 7 e do Windows Server 2008 R2. Para obter mais informações, consulte [reflexão do registro](registry-reflection.md).

O cenário a seguir ilustra o uso dessas exibições lógicas:

-   Um aplicativo x86 de 32 bits verifica a existência da seguinte chave do registro: **HKEY \_ local \_ Machine \\ software \\ Hello**. Se a chave não existir, o aplicativo a criará com um valor padrão de "Olá, mundo de 32 bits x86"; caso contrário, ele lê e exibe o valor.
-   O mesmo aplicativo é modificado para escrever "Hello 64-bit World" em vez de "Hello 32-bit x86 World" e recompilado como um aplicativo de 64-bit x64 ou ARM64.
-   **Windows 10 no ARM:** O mesmo aplicativo é modificado para gravar "Hello 32-bit ARM World" e recompilado como um aplicativo ARM de 32 bits.
-   Quando o aplicativo x86 de 32 bits é executado no Windows de 64 bits, ele exibe "Olá, mundo de 32 de bits x86". Quando o aplicativo de 64 bits é executado, ele exibe "Olá, mundo de 64 bits". **Windows 10 no ARM:** Quando o aplicativo ARM de 32 bits é executado em janelas ARM64 de 64 bits, ele exibe "Olá, mundo de" Hello 32-bit ARM ". Todos os aplicativos chamam as mesmas funções de registro com o mesmo identificador predefinido e o mesmo nome de chave; a diferença é que cada aplicativo opera em sua exibição lógica do registro, e cada exibição é mapeada para um local físico separado do registro, o que mantém todas as versões da cadeia de caracteres intactas.

As chaves redirecionadas são mapeadas para locais físicos em **Wow6432Node**. Por exemplo, **HKEY \_ local \_ Machine \\ software** é redirecionado para **HKEY \_ local \_ Machine \\ software \\ Wow6432Node**. No entanto, o local físico das chaves redirecionadas deve ser considerado reservado pelo sistema. Os aplicativos não devem acessar a localização física de uma chave diretamente, pois esse local pode ser alterado. Para obter mais informações, consulte [acessando uma exibição de registro alternativa](accessing-an-alternate-registry-view.md).

**Windows 10 no ARM:** Chaves ARM de 32 bits redirecionadas são mapeadas para locais físicos em WowAA32Node.

Para ajudar os aplicativos de 32 bits que gravam os dados **reg \_ sz** ou **reg \_ expandem o \_ sz** que contém% ProgramFiles% ou% COMMONPROGRAMFILES% ao registro, o WOW64 intercepta essas operações de gravação e as substitui por "% ProgramFiles (x86)%" e "% CommonProgramFiles (x86)%". Por exemplo, se o diretório arquivos de programas estiver na unidade C, "% ProgramFiles (x86)%" se expandirá para "C: \\ arquivos de programas (x86)". A substituição ocorrerá somente se as seguintes condições forem atendidas:

-   A cadeia de caracteres deve começar com% ProgramFiles% ou% COMMONPROGRAMFILES%. Se a cadeia de caracteres começar com um espaço ou qualquer caractere diferente de%, ela não será substituída.
-   O caso de% ProgramFiles% ou% COMMONPROGRAMFILES% deve ser exatamente como mostrado porque a comparação de cadeia de caracteres diferencia maiúsculas de minúsculas. Por exemplo, se a cadeia de caracteres começar com% CommonProgramFiles% em vez de% COMMONPROGRAMFILES%, ela não será substituída.
-   A cadeia de caracteres não pode exceder o \_ caminho máximo \* 2 + 15 caracteres. Se ele exceder esse comprimento, ele não será substituído.
-   A chave não pode ser aberta com a chave \_ WOW64 \_ 64KEY. Esse sinalizador especifica que as operações na chave devem ser executadas na exibição do registro de 64 bits, portanto, ela não é substituída. Para obter mais informações, consulte [acessando uma exibição de registro alternativa](accessing-an-alternate-registry-view.md).

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** O \_ sinalizador chave WOW \_ 64 \_ 64KEY não afeta se uma chave é substituída. Esse sinalizador afeta a substituição a partir do Windows 7 e do Windows Server 2008 R2.

Além disso, \_ as chaves sz do reg ou reg \_ \_ que contêm system32 são substituídas por SysWOW64. A cadeia de caracteres deve começar com o caminho apontando para ou em% windir% \\ System32. A comparação de cadeia de caracteres não diferencia maiúsculas de minúsculas. As variáveis de ambiente são expandidas antes de corresponder ao caminho, portanto, todos os seguintes caminhos são substituídos:% WINDIR% \\ System32,% SystemRoot% \\ System32 e C: \\ Windows \\ System32. Esse patch é aplicado somente às chaves que foram refletidas antes do Windows 7.

Para mais informações, consulte os seguintes tópicos:

-   [Reflexão do registro](registry-reflection.md)
-   [Chaves do Registro afetadas pelo WOW64](shared-registry-keys.md)
-   [Acessando uma exibição alternativa do registro](accessing-an-alternate-registry-view.md)
-   [Exemplo de redirecionamento de registro no WOW64](example-of-registry-reflection-and-redirection-on-wow64.md)
-   [Acesso remoto ao registro no Windows de 64 bits](remote-registry-access-in-64-bit-windows.md)

 

 




