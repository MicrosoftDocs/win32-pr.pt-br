---
title: Redirecionador de Registro
description: O redirecionador do Registro isola aplicativos de 32 bits e 64 bits fornecendo exibições lógicas separadas de determinadas partes do Registro no WOW64.
ms.assetid: b3989f79-0439-485a-96c1-4f2227d48653
keywords:
- Guia de programação Windows de 64 bits Windows de 64 bits, redirecionador de registro
- Programação do Windows de 64 bits do Windows registro
- programação de Windows redirecionamento de 64 bits
- Wow64 64 bits Windows programação, redirecionador de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fac810a6ce2dba049f7b7e5b9d28386cda89712f2833eb7bf4f7892df59b34ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561502"
---
# <a name="registry-redirector"></a>Redirecionador de Registro

O redirecionador do Registro isola aplicativos de 32 bits e 64 bits fornecendo exibições lógicas separadas de determinadas partes do Registro no WOW64. O redirecionador do Registro intercepta chamadas de registro de 32 bits e 64 bits para suas respectivas exibições lógicas do Registro e as mapeia para o local do Registro físico correspondente. O processo de redirecionamento é transparente para o aplicativo. Portanto, um aplicativo de 32 bits pode acessar dados do Registro como se estivesse em execução em um Windows de 32 bits, mesmo se os dados fossem armazenados em um local diferente em um Windows de 64 bits.

**Windows 10 no ARM:** Além da exibição lógica de 32 bits para aplicativos x86, o Windows 10 no ARM inclui uma exibição lógica separada para aplicativos ARM de 32 bits.

Um subconjunto de chaves em caminhos de registro redirecionados é compartilhado. Chamadas do Registro de 32 bits para chaves compartilhadas não são redirecionadas. Em vez disso, uma cópia física da chave é mapeada para cada exibição lógica do Registro. Para ver uma lista de chaves redirecionadas e chaves compartilhadas, consulte [Chaves do Registro afetadas pelo WOW64.](shared-registry-keys.md)

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Para habilitar a interoperabilidade do aplicativo por meio de COM e outros mecanismos, um subconjunto de chaves do Registro redirecionadas também é *refletido.* O processo de reflexão do Registro copia chaves e valores do Registro entre duas exibições do Registro para mantê-las sincronizadas. A reflexão do Registro foi removida do Windows 7 e Windows Server 2008 R2. Para obter mais informações, consulte [Reflexão do Registro.](registry-reflection.md)

O cenário a seguir ilustra o uso dessas exibições lógicas:

-   Um aplicativo x86 de 32 bits verifica a existência da seguinte chave do Registro: **HKEY \_ LOCAL MACHINE Software \_ \\ \\ Hello**. Se a chave não existir, o aplicativo a criará com um valor padrão de "Olá, mundo x86 de 32 bits"; caso contrário, ele lê e exibe o valor.
-   O mesmo aplicativo é modificado para gravar "Olá, mundo de 64 bits" em vez de "Olá, mundo x86 de 32 bits" e recompilado como um aplicativo x64 ou ARM64 de 64 bits.
-   **Windows 10 no ARM:** O mesmo aplicativo é modificado para gravar "Olá, mundo arm de 32 bits" e recompilado como um aplicativo ARM de 32 bits.
-   Quando o aplicativo x86 de 32 bits é executado em um Windows de 64 bits, ele exibe "Olá, mundo x86 de 32 bits". Quando o aplicativo de 64 bits é executado, ele exibe "Olá, mundo de 64 bits". **Windows 10 no ARM:** Quando o aplicativo ARM de 32 bits é executado no Windows ARM de 64 bits, ele exibe "Olá, mundo arm de 32 bits". Todos os aplicativos chamam as mesmas funções do Registro com o mesmo handle predefinido e o mesmo nome de chave; A diferença é que cada aplicativo opera em sua exibição lógica do Registro e cada exibição é mapeada para um local físico separado do Registro, o que mantém todas as versões da cadeia de caracteres intactas.

As chaves redirecionadas são mapeadas para locais físicos **em Wow6432Node.** Por exemplo, **HKEY \_ LOCAL MACHINE \_ \\ Software** é redirecionado para **HKEY LOCAL MACHINE Software \_ \_ \\ \\ Wow6432Node**. No entanto, o local físico das chaves redirecionadas deve ser considerado reservado pelo sistema. Os aplicativos não devem acessar diretamente a localização física de uma chave, pois esse local pode mudar. Para obter mais informações, [consulte Acessando uma exibição de registro alternativa.](accessing-an-alternate-registry-view.md)

**Windows 10 no ARM:** As chaves ARM de 32 bits redirecionadas são mapeadas para locais físicos em WowAA32Node.

Para ajudar aplicativos de 32 bits que escrevem dados **REG \_ SZ** ou **REG EXPAND \_ \_ SZ** contendo %ProgramFiles% ou %commonprogramfiles% no Registro, o WOW64 intercepta essas operações de gravação e as substitui por "%ProgramFiles(x86)%" e "%commonprogramfiles(x86)%". Por exemplo, se o diretório Arquivos de Programas estiver na unidade C, "%ProgramFiles(x86)%" expandirá para "C: Arquivos de \\ Programas (x86)". A substituição ocorrerá somente se as seguintes condições são atendidas:

-   A cadeia de caracteres deve começar com %ProgramFiles% ou %commonprogramfiles%. Se a cadeia de caracteres começar com um espaço ou qualquer caractere diferente de %, ela não será substituída.
-   O caso de %ProgramFiles% ou %commonprogramfiles% deve ser exatamente como mostrado porque a comparação de cadeias de caracteres faz a redução de minúsculas. Por exemplo, se a cadeia de caracteres começar com %CommonProgramFiles% em vez de %commonprogramfiles%, ela não será substituída.
-   A cadeia de caracteres não pode exceder MAX \_ PATH \* 2+15 caracteres. Se exceder esse comprimento, ele não será substituído.
-   A chave não pode ser aberta com KEY \_ WOW64 \_ 64KEY. Esse sinalizador especifica que as operações na chave devem ser executadas na exibição do Registro de 64 bits, portanto, ela não é substituída. Para obter mais informações, [consulte Acessando uma exibição de registro alternativa.](accessing-an-alternate-registry-view.md)

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** O sinalizador \_ KEY WOW \_ 64 \_ 64KEY não afeta se uma chave é substituída. Esse sinalizador afeta a substituição a partir do Windows 7 e Windows Server 2008 R2.

Além disso, as chaves REG SZ ou REG EXPAND SZ que contêm \_ \_ system32 são \_ substituídas por syswow64. A cadeia de caracteres deve começar com o caminho apontando para ou em %windir% \\ system32. A comparação de cadeia de caracteres não é sensível a minúsculas. As variáveis de ambiente são expandidas antes de corresponderem ao caminho, portanto, todos os seguintes caminhos são substituídos: %windir% \\ system32, %SystemRoot% \\ system32 e C: \\ windows \\ system32. Esse patch é aplicado somente às chaves que foram refletidas antes Windows 7.

Para obter mais informações, consulte estes tópicos:

-   [Reflexão do Registro](registry-reflection.md)
-   [Chaves do Registro afetadas pelo WOW64](shared-registry-keys.md)
-   [Acessando uma exibição de registro alternativa](accessing-an-alternate-registry-view.md)
-   [Exemplo de redirecionamento do Registro no WOW64](example-of-registry-reflection-and-redirection-on-wow64.md)
-   [Acesso remoto ao Registro em um servidor de 64 Windows](remote-registry-access-in-64-bit-windows.md)

 

 




