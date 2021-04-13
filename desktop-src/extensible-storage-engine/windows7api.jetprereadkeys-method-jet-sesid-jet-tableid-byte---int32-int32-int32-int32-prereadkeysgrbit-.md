---
description: 'Saiba mais sobre: método Windows7Api. JetPrereadKeys (JET_SESID, JET_TABLEID, Byte [] [], Int32, Int32, Int32, Int32, PrereadKeysGrbit)'
title: Método Windows7Api. JetPrereadKeys (JET_SESID, JET_TABLEID, Byte [] [], Int32, Int32, Int32, Int32, PrereadKeysGrbit) (Microsoft. ISAM. ESENT. Interop. windows7)
TOCTitle: JetPrereadKeys method (JET_SESID, JET_TABLEID, Byte[][], Int32 , Int32, Int32, Int32, PrereadKeysGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[][],System.Int32[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Windows7.PrereadKeysGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows7.windows7api.jetprereadkeys(v=EXCHG.10)
ms:contentKeyID: 55104374
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a799c890887df730fdad97ad4d08fa500a6dd4b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164768"
---
# <a name="windows7apijetprereadkeys-method-jet_sesid-jet_tableid-byte-int32--int32-int32-int32-prereadkeysgrbit"></a>Método Windows7Api. JetPrereadKeys (JET_SESID, JET_TABLEID, byte \[ \] \[ \] , Int32, Int32, Int32, Int32, PrereadKeysGrbit)

Se os registros com as chaves especificadas não estiverem no cache do buffer, inicie as leituras assíncronas para colocar os registros no cache do buffer de banco de dados.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetPrereadKeys ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    keys As Byte()(), _
    keyLengths As Integer(), _
    keyIndex As Integer, _
    keyCount As Integer, _
    <OutAttribute> ByRef keysPreread As Integer, _
    grbit As PrereadKeysGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim keys As Byte()()
Dim keyLengths As Integer()
Dim keyIndex As Integer
Dim keyCount As Integer
Dim keysPreread As Integer
Dim grbit As PrereadKeysGrbitWindows7Api.JetPrereadKeys(sesid, tableid, _
    keys, keyLengths, keyIndex, keyCount, _
    keysPreread, grbit)
```

``` csharp
public static void JetPrereadKeys(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[][] keys,
    int[] keyLengths,
    int keyIndex,
    int keyCount,
    out int keysPreread,
    PrereadKeysGrbit grbit
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    A tabela na qual os itens são relidos.

<!-- end list -->

  - chaves  
    Escreva \[\]  
    
    As chaves a serem lidas. As chaves devem ser classificadas.

<!-- end list -->

  - Comprimentos de caracteres  
    Escreva \[\]  
    
    Os comprimentos das chaves a serem lidas.

<!-- end list -->

  - keyIndex  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    O índice da primeira chave na matriz de chaves a ser lida.

<!-- end list -->

  - Contagem de keycount  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    O número máximo de chaves a serem lidas.

<!-- end list -->

  - keysPreread  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Retorna o número de chaves para realmente ser lido.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. ESENT. Interop. Windows7. PrereadKeysGrbit](./prereadkeysgrbit-enumeration.md)  
    
    Opções de preread. Usado para especificar a direção da subleitura.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe Windows7Api](./windows7api-class.md)

[Membros do Windows7Api](./windows7api-members.md)

[Sobrecarga de JetPrereadKeys](./windows7api.jetprereadkeys-method.md)

[Namespace Microsoft. ISAM. ESENT. Interop. Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)
