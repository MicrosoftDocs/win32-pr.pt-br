---
description: 'Saiba mais sobre: método Update. Save'
title: Método Update. Save
TOCTitle: 'Save method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.Save
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.save(v=EXCHG.10)
ms:contentKeyID: 55104195
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Update.Save
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 57693d3952f011127e60fdfb70dd2352c2f15207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501903"
---
# <a name="updatesave-method"></a>Método Update. Save

Atualize o TableName.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Sub Save
'Usage
Dim instance As Update

instance.Save()
```

``` csharp
public void Save()
```

## <a name="remarks"></a>Comentários

Save é a etapa final na execução de uma inserção ou atualização. A atualização é iniciada chamando a criação de um objeto de atualização e, em seguida, chamando JetSetColumn ou JetSetColumns uma ou mais vezes para definir o estado do registro. Por fim, a atualização é chamada para concluir a operação de atualização. Os índices são atualizados somente pela atualização ou e não durante JetSetColumn ou JetSetColumns.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Atualizar classe](./update-class.md)

[Atualizar Membros](./update-members.md)

[Salvar sobrecarga](./update.save-method.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
