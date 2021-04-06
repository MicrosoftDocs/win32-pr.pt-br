---
title: Auditoria
description: A WFP (plataforma de filtragem do Windows) fornece auditoria de eventos relacionados a firewall e IPsec.
ms.assetid: 30ff9cf7-bf93-4979-bacd-d76e5dadbef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cef1d4fee81afc366a987575935c1de8880092c
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "103917852"
---
# <a name="auditing"></a>Auditoria

A WFP (plataforma de filtragem do Windows) fornece auditoria de eventos relacionados a firewall e IPsec. Esses eventos são armazenados no log de segurança do sistema.

Os eventos auditados são os seguintes.



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
<td>Alteração de política<br/> {6997984D-797A-11D9-BED3-505054503030}<br/></td>
<td>Filtrando alteração de política da plataforma<br/> {0CCE9233-69AE-11D9-BED3-505054503030}<br/></td>
<td><blockquote>
[!Note]<br />
Os números representam as IDs de evento, conforme exibido pelo Visualizador de Eventos (eventvwr.exe).
</blockquote>
<br/> Adição e remoção de objetos WFP:<br/>
<ul>
<li>5440 balão persistente adicionado</li>
<li>5441 tempo de inicialização ou filtro persistente adicionado</li>
<li>5442 provedor persistente adicionado</li>
<li>5443 contexto de provedor persistente adicionado</li>
<li>5444 subcamada persistente adicionada</li>
<li>texto explicativo de tempo de execução 5446 adicionado ou removido</li>
<li>filtro de tempo de execução adicionado ou removido do 5447</li>
<li>5448 provedor de tempo de execução adicionado ou removido</li>
<li>o contexto do provedor de tempo de execução 5449 foi adicionado ou removido</li>
<li>5450 subcamada em tempo de execução adicionada ou removida</li>
</ul></td>
</tr>
<tr class="even">
<td>Acesso a objetos<br/> {6997984A-797A-11D9-BED3-505054503030}<br/></td>
<td>Remoção de pacote de plataforma de filtragem <br/> {0CCE9225-69AE-11D9-BED3-505054503030}<br/></td>
<td>Pacotes removidos por WFP:<br/>
<ul>
<li>pacote 5152 Descartado</li>
<li>pacote de 5153 vetado</li>
</ul></td>
</tr>
<tr class="odd">
<td>Acesso a objetos<br/></td>
<td>Conexão da plataforma de filtragem <br/> {0CCE9226-69AE-11D9-BED3-505054503030}<br/></td>
<td>Conexões permitidas e bloqueadas:<br/>
<ul>
<li>5154 escuta permitida</li>
<li>5155 escuta bloqueada</li>
<li>5156 conexão permitida</li>
<li>5157 conexão bloqueada</li>
<li>5158 Associação permitida</li>
<li>5159 Associação bloqueada</li>
</ul>
<blockquote>
[!Note]<br />
As conexões permitidas nem sempre auditam a ID do filtro associado. O Filterid para TCP será 0, a menos que um subconjunto dessas condições de filtragem seja usado: UserID, AppID, protocolo, porta remota.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Acesso a objetos<br/></td>
<td>Outros eventos de acesso de objeto<br/> {0CCE9227-69AE-11D9-BED3-505054503030}<br/></td>
<td><blockquote>
[!Note]<br />
Essa subcategoria permite muitas auditorias. As auditorias específicas de WFP são listadas abaixo.
</blockquote>
<br/> Status de prevenção de negação de serviço:<br/>
<ul>
<li>modo de prevenção de DoS 5148 de WFP iniciado</li>
<li>modo de prevenção de DoS 5149 de WFP interrompido</li>
</ul></td>
</tr>
<tr class="odd">
<td>Logon/logoff<br/> {69979849-797A-11D9-BED3-505054503030}<br/></td>
<td>Modo principal do IPsec<br/> {0CCE9218-69AE-11D9-BED3-505054503030}<br/></td>
<td>Negociação de modo principal IKE e AuthIP:<br/>
<ul>
<li>4650, associação de segurança 4651 estabelecida</li>
<li>4652, falha na negociação de 4653</li>
<li>4655 Associação de segurança encerrada</li>
</ul></td>
</tr>
<tr class="even">
<td>Logon/logoff<br/></td>
<td>Modo rápido do IPsec <br/> {0CCE9219-69AE-11D9-BED3-505054503030}<br/></td>
<td>Negociação de modo rápido IKE e AuthIP:<br/>
<ul>
<li>Associação de segurança 5451 estabelecida</li>
<li>5452 Associação de segurança encerrada</li>
<li>4654 a negociação falhou</li>
</ul></td>
</tr>
<tr class="odd">
<td>Logon/logoff <br/></td>
<td>Modo estendido do IPsec<br/> {0CCE921A-69AE-11D9-BED3-505054503030}<br/></td>
<td>Negociação de modo estendido AuthIP:<br/>
<ul>
<li>4978 pacote de negociação inválido</li>
<li>4979, 4980, 4981, 4982 Associação de segurança estabelecida</li>
<li>4983, falha na negociação de 4984</li>
</ul></td>
</tr>
<tr class="even">
<td>Sistema<br/> {69979848-797A-11D9-BED3-505054503030}<br/></td>
<td>Driver IPsec<br/> {0CCE9213-69AE-11D9-BED3-505054503030}<br/></td>
<td>Pacotes removidos pelo driver IPsec:<br/>
<ul>
<li>4963 pacote de texto não criptografado de entrada Descartado</li>
</ul></td>
</tr>
</tbody>
</table>



 

Por padrão, a auditoria para WFP está desabilitada.

A auditoria pode ser habilitada por categoria através do snap-in do Editor de Objeto de Política de Grupo MMC, do snap-in do MMC de diretiva de segurança local ou do comando auditpol.exe.

Por exemplo, para habilitar a auditoria de eventos de alteração de diretiva, você pode:

-   Usar o Editor de Objeto de Política de Grupo

    1.  Execute **gpedit. msc**.
    2.  Expanda política de computador local.
    3.  Expanda Configuração do computador.
    4.  Expanda Configurações do Windows.
    5.  Expanda Configurações de segurança.
    6.  Expanda políticas locais.
    7.  Clique em política de auditoria.
    8.  Clique duas vezes em diretiva de auditoria alterar para iniciar a caixa de diálogo Propriedades.
    9.  Verifique as caixas de seleção êxito e falha.

-   Usar a política de segurança local

    1.  Execute **secpol. msc**.
    2.  Expanda políticas locais.
    3.  Clique em política de auditoria.
    4.  Clique duas vezes em diretiva de auditoria alterar para iniciar a caixa de diálogo Propriedades.
    5.  Verifique as caixas de seleção êxito e falha.

-   Usar o comando auditpol.exe

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

[Log de Eventos](/previous-versions/orphan-topics/ws.10/dd996684(v=ws.10))
</dt> <dt>

[Política de Grupo](/windows/deployment/deploy-whats-new)
</dt> </dl>

