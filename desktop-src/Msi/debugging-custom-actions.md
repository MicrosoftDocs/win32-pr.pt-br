---
description: Você pode depurar ações personalizadas baseadas em bibliotecas de vínculo dinâmico usando ferramentas de depuração para Windows. Não é possível usar a depuração dinâmica com ações personalizadas com base em arquivos executáveis ou scripts.
ms.assetid: 4241a27a-c127-4c65-96a2-1d655b343eba
title: Depurando ações personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 781aaa5bfc8303175e7addfee730908c581575fd
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887014"
---
# <a name="debugging-custom-actions"></a>Depurando ações personalizadas

Você pode depurar ações personalizadas baseadas em bibliotecas de [vínculo](dynamic-link-libraries.md) dinâmico usando as [Ferramentas de Depuração para Windows](https://www.microsoft.com/?ref=go). Não é possível usar a depuração dinâmica com ações personalizadas com base em [arquivos executáveis](executable-files.md) ou [scripts](scripts.md).

As técnicas descritas nesta seção podem ajudá-lo a depurar Windows personalizadas do Instalador. Consulte a seção Ferramentas de Desenvolvimento de Driver do WDK (Kit de Driver Windows) para obter informações sobre ferramentas [de depuração para Windows](https://www.microsoft.com/?ref=go).

Windows O instalador usa a variável de ambiente MsiBreak para determinar qual ação personalizada deve ser depurada. Se você tiver acesso ao código-fonte da ação personalizada, poderá usar a depuração sem msiBreak. Para iniciar a depuração sem msiBreak, coloque uma caixa de mensagem temporária no início do código da ação. Quando a caixa de mensagem for exibida durante a instalação, anexe o depurador ao processo que possui a caixa de mensagem. Em seguida, você pode definir os pontos de interrupção necessários e descartar a caixa de mensagem para retomar a execução. Não é possível depurar as partes anteriores da ação personalizada por esse método.

Para usar a variável de ambiente MsiBreak para depurar a ação personalizada, depure MsiBreak como o nome da ação personalizada na [tabela CustomAction](customaction-table.md). O MsiBreak pode ser um sistema ou uma variável de ambiente de usuário. Se a variável for definida como uma variável do sistema, uma reinicialização do sistema poderá ser necessária quando o valor for alterado para detectar o novo valor.

Para usar a variável de ambiente MsiBreak para depurar uma interface do usuário inserida, depure o valor de MsiBreak como MsiEmbeddedUI.

Windows O instalador verifica apenas a variável de ambiente MsiBreak se o usuário for um Administrador. O instalador ignorará o valor de MsiBreak se o usuário não for um Administrador, mesmo se esse for um [*aplicativo gerenciado.*](m-gly.md)

Se você estiver depurando uma ação personalizada que é executado com privilégios elevados (sistema) na sequência de execução, anexe o depurador ao serviço Windows Instalador. Ao depurar uma ação personalizada que é executado com privilégios personificados na sequência de execução, o sistema solicita uma caixa de diálogo que indica qual processo deve ser depurado. O usuário será solicitado com uma caixa de diálogo indicando qual processo de depuração será depurado. Para obter mais informações sobre ações personalizadas elevadas, consulte [Segurança de ação personalizada.](custom-action-security.md)

Depois que o depurador tiver sido anexado ao processo correto, o instalador disparará um ponto de interrupção do depurador imediatamente antes de chamar o ponto de entrada da DLL. No ponto de interrupção, sua DLL já está carregada no processo e o endereço do ponto de entrada determinado. Se a DLL de ação personalizada não puder ser carregada ou o ponto de entrada de ação personalizada não existir, nenhum ponto de interrupção será disparado. Como o ponto de interrupção é disparado antes de chamar a função DLL, depois que o ponto de interrupção for disparado, você deverá usar o depurador para avançar até que o ponto de entrada de ação personalizado seja chamado. Como alternativa, você pode definir um ponto de interrupção em qualquer lugar em sua ação personalizada e retomar a execução normal.

O Windows instalador executa DLLs não armazenadas na tabela [Binária](binary-table.md) diretamente do local da DLL. O instalador não sabe o nome original de uma DLL armazenada na tabela Binária e executa a ação personalizada da DLL em um nome de arquivo temporário. A forma do nome de arquivo temporário é MSI?????. TMP. No Windows XP, esse arquivo temporário é armazenado em um local seguro, normalmente o &lt; Instalador &gt; \\ windowFolder.

Observe que muitas DLLs criadas para depuração contêm o nome e o caminho do arquivo PDB correspondente como parte da própria DLL. Ao depurar esse tipo de DLL em um sistema em que o PDB pode ser encontrado no local armazenado na DLL, os símbolos podem ser carregados automaticamente pela ferramenta de depurador. Em situações em que o PDB não pode ser encontrado no local armazenado, em que o depurador não dá suporte ao carregamento de símbolos do local armazenado ou em que a DLL não foi criada com informações de depuração, talvez seja necessário colocar os arquivos de símbolo na pasta com o arquivo DLL temporário.

O instalador adiciona informações de depuração para scripts de ação personalizados ao arquivo de log de instalação.

``` syntax
There is a problem with this Windows Installer package. A script 
required for this install to complete could not be run. Contact your 
support personnel or package vendor.  {Custom action [2] script error 
[3], [4]: [5] Line [6], Column [7], [8] }
```

 

 



