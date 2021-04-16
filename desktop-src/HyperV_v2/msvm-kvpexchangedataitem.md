---
description: Representa um par de chave/valor.
ms.assetid: B13E9C5F-5B13-4EE5-AE5F-F51B61BDB9B7
title: Classe Msvm_KvpExchangeDataItem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeDataItem
- Msvm_KvpExchangeDataItem.InstanceID
- Msvm_KvpExchangeDataItem.Caption
- Msvm_KvpExchangeDataItem.Description
- Msvm_KvpExchangeDataItem.ElementName
- Msvm_KvpExchangeDataItem.Source
- Msvm_KvpExchangeDataItem.Name
- Msvm_KvpExchangeDataItem.Data
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 540c54a694dab1c80a32f9648a90c5b5bf1e48a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757837"
---
# <a name="msvm_kvpexchangedataitem-class"></a>\_Classe Msvm KvpExchangeDataItem

Representa um par de chave/valor.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_KvpExchangeDataItem : CIM_ManagedElement
{
  string InstanceID;
  string Caption = "Key-Value Pair Exchange Data Item";
  string Description = "Microsoft Key-Value Pair Exchange Data Item";
  string ElementName = "Key-Value Pair Exchange Data Item";
  uint16 Source;
  string Name;
  string Data;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ KvpExchangeDataItem** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ KvpExchangeDataItem** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma breve descrição do objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Dados**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)
</dt> </dl>

A parte de valor do par chave/valor.

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição do objeto . Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um nome de exibição para o objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Identifica exclusivamente uma instância dessa classe. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)
</dt> </dl>

A parte principal do par chave/valor.



| Chave                                                                                                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>"CSDVersion"</dt> </dl>                 | Uma cadeia de caracteres que representa as service pack mais recentes instaladas no sistema convidado. Por exemplo, "Service Pack 2". Se nenhum service pack tiver sido instalado, essa cadeia de caracteres estará vazia.<br/>                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>FullyQualifiedDomainName</dt> </dl>   | Uma cadeia de caracteres que representa o nome DNS totalmente qualificado que identifica exclusivamente o computador local. Esse nome é uma combinação do nome do host DNS e do nome de domínio DNS, usando o formato *hostname*. *Nome_do_domínio*. Se o computador local for um nó em um cluster, esse valor será o nome DNS totalmente qualificado do servidor virtual de cluster. Esse valor corresponde ao nome retornado pela função [**GetComputerNameEx devia**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) quando o parâmetro *nametype* é "ComputerNameDnsFullyQualified".<br/> |
| <dl> <dt>"IntegrationServicesVersion"</dt> </dl> | Uma cadeia de caracteres que representa a versão do Integration Services instalado atualmente na máquina virtual convidada (por exemplo, "6.1.7000.0").<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>"NetworkAddressIPv4"</dt> </dl>         | Uma cadeia de caracteres que contém uma lista delimitada por ponto-e-vírgula dos endereços IPv4 atribuídos no momento à máquina virtual convidada. A lista é atualizada automaticamente sempre que uma alteração de configuração de TCP/IP ocorre na máquina virtual convidada. Cada endereço é representado na notação de ponto decimal. <br/>                                                                                                                                                                                                                         |
| <dl> <dt>"NetworkAddressIPv6"</dt> </dl>         | Uma cadeia de caracteres que contém uma lista delimitada por ponto-e-vírgula dos endereços IPv6 atribuídos no momento à máquina virtual convidada. A lista é atualizada automaticamente sempre que uma alteração de configuração de TCP/IP ocorre na máquina virtual convidada. Cada endereço é representado em notação hexadecimal de dois-pontos. As listas IPv4 e IPv6 não têm garantia de serem sincronizadas em todos os momentos.<br/>                                                                                                                                             |
| <dl> <dt>"OSBuildNumber"</dt> </dl>              | Uma cadeia de caracteres que representa o número de Build do sistema operacional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>"OSEditionId"</dt> </dl>                | Uma cadeia de caracteres que representa a edição (SKU) do sistema operacional da máquina virtual convidada. Para obter uma lista de valores possíveis, consulte a função [**GetProductInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getproductinfo) .<br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>OSName</dt> </dl>                     | Uma cadeia de caracteres que representa o nome do sistema operacional. Esse valor vem da seguinte entrada do registro: **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ProductName**<br/> <br/>                                                                                                                                                                                                                                                                                |
| <dl> <dt>OSMajorVersion</dt> </dl>             | Uma cadeia de caracteres que representa o número de versão principal do sistema operacional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <dt>OSMinorVersion</dt> </dl>             | Uma cadeia de caracteres que representa o número de versão secundária do sistema operacional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <dt>"OSPlatformId"</dt> </dl>               | Uma cadeia de caracteres que representa a plataforma do sistema operacional. Os valores possíveis da propriedade **Data** são "1" para indicar um sistema Windows sem suporte e "2" para indicar um sistema Windows com suporte.<br/>                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>OSVersion</dt> </dl>                  | Uma cadeia de caracteres que representa a versão do sistema operacional. O formato dessa cadeia de caracteres é *MajorVersion*. *MinorVersion*. *BuildNumber*. Por exemplo, "5.2.3790" para o Windows Server 2003.<br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>ProcessorArchitecture</dt> </dl>      | Uma cadeia de caracteres que representa a arquitetura do processador do sistema operacional. Para obter uma lista de valores, consulte o membro **wProcessorArchitecture** da estrutura de [**\_ informações do sistema**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) .<br/>                                                                                                                                                                                                                                                                                                              |
| <dl> <dt>ProductType</dt> </dl>                | Uma cadeia de caracteres que representa o tipo de produto. Para obter uma lista de valores, consulte o membro **wProductType** da estrutura [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) .<br/>                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>"RDPAddressIPv4"</dt> </dl>             | Uma cadeia de caracteres que contém uma lista delimitada por ponto-e-vírgula dos endereços IPv4 que a pilha RDP da máquina virtual convidada está escutando no momento. Se a pilha RDP não estiver em execução no momento, a cadeia de caracteres estará vazia. A lista é atualizada automaticamente sempre que uma alteração de configuração de TCP/IP afeta a pilha RDP na máquina virtual convidada. Cada endereço é representado na notação de ponto decimal.<br/>                                                                                                                   |
| <dl> <dt>"RDPAddressIPv6"</dt> </dl>             | Uma cadeia de caracteres que contém uma lista delimitada por ponto-e-vírgula dos endereços IPv6 que a pilha RDP da máquina virtual convidada está escutando no momento. Se a pilha RDP não estiver em execução no momento, a cadeia de caracteres estará vazia. A lista é atualizada automaticamente sempre que uma alteração de configuração de TCP/IP afeta a pilha RDP na máquina virtual convidada. Cada endereço é representado em notação hexadecimal de dois-pontos.<br/>                                                                                                             |
| <dl> <dt>"ServicePackMajor"</dt> </dl>           | Uma cadeia de caracteres que representa o número de versão principal do service pack mais recente instalado no sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>"ServicePackMinor"</dt> </dl>           | Uma cadeia de caracteres que representa o número de versão secundária do service pack mais recente instalado no sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>"SuiteMask"</dt> </dl>                  | Uma cadeia de caracteres que representa os pacotes de produto disponíveis no sistema. Essa cadeia de caracteres é uma combinação de qualquer um dos valores do membro **wSuiteMask** da estrutura [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) .<br/>                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

**Origem**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A origem dos dados.



| Valor                                                                        | Significado                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | "HostExchangeItems" quando enviado por push pelo host.<br/>                                                                                                                                                                                      |
| <dl> <dt>1</dt> </dl> | "GuestExchangeItems" quando enviado por push pela máquina virtual convidada.<br/>                                                                                                                                                                    |
| <dl> <dt>2</dt> </dl> | "GuestIntrinsicExchangeItems" quando preenchido automaticamente pela máquina virtual convidada.<br/>                                                                                                                                          |
| <dl> <dt>4</dt> </dl> | Indica que o item é somente host e não compartilhado com a máquina virtual convidada. Usado com a propriedade **HostOnlyItems** da classe [**Msvm \_ KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md) . <br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm \_ KvpExchangeDataItem** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                                 |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Managedelement do CIM**](cim-managedelement.md)
</dt> <dt>

[**\_Managedelement do CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)
</dt> </dl>

 

