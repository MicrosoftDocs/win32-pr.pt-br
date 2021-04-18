---
description: Antes de começar a desenvolver um aplicativo do Microsoft Windows HTTP Services (WinHTTP), primeiro você deve decidir se usará a API C/C++ ou a interface COM.
ms.assetid: 451ad247-962f-4af1-bb21-0aed4ef5f93c
title: Escolhendo uma interface WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc529e6052b0de2de19a7c15ff1cfad226cee2cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765310"
---
# <a name="choosing-a-winhttp-interface"></a>Escolhendo uma interface WinHTTP

Antes de começar a desenvolver um aplicativo do Microsoft Windows HTTP Services (WinHTTP), primeiro você deve decidir se usará a API C/C++ ou a interface COM. A tabela a seguir resume as vantagens e desvantagens associadas a cada uma dessas abordagens.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>API C/C++</th>
<th>Interface COM</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vantagens</td>
<td><ul>
<li>As respostas podem ser processadas em partes, o que é mais eficiente.</li>
<li>As operações POST também podem ser processadas em partes, acelerando o tempo de processamento.</li>
<li>Suporte a AutoProxy.</li>
<li>Acesso ao conjunto completo de recursos do WinHTTP.</li>
<li>Dados binários podem ser facilmente manipulados.</li>
</ul></td>
<td><ul>
<li>A criação de um aplicativo é fácil e requer menos linhas de código do que a API C/C++.</li>
<li>A interface pode ser usada por linguagens de script.</li>
</ul></td>
</tr>
<tr class="even">
<td>Desvantagens</td>
<td><ul>
<li>O processamento é mais complexo.</li>
<li>A API C/C++ requer mais etapas do que a interface COM para executar as mesmas ações.</li>
<li>A configuração de uma solicitação leva mais código.</li>
</ul></td>
<td><ul>
<li>A interface COM não fornece acesso ao conjunto completo de recursos do WinHTTP.</li>
<li>É difícil lidar com tipos de dados binários em algumas linguagens de script, como VBScript e JScript.</li>
<li>A interface COM não oferece suporte a AutoProxy.</li>
<li>Os aplicativos devem usar o modelo de APARTMENT_THREADED COM.</li>
<li>Antes que uma resposta possa começar a ser processada, a resposta inteira deve primeiro ser recebida e armazenada em buffer.</li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



