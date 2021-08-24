---
title: Classe Win32_TSVirtualIP
description: Define as configurações de virtualização de IP (Internet Protocol) para um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
ms.assetid: c37d572c-f6db-438b-8290-006a623c6593
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSVirtualIP Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSVirtualIP classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP
- Win32_TSVirtualIP.Caption
- Win32_TSVirtualIP.Description
- Win32_TSVirtualIP.InstallDate
- Win32_TSVirtualIP.Name
- Win32_TSVirtualIP.Status
- Win32_TSVirtualIP.VirtualIPActive
- Win32_TSVirtualIP.PolicySourceVirtualIPActive
- Win32_TSVirtualIP.VirtualIPMode
- Win32_TSVirtualIP.PolicySourceVirtualIPMode
- Win32_TSVirtualIP.ProgramList
- Win32_TSVirtualIP.PolicySourceProgramList
- Win32_TSVirtualIP.NetworkAdapterDescription
- Win32_TSVirtualIP.NetworkAdapterMacAddress
- Win32_TSVirtualIP.PolicySourceNetworkAdapter
- Win32_TSVirtualIP.NetworkAdapterDescriptionList
- Win32_TSVirtualIP.NetworkAdapterMacList
- Win32_TSVirtualIP.VirtualizeLoopbackAddressesEnabled
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28830e44fd54e9246cb0affc5fdde1427673d92e843adfd3e1e19cd221af370e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769046"
---
# <a name="win32_tsvirtualip-class"></a>\_Classe Win32 TSVirtualIP

Define as configurações de virtualização de IP (Internet Protocol) para um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_WIN32_TSVIRTUALIP_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\TSAppSrv\\VirtualIP"), AMENDMENT]
class Win32_TSVirtualIP : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint32   VirtualIPActive;
  uint32   PolicySourceVirtualIPActive;
  uint32   VirtualIPMode;
  uint32   PolicySourceVirtualIPMode;
  string   ProgramList[];
  uint32   PolicySourceProgramList;
  string   NetworkAdapterDescription;
  string   NetworkAdapterMacAddress;
  uint32   PolicySourceNetworkAdapter;
  string   NetworkAdapterDescriptionList[];
  string   NetworkAdapterMacList[];
  uint32   VirtualizeLoopbackAddressesEnabled;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ TSVirtualIP** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ TSVirtualIP** tem esses métodos.



| Método                                                                                                   | Descrição                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Addprogram**](addprogram-win32-tsvirtualip.md)                                                       | Adiciona um programa à lista de programas que usam a virtualização de IP.<br/>                                                                                                |
| [**RemoveProgram**](removeprogram-win32-tsvirtualip.md)                                                 | Remove um programa da lista de programas que usam a virtualização de IP.<br/>                                                                                           |
| [**SelectNetworkAdapter**](selectnetworkadapter-win32-tsvirtualip.md)                                   | Define o endereço MAC do adaptador de rede a ser usado para virtualização de IP.<br/>                                                                                         |
| [**Setprogramlist**](setprogramlist-win32-tsvirtualip.md)                                               | Substitui a lista de programas que usam a virtualização de IP.<br/>                                                                                                       |
| [**SetVirtualIPActive**](setvirtualipactive-win32-tsvirtualip.md)                                       | Define o valor da propriedade **VirtualIPActive** .<br/>                                                                                                                      |
| [**SetVirtualIPMode**](setvirtualipmode-win32-tsvirtualip.md)                                           | Define o valor da propriedade **VirtualIPMode** .<br/>                                                                                                                        |
| [**SetVirtualizeLoopbackAddressesEnabled**](setvirtualizeloopbackaddressesenabled-win32-tsvirtualip.md) | Define o valor da propriedade **VirtualizeLoopbackAddressesEnabled** .<br/> **Windows Server 2008 R2:** Esse método não está disponível antes de Windows Server 2012.<br/> |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ TSVirtualIP** tem essas propriedades.

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

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**NetworkAdapterDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A descrição do adaptador de rede.

</dd> <dt>

**NetworkAdapterDescriptionList**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A lista de descrições dos adaptadores de rede física disponíveis.

</dd> <dt>

**NetworkAdapterMacAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O endereço MAC do adaptador de rede.

</dd> <dt>

**NetworkAdapterMacList**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A lista de endereços MAC dos adaptadores de rede física disponíveis.

</dd> <dt>

**PolicySourceNetworkAdapter**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o adaptador de rede está configurado pelo servidor ou pela política de grupo.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceProgramList**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **programlist** está configurada pelo servidor ou pela política de grupo.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceVirtualIPActive**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **VirtualIPActive** está configurada pelo servidor ou pela política de grupo.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceVirtualIPMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **VirtualIPMode** está configurada pelo servidor ou pela política de grupo.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> </dl>

</dd> <dt>

**Programalist**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica os programas que são configurados para usar a virtualização de IP. Isso pode ser um nome de programa ou o caminho completo.

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

**VirtualIPActive**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Especifica se a virtualização de IP está ativa no servidor. Isso pode ser um dos valores a seguir.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

A virtualização de IP não está ativa.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)


</dt> <dd>

A virtualização de IP está ativa.

</dd> </dl>

</dd> <dt>

**VirtualIPMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica qual modo de virtualização de IP está sendo usado no servidor. Isso pode ser um dos valores a seguir.

<dt>

<span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>

<span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>**Por sessão** (0)


</dt> <dd>

O modo de virtualização de IP é por sessão.

</dd> <dt>

<span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>

<span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>**Por programa** (1)


</dt> <dd>

O modo de virtualização de IP é por usuário.

</dd> </dl>

</dd> <dt>

**VirtualizeLoopbackAddressesEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se a virtualização de endereço de loopback está habilitada.

**Windows Server 2008 R2:** Essa propriedade não está disponível antes de Windows Server 2012.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

não ativado

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)


</dt> <dd>

habilitado

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentários

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



 

