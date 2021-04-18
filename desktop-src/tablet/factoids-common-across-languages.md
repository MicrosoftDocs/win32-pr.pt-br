---
description: Vários factos descrevem a entrada que é comum a todos os reconhecedores de linguagem e não precisam ter formatos diferentes para idiomas diferentes. A tabela a seguir lista os factos que são comuns em todos os idiomas.
ms.assetid: dae4a28d-0332-4bb2-b040-13a959c7945e
title: Factos comuns entre linguagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1faefbb9991562535f711f867c45bd614c595941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814013"
---
# <a name="factoids-common-across-languages"></a>Factos comuns entre linguagens

Vários factos descrevem a entrada que é comum a todos os reconhecedores de linguagem e não precisam ter formatos diferentes para idiomas diferentes. A tabela a seguir lista os factos que são comuns em todos os idiomas.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Facto</th>
<th>Definição</th>
<th>Exemplos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Dígito</strong></td>
<td>Define a tendência de um único dígito. O reconhecedor é polarizado para retornar apenas dígitos únicos quando esse factor é definido.<br/></td>
<td>0-9<br/></td>
</tr>
<tr class="even">
<td><strong>Email</strong></td>
<td>Define a tendência de um endereço de email.<br/></td>
<td>someone@example.com<br/></td>
</tr>
<tr class="odd">
<td><strong>Web</strong></td>
<td>Define a tendência para vários formatos de URL.<br/>
<blockquote>
[!Note]<br />
As configurações padrão do reconhecedor incluem o facto <strong>da Web</strong> . Por isso, você não pode notar uma grande diferença entre o facto <strong>da Web</strong> e a configuração padrão. No entanto, o facto <strong>da Web</strong> ajuda a eliminar espaços entre palavras em uma URL.
</blockquote>
<br/></td>
<td>http: \\ Microsoft.net<br/> https://microsoft.us/<br/> https: \\ www.Microsoft.au \<br/> https://microsoft.com<br/> www.microsoft_world. com<br/> www.microsoft.us \<br/> http: \\www.microsoft.com\myfile.htm<br/> http: \\www.microsoft.com\myfile.html<br/> http: \\ www. Microsoft. com\myfile.asp<br/> http: \\ www.Microsoft.uk<br/> http: \\ www.Microsoft.info<br/> www.microsoft.biz<br/></td>
</tr>
<tr class="even">
<td><strong>Padrão</strong></td>
<td>Retorna o reconhecedor às suas configurações padrão.<br/></td>
<td>A configuração padrão de factores para idiomas ocidentais inclui o dicionário do sistema, o dicionário do usuário, várias pontuações e as inicializações <strong>da Web</strong> e de <strong>número</strong> .<br/> A configuração padrão para o factos para idiomas do leste asiático inclui todos os caracteres suportados pelo reconhecedor.<br/></td>
</tr>
<tr class="odd">
<td><strong>Nenhuma</strong></td>
<td>Desabilita todos os factos, dicionários e o modelo de linguagem.<br/></td>
<td>Esse factor deve ser usado somente quando você não quiser que o reconhecedor Use quaisquer regras ou dicionários gramaticais, incluindo o dicionário do sistema. Esse factor é útil para entrada de cadeias de caracteres aleatórias, como códigos de produto. Não use o sinalizador de coerção com esse factor.<br/></td>
</tr>
</tbody>
</table>



 

 

 




