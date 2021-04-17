---
description: 'Saiba mais sobre: método API. JetGetAttachInfoInstance'
title: Método API. JetGetAttachInfoInstance
TOCTitle: 'JetGetAttachInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetattachinfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100704
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 94865042edf8b049b7140673a8aee1b4e2d91573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762204"
---
# <a name="apijetgetattachinfoinstance-method"></a>Método API. JetGetAttachInfoInstance

Usado durante um backup iniciado por [JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) para consultar uma instância para obter os nomes dos arquivos de banco de dados que devem se tornar parte do conjunto de arquivos de backup. Somente os bancos de dados atualmente anexados à instância usando [JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md) serão considerados. Esses arquivos podem ser abertos subsequentemente usando [JetOpenFileInstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) e Read usando [JetReadFileInstance (JET_INSTANCE, JET_HANDLE, \[ \] , Int32, Int32)](./api.jetreadfileinstance-method.md).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetGetAttachInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetAttachInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetAttachInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a>Parâmetros

  - instance  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    A instância para a qual obter as informações.

<!-- end list -->

  - files  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Retorna uma lista de cadeias de caracteres terminadas em nulo que descrevem o conjunto de arquivos de banco de dados que deve ser parte do conjunto de arquivos de backup. A lista de cadeias de caracteres retornada nesse buffer está no mesmo formato que uma cadeia de caracteres múltipla usada pelo registro. Cada cadeia de caracteres terminada em nulo é retornada em sequência seguida por um terminador nulo final.

<!-- end list -->

  - maxChars  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Número máximo de caracteres a serem recuperados.

<!-- end list -->

  - actualChars  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Tamanho real da lista de arquivos. Se for maior que maxChars, a lista foi truncada.

## <a name="remarks"></a>Comentários

É importante observar que essa API não retornará um erro ou aviso se o buffer de saída for muito pequeno para aceitar a lista completa de arquivos que devem fazer parte do conjunto de arquivos de backup.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
