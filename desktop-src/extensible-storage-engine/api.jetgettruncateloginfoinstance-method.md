---
description: 'Saiba mais sobre: método API. JetGetTruncateLogInfoInstance'
title: Método API. JetGetTruncateLogInfoInstance
TOCTitle: 'JetGetTruncateLogInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettruncateloginfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100743
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1a0e96bd52b7a6ac196289d554c7376790ceb544823235caf5fd99e4fd5da5e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978226"
---
# <a name="apijetgettruncateloginfoinstance-method"></a>Método API. JetGetTruncateLogInfoInstance

Usado durante um backup iniciado por [JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) para consultar uma instância para obter os nomes dos arquivos de log de transações que podem ser excluídos com segurança depois que o backup for concluído com êxito.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetGetTruncateLogInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetTruncateLogInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetTruncateLogInfoInstance(
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
    
    Retorna uma lista de cadeias de caracteres terminadas em nulo que descrevem o conjunto de arquivos de log de banco de dados que podem ser excluídos com segurança após a conclusão do backup. A lista de cadeias de caracteres retornada nesse buffer está no mesmo formato que uma cadeia de caracteres múltipla usada pelo registro. Cada cadeia de caracteres terminada em nulo é retornada em sequência seguida por um terminador nulo final.

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
