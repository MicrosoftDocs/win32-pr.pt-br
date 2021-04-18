---
title: Classe Win32_TSVmMetadataAssociation
description: Representa uma associação entre uma máquina virtual Área de Trabalho Remota e suas propriedades de metadados.
ms.assetid: 374b1a29-78de-45fd-97b3-c5a5b724e66b
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSVmMetadataAssociation Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSVmMetadataAssociation classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSVmMetadataAssociation
- Win32_TSVmMetadataAssociation.TSVm
- Win32_TSVmMetadataAssociation.MetadataItem
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db3a68c20553eaf52903471d19df9df169ecde21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770443"
---
# <a name="win32_tsvmmetadataassociation-class"></a>\_Classe Win32 TSVmMetadataAssociation

Representa uma associação entre uma máquina virtual Área de Trabalho Remota e suas propriedades de metadados.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, Association, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVmMetadataAssociation
{
  Win32_TSVm             REF TSVm;
  Win32_TSVmMetadataItem REF MetadataItem;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ TSVmMetadataAssociation** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ TSVmMetadataAssociation** tem essas propriedades.

<dl> <dt>

**MetadataItem**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Win32 \_ TSVmMetadataItem**](win32-tsvmmetadataitem.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma instância da classe [**Win32 \_ TSVmMetadataItem**](win32-tsvmmetadataitem.md) que representa os metadados para a máquina virtual.

</dd> <dt>

**TSVm**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Win32 \_ TSVm**](win32-tsvm.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Uma instância da classe [**Win32 \_ TSVm**](win32-tsvm.md) que representa a máquina virtual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                             |
| Namespace<br/>                | \\TerminalServices da cimv2 raiz \\<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

