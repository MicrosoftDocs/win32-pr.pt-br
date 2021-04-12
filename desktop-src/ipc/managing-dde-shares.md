---
description: O DDE de rede fornece funções que permitem excluir um compartilhamento, obter ou definir informações de compartilhamento ou enumerar compartilhamentos.
ms.assetid: d7924e93-75e4-4f94-b159-02408535170d
title: Gerenciando compartilhamentos DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcc8c7d2eb3983aaabd054b9b729daea176bb10
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104297839"
---
# <a name="managing-dde-shares"></a>Gerenciando compartilhamentos DDE

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]

O DDE de rede fornece funções que permitem excluir um compartilhamento, obter ou definir informações de compartilhamento ou enumerar compartilhamentos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tarefa</th>
<th>Procedimento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Excluir um compartilhamento de DDE</td>
<td>Use a função <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a> .</td>
</tr>
<tr class="even">
<td>Obter informações de compartilhamento de DDE</td>
<td>Use a função <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a> .</td>
</tr>
<tr class="odd">
<td>Definir informações de compartilhamento DDE</td>
<td>Use a função <a href="nddesharesetinfo.md"><strong>NDdeShareSetInfo</strong></a> .</td>
</tr>
<tr class="even">
<td>Enumerar compartilhamentos DDE</td>
<td>Use a função <a href="nddeshareenum.md"><strong>NDdeShareEnum</strong></a> . Você também pode enumerar os compartilhamentos DDE confiáveis usando a função <a href="nddetrustedshareenum.md"><strong>NDdeTrustedShareEnum</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td>Enumerar usuários conectados</td>
<td>Use a função <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>NetSessionEnum</strong></a> .</td>
</tr>
<tr class="even">
<td>Alterar o nome do compartilhamento DDE</td>
<td>Exclua o compartilhamento antigo e crie um novo compartilhamento.
<ol>
<li>Recupere as informações de compartilhamento usando <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</li>
<li>Remova o compartilhamento usando <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a>.</li>
<li>Altere o membro <strong>lpszShareName</strong> da estrutura <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> retornada por <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</li>
<li>Passe a estrutura <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> modificada para <a href="nddeshareadd.md"><strong>NDdeShareAdd</strong></a>.</li>
</ol></td>
</tr>
</tbody>
</table>



 

 

