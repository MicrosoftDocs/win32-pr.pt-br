---
title: Classe Win32_TSGeneralSetting
description: Representa as configurações gerais do terminal, como o nível de criptografia e o protocolo de transporte.
ms.assetid: a31d68c0-e446-4d78-85e0-5173e7870255
ms.tgt_platform: multiple
keywords:
- Win32_TSGeneralSetting classe Serviços de Área de Trabalho Remota
- Win32_TSGeneralSetting classe Serviços de Área de Trabalho Remota , descrito
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting
- Win32_TSGeneralSetting.Caption
- Win32_TSGeneralSetting.Description
- Win32_TSGeneralSetting.InstallDate
- Win32_TSGeneralSetting.Name
- Win32_TSGeneralSetting.Status
- Win32_TSGeneralSetting.TerminalName
- Win32_TSGeneralSetting.CertificateName
- Win32_TSGeneralSetting.Certificates
- Win32_TSGeneralSetting.Comment
- Win32_TSGeneralSetting.MinEncryptionLevel
- Win32_TSGeneralSetting.PolicySourceMinEncryptionLevel
- Win32_TSGeneralSetting.PolicySourceSecurityLayer
- Win32_TSGeneralSetting.PolicySourceUserAuthenticationRequired
- Win32_TSGeneralSetting.SecurityLayer
- Win32_TSGeneralSetting.SSLCertificateSHA1Hash
- Win32_TSGeneralSetting.SSLCertificateSHA1HashType
- Win32_TSGeneralSetting.TerminalProtocol
- Win32_TSGeneralSetting.Transport
- Win32_TSGeneralSetting.UserAuthenticationRequired
- Win32_TSGeneralSetting.WindowsAuthentication
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2cc2e7ede46b503e0d33f65c5735d5e0cc653a75184384be2d706bfc8ac9cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999806"
---
# <a name="win32_tsgeneralsetting-class"></a>Classe Win32 \_ TSGeneralSetting

A classe WMI **Win32 \_ TSGeneralSetting** representa configurações gerais do terminal, como o nível de criptografia e o protocolo de transporte.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas e herdadas, em ordem alfabética. Para obter informações de referência sobre métodos, consulte a tabela de métodos mais adiante neste tópico.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_WIN32_TSGENERALSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSGeneralSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   CertificateName;
  uint8    Certificates[];
  string   Comment;
  uint32   MinEncryptionLevel;
  uint32   PolicySourceMinEncryptionLevel;
  uint32   PolicySourceSecurityLayer;
  uint32   PolicySourceUserAuthenticationRequired;
  uint32   SecurityLayer;
  string   SSLCertificateSHA1Hash;
  uint32   SSLCertificateSHA1HashType;
  string   TerminalProtocol;
  string   Transport;
  uint32   UserAuthenticationRequired;
  uint32   WindowsAuthentication;
};
```

## <a name="members"></a>Membros

A **classe Win32 \_ TSGeneralSetting** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe Win32 \_ TSGeneralSetting** tem esses métodos.



| Método                                                                                        | Descrição                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetEncryptionLevel**](win32-tsgeneralsetting-setencryptionlevel.md)                       | Define o nível de criptografia.<br/>                                                                                                                                   |
| [**SetSecurityLayer**](win32-tsgeneralsetting-setsecuritylayer.md)                           | Define a camada de segurança como uma da "Camada de Segurança RDP" (0), "Negociar" (1) ou "SSL" (2).<br/>                                                                   |
| [**SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) | Habilita ou desabilita o requisito de que os usuários devem ser autenticados no momento da conexão definindo o valor da **propriedade UserAuthenticationRequired.**<br/> |



 

### <a name="properties"></a>Propriedades

A **classe Win32 \_ TSGeneralSetting** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Descrição curta (cadeia de caracteres de uma linha) do objeto.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**CertificateName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome de exibição para o nome da assunto do certificado pessoal do computador local.

</dd> <dt>

**Certificados**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Contém um armazenamento de certificados serializado que  contém todos os certificados do meu armazenamento de conta de usuário no computador que são certificados de servidor válidos para uso com sSL (secure sockets layer).

</dd> <dt>

**Comentário**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Nome descritivo da combinação de protocolo de transporte e camada de sessão.

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição do objeto.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5")
</dt> </dl>

A data em que o objeto foi instalado. A falta de um valor não indica que o objeto não está instalado.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**MinEncryptionLevel**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **baixo** ("somente os dados enviados do cliente para o servidor são protegidos pela criptografia com base na força da chave padrão do servidor. Os dados enviados do Servidor para o cliente não estão protegidos."), **Médio** ("Todos os dados enviados entre o servidor e o cliente são protegidos pela criptografia com base na força da chave padrão do servidor."), **Alto** ("Todos os dados enviados entre o servidor e o cliente são protegidos pela criptografia com base na força máxima da chave do servidor").
</dt> </dl>

O nível mínimo de criptografia.

<dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>**Baixo** (1)


</dt> <dd>

Baixo nível de criptografia. Somente os dados enviados do cliente para o servidor são criptografados usando criptografia de 56 bits. Esteja ciente de que os dados enviados do servidor para o cliente não são criptografados.

</dd> <dt>

<span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>

<span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>**Compatível com cliente/médio** (2)


</dt> <dd>

Nível de criptografia compatível com o cliente. Todos os dados enviados do cliente para o servidor e do servidor para o cliente são criptografados no nível máximo de chave com suporte pelo cliente.

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**Alto** (3)


</dt> <dd>

Alto nível de criptografia. Todos os dados enviados do cliente para o servidor e do servidor para o cliente são criptografados usando criptografia forte de 128 bits. Os clientes que não suportam esse nível de criptografia não podem se conectar.

</dd> <dt>

<span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>

<span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>**Compatível com FIPS** (4)


</dt> <dd>

Criptografia em conformidade com FIPS. Todos os dados enviados do cliente para o servidor e do servidor para o cliente são criptografados e descriptografados com os algoritmos de criptografia FIPS (padrão FIPS) usando os módulos criptográficos da Microsoft. FIPS é um padrão intitulado "Requisitos de segurança para módulos criptográficos". FIPS 140-1 (1994) e FIPS 140-2 (2001) descrevem os requisitos governamentais para módulos criptográficos de hardware e software usados no governo dos EUA.

</dd> </dl>

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do objeto.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**PolicySourceMinEncryptionLevel**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a **propriedade MinEncryptionLevel** está configurada pelo servidor, pela política de grupo ou por padrão.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> <dt>

2 (0x2)
</dt> <dd>

Padrão

</dd> </dl>

</dd> <dt>

**PolicySourceSecurityLayer**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a **propriedade SecurityLayer** está configurada pelo servidor, por política de grupo ou por padrão.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> <dt>

2 (0x2)
</dt> <dd>

Padrão

</dd> </dl>

</dd> <dt>

**PolicySourceUserAuthenticationRequired**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a **propriedade UserAuthenticationRequired** está configurada pelo servidor, por política de grupo ou por padrão.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> <dt>

2 (0x2)
</dt> <dd>

Padrão

</dd> </dl>

</dd> <dt>

**SecurityLayer**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **RDPSecurityLayer** ("Camada de Segurança RDP: Comunicação entre o servidor e o cliente usará criptografia RDP nativa."), **Negotiate** ("A camada mais segura com suporte pelo cliente será usada. Se tiver suporte, o TLS 1.0 será usado."), **SSL** ("SSL (TLS 1.0) será usado para autenticação de servidor, bem como para criptografar todos os dados transferidos entre o servidor e o cliente. Essa configuração exige que o servidor tenha um certificado compatível com SSL."), **NEWTBD** ("UMA NOVA CAMADA DE SEGURANÇA em LONG LTDA.")
</dt> </dl>

Especifica a camada de segurança usada entre o cliente e o servidor.

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**Camada de segurança RDP** (1)


</dt> <dd>

A comunicação entre o servidor e o cliente usa criptografia RDP nativa.

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negociar** (2)


</dt> <dd>

A camada mais segura com suporte pelo cliente é usada. Se tiver suporte, o SSL (TLS 1.0) será usado.

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span id="SSL"></span><span id="ssl"></span>**SSL** (3)


</dt> <dd>

O SSL (TLS 1.0) é usado para autenticação de servidor e para criptografar todos os dados transferidos entre o servidor e o cliente. Essa configuração exige que o servidor tenha um certificado compatível com SSL. Essa configuração não é compatível com um **valor MinEncryptionLevel** de 1.

</dd> <dt>

<span id="NEWTBD"></span><span id="newtbd"></span>

<span id="NEWTBD"></span><span id="newtbd"></span>**NEWTBD** (4)


</dt> <dd>

Uma nova camada de segurança.

</dd> </dl>

</dd> <dt>

**SSLCertificateSHA1Hash**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Especifica o hash SHA1 no formato hexadecimal do certificado SSL para o servidor de destino usar.

A impressão digital de um certificado pode ser encontrada usando o snap-in Certificados do MMC na guia Detalhes da página de propriedades do certificado.

</dd> <dt>

**SSLCertificateSHA1HashType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o estado da propriedade **SSLCertificateSHA1Hash.**

<dt>

0 (0x0)
</dt> <dd>

Não válido

</dd> <dt>

1 (0x1)
</dt> <dd>

Auto-assinado padrão

</dd> <dt>

2 (0x2)
</dt> <dd>

Política de grupo padrão imposta

</dd> <dt>

3 (0x3)
</dt> <dd>

Personalizado

</dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Status atual do objeto. Vários status operacionais e não operacionais podem ser definidos. Os status operacionais incluem: "OK", "Degradado" e "Pred Fail" (um elemento, como uma unidade de disco rígido habilitada para SMART, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo). Os status nãooperacionais incluem: "Error", "Starting", "Stopping" e "Service". O último, "Serviço", pode ser aplicado durante o espelhamento de um disco, o recarregamento de uma lista de permissões de usuário ou outro trabalho administrativo. Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros estados.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

<dt>



 ("OK")


</dt> <dd></dd> <dt>



 ("Erro")


</dt> <dd></dd> <dt>



 ("Degradado")


</dt> <dd></dd> <dt>



 ("Desconhecido")


</dt> <dd></dd> <dt>



 ("Pred Fail")


</dt> <dd></dd> <dt>



 ("Iniciando")


</dt> <dd></dd> <dt>



 ("Parando")


</dt> <dd></dd> <dt>



 ("Serviço")


</dt> <dd></dd> </dl>

</dd> <dt>

**TerminalName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do terminal.

Essa propriedade é herdada de [**\_ TerminalSetting do Win32.**](win32-terminalsetting.md)

</dd> <dt>

**TerminalProtocol**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do protocolo de camada de sessão; por exemplo, Microsoft RDP 5.0.

</dd> <dt>

**Transporte**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tipo de transporte usado na conexão; por exemplo, TCP, NetBIOS ou IPX/SPX.

</dd> <dt>

**UserAuthenticationRequired**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica o tipo de autenticação de usuário usado para conexões remotas. Se definido como 1, o que significa habilitado, **UserAuthenticationRequired** exigirá a autenticação do usuário no momento da conexão para aumentar a proteção do servidor contra ataques de rede. Somente [protocolo RDP](remote-desktop-protocol.md) (RDP) que suportam RDP versão 6.0 ou superior podem se conectar. Para evitar interrupções para usuários remotos, é recomendável implantar clientes RDP que deem suporte à versão de protocolo apropriada antes de habilitar a propriedade.

Use o [**método SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) para habilitar ou desabilitar essa propriedade.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

A autenticação do usuário na conexão está desabilitada.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

A autenticação do usuário na conexão está habilitada.

</dd> </dl>

</dd> <dt>

**WindowsAuthentication**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Especifica se a conexão assume como padrão o processo de autenticação Windows padrão ou para outro pacote de autenticação instalado no sistema.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Não assume como padrão o processo de autenticação Windows padrão.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

O padrão é o processo de autenticação Windows padrão.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentários

Esteja ciente de que as estações de janela não associadas à sessão de console não podem acessar os métodos e as propriedades dessa classe. Se for feita uma tentativa de fazer isso especificando "Console" como o valor da propriedade TerminalName, os métodos desse objeto retornarão **WBEM \_ E \_ NOT \_ SUPPORTED**. Esse código de erro também será retornado se uma estação de janela tentar chamar métodos desse objeto com a finalidade de adicionar ou modificar as propriedades de segurança das contas LocalSystem, LocalService ou NetworkService.

Para se conectar ao \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote. Para chamadas C/C++, esse é um nível de autenticação **da \_ \_ privacidade do \_ PCT no \_ nível \_ do autenticação RPC C**. para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "pktPrivacy", com um valor de 6. o exemplo a seguir Visual Basic scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TerminalSetting Win32**](win32-terminalsetting.md)
</dt> </dl>

 

