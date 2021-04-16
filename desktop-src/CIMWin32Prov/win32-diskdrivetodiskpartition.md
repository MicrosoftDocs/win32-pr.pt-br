---
description: A \_ classe WMI de associação DiskDriveToDiskPartition do Win32 relaciona uma unidade de disco e uma partição existente nela.
ms.assetid: 82953097-ebfb-42b8-84b4-fb4ed19f3525
ms.tgt_platform: multiple
title: Classe Win32_DiskDriveToDiskPartition
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
ms.openlocfilehash: b2bd5472bd4ad92ddde47f7d6a492916006a80cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769040"
---
# <a name="win32_diskdrivetodiskpartition-class"></a>\_Classe Win32 DiskDriveToDiskPartition

A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ DiskDriveToDiskPartition do Win32** relaciona uma unidade de disco e uma partição existente nela.

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

A classe **Win32 \_ DiskDriveToDiskPartition** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ DiskDriveToDiskPartition** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ DiskDrive**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DiskDrive")
</dt> </dl>

Referência à instância que representa as propriedades da unidade de disco onde a partição existe.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ DiskPartition**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DiskPartition")
</dt> </dl>

Referência à instância que representa a partição de disco que reside na unidade de disco.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ DiskDriveToDiskPartition** é derivada de [**CIM \_ MediaPresent**](cim-mediapresent.md).

Para obter uma discussão sobre como usar essa classe, consulte [usar o PowerShell para mapear unidades de disco e partições](https://blogs.technet.com/b/heyscriptingguy/archive/2012/12/17/use-powershell-to-map-disk-drives-and-partitions.aspx) e o artigo [como posso correlacionar unidades lógicas e discos físicos?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx) blog.

## <a name="examples"></a>Exemplos

O exemplo do PowerShell [usar o PowerShell para coletar informações de disco/partição/ponto de montagem](https://Gallery.TechNet.Microsoft.Com/Use-Powershell-to-Gather-b5c746d0) usa o **Win32 \_ DiskDriveToDiskPartition** para retornar informações sobre discos/partições locais e pontos de montagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_MEDIAPRESENT CIM**](cim-mediapresent.md)
</dt> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[Tarefas do WMI: discos e sistemas de arquivos](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

