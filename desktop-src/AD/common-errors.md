---
title: Erros comuns (AD DS)
description: A tabela a seguir contém uma lista de erros comuns que podem ocorrer com base no escopo do grupo que está sendo aninhado.
ms.assetid: 844d4280-a943-4906-b0c6-0c650ef9c114
ms.tgt_platform: multiple
keywords:
- ANÚNCIOS de erros comuns
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c719aad39690932de51c58d0f8081a8c855980bd
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/11/2019
ms.locfileid: "104453830"
---
# <a name="common-errors-ad-ds"></a>Erros comuns (AD DS)

A tabela a seguir contém uma lista de erros comuns que podem ocorrer com base no escopo do grupo que está sendo aninhado.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>HRESULT</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0x8007001F</td>
<td>Falha geral. Esse erro ocorrerá se você tentar:
<ul>
<li>Adicione um grupo de domínio local a um grupo global ou universal ou a um grupo de domínio local em outro domínio. Grupos locais de domínio só podem ser adicionados como membros a outros grupos locais de domínio no mesmo domínio.</li>
<li>Adicione um grupo universal a um grupo global. Grupos universais podem ser adicionados a grupos universais e locais de domínio, mas não a grupos globais.</li>
</ul></td>
</tr>
<tr class="even">
<td>0x8007202F</td>
<td><strong>ERROR_DS_CONSTRAINT_VIOLATION</strong>. Esse erro ocorrerá se você tentar adicionar um grupo de segurança a outro grupo em um domínio em execução no modo misto. Os grupos de segurança não podem ser aninhados no modo misto; os grupos de segurança só podem ser aninhados no modo nativo.</td>
</tr>
</tbody>
</table>



 

 

 




