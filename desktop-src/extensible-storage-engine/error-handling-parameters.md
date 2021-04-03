---
description: 'Saiba mais sobre: parâmetros de tratamento de erros'
title: Parâmetros de tratamento de erros
TOCTitle: Error Handling Parameters
ms:assetid: 014996a1-5674-40c7-9538-54cae1681fec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269173(v=EXCHG.10)
ms:contentKeyID: 32765476
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eb225d7dbb67655286635320352060bcf2cb8a5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837247"
---
# <a name="error-handling-parameters"></a>Parâmetros de tratamento de erros


_**Aplica-se a:** Windows | Windows Server_

## <a name="error-handling-parameters"></a>Parâmetros de tratamento de erros

Este tópico contém parâmetros que são usados para tratamento de erros.

*JET_paramErrorToString* 70  

Esse parâmetro pode ser usado para converter um [JET_ERR](./jet-err.md) em uma cadeia de caracteres. Isso é feito usando uma chamada especial para [JetGetSystemParameter](./jetgetsystemparameter-function.md) , em que o buffer de saída de inteiro contém o valor de [JET_ERR](./jet-err.md) a ser convertido (como um parâmetro de entrada) e o buffer de saída de cadeia de caracteres retorna a cadeia de caracteres de erro correspondente. A cadeia de caracteres terá uma aparência semelhante a esta: "JET_errSuccess, operação bem-sucedida". A cadeia de caracteres é composta pelo nome simbólico para a cadeia de caracteres, uma vírgula e uma descrição de texto simples do erro. A cadeia de caracteres de descrição pode conter vírgulas. Se o erro não for reconhecido, a cadeia de caracteres será "erro desconhecido, erro desconhecido".

**Observação**  Esse parâmetro é somente leitura.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>Especial</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Especial</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>Especial</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>

*JET_paramExceptionAction*  
98  

Esse parâmetro controla o que acontece quando uma exceção é lançada pelo mecanismo de banco de dados ou pelo código que é chamado pelo mecanismo de banco de dados. Quando definido como JET_ExceptionMsgBox, qualquer exceção será lançada para o filtro de exceção sem tratamento do Windows. Isso fará com que a exceção seja tratada como uma falha do aplicativo. A intenção é impedir que o código do aplicativo tente detectar erroneamente e ignorar uma exceção gerada pelo mecanismo de banco de dados. Isso não pode ser permitido porque a corrupção do banco de dados pode ocorrer. Se o aplicativo quiser lidar corretamente com essas exceções, a proteção poderá ser desabilitada definindo esse parâmetro como JET_ExceptionNone.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>JET_ExceptionMsgBox</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>JET_ExceptionMsgBox, JET_ExceptionNone</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003:  </strong>  Não</p>
<p><strong>Windows Vista:</strong>  Ok</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003:  </strong>  Não</p>
<p><strong>Windows Vista:</strong>  Ok</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
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
<td><p>Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
</tbody>
</table>

### <a name="see-also"></a>Consulte Também

[Constantes de tratamento de erro](./error-handling-constants.md)  
[Códigos de erro do mecanismo de armazenamento extensível](./extensible-storage-engine-error-codes.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JetInit](./jetinit-function.md)
