---
description: A classe WMI de associação Win32 DiskDriveToDiskPartition relaciona uma unidade de disco e uma \_ partição existentes nele.
ms.assetid: 82953097-ebfb-42b8-84b4-fb4ed19f3525
ms.tgt_platform: multiple
title: Win32_DiskDriveToDiskPartition classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskDriveToDiskPartition
- Win32_DiskDriveToDiskPartition.Antecedent
- Win32_DiskDriveToDiskPartition.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c92e9cc8a71516fa105e350ae8070ca417024c1802e9ea8a676d7355cb3aea7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118675089"
---
# <a name="win32_diskdrivetodiskpartition-class"></a>Classe Win32 \_ DiskDriveToDiskPartition

A classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **Win32 \_ DiskDriveToDiskPartition** relaciona uma unidade de disco e uma partição existentes nele.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskDriveToDiskPartition : CIM_MediaPresent
{
  Win32_DiskDrive     REF Antecedent;
  Win32_DiskPartition REF Dependent;
};
```

## <a name="members"></a>Membros

A **classe Win32 \_ DiskDriveToDiskPartition** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Win32 \_ DiskDriveToDiskPartition** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ DiskDrive**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DiskDrive")
</dt> </dl>

Referência à instância que representa as propriedades da unidade de disco em que a partição existe.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ DiskPartition**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DiskPartition")
</dt> </dl>

Referência à instância que representa a partição de disco que reside na unidade de disco.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe Win32 \_ DiskDriveToDiskPartition** é derivada de [**CIM \_ MediaPresent.**](cim-mediapresent.md)

Para uma discussão sobre como usar essa classe, consulte os artigos do blog Usar o [PowerShell](https://blogs.technet.com/b/heyscriptingguy/archive/2012/12/17/use-powershell-to-map-disk-drives-and-partitions.aspx) para mapear partições e unidades de disco e Como posso correlacionar unidades lógicas e [discos físicos?.](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx)

## <a name="examples"></a>Exemplos

O exemplo usar o Powershell para coletar informações de [disco/partição/ponto](https://Gallery.TechNet.Microsoft.Com/Use-Powershell-to-Gather-b5c746d0) de montagem usa **Win32 \_ DiskDriveToDiskPartition** para retornar informações sobre discos/partições locais e pontos de montagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**CIM \_ MediaPresent**](cim-mediapresent.md)
</dt> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[Tarefas WMI: discos e sistemas de arquivos](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

