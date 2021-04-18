---
description: 'Saiba mais sobre a propriedade: Instanceparameters. LogBuffers'
title: Propriedade instanceparameters. LogBuffers
TOCTitle: 'LogBuffers property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.logbuffers(v=EXCHG.10)
ms:contentKeyID: 55107472
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_LogBuffers
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f58e43ea38792549d384328dc0fd6c5d31616e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768205"
---
# <a name="instanceparameterslogbuffers-property"></a>Propriedade instanceparameters. LogBuffers

Obtém ou define a quantidade de memória usada para armazenar em cache os registros de log antes que eles sejam gravados no arquivo de log de transações. A unidade para esse parâmetro é o tamanho do setor do volume que contém os arquivos de log de transações. O tamanho do setor quase sempre é de 512 bytes, portanto, é seguro assumir esse tamanho para a unidade. Esse parâmetro tem um impacto no desempenho. Quando o mecanismo de banco de dados está sob carga de atualização pesada, esse buffer pode se tornar completo com muita rapidez. Um tamanho de cache maior para o arquivo de log de transações é essencial para um bom desempenho de atualização sob uma condição de alta carga. O padrão é conhecido como muito pequeno para esse caso. Não defina esse parâmetro como um número de buffers que seja maior (em bytes) que metade do tamanho de um arquivo de log de transações.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Property LogBuffers As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.LogBuffers

instance.LogBuffers = value
```

``` csharp
public int LogBuffers { get; set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe instanceparameters](./instanceparameters-class.md)

[Membros de instanceparameters](./instanceparameters-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
