---
description: 'Saiba mais sobre: enumeração de JET_ERRCAT'
title: Enumeração de JET_ERRCAT (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: JET_ERRCAT enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_errcat(v=EXCHG.10)
ms:contentKeyID: 55104419
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e08ec4ce308003dc30edaa32a07000e244dc9f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169796"
---
# <a name="jet_errcat-enumeration"></a>Enumeração de JET_ERRCAT

A categoria de erro. A hierarquia é a seguinte: JET_errcatError | |--JET_errcatOperation | |--JET_errcatFatal | |--JET_errcatIO//problemas de e/s inválidos, pode ou não ser transitório. | |--JET_errcatResource | |--JET_errcatMemory//memória insuficiente (todas as variantes) | |--JET_errcatQuota | |--JET_errcatDisk//sem espaço em disco (todas as variantes) |--JET_errcatData | |--JET_errcatCorruption | |--JET_errcatInconsistent//normalmente causado por um usuário indisponível | |--JET_errcatFragmentation |--JET_errcatApi |--JET_errcatUsage |--JET_errcatState |--JET_errcatObsolete

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Enumeration JET_ERRCAT
'Usage
Dim instance As JET_ERRCAT
```

``` csharp
public enum JET_ERRCAT
```

## <a name="members"></a>Membros

<table>
<thead>
<tr class="header">
<th></th>
<th>Nome do membro</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Unknown</td>
<td>Categoria desconhecida.</td>
</tr>
<tr class="even">
<td></td>
<td>Erro</td>
<td>Uma categoria genérica.</td>
</tr>
<tr class="odd">
<td></td>
<td>Operação</td>
<td>Erros que geralmente podem ocorrer a qualquer momento devido a condições não controláveis. Geralmente temporário, mas nem sempre. Recuperação: provavelmente tentar novamente ou, eventualmente, informar o operador.</td>
</tr>
<tr class="even">
<td></td>
<td>Fatais</td>
<td>Esse erro de classificação ocorre somente quando o ESE encontra uma condição de erro tão grave, que não podemos continuar em uma maneira segura (geralmente transacional) e em vez de dados corrompidos que lançamos erros dessa categoria. Recuperação: reinicie a instância ou o processo. Se o problema persistir, informe o operador.</td>
</tr>
<tr class="odd">
<td></td>
<td>IO</td>
<td>Os erros são provenientes do sistema operacional e estão fora do controle do ESE, esse tipo de erro é possivelmente temporário, possivelmente não. Recuperação: tente novamente. Se não for resolvido, pergunte ao operador sobre o problema do disco.</td>
</tr>
<tr class="even">
<td></td>
<td>Recurso</td>
<td>Essa é uma categoria que indica uma das muitas condições de fora do recurso em potencial.</td>
</tr>
<tr class="odd">
<td></td>
<td>Memória</td>
<td>Condição clássica de memória insuficiente. Recuperação: Aguarde um momento e tente novamente, libere memória ou saia.</td>
</tr>
<tr class="even">
<td></td>
<td>Quota</td>
<td>Determinados &quot; &quot; recursos de especialidade estão em pools de um determinado tamanho, facilitando a detecção de vazamentos desses recursos. Recuperação: pode exigir algumas alterações de código secundárias. Seu aplicativo deve ter uma ação de depuração apenas, como uma declaração, nessas condições para detectá-los durante o desenvolvimento. Para o código de varejo, recomendamos que você trate esse erro como o erro de categoria de memória e tente novamente, libere memória ou saia da operação.</td>
</tr>
<tr class="odd">
<td></td>
<td>Disco</td>
<td>Sem condições de disco. Recuperação: pode tentar novamente mais tarde na esperança de mais espaço disponível ou peça ao operador para liberar espaço em disco.</td>
</tr>
<tr class="even">
<td></td>
<td>Dados</td>
<td>Um erro relacionado a dados.</td>
</tr>
<tr class="odd">
<td></td>
<td>Danos</td>
<td>Minha unidade de disco rígido me tenho minha casa. Problemas de corrupção clássicos, frequentemente permanentes sem ação corretiva. Recuperação: restauração a partir do backup, talvez a operação de reparo de utilitários ESE (que apenas recupera quais dados são deixados/perdidos). Também no caso de recuperação (JetInit), talvez a recuperação possa ser realizada, permitindo a perda de dados.</td>
</tr>
<tr class="even">
<td></td>
<td>Inconsistente</td>
<td>Isso é semelhante à corrupção de que os arquivos de banco de dados e/ou de log estão em um estado inconsistente e não reconciliado entre si. Geralmente, isso é causado por indisponibilidade de aplicativo/administrador. Recuperação: restauração a partir do backup, talvez a operação de reparo de utilitários ESE (que apenas recupera quais dados são deixados/perdidos). Também no caso de recuperação (JetInit), talvez a recuperação possa ser realizada, permitindo a perda de dados.</td>
</tr>
<tr class="odd">
<td></td>
<td>Fragmentação</td>
<td>Essa é uma classe de erros em que algum recurso interno persistente foi executado. Recuperação: para erros de banco de dados, a desfragmentação offline corrigirá o problema, para os arquivos de log, _primeiro_ Recupere todos os bancos de dados anexados para um desligamento limpo e exclua todos os arquivos de log e o ponto de verificação.</td>
</tr>
<tr class="even">
<td></td>
<td>API</td>
<td>Um contêiner para uso e estado.</td>
</tr>
<tr class="odd">
<td></td>
<td>Uso</td>
<td>Erro de uso clássico, isso significa que o código do cliente não passou os argumentos corretos para a API do JET. Esse erro provavelmente não vai desaparecer com a repetição. Recuperação: o código do cliente em geral deve declarar () essa classe de erros não é retornada, de modo que os problemas podem ser detectados durante o desenvolvimento. No varejo, o aplicativo provavelmente terá pouca opção, mas para retornar o problema até o operador.</td>
</tr>
<tr class="even">
<td></td>
<td>Estado</td>
<td>Essa é a classificação para diferentes sinais que a API poderia retornar para descrever o estado do banco de dados, um caso clássico é JET_errRecordNotFound que pode ser retornado por JetSeek () quando o registro solicitado não foi encontrado. Recuperação: não é realmente relevante, depende muito da API.</td>
</tr>
<tr class="odd">
<td></td>
<td>Obsoleto</td>
<td>O erro é reconhecido como um erro válido, mas não se espera que ele seja retornado por esta versão da API.</td>
</tr>
<tr class="even">
<td></td>
<td>Máx</td>
<td>O valor máximo para a enumeração. Isso não deve ser usado.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft. ISAM. ESENT. Interop. windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
