---
description: 'Saiba mais sobre: função JetCloseFileInstance'
title: Função JetCloseFileInstance
TOCTitle: JetCloseFileInstance Function
ms:assetid: 64a38655-b128-453b-9593-46032bd6c470
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269270(v=EXCHG.10)
ms:contentKeyID: 32765572
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d575e90d828159f310a27068ce8d88b29970f4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501294"
---
# <a name="jetclosefileinstance-function"></a>Função JetCloseFileInstance


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetclosefileinstance-function"></a>Função JetCloseFileInstance

A função **JetCloseFileInstance** fecha um arquivo que foi aberto com [JetOpenFileInstance](./jetopenfileinstance-function.md) depois que os dados desse arquivo foram extraídos usando [JetReadFileInstance](./jetreadfileinstance-function.md).

**Windows XP: o JetCloseFileInstance** é introduzido no Windows XP.

```cpp
    JET_ERR JET_API JetCloseFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile
    );
```

### <a name="parameters"></a>Parâmetros

*cópia*

A instância a ser usada para esta chamada.

Para o Windows 2000, a variante de API que aceita esse parâmetro não está disponível porque há suporte para apenas uma instância. O uso dessa instância global é implícito nesse caso.

Para o Windows XP e versões posteriores, a variante de API que não aceita esse parâmetro só pode ser chamada quando o mecanismo está no modo herdado (modo de compatibilidade do Windows 2000), em que apenas uma instância tem suporte. Caso contrário, a operação falhará com JET_errRunningInMultiInstanceMode.

*hfFile*

O identificador do arquivo a ser lido.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código de retorno</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>A operação foi concluída com sucesso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p>
<p>Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um dos parâmetros fornecidos continha um valor inesperado ou a combinação de vários valores de parâmetro gerou um resultado inesperado. Isso pode ocorrer para <strong>JetCloseFileInstance</strong> quando:</p>
<ul>
<li><p>O identificador de instância especificado é inválido (Windows XP e versões posteriores)</p></li>
<li><p>O identificador de arquivo especificado é inválido</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>A operação falhou porque nenhum backup externo está em andamento.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade do Windows 2000) em que apenas uma instância tem suporte quando, na verdade, várias instâncias já existem.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, o identificador do arquivo é fechado. Se um arquivo de banco de dados foi fechado, o arquivo de patch do banco de dados associado (se houver) será destruído.

Em caso de falha, nenhuma alteração ocorre.

#### <a name="remarks"></a>Comentários

O mecanismo de banco de dados atualmente dá suporte apenas a um arquivo aberto por meio de [JetOpenFileInstance](./jetopenfileinstance-function.md) por vez. Se um identificador de arquivo for aberto usando [JetOpenFileInstance](./jetopenfileinstance-function.md) , ele deverá ser fechado usando **JetCloseFileInstance** antes que outro arquivo possa ser aberto.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista ou o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008 ou o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Biblioteca</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFileInstance](./jetopenfileinstance-function.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopServiceInstance](./jetstopserviceinstance-function.md)
