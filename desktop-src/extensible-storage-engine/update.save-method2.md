---
description: 'Saiba mais sobre: Método Update.Save'
title: Método Update.Save
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
ms.openlocfilehash: 75927144f887ab5cd7dbfe05c6d8fbf4c690a0e29786c1834fa00f8e29fae76c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117890057"
---
# <a name="updatesave-method"></a>Método Update.Save

Atualize a tableid.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

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

Salvar é a etapa final na execução de uma inserção ou atualização. A atualização é iniciada chamando a criação de um objeto Update e, em seguida, chamando JetSetColumn ou JetSetColumns uma ou mais vezes para definir o estado do registro. Por fim, Update é chamado para concluir a operação de atualização. Os índices são atualizados apenas por Update ou e não durante JetSetColumn ou JetSetColumns.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe update](./update-class.md)

[Atualizar membros](./update-members.md)

[Salvar sobrecarga](./update.save-method.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
