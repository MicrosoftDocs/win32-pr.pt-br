---
description: O Win32 \_ NetworkLoginProfile&\# 8194; A classe WMI representa as informações de logon de rede de um usuário específico em um sistema de computador que executa o Windows.
ms.assetid: e5a8e934-d5a7-43fa-b140-c3cca972590f
ms.tgt_platform: multiple
title: Classe Win32_NetworkLoginProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkLoginProfile
- Win32_NetworkLoginProfile.Caption
- Win32_NetworkLoginProfile.Description
- Win32_NetworkLoginProfile.SettingID
- Win32_NetworkLoginProfile.AccountExpires
- Win32_NetworkLoginProfile.AuthorizationFlags
- Win32_NetworkLoginProfile.BadPasswordCount
- Win32_NetworkLoginProfile.CodePage
- Win32_NetworkLoginProfile.Comment
- Win32_NetworkLoginProfile.CountryCode
- Win32_NetworkLoginProfile.Flags
- Win32_NetworkLoginProfile.FullName
- Win32_NetworkLoginProfile.HomeDirectory
- Win32_NetworkLoginProfile.HomeDirectoryDrive
- Win32_NetworkLoginProfile.LastLogoff
- Win32_NetworkLoginProfile.LastLogon
- Win32_NetworkLoginProfile.LogonHours
- Win32_NetworkLoginProfile.LogonServer
- Win32_NetworkLoginProfile.MaximumStorage
- Win32_NetworkLoginProfile.Name
- Win32_NetworkLoginProfile.NumberOfLogons
- Win32_NetworkLoginProfile.Parameters
- Win32_NetworkLoginProfile.PasswordAge
- Win32_NetworkLoginProfile.PasswordExpires
- Win32_NetworkLoginProfile.PrimaryGroupId
- Win32_NetworkLoginProfile.Privileges
- Win32_NetworkLoginProfile.Profile
- Win32_NetworkLoginProfile.ScriptPath
- Win32_NetworkLoginProfile.UnitsPerWeek
- Win32_NetworkLoginProfile.UserComment
- Win32_NetworkLoginProfile.UserId
- Win32_NetworkLoginProfile.UserType
- Win32_NetworkLoginProfile.Workstations
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4fb71b27093cb1011b9aebaadf0a6760124b64f9e13ae7b5ef46f5ffc478cce4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972645"
---
# <a name="win32_networkloginprofile-class"></a>\_Classe Win32 NetworkLoginProfile

A  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkLoginProfile do Win32** representa as informações de logon de rede de um usuário específico em um sistema de computador que executa o Windows. Isso inclui, mas não se limita a status de senha, privilégios de acesso, cotas de disco e caminhos de diretório de logon.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkLoginProfile : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  datetime AccountExpires;
  uint32   AuthorizationFlags;
  uint32   BadPasswordCount;
  uint32   CodePage;
  string   Comment;
  uint32   CountryCode;
  uint32   Flags;
  string   FullName;
  string   HomeDirectory;
  string   HomeDirectoryDrive;
  datetime LastLogoff;
  datetime LastLogon;
  string   LogonHours;
  string   LogonServer;
  uint64   MaximumStorage;
  string   Name;
  uint32   NumberOfLogons;
  string   Parameters;
  datetime PasswordAge;
  datetime PasswordExpires;
  uint32   PrimaryGroupId;
  uint32   Privileges;
  string   Profile;
  string   ScriptPath;
  uint32   UnitsPerWeek;
  string   UserComment;
  uint32   UserId;
  string   UserType;
  string   Workstations;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ NetworkLoginProfile** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ NetworkLoginProfile** tem essas propriedades.

<dl> <dt>

**AccountExpires**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management estruturas \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Acct \_ Expires")
</dt> </dl>

A conta vai expirar. Esse valor é calculado a partir do número de segundos decorridos desde 00:00:00, 1º de janeiro de 1970 e é definido neste formato: AAAAMMDDHHMMSS. mmmmmm sutc.

Exemplo: 20521201000230, 0 000

</dd> <dt>

**AuthorizationFlags**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| Gerenciamento de rede de estruturas \| de [**usuário \_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 sinalizadores de \_ autenticação \_ "), [**bitvalues**](../wmisdk/standard-qualifiers.md) ("impressora", "comunicação", "servidor", "contas")
</dt> </dl>

Conjunto de sinalizadores que especificam os recursos que um usuário está autorizado a usar ou modificar.

<dt>

1 (0x1)
</dt> <dd>

Impressora

</dd> <dt>

2 (0x2)
</dt> <dd>

Comunicação

</dd> <dt>

4 (0x4)
</dt> <dd>

Servidor

</dd> <dt>

8 (0x8)
</dt> <dd>

Contas

</dd> </dl>

</dd> <dt>

**BadPasswordCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| funções de gerenciamento de rede \| NetUserEnum")
</dt> </dl>

Número de vezes que o usuário insere uma senha inadequada ao fazer logon em um sistema de computador executando o Windows.

Exemplo: 0

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descrição textual do objeto atual.

Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).

</dd> <dt>

**CodePage**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management estruturas \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Code \_ Page")
</dt> </dl>

Página de código para o idioma de escolha do usuário. Uma página de código é o conjunto de caracteres usado.

</dd> <dt>

**Comentário**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| rede Management structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ comment")
</dt> </dl>

Comentário ou descrição para este perfil de logon.

</dd> <dt>

**CountryCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ país \_ Code")
</dt> </dl>

Código de país/região para o idioma de escolha do usuário.

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição textual do objeto atual.

Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).

</dd> <dt>

**Sinalizadores**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ flags"), [**bitmap**](../wmisdk/standard-qualifiers.md) ("0", "1", "3", "4", "5", "6", "7", "8", "9", "11", "12", "13", "16", "17", "18", "19", "20", "21", "22", "23"), [**bitvalues**](../wmisdk/standard-qualifiers.md) ("script", "conta desabilitada", "página inicial necessária", "bloqueio", "senha não necessária", "paswword não pode mudar", "senha de teste criptografada permitida", "conta duplicada temporária", "conta normal", "conta de confiança entre domínios", "conta de confiança de estação de trabalho", "conta de confiança do servidor", "não expirar senha", "conta de logon MNS", "cartão inteligente necessário", "confiável para delegação", "não delegado", "usar somente chave des", "não exigir preautoria", "senha expirada")
</dt> </dl>

As propriedades disponíveis para este perfil de rede.

As propriedades que podem ser definidas incluem:

<dt>

1 (0x1)
</dt> <dd>

Script

Um script de logon executado. Esse valor deve ser definido para o Gerenciador de LAN 2,0.

</dd> <dt>

2 (0x2)
</dt> <dd>

Conta desabilitada

A conta do usuário está desabilitada.

</dd> <dt>

8 (0x8)
</dt> <dd>

Diretório base necessário

Um diretório base é necessário.

</dd> <dt>

16 (0x10)
</dt> <dd>

Bloquear

A conta está bloqueada no momento. Para [**NetUserSetInfo**](/windows/win32/api/lmaccess/nf-lmaccess-netusersetinfo), esse valor pode ser limpo para desbloquear uma conta bloqueada anteriormente. Esse valor não pode ser usado para bloquear uma conta desbloqueada anteriormente.

</dd> <dt>

32 (0x20)
</dt> <dd>

Senha não necessária

Nenhuma senha é necessária.

</dd> <dt>

64 (0x40)
</dt> <dd>

A senha não pode ser alterada

O usuário não pode alterar a senha.

</dd> <dt>

128 (0x80)
</dt> <dd>

Senha de teste criptografada permitida

</dd> <dt>

256 (0x100)
</dt> <dd>

Conta duplicada temporária

Uma conta para usuários cuja conta primária está em outro domínio. Essa conta fornece acesso de usuário a esse domínio, mas não a qualquer domínio que confie nesse domínio. O gerente de usuário refere-se a esse tipo de conta como uma conta de usuário local.

</dd> <dt>

512 (0x200)
</dt> <dd>

Conta normal

Tipo de conta padrão que representa um usuário típico.

</dd> <dt>

2048 (0x800)
</dt> <dd>

Conta de confiança entre domínios

Uma permissão para uma conta de confiança para um domínio que confia em outros domínios.

</dd> <dt>

4096 (0x1000)
</dt> <dd>

Conta de confiança da estação de trabalho

Uma conta de computador para uma Windows de trabalho ou servidor que seja membro desse domínio.

</dd> <dt>

8192 (0x2000)
</dt> <dd>

Conta de Confiança do Servidor

Uma conta de computador para um controlador de domínio de backup que seja membro desse domínio.

</dd> <dt>

65536 (0x10000)
</dt> <dd>

Não expirar senha

</dd> <dt>

131072 (0x20000)
</dt> <dd>

Conta de Logon do MNS

Tipo de conta de logon MNS (Majority Node Set) que representa um usuário MNS.

</dd> <dt>

262144 (0x40000)
</dt> <dd>

Cartão inteligente necessário

</dd> <dt>

524288 (0x80000)
</dt> <dd>

Confiável para delegação

</dd> <dt>

1048576 (0x100000)
</dt> <dd>

Não Delegado

</dd> <dt>

2097152 (0x200000)
</dt> <dd>

Usar somente chave DES

</dd> <dt>

4194304 (0x400000)
</dt> <dd>

Não exigir pré-autorização

</dd> <dt>

8388608 (0x800000)
</dt> <dd>

Senha expirada

Indica que a senha expirou.

</dd> </dl>

As propriedades a seguir descrevem o tipo de conta. Somente um valor pode ser definido:

-   CONTA NORMAL DA UF \_ \_
-   CONTA \_ \_ DUPLICADA TEMP DA UF \_
-   CONTA CONFIÁVEL DA ESTAÇÃO \_ \_ DE TRABALHO \_ DA UF
-   CONTA \_ DE CONFIANÇA DO \_ SERVIDOR \_ DA UNIVERSIDADE
-   CONTA \_ DE CONFIANÇA INTERDOMÍNIO \_ \_ DA UNIVERSIDADE

</dd> <dt>

**FullName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ full \_ name")
</dt> </dl>

Nome completo do usuário que pertence ao perfil de logon de rede. Essa cadeia de caracteres poderá estar vazia se o usuário optar por não associar um nome completo a um nome de usuário.

</dd> <dt>

**HomeDirectory**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ home \_ dir")
</dt> </dl>

Caminho para o diretório home do usuário. Essa cadeia de caracteres poderá estar vazia se o usuário optar por não especificar um diretório home.

Exemplo:" \\ HOMEDIR"

</dd> <dt>

**HomeDirectoryDrive**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ home dir \_ \_ drive")
</dt> </dl>

Letra da unidade atribuída ao diretório base do usuário para fins de log.

Exemplo: "C:"

</dd> <dt>

**LastLogoff**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ last \_ logoff")
</dt> </dl>

O usuário registrou o sistema pela última vez. Esse valor é calculado com base no número de segundos decorridos desde 00:00:00, 1º de janeiro de 1970. Um valor de " \* \* \* \* \* \* \* \* \* \* \* \* \* \* . \* \* \* \* \* \* + \* \* \* " significa que a hora do último logoff é desconhecida. O formato desse valor é yyyymmddhhmmss.mmmmmm sutc. Para obter informações sobre como traduzir essa propriedade para a hora local, consulte [Tarefas WMI: datas e horas.](../wmisdk/wmi-tasks--dates-and-times.md)

Exemplo: 19521201000230.000000 000

</dd> <dt>

**LastLogon**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ last \_ logon")
</dt> </dl>

O usuário logou pela última vez no sistema. Esse valor é calculado com base no número de segundos decorridos desde 00:00:00, 1º de janeiro de 1970. O formato desse valor é yyyymmddhhmmss.mmmmmm sutc. Para obter informações sobre como traduzir essa propriedade para a hora local, consulte [Tarefas WMI: datas e horas.](../wmisdk/wmi-tasks--dates-and-times.md)

Exemplo: 19521201000230.000000 000

</dd> <dt>

**LogonHours**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (147), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ logon \_ hours")
</dt> </dl>

Horários durante a semana em que o usuário pode fazer logoff. Cada bit representa uma unidade de tempo especificada pela **propriedade UnitsPerWeek.** Por exemplo, se a unidade de tempo for por hora, o primeiro bit (bit 0, palavra 0) será domingo, 0:00 a 0:59, o segundo bit (bit 1, palavra 0) é domingo, 1:00 a 1:59 e assim por diante. Se esse membro for definido como **NULL,** não haverá nenhuma restrição de tempo. A hora é definida como GMT e deve ser ajustada para outros fusos horários (por exemplo, GMT menos 8 horas para PST).

</dd> <dt>

**LogonServer**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ logon \_ server")
</dt> </dl>

Nome do servidor para o qual as solicitações de logon são enviadas. Os nomes de servidor devem ser precedido por duas malhas in-back ( \\ \\ ). Um nome de servidor com um asterisco ( ) indica que a solicitação de logon pode ser tratada \\ \\ \* por qualquer servidor de logon. Uma cadeia de caracteres nula indica que as solicitações são enviadas ao controlador de domínio.

Exemplo: \\ \\ "MyServer"

</dd> <dt>

**MaximumStorage**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ max \_ storage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Quantidade máxima de espaço em disco disponível para o usuário. Se MaximumStorage estiver definido como USER MAXSTORAGE UNLIMITED, o usuário poderá usar todo \_ o espaço em disco \_ disponível.

Exemplo: 10000000

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management estruturas \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ name")
</dt> </dl>

Conta de usuário em um determinado domínio ou computador. O número de caracteres no nome não pode exceder o valor de UNLEN.

Exemplo: "algumdomínio \\ davibarros"

</dd> <dt>

**NumberOfLogons**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management estruturas \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ num \_ logons")
</dt> </dl>

Número de vezes com êxito que o usuário tentou fazer logon nesta conta. Um valor de 0xFFFFFFFF indica que o valor é desconhecido. Essa propriedade é mantida separadamente em cada BDC (controlador de domínio de backup) no domínio. Para obter um valor preciso, somente o maior valor de todos os BDCs deve ser usado.

Exemplo: 4

</dd> <dt>

**Parâmetros**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| Gerenciamento de rede de estruturas de \| [**usuário \_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ parms")
</dt> </dl>

Espaço reservado para uso por aplicativos. Essa cadeia de caracteres pode ser nula ou pode ter qualquer número de caracteres antes do caractere nulo de terminação. Os produtos da Microsoft usam esse membro para armazenar informações de configuração do usuário. Não modifique essas informações, pois esse valor é específico de um aplicativo.

</dd> <dt>

**Senha**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| Gerenciamento de rede de estruturas de \| [**usuário \_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 duração da \_ senha \_ ")
</dt> </dl>

Período de tempo em que uma senha esteve em vigor. Esse valor é medido a partir do número de segundos decorridos desde a última alteração da senha.

Exemplo: 1201000230, 0 000

</dd> <dt>

**PasswordExpires**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| estruturas de gerenciamento de rede de \| [**usuário \_ modal \_ info \_ 0**](/windows/win32/api/lmaccess/ns-lmaccess-user_modals_info_0) \| usrmod0 \_ Max \_ passwd \_ age")
</dt> </dl>

Data e hora em que a senha expira. O valor é definido neste formato: AAAAMMDDHHMMSS. mmmmmm sutc

Exemplo: 19521201000230, 0 000

</dd> <dt>

**PrimaryGroupId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management estruturas \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Primary \_ Group \_ ID")
</dt> </dl>

O identificador relativo (RID) do grupo global primário deste usuário. O identificador verifica o grupo primário ao qual o perfil do usuário pertence.

</dd> <dt>

**Privilégios**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ priv")
</dt> </dl>

Nível de privilégio atribuído à propriedade **de \_ nome usri3** .

<dt>

<span id="Guest"></span><span id="guest"></span><span id="GUEST"></span>

**Convidado** (0)


</dt> <dd></dd> <dt>

<span id="User"></span><span id="user"></span><span id="USER"></span>

**Usuário** (1)


</dt> <dd></dd> <dt>

<span id="Administrator"></span><span id="administrator"></span><span id="ADMINISTRATOR"></span>

**Administrador** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Perfil**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Profile")
</dt> </dl>

Caminho para o perfil do usuário. Esse valor pode ser uma cadeia de caracteres nula, um caminho absoluto local ou um caminho UNC. Um perfil de usuário contém configurações que são personalizáveis para cada usuário, como as cores da área de trabalho.

Exemplo: "C: \\ Windows"

</dd> <dt>

**ScriptPath**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| rede Management structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ script \_ caminho")
</dt> </dl>

Caminho do diretório para o script de logon do usuário. Um script de logon executa automaticamente um conjunto de comandos sempre que um usuário faz logon em um sistema.

Exemplo: "C: \\ Win \\ Profiles \\ ThomasSteven"

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificador pelo qual o objeto atual é conhecido.

Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).

</dd> <dt>

**UnitsPerWeek**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management estruturas \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ unidades \_ por \_ semana")
</dt> </dl>

Número de unidades de tempo em que a semana está dividida. Ele é usado com a propriedade **LogonHours** para limitar o acesso do usuário ao computador.

Exemplo: 168 (horas por semana)

</dd> <dt>

**UserComment**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| rede Management structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ usr \_ Comentário")
</dt> </dl>

Descrição ou comentário definido pelo usuário para este perfil.

</dd> <dt>

**UserId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| rede Management structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ user \_ ID")
</dt> </dl>

RID do usuário. O identificador verifica se o usuário existe e se é exclusivo para esse domínio.

</dd> <dt>

**UserType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ flags")
</dt> </dl>

Tipo de conta à qual o usuário tem privilégios.

Os valores são:

-   "Conta normal"
-   "Conta duplicada"
-   "Conta de confiança da estação de trabalho"
-   "Conta de confiança do servidor"
-   "Conta de confiança entre domínios"
-   "Desconhecido"

<dt>

<span id="Normal_Account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

**Conta normal** ("Conta Normal")


</dt> <dd></dd> <dt>

<span id="Duplicate_Account"></span><span id="duplicate_account"></span><span id="DUPLICATE_ACCOUNT"></span>

**Conta duplicada** ("conta duplicada")


</dt> <dd></dd> <dt>

<span id="Workstation_Trust_Account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

**Conta de confiança da estação de trabalho** ("Conta de Confiança da Estação de Trabalho")


</dt> <dd></dd> <dt>

<span id="Server_Trust_Account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

**Conta de Confiança do Servidor** ("Conta de Confiança do Servidor")


</dt> <dd></dd> <dt>

<span id="Interdomain_Trust_Account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

**Conta de confiança entre domínios** ("conta de confiança entre domínios")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** ("Desconhecido")


</dt> <dd></dd> </dl>

</dd> <dt>

**Estações**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ workstations")
</dt> </dl>

Nomes de estações de trabalho das quais o usuário pode fazer logoff. Até oito estações de trabalho podem ser especificadas; os nomes devem ser separados por vírgulas (,). Uma cadeia de caracteres nula não indica nenhuma restrição. Para desabilitar logons de todas as estações de trabalho para essa conta, de definido como UF ACCOUNTDISABLE na propriedade \_ **Flags** dessa classe.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ NetworkLoginProfile do Win32** é derivada da [**configuração cim \_**](cim-setting.md).

O processo de chamada que usa essa classe deve ter ES **\_ privilégio RESTORE \_ NAME** no computador no qual o Registro reside. Para obter mais informações, consulte [Executando operações privilegiadas.](../wmisdk/executing-privileged-operations.md)

## <a name="examples"></a>Exemplos

O [exemplo Listar Perfis de Logon](https://Gallery.TechNet.Microsoft.Com/4b84fb8a-964e-4811-98d2-de1009685a14) de Rede do PowerShell retorna informações de logon de rede para todos os usuários de um computador.

O exemplo de VBScript a seguir retorna informações de logon de rede.


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_NetworkLoginProfile") 
 
For Each objItem in colItems 
    dtmWMIDate = objItem.AccountExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Account Expires: " & strReturn 
    Wscript.Echo "Authorization Flags: " & objItem.AuthorizationFlags 
    Wscript.Echo "Bad Password Count: " & objItem.BadPasswordCount 
    Wscript.Echo "Caption: " & objItem.Caption 
    Wscript.Echo "CodePage: " & objItem.CodePage 
    Wscript.Echo "Comment: " & objItem.Comment 
    Wscript.Echo "Country Code: " & objItem.CountryCode 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Flags: " & objItem.Flags 
    Wscript.Echo "Full Name: " & objItem.FullName 
    Wscript.Echo "Home Directory: " & objItem.HomeDirectory 
    Wscript.Echo "Home Directory Drive: " & objItem.HomeDirectoryDrive 
    dtmWMIDate = objItem.LastLogoff 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logoff: " & strReturn 
    dtmWMIDate = objItem.LastLogon 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logon: " & strReturn 
    Wscript.Echo "Logon Hours: " & objItem.LogonHours 
    Wscript.Echo "Logon Server: " & objItem.LogonServer 
    Wscript.Echo "Maximum Storage: " & objItem.MaximumStorage 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Number Of Logons: " & objItem.NumberOfLogons 
    Wscript.Echo "Password Age: " & objItem.PasswordAge 
    dtmWMIDate = objItem.PasswordExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Password Expires: " & strReturn 
    Wscript.Echo "Primary Group ID: " & objItem.PrimaryGroupId 
    Wscript.Echo "Privileges: " & objItem.Privileges 
    Wscript.Echo "Profile: " & objItem.Profile 
    Wscript.Echo "Script Path: " & objItem.ScriptPath 
    Wscript.Echo "Setting ID: " & objItem.SettingID 
    Wscript.Echo "Units Per Week: " & objItem.UnitsPerWeek 
    Wscript.Echo "User Comment: " & objItem.UserComment 
    Wscript.Echo "User Id: " & objItem.UserId 
    Wscript.Echo "User Type: " & objItem.UserType 
    Wscript.Echo "Workstations: " & objItem.Workstations 
    Wscript.Echo 
Next 
  
Function WMIDateStringToDate(dtmWMIDate) 
    If Not IsNull(dtmWMIDate) Then 
    WMIDateStringToDate = CDate(Mid(dtmWMIDate, 5, 2) & "/" & _ 
         Mid(dtmWMIDate, 7, 2) & "/" & Left(dtmWMIDate, 4) _ 
             & " " & Mid (dtmWMIDate, 9, 2) & ":" & _ 
                 Mid(dtmWMIDate, 11, 2) & ":" & Mid(dtmWMIDate, 13, 2)) 
    End If 
End Function 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configuração cim \_**](cim-setting.md)
</dt> <dt>

[Classes do sistema operacional](./operating-system-classes.md)
</dt> </dl>

 

 
