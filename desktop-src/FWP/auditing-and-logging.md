---
title: Auditoria
description: Windows A WFP (Plataforma de Filtragem) fornece auditoria de eventos relacionados ao firewall e ao IPsec.
ms.assetid: 30ff9cf7-bf93-4979-bacd-d76e5dadbef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 854841685bab015fc0b9a4bc985762df46a7f0c89eae3d38b4b63e081107b70b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015404"
---
# <a name="auditing"></a>Auditoria

O Windows WFP (Plataforma de Filtragem de Dados) fornece auditoria de eventos relacionados ao firewall e ao IPsec. Esses eventos são armazenados no log de segurança do sistema.

Os eventos auditados são os a seguir.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Categoria de auditoria</th>
<th>Subcategoria de auditoria</th>
<th>Eventos auditados</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Alteração da Política<br/> {6997984D-797A-11D9-BED3-505054503030}<br/></td>
<td>Filtragem de alteração de política de plataforma<br/> {0CCE9233-69AE-11D9-BED3-505054503030}<br/></td>
<td><blockquote>
[!Note]<br />
Os números representam as IDs de evento, conforme exibido por Visualizador de Eventos (eventvwr.exe).
</blockquote>
<br/> Adição e remoção do objeto WFP:<br/>
<ul>
<li>5440 Chamada persistente adicionada</li>
<li>5441 Tempo de inicialização ou filtro persistente adicionado</li>
<li>5442 Provedor persistente adicionado</li>
<li>5443 Contexto de provedor persistente adicionado</li>
<li>5444 Sub-camada persistente adicionada</li>
<li>5446 Tempo de run-time adicionado ou removido</li>
<li>5447 Filtro de tempo de run-time adicionado ou removido</li>
<li>5448 Provedor de tempo de run-time adicionado ou removido</li>
<li>5449 Contexto do provedor de tempo de run-time adicionado ou removido</li>
<li>5450 Sub-camada de tempo de run-time adicionada ou removida</li>
</ul></td>
</tr>
<tr class="even">
<td>Acesso a objetos<br/> {6997984A-797A-11D9-BED3-505054503030}<br/></td>
<td>Filtrando a queda de pacotes da plataforma <br/> {0CCE9225-69AE-11D9-BED3-505054503030}<br/></td>
<td>Pacotes descartados pelo WFP:<br/>
<ul>
<li>Pacote 5152 descartado</li>
<li>5153 Pacote vetado</li>
</ul></td>
</tr>
<tr class="odd">
<td>Acesso a objetos<br/></td>
<td>Filtragem de conexão de plataforma <br/> {0CCE9226-69AE-11D9-BED3-505054503030}<br/></td>
<td>Conexões permitidas e bloqueadas:<br/>
<ul>
<li>5154 Escutar permitido</li>
<li>5155 Escutar bloqueado</li>
<li>5156 Conexão permitida</li>
<li>5157 Conexão bloqueada</li>
<li>5158 A vinculação permitida</li>
<li>5159 Vinculação bloqueada</li>
</ul>
<blockquote>
[!Note]<br />
As conexões permitidas nem sempre auditam a ID do filtro associado. A FilterID para TCP será 0, a menos que um subconjunto dessas condições de filtragem seja usado: UserID, AppID, Protocol, Remote Port.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Acesso a objetos<br/></td>
<td>Outros eventos de acesso a objetos<br/> {0CCE9227-69AE-11D9-BED3-505054503030}<br/></td>
<td><blockquote>
[!Note]<br />
Essa subcategoria permite muitas auditorias. As auditorias específicas do WFP estão listadas abaixo.
</blockquote>
<br/> Status de prevenção de negação de serviço:<br/>
<ul>
<li>5148 O modo de prevenção do DoS do WFP foi iniciado</li>
<li>5149 Modo de prevenção do DoS WFP interrompido</li>
</ul></td>
</tr>
<tr class="odd">
<td>Logon/Logoff<br/> {69979849-797A-11D9-BED3-505054503030}<br/></td>
<td>Modo Principal do IPsec<br/> {0CCE9218-69AE-11D9-BED3-505054503030}<br/></td>
<td>Negociação do modo principal IKE e AuthIP:<br/>
<ul>
<li>4650, 4651 Associação de segurança estabelecida</li>
<li>Falha na negociação 4652, 4653</li>
<li>4655 Associação de segurança encerrada</li>
</ul></td>
</tr>
<tr class="even">
<td>Logon/Logoff<br/></td>
<td>Modo Rápido do IPsec <br/> {0CCE9219-69AE-11D9-BED3-505054503030}<br/></td>
<td>Negociação do modo rápido IKE e AuthIP:<br/>
<ul>
<li>5451 Associação de segurança estabelecida</li>
<li>5452 Associação de segurança encerrada</li>
<li>Falha na negociação 4654</li>
</ul></td>
</tr>
<tr class="odd">
<td>Logon/Logoff <br/></td>
<td>Modo Estendido IPsec<br/> {0CCE921A-69AE-11D9-BED3-505054503030}<br/></td>
<td>Negociação do Modo Estendido do AuthIP:<br/>
<ul>
<li>4978 Pacote de negociação inválido</li>
<li>4979, 4980, 4981, 4982 Associação de segurança estabelecida</li>
<li>Falha na negociação 4983, 4984</li>
</ul></td>
</tr>
<tr class="even">
<td>Sistema<br/> {69979848-797A-11D9-BED3-505054503030}<br/></td>
<td>IPsec Driver<br/> {0CCE9213-69AE-11D9-BED3-505054503030}<br/></td>
<td>Pacotes descartados pelo driver IPsec:<br/>
<ul>
<li>4963 Pacote de texto não limpo de entrada descartado</li>
</ul></td>
</tr>
</tbody>
</table>



 

Por padrão, a auditoria do WFP está desabilitada.

A auditoria pode ser habilitada por categoria por meio do snap-in do MMC do Editor de Objeto de Política de Grupo, do snap-in do MMC da Política de Segurança Local ou do comando auditpol.exe.

Por exemplo, para habilitar a auditoria de eventos de Alteração de Política, você pode:

-   Usar o Editor de Objeto de Política de Grupo

    1.  Execute **gpedit.msc**.
    2.  Expanda Política de Computador Local.
    3.  Expanda Configuração do Computador.
    4.  Expanda Configurações do Windows.
    5.  Expanda Segurança Configurações.
    6.  Expanda Políticas Locais.
    7.  Clique em Política de Auditoria.
    8.  Clique duas vezes em Alterar política de auditoria para iniciar a caixa de diálogo Propriedades.
    9.  Marque as caixas de seleção Êxito e Falha.

-   Usar a política de segurança local

    1.  Execute **secpol.msc**.
    2.  Expanda Políticas Locais.
    3.  Clique em Política de Auditoria.
    4.  Clique duas vezes em Alterar política de auditoria para iniciar a caixa de diálogo Propriedades.
    5.  Marque as caixas de seleção Êxito e Falha.

-   Usar o auditpol.exe comando

    -   **Auditpol/set/Category: "alteração de política"/success: habilitar/Failure: habilitar**

A auditoria pode ser habilitada em uma base por subcategoria somente por meio do comando auditpol.exe.

Os nomes de categoria e subcategoria de auditoria são localizados. Para evitar a localização de scripts de auditoria, os GUIDs correspondentes podem ser usados no lugar dos nomes.

Por exemplo, para habilitar a auditoria de filtragem de eventos de alteração de política de plataforma, você pode usar um dos seguintes comandos:

-   **Auditpol/set/SubCategory: "filtro de alteração de política da plataforma de filtragem"/success: habilitar/Failure: habilitar**
-   **Auditpol/set/SubCategory: "{0CCE9233-69AE-11D9-BED3-505054503030}"/success: habilitar/Failure: Enable**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Auditpol](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc731451(v=ws.11))
</dt> <dt>

[Log de eventos](/previous-versions/orphan-topics/ws.10/dd996684(v=ws.10))
</dt> <dt>

[Política de Grupo](/windows/deployment/deploy-whats-new)
</dt> </dl>

