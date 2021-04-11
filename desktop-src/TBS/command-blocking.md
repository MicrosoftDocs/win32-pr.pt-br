---
title: Bloqueio de comando
description: Para preservar a integridade das operações, determinados comandos do TPM não podem ser executados pelo software na plataforma.
ms.assetid: 47402a4a-5f8d-4648-b3ea-06c95b2a1fc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b9a302f12e7838240ee8bfeac1ea78a3884a1
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "104365796"
---
# <a name="command-blocking"></a>Bloqueio de comando

Para preservar a integridade das operações, determinados comandos do TPM não podem ser executados pelo software na plataforma. Por exemplo, alguns comandos são executados apenas pelo software do sistema. Quando o TBS bloqueia um comando, um erro é retornado conforme apropriado. Por padrão, o TBS bloqueia comandos que poderiam afetar a privacidade, a segurança e a estabilidade do sistema. O TBS também pressupõe que outras partes da pilha de software possam restringir o acesso a determinados comandos a entidades autorizadas.

Para comandos do TPM versão 1,2, há três listas de comandos bloqueados: uma lista controlada pela política de grupo, uma lista controlada por administradores locais e uma lista padrão. Um comando do TPM será bloqueado se estiver em qualquer uma das listas. No entanto, há sinalizadores de política de grupo para permitir que o TBS ignore a lista local e a lista padrão. Os sinalizadores de política de grupo podem ser editados diretamente ou acessados por meio do Editor de Objeto de Política de Grupo.

> [!Note]  
> A lista de comandos bloqueados localmente não é preservada após uma atualização para o sistema operacional. Os comandos que são bloqueados na lista de Política de Grupo são preservados.

 

Para comandos do TPM versão 2,0, a lógica para o bloqueio é invertida; Ele usa uma lista de comandos permitidos. Essa lógica bloqueará automaticamente os comandos que não eram conhecidos quando a lista foi feita pela primeira vez. Quando os comandos são adicionados à especificação do TPM após a entrega de uma versão do Windows, esses novos comandos são bloqueados automaticamente. Somente uma atualização do registro adicionará esses novos comandos à lista de comandos permitidos.

A partir do Windows 10 1809 (Windows Server 2019), os comandos permitidos do TPM 2,0 não podem mais ser manipulados por meio de configurações do registro. Para essas versões do Windows 10, os comandos do TPM 2,0 permitidos são corrigidos no driver do TPM. Os comandos do TPM 1,2 ainda podem ser bloqueados e desbloqueados por meio de alterações no registro. 

## <a name="direct-registry-access"></a>Acesso direto ao registro

Os sinalizadores de política de grupo estão na chave do registro **HKEY \_ local \_ Machine** \\ **software** \\ **Policies** \\ **Microsoft** \\ **TPM** \\ **BlockedCommands**.

Para determinar quais listas devem ser usadas para bloquear comandos do TPM, há dois valores **DWORD** que são usados como sinalizadores boolianos:

-   "IgnoreDefaultList"

    Se definido (o valor existe e é diferente de zero), o TBS ignora a lista de comandos bloqueados padrão.

-   "IgnoreLocalList"

    Se definido (o valor existe e é diferente de zero), o TBS ignora a lista de comandos bloqueados locais.

## <a name="group-policy-object-editor"></a>Editor de objeto de política de grupo

**Para acessar o editor de objeto de Política de Grupo**

1.  Clique em **Iniciar**.
2.  Clique em **Executar**.
3.  Na caixa **Abrir** , digite **gpedit.msc**. Clique em **OK**. O editor de objeto Política de Grupo é aberto.
4.  Expanda **configuração do computador**.
5.  Expanda **modelos administrativos**.
6.  Expanda **sistema**.
7.  Expanda **serviços Trusted Platform modules**.

As listas de comandos do TPM 1.2 bloqueados específicos podem ser editadas diretamente nos locais a seguir.

-   Lista de políticas de Grupo:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Policies
             Microsoft
                Tpm
                   BlockedCommands
                      List
    ```

-   Lista local:

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                SharedAccess
                   Parameters
                      Tpm
                         BlockedCommands
                            List
    ```

-   Lista padrão:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                BlockedCommands
                   List
    ```

Em cada uma dessas chaves do registro, há uma lista de valores do registro do \_ tipo reg sz. Cada valor representa um comando bloqueado do TPM. Cada chave do registro tem um campo "nome do valor" e um campo "dados do valor". Os dois campos ("nome do valor" e "dados do valor") devem corresponder exatamente ao valor decimal do ordinal do comando do TPM a ser bloqueado.

A lista de comandos específicos do TPM 2,0 permitidos pode ser editada diretamente no seguinte local. Na chave do registro, há uma lista de valores do registro do \_ tipo reg DWORD. Cada valor representa um comando do TPM 2,0 permitido. Cada valor de registro tem um **nome** e um campo de **valor** . O **nome** corresponde ao ordinal de comando do TPM 2,0 hexadecimal que deve ser permitido. O **valor** terá um valor de 1 se o comando for permitido. Se um ordinal de comando não estiver presente ou tiver um valor de 0, o comando será bloqueado.

-   Lista padrão:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                AllowedW8Commands
                   List
    ```

Para o Windows 8, o Windows Server 2012 e posterior, as chaves do registro **BlockedCommands** e **AllowedW8Commands** respectivamente determinam os comandos do TPM bloqueados ou permitidos para contas de administrador. As contas de usuário têm uma lista de comandos do TPM bloqueados ou permitidos nas chaves do registro **BlockedUserCommands** e **AllowedW8UserCommands** , respectivamente. No Windows 10, versão 1607, novas chaves do registro foram introduzidas para aplicativos do AppContainer: **BlockedAppContainerCommands** e **AllowedW8AppContainerCommands**.

 

 




