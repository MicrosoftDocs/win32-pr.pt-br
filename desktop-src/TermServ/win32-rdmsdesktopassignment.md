---
title: Classe Win32_RDMSDesktopAssignment
description: Descreve a atribuição da área de trabalho do usuário da coleção RD.
ms.assetid: d3370cf2-65db-4e01-9ea3-9a71340bf71b
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDMSDesktopAssignment Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDMSDesktopAssignment classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment
- Win32_RDMSDesktopAssignment.CollectionAlias
- Win32_RDMSDesktopAssignment.DesktopName
- Win32_RDMSDesktopAssignment.UserName
- Win32_RDMSDesktopAssignment.UserDomain
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72bb252bd2efb71e3192ebd16160cecf18196cb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295779"
---
# <a name="win32_rdmsdesktopassignment-class"></a>\_Classe Win32 RDMSDesktopAssignment

Descreve a atribuição da área de trabalho do usuário da coleção RD.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSDesktopAssignment
{
  string CollectionAlias;
  string DesktopName;
  string UserName;
  string UserDomain;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ RDMSDesktopAssignment** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ RDMSDesktopAssignment** tem esses métodos.



| Método                                                                                 | Descrição                              |
|:---------------------------------------------------------------------------------------|:-----------------------------------------|
| [**AddDesktopAssignment**](win32-rdmsdesktopassignment-adddesktopassignment.md)       | Adiciona uma atribuição de área de trabalho.<br/>    |
| [**RemoveDesktopAssignment**](win32-rdmsdesktopassignment-removedesktopassignment.md) | Remove uma atribuição de desktop.<br/> |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ RDMSDesktopAssignment** tem essas propriedades.

<dl> <dt>

**CollectionAlias**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Alias da coleção.

</dd> <dt>

**Área de trabalho**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

O nome da área de trabalho.

</dd> <dt>

**UserDomain**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

O nome de domínio da conta de usuário.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

O nome da conta de usuário.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                              |
| Namespace<br/>                | \\RDMs cimv2 \\ raiz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



 

