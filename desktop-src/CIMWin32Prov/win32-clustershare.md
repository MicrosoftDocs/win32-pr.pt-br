---
description: A classe ClusterShare do Win32 \_ representa um recurso compartilhado em um cluster.
ms.assetid: 6c8b40e3-431f-4728-a389-affbc04b8415
ms.tgt_platform: multiple
title: Win32_ClusterShare classe
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
ms.openlocfilehash: 66be06bf3a8433a7dba1eb28e6123adb03d622803745838158aa80bda0e8e594
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118417987"
---
# <a name="win32_clustershare-class"></a>Classe ClusterShare do Win32 \_

\[A **classe \_ ClusterShare do Win32** foi preterida. Use as [**classes MSFT \_ FileShare**](/previous-versions/windows/desktop/stormgmt/msft-fileshare) e [**\_ MSFT SMFileShare.**](/previous-versions/windows/desktop/msftstrgmanprov/msft-smfileshare)\]

A classe ClusterShare do Win32 \_ representa um recurso compartilhado em um cluster.

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

A **classe \_ ClusterShare win32** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ ClusterShare do Win32** tem esses métodos.



| Método                                                    | Descrição                                                      |
|:----------------------------------------------------------|:-----------------------------------------------------------------|
| [**Criar**](create-win32-clustershare.md)               | Cria uma nova **instância \_ ClusterShare do Win32.**<br/>       |
| [**Excluir**](delete-win32-clustershare.md)               | Exclui uma **instância \_ ClusterShare do Win32.**<br/>           |
| [**GetAccessMask**](getaccessmask-win32-clustershare.md) | Retorna um bitmap com os direitos de acesso ao compartilhamento.<br/> |
| [**SetShareInfo**](setshareinfo-win32-clustershare.md)   | Define os parâmetros do recurso compartilhado.<br/>           |



 

### <a name="properties"></a>Propriedades

A **classe \_ ClusterShare do Win32** tem essas propriedades.

<dl> <dt>

**Accessmask**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **PRETERIDO**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Essa propriedade está obsoleta e não é mais usada. Em vez disso, use o método [**\_ Win32 Share.GetAccessMask.**](getaccessmask-method-in-class-win32-share.md) O valor da **propriedade AccessMask** é definido como **nulo** pelo WMI. Para obter mais informações sobre como definir o acesso quando um compartilhamento é criado, consulte o [**método**](create-method-in-class-win32-share.md) Create.

Essa propriedade é herdada do [**Compartilhamento Win32. \_**](win32-share.md)

</dd> <dt>

**AllowMaximum**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures SHARE INFO \| [**\_ \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| ltd502 \_ max \_ uses")
</dt> </dl>

O número de usuários simultâneos para esse recurso foi limitado. Se **True**, o valor na **propriedade MaximumAllowed** será ignorado.

Essa propriedade é herdada do [**Compartilhamento Win32. \_**](win32-share.md)

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Legenda")
</dt> </dl>

Uma breve descrição textual do objeto .

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")
</dt> </dl>

Uma descrição textual do objeto .

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Data de instalação")
</dt> </dl>

Indica quando o objeto foi instalado. A falta de um valor não indica que o objeto não está instalado.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**MaximumAllowed**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures SHARE INFO \| [**\_ \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| ltd502 \_ max \_ uses")
</dt> </dl>

Limite o número máximo de usuários permitidos para usar esse recurso simultaneamente. O valor só será válido se a **propriedade AllowMaximum** estiver definida como **FALSE.**

Essa propriedade é herdada do [**Compartilhamento Win32. \_**](win32-share.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures SHARE INFO \| [**\_ \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1) \| www1 \_ netname")
</dt> </dl>

Alias dado a um caminho definido como um compartilhamento em um sistema de computador executando Windows.

Windows exemplo de 2008: \\ "SERVER01 \\ public" – Windows Server 2008 exige que você coloque UNC no nome.

Essa propriedade é herdada do [**Compartilhamento Win32. \_**](win32-share.md)

</dd> <dt>

**Caminho**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures SHARE INFO \| [**\_ \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| ltd502 \_ path")
</dt> </dl>

Caminho local do Windows compartilhamento.

Exemplo: "C: \\ Arquivos de Programas"

Essa propriedade é herdada do [**Compartilhamento Win32. \_**](win32-share.md)

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("ServerName"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures SHARE INFO \| [**\_ \_ 503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503) \| ltd503 \_ servername")
</dt> </dl>

O servidor de cluster no qual o compartilhamento está hospedado.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Cadeia de caracteres que indica o status atual do objeto. O status operacional e não operacional pode ser definido. O status operacional pode incluir "OK", "Degradado" e "Pred Fail". "Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para SMART).

O status não operacional pode incluir "Erro", "Iniciando", "Parando" e "Serviço". O "Serviço" pode ser aplicado durante a resilvering de espelhamento de disco, o recarregamento de uma lista de permissões de usuário ou outro trabalho administrativo. Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros estados.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Os valores incluem o seguinte:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erro** ("Erro")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("Degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** ("Desconhecido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Iniciando** ("Iniciando")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Parando** ("Parando")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Serviço** ("Serviço")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Stressed** ("Stressed")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sem contato** ("Sem contato")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Perda de vírgula** ("comm perdida")


</dt> <dd></dd> </dl>

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures SHARE INFO \| [**\_ \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| ltd502 \_ type")
</dt> </dl>

Tipo de recurso que está sendo compartilhado. Os tipos incluem: unidades de disco, filas de impressão, IPC (comunicação entre processos) e dispositivos gerais.

Essa propriedade é herdada do [**Compartilhamento Win32. \_**](win32-share.md)

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

**Unidade de disco** (0)


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

**Fila de Impressão** (1)


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

**Dispositivo** (2)


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (3)


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

**Administrador de unidade de** disco (2147483648)


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

**Imprimir Administrador de Fila** (2147483649)


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

**Administrador do** dispositivo (2147483650)


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
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Compartilhamento \_ win32**](win32-share.md)
</dt> </dl>

 

