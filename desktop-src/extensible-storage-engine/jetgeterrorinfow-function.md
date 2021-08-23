---
description: 'Saiba mais sobre: função JetGetErrorInfoW'
title: Função JetGetErrorInfoW
TOCTitle: JetGetErrorInfoW Function
ms:assetid: 7a84f937-7a16-434e-896d-789f316ee833
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475859(v=EXCHG.10)
ms:contentKeyID: 37033565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetErrorInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 52f67063ecd4c2cf3828ecccacf4e37a4c30fb1aad534cd6ae1853411d6a28c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119719166"
---
# <a name="jetgeterrorinfow-function"></a>Função JetGetErrorInfoW


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgeterrorinfow-function"></a>Função JetGetErrorInfoW

A função **JetGetErrorInfoW** BAS_ do mecanismo de banco de dados.

observação: esta documentação se baseia em uma versão preliminar do mecanismo de Armazenamento extensível. Essas informações estão sujeitas a alterações.

```cpp
JET_ERR JET_API JetGetErrorInfoW( 
    _In_opt_ void *                      pvContext, 
    _Out_writes_bytes_( cbMax ) void *   pvResult, 
    _In_ unsigned long                   cbMax, 
    _In_ unsigned long                   InfoLevel, 
    _In_ JET_GRBIT                       grbit );
```

### <a name="parameters"></a>Parâmetros

*pvContext*

O contexto ou o valor de erro para o qual as informações de erro estendidas são necessárias. O valor transmitido depende do valor do parâmetro *InfoLevel* .

*pvResult*

Um ponteiro para um buffer que receberá as informações. O tipo do buffer depende do valor do parâmetro *InfoLevel* . O chamador deve ser configurado para alinhar o buffer adequadamente.

*cbMax*

O tamanho máximo da estrutura *pvResult* que é passada.

*InfoLevel*

O tipo de informações que serão recuperadas para as informações de erro/contexto é especificado pelo parâmetro *pvContext* . O formato dos dados armazenados em *pvResult* é dependente de *InfoLevel*.

A tabela a seguir lista os possíveis valores para esse parâmetro.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_ErrorInfoSpecificErr</p></td>
<td><p><em>pvContext</em> é interpretado como um código de/Error <a href="gg269297(v=exchg.10).md">JET_ERR</a>, <em>pvResult</em> é interpretado como um <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>e os campos da estrutura de <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> são preenchidos adequadamente.</p></td>
</tr>
</tbody>
</table>


*grbit*

Reservado.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./extensible-storage-engine-error-codes.md) com um dos códigos de retorno listados na tabela a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

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
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um dos parâmetros fornecidos contém um valor inesperado ou contém um valor que não faz sentido quando combinado com o valor de outro parâmetro. Isso pode ocorrer para <strong>JetGetErrorInfo</strong> quando ocorre o seguinte:</p>
<ul>
<li><p>O valor do parâmetro <em>InfoLevel</em> especificado é inválido.</p></li>
<li><p>O valor de <em>grbit</em> especificado é inválido.</p></li>
<li><p>O valor de <em>cbMax</em> do buffer de parâmetro <em>pvResult</em> especificado é menor que o tamanho necessário para a saída desse parâmetro <em>InfoLevel</em> .</p></li>
<li><p>Para <em>InfoLevel</em> = JET_ErrorInfoSpecificErr, o valor de <a href="gg294092(v=exchg.10).md">JET_ERR</a> passado é desconhecido para o mecanismo.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errDisabledFunctionality</p></td>
<td><p>Se esse SKU do Windows não oferecer suporte a essa função, esse erro será retornado.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, o buffer de saída apropriado para o contexto/valor de erro solicitado será definido para as informações de erro estendidas solicitadas.

Em caso de falha, o estado dos buffers de saída será indefinido.

### <a name="remarks"></a>Comentários

A função [JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md) e [JET_ERRCAT](./jet-errcat.md) grupo de constantes contêm documentação sobre as informações de erro estendidas que são retornadas para *InfoLevel* = JET_ErrorInfoSpecificErr.

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>requer Windows 8 Server.</p></td>
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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Observação: somente o <strong>JetGetErrorInfoW</strong> (Unicode) é implementado. Esta API não tem uma versão (ANSI).</p></td>
</tr>
</tbody>
</table>
