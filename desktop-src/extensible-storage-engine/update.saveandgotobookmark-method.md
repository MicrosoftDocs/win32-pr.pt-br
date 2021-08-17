---
description: 'Saiba mais sobre: método Update. SaveAndGotoBookmark'
title: Método Update. SaveAndGotoBookmark
TOCTitle: 'SaveAndGotoBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.saveandgotobookmark(v=EXCHG.10)
ms:contentKeyID: 55104204
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 566be9b1af403a794b6ac87259a0fd6b6c0fea46c0b45287c536f336ee734b6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119106950"
---
# <a name="updatesaveandgotobookmark-method"></a>Método Update. SaveAndGotoBookmark

Atualize a TableName e posicione a TableName no registro que foi modificado. Isso pode ser útil ao inserir um registro porque, por padrão, o TableName permanece em seu local antigo.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Sub SaveAndGotoBookmark
'Usage
Dim instance As Update

instance.SaveAndGotoBookmark()
```

``` csharp
public void SaveAndGotoBookmark()
```

## <a name="remarks"></a>Comentários

Save é a etapa final na execução de uma inserção ou atualização. A atualização é iniciada chamando a criação de um objeto de atualização e, em seguida, chamando JetSetColumn ou JetSetColumns uma ou mais vezes para definir o estado do registro. Por fim, a atualização é chamada para concluir a operação de atualização. Os índices são atualizados somente pela atualização ou e não durante JetSetColumn ou JetSetColumns.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Atualizar classe](./update-class.md)

[Atualizar Membros](./update-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
