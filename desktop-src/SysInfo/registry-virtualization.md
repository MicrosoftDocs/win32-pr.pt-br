---
description: A virtualização do Registro é uma tecnologia de compatibilidade de aplicativos que permite que as operações de gravação do Registro que têm impacto global sejam redirecionadas para locais por usuário.
ms.assetid: dace2f65-df60-419a-8be8-ab60668e6396
title: Virtualização do Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f14d8a82a12be74d3c5f2963e8b4edf47baaa85c4a8299e4ff632284bbac83fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763583"
---
# <a name="registry-virtualization"></a>Virtualização do Registro

*A virtualização do Registro* é uma tecnologia de compatibilidade de aplicativos que permite que as operações de gravação do Registro que têm impacto global sejam redirecionadas para locais por usuário. Esse redirecionamento é transparente para aplicativos que lêem ou escrevem no Registro. Há suporte para ele a partir do Windows Vista.

Essa forma de virtualização é uma tecnologia de compatibilidade de aplicativo provisório; A Microsoft pretende removê-lo de versões futuras do sistema operacional Windows à medida que mais aplicativos são compatíveis com o Windows Vista e versões posteriores do Windows. Portanto, é importante que seu aplicativo não se torne dependente do comportamento da virtualização do Registro no sistema.

A virtualização destina-se apenas a fornecer compatibilidade para aplicativos existentes. Os aplicativos projetados para Windows Vista e versões posteriores do Windows não devem gravar em áreas confidenciais do sistema nem devem depender da virtualização para corrigir problemas. Ao atualizar o código existente para ser executado no Windows Vista e em versões posteriores do Windows, os desenvolvedores devem garantir que os aplicativos armazenem apenas dados em locais por usuário ou em locais de computador dentro de %alluserprofile% que usem corretamente uma ACL (lista de controle de acesso).

Para obter mais informações sobre como criar aplicativos compatíveis com UAC, consulte o [Guia do desenvolvedor do UAC.](/previous-versions/dotnet/articles/aa480150(v=msdn.10))

## <a name="virtualization-overview"></a>Visão geral da virtualização

Antes do Windows Vista, os aplicativos normalmente eram executados pelos administradores. Como resultado, os aplicativos podem acessar gratuitamente os arquivos do sistema e as chaves do Registro. Se esses aplicativos fossem executados por um usuário padrão, eles falhariam devido a direitos de acesso insuficientes. Windows O Vista e versões posteriores do Windows melhoram a compatibilidade de aplicativos para esses aplicativos redirecionando automaticamente essas operações. Por exemplo, as operações do Registro para o repositório global (**HKEY \_ LOCAL MACHINE \_ \\ Software**) são redirecionadas para um local por usuário dentro do perfil do usuário conhecido como repositório *virtual* (**HKEY USERS \_ Classes \\ <User SID> \_ \\ VirtualStore Machine \\ \\ Software**).

A virtualização do Registro pode ser amplamente classificada nos seguintes tipos:

<dl> <dt>

<span id="Open_Registry_Virtualization"></span><span id="open_registry_virtualization"></span><span id="OPEN_REGISTRY_VIRTUALIZATION"></span>Abrir Virtualização do Registro
</dt> <dd>

Se o chamador não tiver acesso de gravação a uma chave e tentar abrir a chave, a chave será aberta com o acesso máximo permitido para esse chamador.

Se o sinalizador REG KEY DONT SILENT FAIL for definido para a chave, a operação \_ \_ \_ \_ falhará e a chave não será aberta. Para obter mais informações, consulte "Controlando a virtualização do Registro" mais adiante neste tópico.

</dd> <dt>

<span id="Write_Registry_Virtualization"></span><span id="write_registry_virtualization"></span><span id="WRITE_REGISTRY_VIRTUALIZATION"></span>Virtualização do Registro de Gravação
</dt> <dd>

Se o chamador não tiver acesso de gravação a uma chave e tentar gravar um valor nele ou criar uma sub-chave, o valor será gravado no armazenamento virtual.

Por exemplo, se um usuário limitado tentar gravar um valor na seguinte chave: **HKEY \_ LOCAL MACHINE \_ \\ Software** AppKey1 , a virtualização redireciona a operação de gravação para classes \\  **HKEY \_ USERS \\ <User SID> \_ \\ VirtualStore Machine \\ \\ Software** \\ *AppKey1*.

</dd> <dt>

<span id="Read_Registry_Virtualization"></span><span id="read_registry_virtualization"></span><span id="READ_REGISTRY_VIRTUALIZATION"></span>Ler Virtualização do Registro
</dt> <dd>

Se o chamador ler de uma chave virtualizada, o Registro apresentará uma exibição mesclada dos valores virtualizados (do armazenamento virtual) e dos valores não virtuais (do armazenamento global) para o chamador.

Por exemplo, suponha **que HKEY \_ LOCAL MACHINE \_ \\ Software** AppKey1 contém dois valores V1 e V2 e que um usuário limitado grava um valor \\  V3 na chave. Quando o usuário tenta ler valores dessa chave, a exibição mesclada inclui os valores V1 e V2 do armazenamento global e do valor V3 do armazenamento virtual.

Observe que os valores virtuais têm precedência sobre valores globais quando presentes. No exemplo acima, mesmo que o armazenamento global tivesse o valor V3 sob essa chave, o valor V3 ainda seria retornado ao chamador da loja virtual. Se a V3 fosse excluída da loja virtual, a V3 seria retornada do armazenamento global. Em outras palavras, se a V3 fosse excluída das classes **HKEY \_ USERS \\ <User SID> \_ \\ VirtualStore \\ Machine \\ Software** \\ *AppKey1,* mas **HKEY LOCAL MACHINE \_ \_ \\ Software** \\ *AppKey1* tivesse um valor V3, esse valor seria retornado do repositório global.

</dd> </dl>

## <a name="registry-virtualization-scope"></a>Escopo da Virtualização do Registro

A virtualização do Registro está habilitada somente para o seguinte:

-   Processos interativos de 32 bits.
-   Chaves no **HKEY \_ LOCAL MACHINE \_ \\ Software**.
-   Chaves nas que um administrador pode gravar. (Se um administrador não puder gravar em uma chave, o aplicativo terá falhado nas versões anteriores do Windows mesmo se fosse executado por um administrador.)

A virtualização do Registro está desabilitada para o seguinte:

-   Processos de 64 bits.
-   Processos que não são interativos, como serviços.

    Observe que o uso do Registro como um mecanismo de comunicação entre processos (IPC) entre um serviço (ou qualquer outro processo que não tenha a virtualização habilitada) e um aplicativo não funcionará corretamente se a chave for virtualizada. Por exemplo, se um serviço antivírus atualizar seus arquivos de assinatura com base em um valor definido por um aplicativo, o serviço nunca atualizará seus arquivos de assinatura porque o serviço lê do armazenamento global, mas o aplicativo grava no armazenamento virtual.

-   Processos que representa um usuário. Se um processo tentar uma operação ao representar um usuário, essa operação não será virtualizada.
-   Processos de modo kernel, como drivers.
-   Processos que **solicitaramExecutionLevel** especificado em seus manifestos.
-   Chaves e sub-chaves das classes de **software HKEY \_ LOCAL \_ MACHINE, \\ \\** **HKEY LOCAL MACHINE Software \_ \_ Microsoft \\ \\ \\ Windows** e **HKEY LOCAL MACHINE Software \_ Microsoft \_ \\ \\ \\ Windows NT**.

## <a name="controlling-registry-virtualization"></a>Controlando a virtualização do Registro

Além de controlar a virtualização em um nível de aplicativo usando **requestedExecutionLevel** no manifesto, um administrador pode habilitar ou desabilitar a virtualização por chave para chaves no **HKEY \_ LOCAL MACHINE \_ \\ Software.** Para fazer isso, use a Reg.exe FLAGS do utilitário de linha de comando com os sinalizadores listados na tabela a seguir.



| Sinalizador                         | Significado                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FALHA \_ SILENCIOSA DE REG KEY \_ DONT \_ \_ | Esse sinalizador desabilita a virtualização aberta do Registro. Se esse sinalizador for definido e uma operação aberta falhar em uma chave que tenha a virtualização habilitada, o Registro não tentará reabrir a chave. Se esse sinalizador estiver claro, o Registro tentará reabrir a chave com acesso MÁXIMO PERMITIDO em \_ vez do acesso solicitado.                                                                   |
| REG \_ KEY \_ DONT \_ VIRTUALIZE   | Esse sinalizador desabilita a virtualização do registro de gravação. Se esse sinalizador for definido e uma operação criar chave ou definir valor falhar porque o chamador não tem direito de acesso suficiente à chave pai, o Registro falhará na operação. Se esse sinalizador estiver claro, o Registro tentará gravar a chave ou o valor no armazenamento virtual. O chamador deve ter a tecla KEY \_ READ à direita na chave pai. |
| SINALIZADOR REG \_ KEY \_ RECURSE \_      | Se esse sinalizador for definido, os sinalizadores de virtualização do Registro serão propagados da chave pai. Se esse sinalizador estiver claro, os sinalizadores de virtualização do Registro não serão propagados. Alterar esse sinalizador afeta apenas novas chaves decrescentes criadas depois que o sinalizador é alterado. Ele não definirá nem limpará esses sinalizadores para chaves decrescentes existentes.                                                                  |



 

O exemplo a seguir mostra o uso do utilitário de linha de comando Reg.exe com a opção FLAGS para consultar o estado dos sinalizadores de virtualização para uma chave.

``` syntax
C:\>reg flags HKLM\Software\AppKey1 QUERY

HKEY_LOCAL_MACHINE\Software\AppKey1

        REG_KEY_DONT_VIRTUALIZE: CLEAR
        REG_KEY_DONT_SILENT_FAIL: CLEAR
        REG_KEY_RECURSE_FLAG: CLEAR

The operation completed successfully.
```

Sempre que a auditoria estiver habilitada em uma chave que está sendo virtualizada, um novo evento de auditoria de virtualização será gerado para indicar que a chave está sendo virtualizada (além dos eventos de auditoria usuais). Os administradores podem usar essas informações para monitorar o status da virtualização em seus sistemas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ponto de Partida com controle de conta de usuário](/previous-versions/windows/it-pro/windows-vista/cc507861(v=technet.10))
</dt> <dt>

[Noções básicas e configuração do controle de conta de usuário](/previous-versions/windows/it-pro/windows-vista/cc709628(v=ws.10))
</dt> <dt>

[Práticas recomendadas e diretrizes para aplicativos em um ambiente com privilégios mínimos](/previous-versions/dotnet/articles/aa480150(v=msdn.10))
</dt> </dl>

 

 
