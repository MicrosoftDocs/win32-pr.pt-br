---
description: Os termos a seguir são usados ao descrever a depuração.
ms.assetid: 580f2787-d944-4350-a2c2-c00816b3f515
title: Terminologia de depuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa12e24a6c763f9cda983ad961ba85a41c63cec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920118"
---
# <a name="debugging-terminology"></a>Terminologia de depuração

Os termos a seguir são usados ao descrever a depuração.

<dl> <dt>

<span id="Blue_screen"></span><span id="blue_screen"></span><span id="BLUE_SCREEN"></span>Tela azul
</dt> <dd>

Quando o sistema encontra um problema de hardware, inconsistência de dados ou erro semelhante, ele pode exibir uma tela azul contendo informações que podem ser usadas para determinar a causa do erro. Essas informações incluem o código de parada e se um arquivo de despejo de memória foi criado. Ele também pode incluir uma lista de Drivers carregados e um rastreamento de pilha.

</dd> <dt>

<span id="Crash_dump_file"></span><span id="crash_dump_file"></span><span id="CRASH_DUMP_FILE"></span>Arquivo de despejo de memória
</dt> <dd>

Você pode configurar o sistema para gravar informações em um arquivo de despejo de memória no disco rígido sempre que um código de parada for gerado. O arquivo contém informações que o depurador pode usar para analisar o erro. Esse arquivo pode ser tão grande quanto a memória física contida no computador.

</dd> <dt>

<span id="Debugger"></span><span id="debugger"></span><span id="DEBUGGER"></span>Depurador
</dt> <dd>

Um programa projetado para ajudar a detectar, localizar e corrigir erros em outro programa. Ele permite que o desenvolvedor percorra a execução do processo e seus threads, memória de monitoramento, variáveis e outros elementos de contexto de processo e thread.

</dd> <dt>

<span id="Kernel_mode"></span><span id="kernel_mode"></span><span id="KERNEL_MODE"></span>Modo kernel
</dt> <dd>

O modo do processador no qual os serviços do sistema e os drivers de dispositivo são executados. Todas as interfaces e instruções de CPU estão disponíveis e toda a memória está acessível.

</dd> <dt>

<span id="Minidump_file"></span><span id="minidump_file"></span><span id="MINIDUMP_FILE"></span>Arquivo de minidespejo
</dt> <dd>

Os aplicativos podem produzir arquivos de minidespejo de modo de usuário, que contêm um subconjunto útil das informações contidas em um arquivo de despejo de memória. Para obter mais informações, consulte [arquivos de minidespejo](minidump-files.md).

</dd> <dt>

<span id="STOP_code"></span><span id="stop_code"></span><span id="STOP_CODE"></span>Código de parada
</dt> <dd>

O código de erro que identifica o erro que interrompeu o kernel do sistema de continuar a execução.

</dd> <dt>

<span id="Symbol_files"></span><span id="symbol_files"></span><span id="SYMBOL_FILES"></span>Arquivos de símbolo
</dt> <dd>

Todos os aplicativos de sistema, drivers e DLLs são criados de forma que suas informações de depuração residam em arquivos separados conhecidos como arquivos de símbolo. Portanto, o sistema é menor e mais rápido, embora ainda possa ser depurado se os arquivos de símbolo estiverem instalados. Para obter mais informações, consulte [Symbol files](symbol-files.md).

</dd> <dt>

<span id="User_mode"></span><span id="user_mode"></span><span id="USER_MODE"></span>Modo de usuário
</dt> <dd>

O modo de processador no qual os aplicativos são executados. Um conjunto limitado de interfaces está disponível nesse modo e o acesso aos dados do sistema é limitado.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando a depuração automática](configuring-automatic-debugging.md)
</dt> </dl>

 

 



