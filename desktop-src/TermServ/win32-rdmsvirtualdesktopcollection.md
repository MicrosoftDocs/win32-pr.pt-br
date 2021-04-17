---
title: Classe Win32_RDMSVirtualDesktopCollection
description: Cria e gerencia uma coleção de áreas de trabalho virtuais.
ms.assetid: fe0a484e-f9e3-4b99-8e69-da8f337ae957
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDMSVirtualDesktopCollection Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDMSVirtualDesktopCollection classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection.Alias
- Win32_RDMSVirtualDesktopCollection.Type
- Win32_RDMSVirtualDesktopCollection.IsManaged
- Win32_RDMSVirtualDesktopCollection.Name
- Win32_RDMSVirtualDesktopCollection.CollectionDescription
- Win32_RDMSVirtualDesktopCollection.SecurityDescriptor
- Win32_RDMSVirtualDesktopCollection.VmFarmSettings
- Win32_RDMSVirtualDesktopCollection.UserVHDSetting
- Win32_RDMSVirtualDesktopCollection.IconContents
- Win32_RDMSVirtualDesktopCollection.ShowInPortal
- Win32_RDMSVirtualDesktopCollection.IsHA
- Win32_RDMSVirtualDesktopCollection.IsUserAdmin
- Win32_RDMSVirtualDesktopCollection.RollbackEnabled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a6da0c13b6ab223afc7afe6e92039a5388c6204
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105780567"
---
# <a name="win32_rdmsvirtualdesktopcollection-class"></a>\_Classe Win32 RDMSVirtualDesktopCollection

Cria e gerencia uma coleção de áreas de trabalho virtuais.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktopCollection
{
  string  Alias;
  uint32  Type;
  boolean IsManaged;
  string  Name;
  string  CollectionDescription;
  string  SecurityDescriptor;
  string  VmFarmSettings;
  string  UserVHDSetting;
  uint8   IconContents[];
  boolean ShowInPortal;
  boolean IsHA;
  boolean IsUserAdmin;
  boolean RollbackEnabled;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ RDMSVirtualDesktopCollection** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ RDMSVirtualDesktopCollection** tem esses métodos.



| Método                                                                                            | Descrição                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddVirtualDesktop**](addvirtualdesktop-win32-rdmsvirtualdesktopcollection.md)                 | Adiciona uma área de trabalho virtual a uma coleção de áreas de trabalho virtuais.<br/>                                                                              |
| [**CancelPatch**](cancelpatch-win32-rdmsvirtualdesktopcollection.md)                             | Cancela um trabalho de provisionamento de atualização de software para as máquinas virtuais em uma coleção de áreas de trabalho virtuais.<br/>                                 |
| [**Getint32property**](getint32property-win32-rdmsvirtualdesktopcollection.md)                   | Recupera um valor de propriedade de número inteiro de uma coleção de áreas de trabalho virtuais.<br/>                                                               |
| [**Getpatchproperties**](getpatchproperties-win32-rdmsvirtualdesktopcollection.md)               | Recupera as propriedades de um trabalho de provisionamento de atualização de software para as máquinas virtuais em uma coleção de áreas de trabalho virtuais.<br/>             |
| [**Getstringproperty**](getstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | Recupera um valor de propriedade de cadeia de caracteres de uma coleção de áreas de trabalho virtuais.<br/>                                                                 |
| [**ProvisioningEnumerateJobs**](provisioningenumeratejobs-win32-rdmsvirtualdesktopcollection.md) | Enumera os trabalhos de provisionamento de área de trabalho virtual para este serviço.<br/>                                                                       |
| [**ProvisioningJobCancel**](provisioningjobcancel-win32-rdmsvirtualdesktopcollection.md)         | Cancela um trabalho de provisionamento de área de trabalho virtual.<br/>                                                                                          |
| [**ProvisioningJobExecute**](provisioningjobexecute-win32-rdmsvirtualdesktopcollection.md)       | Executa um trabalho de provisionamento de área de trabalho virtual.<br/>                                                                                             |
| [**ProvisioningJobGetReport**](provisioningjobgetreport-win32-rdmsvirtualdesktopcollection.md)   | Obtém um relatório sobre o status de um trabalho de provisionamento de área de trabalho virtual.<br/>                                                                |
| [**ProvisioningPrepJob**](win32-rdmsvirtualdesktopcollection-provisioningprepjob.md)             | Cria um trabalho de provisionamento de área de trabalho virtual.<br/>                                                                                          |
| [**RemoveVirtualDesktop**](removevirtualdesktop-win32-rdmsvirtualdesktopcollection.md)           | Remove uma área de trabalho virtual de uma coleção de áreas de trabalho virtuais.<br/>                                                                         |
| [**SchedulePatch**](schedulepatch-win32-rdmsvirtualdesktopcollection.md)                         | Agenda um trabalho de provisionamento de atualização de software que instala atualizações de software nas máquinas virtuais em uma coleção de áreas de trabalho virtuais.<br/> |
| [**Setint32property**](setint32property-win32-rdmsvirtualdesktopcollection.md)                   | Atualiza um valor de propriedade de inteiro de uma coleção de áreas de trabalho virtuais.<br/>                                                                   |
| [**Setstringproperty**](setstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | Atualiza um valor de propriedade de cadeia de caracteres de uma coleção de área de trabalho virtual.<br/>                                                                     |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ RDMSVirtualDesktopCollection** tem essas propriedades.

<dl> <dt>

**Alias**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtém ou define o alias da coleção

</dd> <dt>

**CollectionDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtém ou define a descrição da coleção

</dd> <dt>

**IconContents**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtém ou define uma matriz de valores que especificam ícones para a coleção.

</dd> <dt>

**IsHA**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Obtém ou define um valor que indica se a coleção contém VMs altamente disponíveis. **True** se a coleção contiver VMs altamente disponíveis; caso contrário, **false**.

</dd> <dt>

**IsManaged**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Obtém ou define um valor que indica se a coleção é gerenciada. **True** se a coleção for gerenciada; caso contrário, **false**.

</dd> <dt>

**IsUserAdmin**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Obtém ou define um valor que indica se um usuário é um administrador em uma VM. **True** se o usuário for um administrador em uma VM; caso contrário, **false**.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Obtém ou define o nome da coleção.

</dd> <dt>

**RollbackEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Obtém ou define um valor que indica se uma VM foi revertida com um instantâneo de VM. **True** se a VM foi revertida com um instantâneo de VM; caso contrário, **false**.

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtém ou define um descritor de segurança com formato SSDL que controla o acesso à coleção.

</dd> <dt>

**ShowInPortal**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Obtém ou define um valor que indica se a coleção é exibida no Terminal Services Acesso via Web (TS Acesso via Web). **True** para exibir a coleção no TS acesso via Web; caso contrário, **false**.

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Obtém ou define um valor que indica o tipo de sessões de máquina virtual hospedadas pela coleção.

Essa propriedade contém um dos seguintes valores:

<dt>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>**TempVM** (1)


</dt> <dd>

Máquinas virtuais temporárias.

</dd> <dt>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>**ManualPersonalVM** (2)


</dt> <dd>

Máquinas virtuais criadas manualmente.

</dd> <dt>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>**AutoPersonalVM** (3)


</dt> <dd>

Máquinas virtuais geradas automaticamente.

</dd> </dl>

</dd> <dt>

**UserVHDSetting**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtém ou define a configuração de VHD de dados de usuário para a coleção.

</dd> <dt>

**VmFarmSettings**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtém ou define as configurações da área de trabalho das máquinas virtuais na coleção.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\RDMs cimv2 \\ raiz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Provedor de serviços de gerenciamento de Área de Trabalho Remota](rdms-api-reference.md)
</dt> </dl>

 

