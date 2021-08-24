---
title: Win32_TSDeploymentSettings classe
description: Define as configurações padrão que o Gerenciador RemoteApp usa ao criar arquivos protocolo RDP (RDP).
ms.assetid: b3eeef86-e6cb-40ea-99f8-200c5993f31e
ms.tgt_platform: multiple
keywords:
- Win32_TSDeploymentSettings classe Serviços de Área de Trabalho Remota
- Win32_TSDeploymentSettings classe Serviços de Área de Trabalho Remota , descrito
topic_type:
- apiref
api_name:
- Win32_TSDeploymentSettings
- Win32_TSDeploymentSettings.Caption
- Win32_TSDeploymentSettings.Description
- Win32_TSDeploymentSettings.InstallDate
- Win32_TSDeploymentSettings.Name
- Win32_TSDeploymentSettings.Status
- Win32_TSDeploymentSettings.Port
- Win32_TSDeploymentSettings.FarmName
- Win32_TSDeploymentSettings.GatewayUsage
- Win32_TSDeploymentSettings.GatewayName
- Win32_TSDeploymentSettings.GatewayAuthMode
- Win32_TSDeploymentSettings.GatewayUseCachedCreds
- Win32_TSDeploymentSettings.RequireServerAuth
- Win32_TSDeploymentSettings.ColorBitDepth
- Win32_TSDeploymentSettings.AllowFontSmoothing
- Win32_TSDeploymentSettings.UseMultimon
- Win32_TSDeploymentSettings.RedirectionOptions
- Win32_TSDeploymentSettings.HasCertificate
- Win32_TSDeploymentSettings.CertificateHash
- Win32_TSDeploymentSettings.CertificateIssuedTo
- Win32_TSDeploymentSettings.CertificateIssuedBy
- Win32_TSDeploymentSettings.CertificateExpiresOn
- Win32_TSDeploymentSettings.CustomRDPSettings
- Win32_TSDeploymentSettings.DeploymentRDPSettings
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3f5b5cde779cbd9b8120fa648138611236935080f3517a28a6f19dcee8864b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349304"
---
# <a name="win32_tsdeploymentsettings-class"></a>Classe Win32 \_ TSDeploymentSettings

Define as configurações padrão que o Gerenciador RemoteApp usa ao criar arquivos protocolo RDP (RDP). Essas configurações não afetam nenhum aplicativo publicado ou áreas de trabalho.

## <a name="syntax"></a>Sintaxe

``` syntax
class Win32_TSDeploymentSettings : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  sint32   Port;
  string   FarmName;
  sint32   GatewayUsage;
  string   GatewayName;
  sint32   GatewayAuthMode;
  boolean  GatewayUseCachedCreds;
  boolean  RequireServerAuth;
  sint32   ColorBitDepth;
  boolean  AllowFontSmoothing;
  boolean  UseMultimon;
  sint32   RedirectionOptions;
  boolean  HasCertificate;
  uint8    CertificateHash[];
  string   CertificateIssuedTo;
  string   CertificateIssuedBy;
  string   CertificateExpiresOn;
  string   CustomRDPSettings;
  string   DeploymentRDPSettings;
};
```

## <a name="members"></a>Membros

A **classe Win32 \_ TSDeploymentSettings** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Win32 \_ TSDeploymentSettings** tem essas propriedades.

<dl> <dt>

**AllowFontSmoothing**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Indica se a suavização de fonte deve ser permitida.

</dd> <dt>

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

**CertificateExpiresOn**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

A data em que o certificado expira. Esse valor é armazenado como um formato [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) de 64 bits.

</dd> <dt>

**CertificateHash**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint8**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

A impressão digital do certificado usado para assinar arquivos RDP.

</dd> <dt>

**CertificateIssuedBy**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Especifica por quem o certificado é emitido.

</dd> <dt>

**CertificateIssuedTo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Especifica para quem o certificado é emitido.

</dd> <dt>

**ColorBitDepth**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

A profundidade do bit de cor da exibição. Os valores possíveis são 4, 8, 15, 16, 24 e 32.

</dd> <dt>

**CustomRDPSettings**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O conteúdo do arquivo RDP que corresponde ao RDP personalizado Configurações em Gerenciador RemoteApp.

</dd> <dt>

**DeploymentRDPSettings**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O conteúdo do arquivo RDP que corresponde às configurações de implantação no Gerenciador RemoteApp. Se esse valor for definido, as configurações de implantação de RDP serão as configurações padrão nesta classe. Por exemplo, se você definir a propriedade **GatewayAuthMode** nessa classe e definir a propriedade **DeploymentRDPSettings,** a propriedade **GatewayAuthMode** dessa classe será ignorada e o valor **gatewayAuthMode** de **DeploymentRDPSettings** será usado.

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

**FarmName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O nome do servidor Host da Sessão RD ou o FQDN (nome de domínio totalmente qualificado) do farm Host da Sessão RD servidor.

</dd> <dt>

**GatewayAuthMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O método de autenticação do Gateway de RD. Os valores a seguir são possíveis.

<dt>

0
</dt> <dd>

Senha

</dd> <dt>

1
</dt> <dd>

Cartão inteligente

</dd> <dt>

4
</dt> <dd>

Permitir que o usuário selecione durante a conexão.

</dd> </dl>

</dd> <dt>

**GatewayName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O nome do servidor de Gateway de RD a ser usado.

</dd> <dt>

**GatewayUsage**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Indica se um servidor de Gateway de Área de Trabalho Avançada deve ser usado para se conectar ao servidor Host da Sessão RD destino em um firewall. Os valores a seguir são possíveis.

<dt>

0
</dt> <dd>

Não use um servidor de Gateway de Área de Trabalho Local.

</dd> <dt>

1
</dt> <dd>

Use um servidor de Gateway de Área de Trabalho Remoto. Ignore o servidor do Gateway de Área de Trabalho Local para endereços locais.

</dd> <dt>

2
</dt> <dd>

Use um servidor de Gateway de Área de Trabalho Remoto.

</dd> <dt>

3
</dt> <dd>

Detectar automaticamente as configurações do servidor do Gateway de RD.

</dd> </dl>

</dd> <dt>

**GatewayUseCachedCreds**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Quando possível, use as mesmas credenciais de usuário para o servidor de Gateway de RD e o Host da Sessão RD servidor.

</dd> <dt>

**HasCertificate**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Indica se um certificado deve ser usado para assinar os arquivos RDP.

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

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do objeto.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Porta**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

A porta RDP a ser usada.

</dd> <dt>

**RedirectionOptions**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Especifica as opções de redirecionamento de dispositivo e recurso para conexões remoteApp. Sinalizadores para **RedirectionOptions** podem ser combinados. Os valores a seguir são possíveis.

<dt>

0
</dt> <dd>

Nenhum redirecionamento de dispositivo ou recurso.

</dd> <dt>

1
</dt> <dd>

Redirecionar unidades de disco.

</dd> <dt>

2
</dt> <dd>

Redirecionar impressoras.

</dd> <dt>

4
</dt> <dd>

Redirecione a Área de Transferência.

</dd> <dt>

8
</dt> <dd>

Redirecionar dispositivos Plug and Play suporte.

</dd> <dt>

16
</dt> <dd>

Redirecionar cartões inteligentes.

</dd> <dt>

32
</dt> <dd>

Redirecionar áudio.

</dd> <dt>

64
</dt> <dd>

Redirecionar portas seriais.

</dd> </dl>

</dd> <dt>

**RequireServerAuth**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Indica se a autenticação do servidor deve ser necessária.

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

**UseMulndon**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Indica se vários monitores estão habilitados para a área de trabalho.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para definir propriedades usando essa classe.

Se **RequireServerAuth** estiver definido como **TRUE,** considere o seguinte:

-   Se o programa RemoteApp for para uso na intranet e todos os computadores cliente estão executando o Windows Server 2008 ou o Windows Vista, você não precisa configurar o servidor Host da Sessão RD para usar um certificado SSL. Nesse caso, o Autenticação no Nível da Rede é usado.
-   Você deve especificar o FQDN do servidor ou farm para o valor da **propriedade FarmName.**

Para se conectar ao namespace "CIMV2 \\ TerminalServices", o nível de autenticação deve incluir a privacidade do pacote. Para chamadas C/C++, esse é um nível de autenticação de **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**, que pode ser definido usando a função [**COM CoSetProxyBlanket.**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) Para Visual Basic e scripts, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "pktPrivacy", com um valor de 6. O exemplo Visual Basic VBScript (Scripting Edition) a seguir mostra como se conectar a um computador remoto com privacidade de pacote.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Eles são instalados no computador quando você adiciona a função associada. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow.mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



 

