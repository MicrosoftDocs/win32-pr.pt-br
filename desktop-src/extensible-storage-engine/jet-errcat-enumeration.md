---
description: 'Saiba mais sobre: JET_ERRCAT enumeração'
title: JET_ERRCAT enumeração (Microsoft.Isam.Esent.Interop.Windows8)
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
ms.openlocfilehash: f259edf0e087831cfb667caa5fa8dcf215638ab6d739812fa2e6208327a22f7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119232796"
---
# <a name="jet_errcat-enumeration"></a>JET_ERRCAT enumeração

A categoria de erro. A hierarquia é a seguinte: JET_errcatError | |-- JET_errcatOperation | |-- JET_errcatFatal | |-- JET_errcatIO // problemas de E/S ruins, podem ou não ser transitórios. | |-- JET_errcatResource | |-- JET_errcatMemory // sem memória (todas as variantes) | |-- JET_errcatQuota | |-- JET_errcatDisk // sem espaço em disco (todas as variantes) |-- JET_errcatData | |-- JET_errcatCorruption | |-- JET_errcatInconsistent // normalmente causado por | | JET_errcatFragmentation |-- JET_errcatApi |-- JET_errcatUsage |-- JET_errcatState |-- JET_errcatObsolete-- JET_errcatObsolete

**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

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
<td>Erro do</td>
<td>Uma categoria genérica.</td>
</tr>
<tr class="odd">
<td></td>
<td>Operação</td>
<td>Erros que geralmente podem ocorrer a qualquer momento devido a condições não controláveis. Frequentemente temporário, mas nem sempre. Recuperação: provavelmente, tentar novamente ou, eventualmente, informar o operador.</td>
</tr>
<tr class="even">
<td></td>
<td>Fatal</td>
<td>Esse erro de classificação ocorre somente quando o ESE encontra uma condição de erro tão grave, que não podemos continuar de maneira segura (geralmente transacional) e, em vez de dados corrompidos, lançamos erros dessa categoria. Recuperação: reinicie a instância ou o processo. Se o problema persistir, informe o operador .</td>
</tr>
<tr class="odd">
<td></td>
<td>IO</td>
<td>Os erros vêm do sistema operacional e estão fora do controle do ESE, esse tipo de erro é possivelmente temporário, possivelmente não. Recuperação: tentar novamente. Se não for resolvido, pergunte ao operador sobre o problema de disco.</td>
</tr>
<tr class="even">
<td></td>
<td>Recurso</td>
<td>Essa é uma categoria que indica uma das muitas condições potenciais fora do recurso.</td>
</tr>
<tr class="odd">
<td></td>
<td>Memória</td>
<td>Condição clássica de memória fora da memória. Recuperação: aguarde um pouco e tentar novamente, liberar memória ou sair.</td>
</tr>
<tr class="even">
<td></td>
<td>Quota</td>
<td>Determinados recursos de especialização estão em pools de um determinado tamanho, facilitando a &quot; &quot; detecção de vazamentos desses recursos. Recuperação: pode exigir algumas pequenas alterações de código. Seu aplicativo deve ter uma ação somente de depuração, como uma Assert, nessas condições para detectá-las durante o desenvolvimento. Para código de varejo, recomendamos que você trate esse erro como o erro de categoria Memória e tentar novamente, liberar memória ou encerrar a operação.</td>
</tr>
<tr class="odd">
<td></td>
<td>Disco</td>
<td>Condições fora do disco. Recuperação: pode tentar novamente mais tarde na expectativa de que mais espaço esteja disponível ou pedir ao operador para liberar algum espaço em disco.</td>
</tr>
<tr class="even">
<td></td>
<td>Dados</td>
<td>Um erro relacionado a dados.</td>
</tr>
<tr class="odd">
<td></td>
<td>Corrupção</td>
<td>Meu disco rígido comia minha lição de casa. Problemas de corrupção clássicos, frequentemente permanentes sem ação corretiva. Recuperação: restauração do backup, talvez a operação de reparo de utilitários ese (que apenas salva quais dados são deixados/com perda) . Além disso, no caso de recuperação (JetInit), talvez a recuperação possa ser executada permitindo a perda de dados.</td>
</tr>
<tr class="even">
<td></td>
<td>Inconsistente</td>
<td>Isso é semelhante ao Corruption, em que os arquivos de banco de dados e/ou de log estão em um estado inconsistente e irreconciliável entre si. Geralmente, isso é causado pelo uso indado do aplicativo/administrador. Recuperação: restauração do backup, talvez a operação de reparo de utilitários ese (que apenas salva quais dados são deixados/com perda). Além disso, no caso de recuperação (JetInit), talvez a recuperação possa ser executada permitindo a perda de dados.</td>
</tr>
<tr class="odd">
<td></td>
<td>Fragmentação</td>
<td>Essa é uma classe de erros em que alguns recursos internos persistentes se esgotaram. Recuperação: para erros de banco de dados, a desfragmentação offline corrigirá o problema, para que os arquivos de log recuperem primeiro todos os bancos de dados anexados a um desligamento limpo e, em seguida, exclua todos os arquivos de log e ponto de verificação. </td>
</tr>
<tr class="even">
<td></td>
<td>Api</td>
<td>Um contêiner para Uso e Estado.</td>
</tr>
<tr class="odd">
<td></td>
<td>Uso</td>
<td>Erro de uso clássico, isso significa que o código do cliente não passou argumentos corretos para a API jet. Esse erro provavelmente não desaparecerá com a tentativa de novamente. Recuperação: em termos gerais, o código do cliente deve Assert() essa classe de erros não é retornada, portanto, os problemas podem ser capturados durante o desenvolvimento. No varejo, o aplicativo provavelmente terá pouca opção, mas retornar o problema para o operador.</td>
</tr>
<tr class="even">
<td></td>
<td>Estado</td>
<td>Essa é a classificação para diferentes sinais que a API pode retornar descrever o estado do banco de dados, um caso clássico é JET_errRecordNotFound que pode ser retornado pelo JetSeek() quando o registro solicitado não foi encontrado. Recuperação: não é realmente relevante, depende muito da API.</td>
</tr>
<tr class="odd">
<td></td>
<td>Obsoleto</td>
<td>O erro é reconhecido como um erro válido, mas não deve ser retornado por esta versão da API.</td>
</tr>
<tr class="even">
<td></td>
<td>Máx.</td>
<td>O valor máximo para a enum. Isso não deve ser usado.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
