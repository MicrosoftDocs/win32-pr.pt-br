---
description: Os usuários podem configurar a depuração automática para ajudá-los a determinar por que o sistema ou um aplicativo parou de responder.
ms.assetid: c3c7aa98-c298-452c-b8d0-10a08b4d82a3
title: Configurando a depuração automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990f2f52e6227e4b1a2cf92656794c90fb5d465915a5d888025d0f3b2c438630
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076500"
---
# <a name="configuring-automatic-debugging"></a>Configurando a depuração automática

Os usuários podem configurar a depuração automática para ajudá-los a determinar por que o sistema ou um aplicativo parou de responder.

## <a name="configuring-automatic-debugging-for-system-crashes"></a>Configurando a depuração automática para falhas do sistema

Para configurar o computador de destino para gerar um arquivo de despejo de falha quando o sistema parar de responder, use o **aplicativo System** no Painel de Controle. Clique **em Configurações avançadas do sistema,** que exibe a caixa **de diálogo Propriedades do** Sistema . Na guia **Avançado** dessa caixa, clique em Configurações **em** Inicialização e **Recuperação** e use as opções de recuperação apropriadas. Como alternativa, você pode configurar opções de despejo de falha usando a seguinte chave do Registro:

**HKEY \_ Controle \_ LOCAL MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\  \\ **CrashControl**

O arquivo que você pode especificar é o arquivo de despejo de falha. Seu nome padrão é Memory.dmp. Você pode depurar um despejo de falha com um depurador de modo kernel, como WinDbg ou KD. Para obter mais informações, consulte a documentação incluída com o depurador.

## <a name="configuring-automatic-debugging-for-application-crashes"></a>Configurando a depuração automática para falhas de aplicativo

Quando um aplicativo para de responder (por exemplo, após uma violação de acesso), o sistema invoca automaticamente um depurador especificado no Registro para depuração post-mortem, a ID do processo e o tratamento de evento são passados para o depurador se a linha de comando estiver configurada corretamente. O procedimento a seguir descreve como especificar um depurador no Registro.

**Para definir um depurador como o depurador post-mortem**

1.  Vá para a seguinte chave do Registro:

    **HKEY \_ SOFTWARE \_ DO COMPUTADOR LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AeDebug**

2.  Adicione ou edite o **valor do Depurador** usando uma cadeia de caracteres REG SZ que especifica a linha de \_ comando para o depurador.

    A cadeia de caracteres deve incluir o caminho totalmente qualificado para o executável do depurador. Indique a ID do processo e o handle de evento com parâmetros "%ld" para a linha de comando do depurador. Depurdores diferentes podem ter suas próprias sintaxes de parâmetro para indicar esses valores. Quando o depurador é invocado, o primeiro "%ld" é substituído pela ID do processo e o segundo "%ld" é substituído pelo handle de evento.

    O texto a seguir é um exemplo de como configurar o WinDbg como o depurador.

    ``` syntax
    "C:\debuggers\windbg.exe" -p %ld -e %ld -g
    ```

3.  Se você quiser que o depurador seja invocado  sem interação do usuário, adicione ou edite o valor Automático, usando uma cadeia de caracteres REG SZ que especifica se o sistema deve exibir uma caixa de diálogo para o usuário antes que o \_ depurador seja invocado. A cadeia de caracteres "1" desabilita a caixa de diálogo; a cadeia de caracteres "0" habilita a caixa de diálogo.

## <a name="excluding-an-application-from-automatic-debugging"></a>Excluindo um aplicativo da depuração automática

O procedimento a seguir descreve como excluir um aplicativo  da depuração automática após o valor Automático na **chave AeDebug** ter sido definido como 1.

**Para excluir um aplicativo da depuração automática**

1.  Vá para a seguinte chave do Registro:

    **HKEY \_ SOFTWARE \_ DO COMPUTADOR LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AeDebug**

2.  Adicione um valor REG DWORD à \_ sub-chave **AutoExclusionList,** em que o nome é o nome do arquivo executável e o valor é 1. Por padrão, o Gerenciador de Janelas da Área de Trabalho (Dwm.exe) é excluído da depuração automática porque, caso contrário, um deadlock do sistema pode ocorrer se o Dwm.exe parar de responder (o usuário não pode ver a interface exibida pelo depurador porque o Dwm.exe não está respondendo e o Dwm.exe não pode terminar porque ele é mantido pelo depurador).

    **Windows Server 2003 e Windows XP:** A **sub-chave AutoExclusionList** não está disponível; portanto, você não pode excluir nenhum aplicativo, incluindo Dwm.exe, da depuração automática.

As entradas **padrão do Registro AeDebug** podem ser representadas da seguinte forma:

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

[Habilitando a depuração post-mortem com o WinDbg](/windows-hardware/drivers/debugger/enabling-postmortem-debugging)
</dt> </dl>

 

 
