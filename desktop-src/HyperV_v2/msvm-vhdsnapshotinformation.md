---
description: Fornece informações sobre um instantâneo em um arquivo de conjunto de VHD.
ms.assetid: 922bf0b8-523d-488e-9a41-1a27594e2e44
title: Classe Msvm_VHDSnapshotInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VHDSnapshotInformation
- Msvm_VHDSnapshotInformation.FilePath
- Msvm_VHDSnapshotInformation.SnapshotId
- Msvm_VHDSnapshotInformation.SnapshotPath
- Msvm_VHDSnapshotInformation.ParentPathsList
- Msvm_VHDSnapshotInformation.CreationTime
- Msvm_VHDSnapshotInformation.ResilientChangeTrackingId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c256ee2d3fb277fc98fa440403cf385377d7f64160267ff39a2d905c59f9d3ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068446"
---
# <a name="msvm_vhdsnapshotinformation-class"></a>\_Classe Msvm VHDSnapshotInformation

Fornece informações sobre um instantâneo em um arquivo de conjunto de VHD

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[AMENDMENT]
class Msvm_VHDSnapshotInformation
{
  string   FilePath;
  string   SnapshotId;
  string   SnapshotPath;
  string   ParentPathsList[];
  DATETIME CreationTime;
  string   ResilientChangeTrackingId;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ VHDSnapshotInformation** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ VHDSnapshotInformation** tem essas propriedades.

<dl> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A data e a hora da criação do instantâneo.

</dd> <dt>

**FilePath**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho do arquivo de conjunto de VHD.

</dd> <dt>

**ParentPathsList**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma lista de caminhos de arquivo que representa todos os arquivos dos quais esse instantâneo depende. Este campo estará vazio, a menos que solicitado especificamente. A primeira entrada é o pai imediato do arquivo, com a última entrada sendo a raiz.

</dd> <dt>

**ResilientChangeTrackingId**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A ID de controle de alteração resiliente, se houver, associada a esse instantâneo.

</dd> <dt>

**SnapshotId**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um GUID que identifica exclusivamente esse instantâneo dentro do arquivo de conjunto VHD.

</dd> <dt>

**SnapshotPath**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho do arquivo representado por esse instantâneo. Esse campo pode estar vazio se não houver nenhum arquivo associado a esse instantâneo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




