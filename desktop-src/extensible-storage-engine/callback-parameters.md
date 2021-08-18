---
description: 'Saiba mais sobre: Parâmetros de retorno de chamada'
title: Parâmetros de retorno de chamada
TOCTitle: Callback Parameters
ms:assetid: 7f3cdc13-ffbd-4e5a-b650-1c6388e784dc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269310(v=EXCHG.10)
ms:contentKeyID: 32765600
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a9c14940ee98d4f664914794cd4ff6185b78dd04f438b982179a7ab3c5eb6504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118982806"
---
# <a name="callback-parameters"></a>Parâmetros de retorno de chamada


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="callback-parameters"></a>Parâmetros de retorno de chamada

Este tópico contém parâmetros usados para retornos de chamada.

*JET_paramDisableCallbacks*  
65  

Esse parâmetro desabilita todos os retornos de chamada do mecanismo de banco de dados para as funções fornecidas pelo aplicativo. Ele destina-se principalmente a dar suporte aos utilitários do mecanismo de banco de dados e não se destina a ser usado em seu aplicativo.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>Falso</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta recursos:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows XP e versões posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramEnablePersistedCallbacks*  
156  

Esse parâmetro permite o uso de retornos de chamada persistentes no banco de dados. Em versões anteriores ao Windows Vista, o uso de retornos de chamada persistentes era habilitado por padrão. Os aplicativos agora devem habilitar explicitamente o uso de retornos de chamada persistentes em runtime usando esse parâmetro. Se esse parâmetro não estiver definido, qualquer operação de banco de dados que exija a invocação de um retorno de chamada falhará com JET_errCallbackFailed. Esse parâmetro não afeta nenhum retorno de chamada especificado em runtime com os seguintes mecanismos: JET_paramRuntimeCallback, [JetRegisterCallback](./jetregistercallback-function.md)ou um parâmetro de retorno de chamada explícito para uma API JET. Ainda é possível criar elementos de esquema que contêm retornos de chamada persistentes mesmo quando o uso desses retornos de chamada persistentes não é permitido. Quando esse parâmetro é definido como false, ele substitui JET_paramDisableCallbacks.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>Falso</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta recursos:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows Vista e versões posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramRuntimeCallback*  
73  

Esse parâmetro configura o mecanismo com uma função de retorno de chamada de runtime que implementa a [JET_CALLBACK](./jet-callback-callback-function.md) interface. Esse retorno de chamada pode ser chamado pelos seguintes motivos: [JET_cbtypFreeCursorLS](./jet-cbtyp.md), [JET_cbtypFreeTableLS](./jet-cbtyp.md)ou [JET_cbtypNull](./jet-cbtyp.md). Consulte [JetSetLS para](./jetsetls-function.md) obter mais informações.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>NULO</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Ponteiro de função (JET_API_PTR)</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>NULL, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>*</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta recursos:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows XP e versões posteriores</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer Windows Vista ou Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer Windows Server 2008 ou Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JET_API_PTR](./jet-api-ptr.md)  
[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetLS](./jetsetls-function.md)
