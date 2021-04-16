---
description: A virtualização do registro é uma tecnologia de compatibilidade de aplicativos que permite que operações de gravação do registro que têm impacto global sejam redirecionadas para locais por usuário.
ms.assetid: dace2f65-df60-419a-8be8-ab60668e6396
title: Virtualização do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642bda46b43fc0b4f7efa60cfcd9e2178643811f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751055"
---
# <a name="registry-virtualization"></a>Virtualização do registro

A *virtualização do registro* é uma tecnologia de compatibilidade de aplicativos que permite que operações de gravação do registro que têm impacto global sejam redirecionadas para locais por usuário. Esse redirecionamento é transparente para os aplicativos que lêem ou gravam no registro. Há suporte a partir do Windows Vista.

Essa forma de virtualização é uma tecnologia de compatibilidade de aplicativos provisória; A Microsoft pretende removê-la de versões futuras do sistema operacional Windows, pois mais aplicativos são compatíveis com o Windows Vista e versões posteriores do Windows. Portanto, é importante que seu aplicativo não se torne dependente do comportamento da virtualização do registro no sistema.

A virtualização destina-se apenas a fornecer compatibilidade para aplicativos existentes. Os aplicativos projetados para o Windows Vista e versões posteriores do Windows não devem gravar em áreas confidenciais do sistema, nem devem confiar na virtualização para solucionar problemas. Ao atualizar o código existente para ser executado no Windows Vista e em versões posteriores do Windows, os desenvolvedores devem garantir que os aplicativos só armazenem dados em locais por usuário ou em locais de computadores dentro de% USERPROFILE% que usem corretamente uma ACL (lista de controle de acesso).

Para obter mais informações sobre a criação de aplicativos em conformidade com o UAC, consulte o [Guia do desenvolvedor do UAC](/previous-versions/dotnet/articles/aa480150(v=msdn.10)).

## <a name="virtualization-overview"></a>Visão geral da virtualização

Antes do Windows Vista, os aplicativos eram normalmente executados por administradores. Como resultado, os aplicativos podem acessar livremente os arquivos do sistema e as chaves do registro. Se esses aplicativos foram executados por um usuário padrão, eles falharão devido a direitos de acesso insuficientes. O Windows Vista e versões posteriores do Windows melhoram a compatibilidade de aplicativos para esses aplicativos ao redirecionar automaticamente essas operações. Por exemplo, as operações de registro para o repositório global (**HKEY \_ local \_ Machine \\ software**) são redirecionadas para um local por usuário dentro do perfil do usuário conhecido como o *repositório virtual* (**HKEY \_ Users \\ <User SID> \_ classes \\ VirtualStore \\ Machine \\ software**).

A virtualização do registro pode ser classificada em grande escala nos seguintes tipos:

<dl> <dt>

<span id="Open_Registry_Virtualization"></span><span id="open_registry_virtualization"></span><span id="OPEN_REGISTRY_VIRTUALIZATION"></span>Abrir a virtualização do registro
</dt> <dd>

Se o chamador não tiver acesso de gravação a uma chave e tentar abrir a chave, a chave será aberta com o acesso máximo permitido para esse chamador.

Se o \_ sinalizador de falha silenciosa da chave do registro \_ \_ \_ estiver definido para a chave, a operação falhará e a chave não será aberta. Para obter mais informações, consulte "controlando a virtualização do registro" mais adiante neste tópico.

</dd> <dt>

<span id="Write_Registry_Virtualization"></span><span id="write_registry_virtualization"></span><span id="WRITE_REGISTRY_VIRTUALIZATION"></span>Gravar a virtualização do registro
</dt> <dd>

Se o chamador não tiver acesso de gravação a uma chave e tentar gravar um valor nele ou criar uma subchave, o valor será gravado no repositório virtual.

Por exemplo, se um usuário limitado tentar gravar um valor na seguinte chave: **HKEY \_ local \_ Machine \\ software** \\ *AppKey1*, Virtualization redireciona a operação de gravação para **HKEY \_ Users \\ <User SID> \_ classes \\ VirtualStore \\ Machine \\ software** \\ *AppKey1*.

</dd> <dt>

<span id="Read_Registry_Virtualization"></span><span id="read_registry_virtualization"></span><span id="READ_REGISTRY_VIRTUALIZATION"></span>Ler a virtualização do registro
</dt> <dd>

Se o chamador lê de uma chave que é virtualizada, o registro apresenta uma exibição mesclada dos valores virtualizados (do repositório virtual) e os valores não virtuais (do repositório global) para o chamador.

Por exemplo, suponha que **HKEY \_ local \_ Machine \\ software** \\ *AppKey1* contenha dois valores v1 e V2 e que um usuário limitado grave um valor V3 na chave. Quando o usuário tenta ler valores dessa chave, a exibição mesclada inclui os valores v1 e v2 do repositório global e o valor V3 do repositório virtual.

Observe que os valores virtuais têm precedência sobre valores globais quando presentes. No exemplo acima, mesmo que o repositório global tenha o valor v3 sob essa chave, o valor v3 ainda seria retornado para o chamador do repositório virtual. Se v3 fosse excluído do repositório virtual, o V3 seria retornado do repositório global. Em outras palavras, se v3 fosse excluído de **HKEY \_ Users \\ <User SID> \_ classes \\ VirtualStore \\ Machine \\ software** \\ *AppKey1* , mas **HKEY \_ local \_ Machine \\ software** \\ *AppKey1* tinha um valor v3, esse valor seria retornado do repositório global.

</dd> </dl>

## <a name="registry-virtualization-scope"></a>Escopo de virtualização do registro

A virtualização do registro é habilitada apenas para o seguinte:

-   processos interativos de 32 bits.
-   Chaves em **HKEY \_ local \_ Machine \\ software**.
-   Chaves para as quais um administrador pode gravar. (Se um administrador não puder gravar em uma chave, o aplicativo terá falhado em versões anteriores do Windows, mesmo que fosse executado por um administrador.)

A virtualização do registro está desabilitada para o seguinte:

-   processos de 64 bits.
-   Processos que não são interativos, como serviços.

    Observe que usar o registro como um mecanismo de comunicação entre processos (IPC) entre um serviço (ou qualquer outro processo que não tenha a virtualização habilitada) e um aplicativo não funcionará corretamente se a chave for virtualizada. Por exemplo, se um serviço antivírus atualizar seus arquivos de assinatura com base em um valor definido por um aplicativo, o serviço nunca atualizará seus arquivos de assinatura porque o serviço lê do repositório global, mas o aplicativo grava no repositório virtual.

-   Processos que representam um usuário. Se um processo tentar uma operação enquanto representa um usuário, essa operação não será virtualizada.
-   Processos de modo kernel, como drivers.
-   Processos que têm **requestedExecutionLevel** especificado em seus manifestos.
-   Chaves e subchaves **das \_ \_ classes de \\ software \\ do computador local** hKey, **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows** e **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT**.

## <a name="controlling-registry-virtualization"></a>Controlando a virtualização do registro

Além de controlar a virtualização em um nível de aplicativo usando **requestedExecutionLevel** no manifesto, um administrador pode habilitar ou desabilitar a virtualização por chave para chaves no software da **\_ \_ máquina \\ local hKey**. Para fazer isso, use a opção Reg.exe sinalizadores do utilitário de linha de comando com os sinalizadores listados na tabela a seguir.



| Sinalizador                         | Significado                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| a chave do registro não apresenta \_ \_ \_ \_ falha silenciosa | Esse sinalizador desabilita a virtualização do registro aberto. Se esse sinalizador for definido e uma operação de abertura falhar em uma chave com virtualização habilitada, o registro não tentará reabrir a chave. Se esse sinalizador estiver claro, o registro tentará reabrir a chave com o \_ acesso máximo permitido em vez do acesso solicitado.                                                                   |
| a chave do registro não \_ \_ \_ virtualiza   | Esse sinalizador desabilita a virtualização do registro de gravação. Se esse sinalizador for definido e uma operação Create Key ou Set Value falhar porque o chamador não tem direito de acesso suficiente para a chave pai, o registro falha na operação. Se esse sinalizador for claro, o registro tentará gravar a chave ou o valor no repositório virtual. O chamador deve ter o direito de leitura de chave \_ na chave pai. |
| \_sinalizador de \_ recursão de chave de registro \_      | Se esse sinalizador for definido, os sinalizadores de virtualização do registro serão propagados da chave pai. Se esse sinalizador for claro, os sinalizadores de virtualização do registro não serão propagados. A alteração desse sinalizador afeta apenas as novas chaves descendentes criadas depois que o sinalizador é alterado. Ele não define nem limpa esses sinalizadores para chaves descendentes existentes.                                                                  |



 

O exemplo a seguir mostra o uso do utilitário de linha de comando Reg.exe com a opção FLAGS para consultar o estado dos sinalizadores de virtualização de uma chave.

``` syntax
C:\>reg flags HKLM\Software\AppKey1 QUERY

HKEY_LOCAL_MACHINE\Software\AppKey1

        REG_KEY_DONT_VIRTUALIZE: CLEAR
        REG_KEY_DONT_SILENT_FAIL: CLEAR
        REG_KEY_RECURSE_FLAG: CLEAR

The operation completed successfully.
```

Sempre que a auditoria é habilitada em uma chave que está sendo virtualizada, um novo evento de auditoria de virtualização é gerado para indicar que a chave está sendo virtualizada (além dos eventos de auditoria usuais). Os administradores podem usar essas informações para monitorar o status da virtualização em seus sistemas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com controle de conta de usuário](/previous-versions/windows/it-pro/windows-vista/cc507861(v=technet.10))
</dt> <dt>

[Compreendendo e Configurando o controle de conta de usuário](/previous-versions/windows/it-pro/windows-vista/cc709628(v=ws.10))
</dt> <dt>

[Práticas recomendadas e diretrizes do desenvolvedor para aplicativos em um ambiente com privilégios mínimos](/previous-versions/dotnet/articles/aa480150(v=msdn.10))
</dt> </dl>

 

 
