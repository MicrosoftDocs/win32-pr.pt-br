---
description: Os usuários podem configurar a depuração automática para ajudá-los a determinar por que o sistema ou um aplicativo parou de responder.
ms.assetid: c3c7aa98-c298-452c-b8d0-10a08b4d82a3
title: Configurando a depuração automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2630784d678e08b67a93d00ec52d9bc67c949bc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088854"
---
# <a name="configuring-automatic-debugging"></a>Configurando a depuração automática

Os usuários podem configurar a depuração automática para ajudá-los a determinar por que o sistema ou um aplicativo parou de responder.

## <a name="configuring-automatic-debugging-for-system-crashes"></a>Configurando a depuração automática para falhas do sistema

Para configurar o computador de destino para gerar um arquivo de despejo de memória quando o sistema parar de responder, use o aplicativo do **sistema** no painel de controle. Clique em **Configurações avançadas do sistema**, que exibe a caixa de diálogo **Propriedades do sistema** . Na guia **avançado** da caixa, clique em **configurações** em **inicialização e recuperação** e, em seguida, use as opções de recuperação apropriadas. Como alternativa, você pode configurar as opções de despejo de memória usando a seguinte chave do registro:

**HKEY \_ \_** Controle do sistema de computador local \\  \\ **CurrentControlSet** \\  \\ **CrashControl**

O arquivo que você pode especificar é o arquivo de despejo de memória. Seu nome padrão é Memory. dmp. Você pode depurar um despejo de memória com um depurador do modo kernel, como o WinDbg ou o KD. Para obter mais informações, consulte a documentação incluída com o depurador.

## <a name="configuring-automatic-debugging-for-application-crashes"></a>Configurando a depuração automática para falhas do aplicativo

Quando um aplicativo para de responder (por exemplo, após uma violação de acesso), o sistema invoca automaticamente um depurador que é especificado no registro para depuração postmortem, a ID do processo e o identificador de evento são passados para o depurador se a linha de comando estiver configurada corretamente. O procedimento a seguir descreve como especificar um depurador no registro.

**Para definir um depurador como o depurador postmortem**

1.  Vá para a seguinte chave do registro:

    **HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AeDebug**

2.  Adicione ou edite o valor do **depurador** usando uma \_ cadeia de caracteres reg sz que especifica a linha de comando para o depurador.

    A cadeia de caracteres deve incluir o caminho totalmente qualificado para o executável do depurador. Indique a ID do processo e o identificador de evento com os parâmetros "% ld" para a linha de comando do depurador. Depuradores diferentes podem ter suas próprias sintaxes de parâmetro para indicar esses valores. Quando o depurador é invocado, o primeiro "% ld" é substituído pela ID do processo e o segundo "% ld" é substituído pelo identificador de evento.

    O texto a seguir é um exemplo de como configurar o WinDbg como o depurador.

    ``` syntax
    "C:\debuggers\windbg.exe" -p %ld -e %ld -g
    ```

3.  Se você quiser que o depurador seja invocado sem interação do usuário, adicione ou edite o valor **automático** , usando uma \_ cadeia de caracteres reg sz que especifica se o sistema deve exibir uma caixa de diálogo para o usuário antes do depurador ser invocado. A cadeia de caracteres "1" desabilita a caixa de diálogo; a cadeia de caracteres "0" habilita a caixa de diálogo.

## <a name="excluding-an-application-from-automatic-debugging"></a>Excluindo um aplicativo da depuração automática

O procedimento a seguir descreve como excluir um aplicativo da depuração automática depois que o valor **automático** na chave **AeDebug** tiver sido definido como 1.

**Para excluir um aplicativo da depuração automática**

1.  Vá para a seguinte chave do registro:

    **HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AeDebug**

2.  Adicione um \_ valor reg DWORD à subchave autodelelist, em que o nome é o nome do arquivo executável e o valor é 1.  Por padrão, o Gerenciador de Janelas da Área de Trabalho (Dwm.exe) é excluído da depuração automática porque, caso contrário, um deadlock do sistema pode ocorrer se Dwm.exe para de responder (o usuário não pode ver a interface exibida pelo depurador porque Dwm.exe não está respondendo e Dwm.exe não pode terminar porque ele é mantido pelo depurador).

    **Windows Server 2003 e Windows XP:** A subchave **ExclusionList** não está disponível; Portanto, você não pode excluir nenhum aplicativo, incluindo Dwm.exe, da depuração automática.

As entradas de registro **AeDebug** padrão podem ser representadas da seguinte maneira:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               AeDebug
                  Auto = 1
                  AutoExclusionList
                     DWM.exe = 1
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Habilitando a depuração do postmortem com o WinDbg](/windows-hardware/drivers/debugger/enabling-postmortem-debugging)
</dt> </dl>

 

 
