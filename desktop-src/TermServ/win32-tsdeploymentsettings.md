---
title: Classe Win32_TSDeploymentSettings
description: Define as configurações padrão que o Gerenciador RemoteApp usa ao criar arquivos de protocolo RDP (RDP).
ms.assetid: b3eeef86-e6cb-40ea-99f8-200c5993f31e
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSDeploymentSettings Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSDeploymentSettings classe, descrita
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
ms.openlocfilehash: 0f254363968099ab73c5f3f14f1f15ab8554f62a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455038"
---
# <a name="win32_tsdeploymentsettings-class"></a>\_Classe Win32 TSDeploymentSettings

Define as configurações padrão que o Gerenciador RemoteApp usa ao criar arquivos de protocolo RDP (RDP). Essas configurações não afetam nenhum aplicativo ou área de trabalho publicada.

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

A classe **Win32 \_ TSDeploymentSettings** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ TSDeploymentSettings** tem essas propriedades.

<dl> <dt>

**AllowFontSmoothing**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se a suavização de fonte deve ser permitida.

</dd> <dt>

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

**CertificateExpiresOn**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

A data em que o certificado expira. Esse valor é armazenado como um formato [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) de 64 bits.

</dd> <dt>

**CertificateHash**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

A impressão digital do certificado que é usado para assinar arquivos RDP.

</dd> <dt>

**CertificateIssuedBy**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica a quem o certificado é emitido.

</dd> <dt>

**CertificateIssuedTo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica para quem o certificado é emitido.

</dd> <dt>

**ColorBitDepth**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

A intensidade de bit de cor da exibição. Os valores possíveis são 4, 8, 15, 16, 24 e 32.

</dd> <dt>

**CustomRDPSettings**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O conteúdo do arquivo RDP que corresponde às configurações personalizadas de RDP no Gerenciador RemoteApp.

</dd> <dt>

**DeploymentRDPSettings**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O conteúdo do arquivo RDP que corresponde às configurações de implantação no Gerenciador RemoteApp. Se esse valor for definido, as configurações de implantação de RDP substituirão as configurações padrão nessa classe. Por exemplo, se você definir a propriedade **GatewayAuthMode** nessa classe e definir a propriedade **DeploymentRDPSettings** , a propriedade **GatewayAuthMode** dessa classe será ignorada e o valor **GatewayAuthMode** de **DeploymentRDPSettings** será usado.

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

**Farmname**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O nome do servidor de Host da Sessão RD ou o FQDN (nome de domínio totalmente qualificado) do farm de servidores do Host da Sessão RD.

</dd> <dt>

**GatewayAuthMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O método de autenticação de gateway de área de trabalho remota. Os valores a seguir são possíveis.

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

Tipo de acesso: leitura/gravação
</dt> </dl>

O nome do servidor de gateway de área de trabalho remota a ser usado.

</dd> <dt>

**GatewayUsage**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se um servidor de gateway de área de trabalho remota deve ser usado para se conectar ao servidor de Host da Sessão RD de destino por um firewall. Os valores a seguir são possíveis.

<dt>

0
</dt> <dd>

Não use um servidor de gateway de área de trabalho remota.

</dd> <dt>

1
</dt> <dd>

Use um servidor de gateway de área de trabalho remota. Ignore o servidor de gateway de área de trabalho remota para endereços locais.

</dd> <dt>

2
</dt> <dd>

Use um servidor de gateway de área de trabalho remota.

</dd> <dt>

3
</dt> <dd>

Detectar automaticamente as configurações do servidor Gateway RD.

</dd> </dl>

</dd> <dt>

**GatewayUseCachedCreds**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Quando possível, use as mesmas credenciais de usuário para o servidor de gateway de área de trabalho remota e o servidor de Host da Sessão RD.

</dd> <dt>

**HasCertificate**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se um certificado deve ser usado para assinar os arquivos RDP.

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

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Porta**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

A porta RDP a ser usada.

</dd> <dt>

**Redireçãooptions**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica as opções de redirecionamento de dispositivo e de recurso para conexões do RemoteApp. Os sinalizadores para **redireçãooptions** podem ser combinados. Os valores a seguir são possíveis.

<dt>

0
</dt> <dd>

Nenhum redirecionamento de dispositivo ou recurso.

</dd> <dt>

1
</dt> <dd>

Redirecione unidades de disco.

</dd> <dt>

2
</dt> <dd>

Redirecionar impressoras.

</dd> <dt>

4
</dt> <dd>

Redirecionar a área de transferência.

</dd> <dt>

8
</dt> <dd>

Redirecionar dispositivos Plug and Play com suporte.

</dd> <dt>

16
</dt> <dd>

Redirecionar cartões inteligentes.

</dd> <dt>

32
</dt> <dd>

Redirecione o áudio.

</dd> <dt>

64
</dt> <dd>

Redirecione portas seriais.

</dd> </dl>

</dd> <dt>

**RequireServerAuth**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se a autenticação do servidor deve ser necessária.

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

**UseMultimon**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se vários monitores estão habilitados para a área de trabalho.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para definir propriedades usando essa classe.

Se **RequireServerAuth** for definido como **true**, considere o seguinte:

-   Se o programa do RemoteApp for para uso na intranet e todos os computadores cliente estiverem executando o Windows Server 2008 ou o Windows Vista, você não precisará configurar o servidor de Host da Sessão RD para usar um certificado SSL. Nesse caso, Autenticação no Nível da Rede é usado.
-   Você deve especificar o FQDN do servidor ou farm para o valor da propriedade **farmname** .

Para se conectar ao namespace "CIMV2 \\ TerminalServices", o nível de autenticação deve incluir a privacidade do pacote. Para chamadas C/C++, esse é um nível de autenticação **de \_ \_ privacidade do \_ PCT no \_ nível \_** de autenticado RPC C, que pode ser definido usando a função com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) . Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6. O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Eles são instalados no computador quando você adiciona a função associada. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow. mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



 

