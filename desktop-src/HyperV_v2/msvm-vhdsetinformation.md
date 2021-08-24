---
description: Fornece informações sobre um arquivo de conjunto de VHD.
ms.assetid: a975c131-d3f3-4be3-bc69-e277e3ce4d28
title: Msvm_VHDSetInformation classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VHDSetInformation
- Msvm_VHDSetInformation.Path
- Msvm_VHDSetInformation.SnapshotIdList
- Msvm_VHDSetInformation.AllPaths
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d8cef737c02629ac0a1a026a459adf6eb7060e0dbdf8c0f9ecb20c66fce1259e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789426"
---
# <a name="msvm_vhdsetinformation-class"></a>Classe Msvm \_ VHDSetInformation

Fornece informações sobre um arquivo de conjunto de VHD.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[AMENDMENT]
class Msvm_VHDSetInformation
{
  string Path;
  string SnapshotIdList[];
  string AllPaths[];
};
```

## <a name="members"></a>Membros

A **classe Msvm \_ VHDSetInformation** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ VHDSetInformation** tem essas propriedades.

<dl> <dt>

**AllPaths**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma lista de todos os arquivos abrangida pelo arquivo conjunto de VHD, incluindo arquivos não relacionados e quaisquer pais do disco rígido virtual raiz. Todos os arquivos listados após o disco rígido virtual raiz não sãomanados por esse arquivo de conjunto de VHDs. Esse campo poderá estar vazio se essas informações não foram especificamente solicitadas.

</dd> <dt>

**Caminho**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho do arquivo de conjunto de VHD.

</dd> <dt>

**SnapshotIdList**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma lista de GUIDs que representam todos os instantâneos contidos por esse arquivo de conjunto de VHDs.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




