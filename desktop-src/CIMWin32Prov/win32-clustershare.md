---
description: A \_ classe Win32 ClusterShare representa um recurso compartilhado em um cluster.
ms.assetid: 6c8b40e3-431f-4728-a389-affbc04b8415
ms.tgt_platform: multiple
title: Classe Win32_ClusterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare
- Win32_ClusterShare.Caption
- Win32_ClusterShare.Description
- Win32_ClusterShare.InstallDate
- Win32_ClusterShare.Status
- Win32_ClusterShare.AccessMask
- Win32_ClusterShare.AllowMaximum
- Win32_ClusterShare.MaximumAllowed
- Win32_ClusterShare.Name
- Win32_ClusterShare.Path
- Win32_ClusterShare.Type
- Win32_ClusterShare.ServerName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ccff6ad8d99692d066728c99dd74ab07640af4fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089473"
---
# <a name="win32_clustershare-class"></a>\_Classe Win32 ClusterShare

\[A classe **Win32 \_ ClusterShare** foi preterida. Em vez disso, use as classes de [**\_ compartilhamento MSFT**](/previous-versions/windows/desktop/stormgmt/msft-fileshare) e [**MSFT \_ SMFileShare**](/previous-versions/windows/desktop/msftstrgmanprov/msft-smfileshare) .\]

A \_ classe Win32 ClusterShare representa um recurso compartilhado em um cluster.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), AMENDMENT]
class Win32_ClusterShare : Win32_Share
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  boolean  AllowMaximum;
  uint32   MaximumAllowed;
  string   Name;
  string   Path;
  uint32   Type;
  string   ServerName;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ ClusterShare** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ ClusterShare** tem esses métodos.



| Método                                                    | Descrição                                                      |
|:----------------------------------------------------------|:-----------------------------------------------------------------|
| [**Criada**](create-win32-clustershare.md)               | Cria uma nova instância de **\_ ClusterShare do Win32** .<br/>       |
| [**Excluir**](delete-win32-clustershare.md)               | Exclui uma instância de **\_ ClusterShare do Win32** .<br/>           |
| [**GetAccessMask**](getaccessmask-win32-clustershare.md) | Retorna um bitmap com os direitos de acesso ao compartilhamento.<br/> |
| [**SetShareInfo**](setshareinfo-win32-clustershare.md)   | Define os parâmetros do recurso compartilhado.<br/>           |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ ClusterShare** tem essas propriedades.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Esta propriedade é obsoleta e não é mais usada. Em vez disso, use o método [**Win32 \_ share. GetAccessMask**](getaccessmask-method-in-class-win32-share.md) . O valor da propriedade **AccessMask** é definido como **NULL** pelo WMI. Para obter mais informações sobre como definir o acesso quando um compartilhamento é criado, consulte o método [**Create**](create-method-in-class-win32-share.md) .

Essa propriedade é herdada [**do \_ compartilhamento do Win32**](win32-share.md).

</dd> <dt>

**AllowMaximum**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("as \| estruturas de gerenciamento de rede do Win32API \| [**compartilham \_ informações \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ use")
</dt> </dl>

O número de usuários simultâneos deste recurso foi limitado. Se **for true**, o valor na propriedade **MaximumAllowed** será ignorado.

Essa propriedade é herdada [**do \_ compartilhamento do Win32**](win32-share.md).

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Uma breve descrição textual do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")
</dt> </dl>

Uma descrição textual do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")
</dt> </dl>

Indica quando o objeto foi instalado. A falta de um valor não indica que o objeto não está instalado.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**MaximumAllowed**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("as \| estruturas de gerenciamento de rede do Win32API \| [**compartilham \_ informações \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ use")
</dt> </dl>

Limite do número máximo de usuários com permissão para usar este recurso simultaneamente. O valor só será válido se a propriedade **AllowMaximum** estiver definida como **false**.

Essa propriedade é herdada [**do \_ compartilhamento do Win32**](win32-share.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| estruturas de gerenciamento de rede \| [**compartilham \_ informações \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1) \| shi1 \_ NetName")
</dt> </dl>

Alias fornecido a um caminho configurado como um compartilhamento em um sistema de computador executando o Windows.

Windows 2008 exemplo: " \\ Server01 \\ Public"-o windows Server 2008 requer que você coloque o UNC no nome.

Essa propriedade é herdada [**do \_ compartilhamento do Win32**](win32-share.md).

</dd> <dt>

**Caminho**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("estruturas de gerenciamento de rede do win32api \| \| [**compartilham \_ informações \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ caminho")
</dt> </dl>

Caminho local do compartilhamento do Windows.

Exemplo: "C: \\ arquivos de programas"

Essa propriedade é herdada [**do \_ compartilhamento do Win32**](win32-share.md).

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("servername"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Network Management estruturas \| [**share \_ info \_ 503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503) \| shi503 \_ ServerName")
</dt> </dl>

O servidor de cluster no qual o compartilhamento está hospedado.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")
</dt> </dl>

Cadeia de caracteres que indica o status atual do objeto. O status operacional e não operacional pode ser definido. O status operacional pode incluir "OK", "degradado" e "Pred falha". "Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).

O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço". O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo. Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Os valores incluem o seguinte:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erro** ("erro")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** ("desconhecido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Falha de Pred** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Iniciando** ("Iniciando")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Parando** ("parando")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Serviço** ("serviço")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Sob estresse** ("sob estresse")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

Não **recuperar** ("Recover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sem contato** ("sem contato")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Perda de comunicação** ("perda de comunicação")


</dt> <dd></dd> </dl>

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estruturas de gerenciamento de rede win32api informações de \| [**compartilhamento \_ \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ tipo")
</dt> </dl>

Tipo de recurso que está sendo compartilhado. Os tipos incluem: unidades de disco, filas de impressão, IPC (comunicações entre processos) e dispositivos gerais.

Essa propriedade é herdada [**do \_ compartilhamento do Win32**](win32-share.md).

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

**Unidade de disco** (0)


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

**Fila de impressão** (1)


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

**Dispositivo** (2)


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (3)


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

**Administrador da unidade de disco** (2147483648)


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

**Administrador da fila de impressão** (2147483649)


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

**Administrador do dispositivo** (2147483650)


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

**Administrador de IPC** (2147483651)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Compartilhamento do Win32 \_**](win32-share.md)
</dt> </dl>

 

