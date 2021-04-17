---
description: Você pode fornecer todas as informações necessárias para configurar adicionar ou remover programas no painel de controle definindo os valores de determinadas propriedades do instalador no pacote de Windows Installer do seu aplicativo.
ms.assetid: 2eb00fe5-e441-4fce-9623-81a089269a2b
title: Configurando adicionar/remover programas com Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6850163e18af94aa9cceaf6c4bb2e8059dcf2121
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/30/2021
ms.locfileid: "105994504"
---
# <a name="configuring-addremove-programs-with-windows-installer"></a>Configurando adicionar/remover programas com Windows Installer

Você pode fornecer todas as informações necessárias para configurar adicionar ou remover programas no painel de controle definindo os valores de determinadas propriedades do instalador no pacote de Windows Installer do seu aplicativo. Definir essas propriedades grava automaticamente os valores correspondentes no registro. Se o instalador detectar que o produto está marcado para remoção completa, as operações serão adicionadas automaticamente ao script para remover a pasta adicionar/remover programas nas informações do painel de controle do produto.

Se um aplicativo não estiver registrado, ele não estará listado em Adicionar/remover programas no painel de controle. Para obter mais informações, consulte [adicionando e removendo um aplicativo e não deixando nenhum rastreamento no registro](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).

Os aplicativos que foram instalados no [contexto de instalação](installation-context.md) por usuário são exibidos em Adicionar/remover programas do usuário atual. Os aplicativos que foram instalados no contexto de instalação por máquina são exibidos em Adicionar ou remover programas de todos os usuários. Aplicativos que não foram instalados por computador e foram instalados apenas como aplicativos por usuário para usuários que não sejam o usuário atual, não aparecem em Adicionar ou remover programas do usuário atual.

Observe que os pacotes de instalação que usam a propriedade [**LIMITUI**](limitui.md) também devem conter o [**ARPNOMODIFY**](arpnomodify.md). Isso é necessário para que um usuário obtenha o comportamento correto em Adicionar ou remover programas no utilitário do painel de controle ao tentar configurar um produto.

O instalador usa as [Propriedades públicas](public-properties.md) a seguir para gerenciar adicionar/remover programas no painel de controle.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome da propriedade</th>
<th>Breve descrição da propriedade</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="arpauthorizedcdfprefix.md"><strong>ARPAUTHORIZEDCDFPREFIX</strong></a></td>
<td>URL do canal de atualização do aplicativo. O valor que o instalador grava na <a href="uninstall-registry-key.md">chave de registro de desinstalação</a>.</td>
</tr>
<tr class="even">
<td><a href="arpcomments.md"><strong>ARPCOMMENTS</strong></a></td>
<td>Fornece comentários para adicionar ou remover programas no painel de controle. O valor que o instalador grava na <a href="uninstall-registry-key.md">chave de registro de desinstalação</a>.</td>
</tr>
<tr class="odd">
<td><a href="arpcontact.md"><strong>ARPCONTACT</strong></a></td>
<td>Fornece o contato para adicionar ou remover programas no painel de controle. O valor que o instalador grava na <a href="uninstall-registry-key.md">chave de registro de desinstalação</a>.</td>
</tr>
<tr class="even">
<td><a href="arpinstalllocation.md"><strong>ARPINSTALLLOCATION</strong></a></td>
<td>Caminho totalmente qualificado para a pasta principal do aplicativo. O valor que o instalador grava na <a href="uninstall-registry-key.md">chave de registro de desinstalação</a>.</td>
</tr>
<tr class="odd">
<td><a href="arphelplink.md"><strong>ARPHELPLINK</strong></a></td>
<td>Endereço da Internet, ou URL, para obter suporte técnico. O valor que o instalador grava na <a href="uninstall-registry-key.md">chave de registro de desinstalação</a>.</td>
</tr>
<tr class="even">
<td><a href="arphelptelephone.md"><strong>ARPHELPTELEPHONE</strong></a></td>
<td>Números de telefone de suporte técnico. O valor que o instalador grava na <a href="uninstall-registry-key.md">chave de registro de desinstalação</a>.</td>
</tr>
<tr class="odd">
<td><a href="arpnomodify.md"><strong>ARPNOMODIFY</strong></a></td>
<td>Impede a exibição de um botão de alteração para o produto em Adicionar ou remover programas no painel de controle.
<blockquote>
<b>Observação:</b> Isso afeta apenas a exibição no ARP. O Windows Installer ainda é capaz de reparar, instalar sob demanda e desinstalar aplicativos por meio de uma linha de comando ou da interface de programação.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a></td>
<td>Impede a exibição de um botão remover do produto em Adicionar ou remover programas no painel de controle. O produto ainda pode ser removido selecionando o botão alterar se o pacote de instalação tiver sido criado com uma interface do usuário que fornece a remoção do produto como uma opção.
<blockquote>
<b>Observação:</b> Isso afeta apenas a exibição no ARP. O Windows Installer ainda é capaz de reparar, instalar sob demanda e desinstalar aplicativos por meio de uma linha de comando ou da interface de programação.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="arpnorepair.md"><strong>ARPNOREPAIR</strong></a></td>
<td>Desabilita o botão reparar em Adicionar ou remover programas no painel de controle.
<blockquote>
<b>Observação:</b> Isso afeta apenas a exibição no ARP. O Windows Installer ainda é capaz de reparar, instalar sob demanda e desinstalar aplicativos por meio de uma linha de comando ou da interface de programação.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpproducticon.md"><strong>ARPPRODUCTICON</strong></a></td>
<td>Identifica o ícone exibido em Adicionar ou remover programas. Se essa propriedade não for definida, adicionar/remover programas especificará o ícone de exibição.</td>
</tr>
<tr class="odd">
<td><a href="arpreadme.md"><strong>ARPREADME</strong></a></td>
<td>Fornece o Leiame para adicionar ou remover programas no painel de controle. O valor que o instalador grava na <a href="uninstall-registry-key.md">chave de registro de desinstalação</a>.</td>
</tr>
<tr class="even">
<td><a href="arpsize.md"><strong>ARPSIZE</strong></a></td>
<td>Tamanho estimado do aplicativo em KB.</td>
</tr>
<tr class="odd">
<td><a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a></td>
<td>Impede a exibição do aplicativo na lista de programas de adicionar/remover programas no painel de controle.
<blockquote>
<b>Observação:</b> Isso afeta apenas a exibição no ARP. O Windows Installer ainda é capaz de reparar, instalar sob demanda e desinstalar aplicativos por meio de uma linha de comando ou da interface de programação.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpurlinfoabout.md"><strong>ARPURLINFOABOUT</strong></a></td>
<td>URL para home page do aplicativo. O valor que o instalador grava na <a href="uninstall-registry-key.md">chave de registro de desinstalação</a>.</td>
</tr>
<tr class="odd">
<td><a href="arpurlupdateinfo.md"><strong>ARPURLUPDATEINFO</strong></a></td>
<td>URL para informações de atualização do aplicativo. O valor que o instalador grava na <a href="uninstall-registry-key.md">chave de registro de desinstalação</a>.</td>
</tr>
</tbody>
</table>

> [!Note]  
> Para obter informações sobre a ferramenta definir programas e padrões, consulte a seção [trabalhando com definir acesso do programa e padrões do computador](/previous-versions//bb776877(v=vs.85)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desinstalar chave do registro](uninstall-registry-key.md)
</dt> </dl>
