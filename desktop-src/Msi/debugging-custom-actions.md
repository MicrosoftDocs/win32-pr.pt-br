---
description: Você pode depurar ações personalizadas baseadas em bibliotecas de vínculo dinâmico usando as ferramentas de depuração para Windows. Não é possível usar a depuração dinâmica com ações personalizadas com base em arquivos ou scripts executáveis.
ms.assetid: 4241a27a-c127-4c65-96a2-1d655b343eba
title: Depurando ações personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ddfbc9952f0dd7fc1b85b5c64fa6a23381ceafe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768473"
---
# <a name="debugging-custom-actions"></a>Depurando ações personalizadas

Você pode depurar ações personalizadas baseadas em bibliotecas de [vínculo dinâmico](dynamic-link-libraries.md) usando as [ferramentas de depuração para Windows](https://www.microsoft.com/?ref=go). Não é possível usar a depuração dinâmica com ações personalizadas com base em arquivos ou [scripts](scripts.md) [executáveis](executable-files.md) .

As técnicas descritas nesta seção podem ajudá-lo a depurar Windows Installer ações personalizadas. Consulte a seção ferramentas de desenvolvimento de driver do WDK (Kit de driver do Windows) para obter informações sobre as [ferramentas de depuração para Windows](https://www.microsoft.com/?ref=go).

Windows Installer usa a variável de ambiente MsiBreak para determinar qual ação personalizada deve ser depurada. Se você tiver acesso ao código-fonte da ação personalizada, talvez seja possível usar a depuração sem MsiBreak. Para iniciar a depuração sem MsiBreak, coloque uma caixa de mensagem temporária no início do código da ação. Quando a caixa de mensagem aparecer durante a instalação, anexe o depurador ao processo que possui a caixa de mensagem. Em seguida, você pode definir todos os pontos de interrupção necessários e ignorar a caixa de mensagem para retomar a execução. Não é possível depurar as partes anteriores da ação personalizada por este método.

Para usar a variável de ambiente MsiBreak para depurar a ação personalizada, defina MsiBreak como o nome da ação personalizada na [tabela CustomAction](customaction-table.md). MsiBreak pode ser um sistema ou uma variável de ambiente de usuário. Se a variável for definida como uma variável do sistema, uma reinicialização do sistema poderá ser necessária quando o valor for alterado para detectar o novo valor.

Para usar a variável de ambiente MsiBreak para depurar uma interface de usuário inserida, defina o valor de MsiBreak como MsiEmbeddedUI.

Windows Installer verificará apenas a variável de ambiente MsiBreak se o usuário for um administrador. O instalador ignora o valor de MsiBreak se o usuário não for um administrador, mesmo que este seja um [*aplicativo gerenciado*](m-gly.md).

Se você estiver Depurando uma ação personalizada que é executada com privilégios elevados (sistema) na sequência de execução, anexe o depurador ao serviço de Windows Installer. Ao depurar uma ação personalizada que é executada com privilégios representados na sequência de execução, o sistema solicita uma caixa de diálogo que indica qual processo deve ser depurado. O usuário recebe uma caixa de diálogo indicando qual processo Depurar. Para obter mais informações sobre ações personalizadas elevadas, consulte [segurança de ação personalizada](custom-action-security.md).

Depois que o depurador tiver sido anexado ao processo correto, o instalador acionará um ponto de interrupção do depurador imediatamente antes de chamar o Point de entrada da DLL. No ponto de interrupção, sua DLL já está carregada no processo e o endereço do ponto de entrada foi determinado. Se não foi possível carregar a DLL de ação personalizada ou se o ponto de entrada da ação personalizada não existia, nenhuma interrupção é disparada. Como o ponto de interrupção é disparado antes de chamar a função de DLL, depois de disparado, você deve usar o depurador para avançar até que o pontos de entrada de ação personalizada seja chamado. Como alternativa, você pode definir um ponto de interrupção em qualquer lugar em sua ação personalizada e retomar a execução normal.

O Windows Installer executa DLLs não armazenadas na [tabela binária](binary-table.md) diretamente do local da dll. O instalador não sabe o nome original de uma DLL armazenada na tabela binária e executa a ação personalizada de DLL em um nome de arquivo temporário. A forma do nome de arquivo temporário é MSI?????. TMP. No Windows XP, esse arquivo temporário é armazenado em um local seguro, geralmente o <WindowFolder> \\ instalador.

Observe que muitas DLLs criadas para depuração contêm o nome e o caminho do arquivo PDB correspondente como parte da própria DLL. Ao depurar esse tipo de DLL em um sistema em que o PDB pode ser encontrado no local armazenado na DLL, os símbolos podem ser carregados automaticamente pela ferramenta do depurador. Em situações em que o PDB não pode ser encontrado no local armazenado, em que o depurador não oferece suporte ao carregamento de símbolos a partir do local armazenado, ou onde a DLL não foi criada com informações de depuração, talvez seja necessário posicionar os arquivos de símbolo na pasta com o arquivo DLL temporário.

O instalador adiciona informações de depuração para scripts de ação personalizados ao arquivo de log de instalação.

``` syntax
There is a problem with this Windows Installer package. A script 
required for this install to complete could not be run. Contact your 
support personnel or package vendor.  {Custom action [2] script error 
[3], [4]: [5] Line [6], Column [7], [8] }
```

 

 



