---
description: 'Saiba mais sobre: Método Api.JetGetLogInfoInstance'
title: Método Api.JetGetLogInfoInstance
TOCTitle: 'JetGetLogInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetLogInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetloginfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100726
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetLogInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetLogInfoInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 044e3a214a520ecb331956108eb83449b689decbd995f4b5b9330fdef6729a53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670366"
---
# <a name="apijetgetloginfoinstance-method"></a>Método Api.JetGetLogInfoInstance

Usado durante um backup iniciado por [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) para consultar uma instância para os nomes de arquivos de patch de banco de dados e arquivos de log que devem se tornar parte do conjunto de arquivos de backup. Esses arquivos podem ser abertos posteriormente usando [JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) e lidos usando [JetReadFileInstance(JET_INSTANCE, JET_HANDLE, \[ \] , Int32, Int32)](./api.jetreadfileinstance-method.md).

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetGetLogInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetLogInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetLogInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a>Parâmetros

  - instance  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    A instância para a que obter as informações.

<!-- end list -->

  - files  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Retorna uma lista de cadeias de caracteres terminadas em nulo que descrevem o conjunto de arquivos de patch de banco de dados e arquivos de log que devem fazer parte do conjunto de arquivos de backup. A lista de cadeias de caracteres retornadas nesse buffer está no mesmo formato que uma cadeia de caracteres multi-cadeia de caracteres usada pelo Registro. Cada cadeia de caracteres terminada em nulo é retornada em sequência seguida por um terminador nulo final.

<!-- end list -->

  - maxChars  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Número máximo de caracteres a recuperar.

<!-- end list -->

  - actualChars  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Tamanho real da lista de arquivos. Se isso for maior que maxChars, a lista será truncada.

## <a name="remarks"></a>Comentários

É importante observar que essa API não retornará um erro ou aviso se o buffer de saída for muito pequeno para aceitar a lista completa de arquivos que devem fazer parte do conjunto de arquivos de backup.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
