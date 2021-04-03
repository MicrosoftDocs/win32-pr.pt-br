---
title: Classe Win32_TSGeneralSetting
description: Representa as configurações gerais do terminal, como o nível de criptografia e o protocolo de transporte.
ms.assetid: a31d68c0-e446-4d78-85e0-5173e7870255
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSGeneralSetting Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSGeneralSetting classe, descrita
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
ms.openlocfilehash: 172f18bbddd364d74dfcfb00e7e665628267af36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644718"
---
# <a name="win32_tsgeneralsetting-class"></a>\_Classe Win32 TSGeneralSetting

A classe WMI **\_ TSGeneralSetting do Win32** representa as configurações gerais do terminal, como o nível de criptografia e o protocolo de transporte.

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

A classe **Win32 \_ TSGeneralSetting** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ TSGeneralSetting** tem esses métodos.



| Método                                                                                        | Descrição                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetEncryptionLevel**](win32-tsgeneralsetting-setencryptionlevel.md)                       | Define o nível de criptografia.<br/>                                                                                                                                   |
| [**SetSecurityLayer**](win32-tsgeneralsetting-setsecuritylayer.md)                           | Define a camada de segurança como uma "camada de segurança RDP" (0), "Negotiate" (1) ou "SSL" (2).<br/>                                                                   |
| [**SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) | Habilita ou desabilita o requisito de que os usuários devem ser autenticados no momento da conexão, definindo o valor da propriedade **UserAuthenticationRequired** .<br/> |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ TSGeneralSetting** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrição (cadeia de caracteres de uma linha) do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**CertificateName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome de exibição do nome da entidade do certificado pessoal do computador local.

</dd> <dt>

**Certificados**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Contém um repositório de certificados serializado que contém todos os certificados do repositório de **contas do meu usuário** no computador que são certificados de servidor válidos para uso com SSL (Secure Sockets Layer).

</dd> <dt>

**Comentário**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Nome descritivo da combinação de camada de sessão e protocolo de transporte.

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")
</dt> </dl>

A data em que o objeto foi instalado. A falta de um valor não indica que o objeto não está instalado.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**MinEncryptionLevel**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **baixo** ("somente os dados enviados do cliente para o servidor são protegidos pela criptografia com base na intensidade de chave padrão do servidor. Os dados enviados do servidor para o cliente não estão protegidos. "), **médio** (" todos os dados enviados entre o servidor e o cliente são protegidos pela criptografia com base na intensidade de chave padrão do servidor. "), **alta** (" todos os dados enviados entre o servidor e o cliente são protegidos pela criptografia de chave máxima baseada no servidor. ")
</dt> </dl>

O nível mínimo de criptografia.

<dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>**Baixo** (1)


</dt> <dd>

Nível baixo de criptografia. Somente os dados enviados do cliente para o servidor são criptografados usando a criptografia de 56 bits. Lembre-se de que os dados enviados do servidor para o cliente não são criptografados.

</dd> <dt>

<span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>

<span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>**Compatível com médio/cliente** (2)


</dt> <dd>

Nível de criptografia compatível com o cliente. Todos os dados enviados do cliente para o servidor e do servidor para o cliente são criptografados na força de chave máxima com suporte do cliente.

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**Alta** (3)


</dt> <dd>

Alto nível de criptografia. Todos os dados enviados do cliente para o servidor e do servidor para o cliente são criptografados usando criptografia de 128 bits de alta segurança. Os clientes que não dão suporte a esse nível de criptografia não podem se conectar.

</dd> <dt>

<span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>

<span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>**Compatível com FIPS** (4)


</dt> <dd>

Criptografia compatível com FIPS. Todos os dados enviados do cliente para o servidor e do servidor para o cliente são criptografados e descriptografados com os algoritmos de criptografia do padrão FIPS (FIPS) usando os módulos criptográficos da Microsoft. O FIPS é um padrão intitulado "requisitos de segurança para módulos criptográficos". O FIPS 140-1 (1994) e o FIPS 140-2 (2001) descrevem os requisitos governamentais dos módulos de criptografia de hardware e software usados no governo dos EUA.

</dd> </dl>

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**PolicySourceMinEncryptionLevel**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **MinEncryptionLevel** está configurada pelo servidor, por política de grupo ou por padrão.

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

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **SecurityLayer** está configurada pelo servidor, por política de grupo ou por padrão.

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

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **UserAuthenticationRequired** está configurada pelo servidor, por política de grupo ou por padrão.

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

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **RDPSecurityLayer** ("camada de segurança de RDP: comunicação entre o serverand o cliente usará a criptografia RDP nativa."), **Negotiate** ("a camada mais segura com suporte do cliente será usada. Se houver suporte, o TLS 1,0 será usado. "), o **SSL** (" SSL (TLS 1,0) será usado para autenticação de servidor, bem como forencrypting todos os dados transferidos entre o servidor e o cliente. Essa configuração exige que o servidor tenha um certificado compatível com SSL. "), **NEWTBD** (" uma nova camada de segurança no Longhorn. ")
</dt> </dl>

Especifica a camada de segurança usada entre o cliente e o servidor.

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**Camada de segurança RDP** (1)


</dt> <dd>

A comunicação entre o servidor e o cliente usa a criptografia RDP nativa.

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negociar** (2)


</dt> <dd>

A camada mais segura com suporte do cliente é usada. Se houver suporte, o SSL (TLS 1,0) será usado.

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span id="SSL"></span><span id="ssl"></span>**SSL** (3)


</dt> <dd>

SSL (TLS 1,0) é usado para autenticação de servidor e para criptografar todos os dados transferidos entre o servidor e o cliente. Essa configuração requer que o servidor tenha um certificado compatível com SSL. Essa configuração não é compatível com um valor de **MinEncryptionLevel** de 1.

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

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica o hash SHA1 no formato hexadecimal do certificado SSL para o servidor de destino a ser usado.

A impressão digital de um certificado pode ser encontrada usando o snap-in de certificados do MMC na guia detalhes da página Propriedades do certificado.

</dd> <dt>

**SSLCertificateSHA1HashType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o estado da propriedade **SSLCertificateSHA1Hash** .

<dt>

0 (0x0)
</dt> <dd>

Inválido

</dd> <dt>

1 (0x1)
</dt> <dd>

Padrão autoassinado

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

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Status atual do objeto. Vários status de operação e não operacional podem ser definidos. Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo). Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço". O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo. Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

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

**Terminalname**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do terminal.

Esta propriedade é herdada do [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).

</dd> <dt>

**TerminalProtocol**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do protocolo de camada de sessão; por exemplo, Microsoft RDP 5,0.

</dd> <dt>

**Transport**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tipo de transporte usado na conexão; por exemplo, TCP, NetBIOS ou IPX/SPX.

</dd> <dt>

**UserAuthenticationRequired**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica o tipo de autenticação de usuário usado para conexões remotas. Se definido como 1, o que significa habilitado, o **UserAuthenticationRequired** exigirá a autenticação do usuário no momento da conexão para aumentar a proteção do servidor contra ataques à rede. Somente clientes [protocolo RDP](remote-desktop-protocol.md) (RDP) que oferecem suporte a rdp versão 6,0 ou superior são capazes de se conectar. Para evitar interrupções para usuários remotos, é recomendável implantar clientes RDP que dão suporte à versão de protocolo apropriada antes de habilitar a propriedade.

Use o método [**SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) para habilitar ou desabilitar essa propriedade.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

A autenticação do usuário na conexão está desabilitada.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)


</dt> <dd>

A autenticação de usuário na conexão está habilitada.

</dd> </dl>

</dd> <dt>

**WindowsAuthentication**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica se a conexão usa como padrão o processo de autenticação padrão do Windows ou para outro pacote de autenticação que foi instalado no sistema.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

O não usa como padrão o processo de autenticação padrão do Windows.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)


</dt> <dd>

O padrão é o processo de autenticação padrão do Windows.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentários

Lembre-se de que as estações de janela não associadas à sessão de console não podem acessar os métodos e as propriedades dessa classe. Se for feita uma tentativa de fazer isso especificando "console" como o valor da propriedade Terminalname, os métodos desse objeto retornarão o **WBEM \_ E não \_ terão \_ suporte**. Esse código de erro também será retornado se uma estação de janela tentar chamar métodos desse objeto com a finalidade de adicionar ou modificar as propriedades de segurança das contas LocalSystem, LocalService ou NetworkService.

Para se conectar ao \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote. Para chamadas C/C++, esse é um nível de autenticação **da \_ \_ privacidade do \_ PCT no \_ nível \_ do autenticação RPC C**. Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6. O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

