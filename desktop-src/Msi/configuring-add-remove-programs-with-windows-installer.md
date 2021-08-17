---
description: Você pode fornecer todas as informações necessárias para configurar Adicionar/Remover Programas no Painel de Controle definindo os valores de determinadas propriedades do instalador no pacote do instalador Windows aplicativo.
ms.assetid: 2eb00fe5-e441-4fce-9623-81a089269a2b
title: Configurando Adicionar/Remover Programas com Windows Instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99e1393eb586cfe1067840e4622fddd777a84512f55f9e82f7c9fad3b1f5688f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638745"
---
# <a name="configuring-addremove-programs-with-windows-installer"></a>Configurando Adicionar/Remover Programas com Windows Instalador

Você pode fornecer todas as informações necessárias para configurar Adicionar/Remover Programas no Painel de Controle definindo os valores de determinadas propriedades do instalador no pacote do instalador Windows aplicativo. Definir essas propriedades grava automaticamente os valores correspondentes no Registro. Se o instalador detectar que o produto está marcado para remoção completa, as operações serão adicionadas automaticamente ao script para remover a pasta Adicionar/Remover Programas Painel de Controle informações do produto.

Se um aplicativo não estiver registrado, ele não será listado em Adicionar/Remover Programas no Painel de Controle. Para obter mais informações, [consulte Adicionando e removendo um aplicativo e Deixando nenhum rastreamento no Registro](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).

Os aplicativos que foram instalados [](installation-context.md) no contexto de instalação por usuário são exibidos em Adicionar/Remover Programas do usuário atual. Os aplicativos que foram instalados no contexto de instalação por computador são exibidos em Adicionar/Remover Programas de todos os usuários. Os aplicativos que não foram instalados por computador e foram instalados apenas como aplicativos por usuário para usuários diferentes do usuário atual não aparecem em Adicionar/Remover Programas do usuário atual.

Observe que os pacotes de instalação que usam [**a propriedade LIMITUI**](limitui.md) também devem conter [**o ARPNOMODIFY.**](arpnomodify.md) Isso é necessário para que um usuário obtenha o comportamento correto de Adicionar/Remover Programas no utilitário Painel de Controle ao tentar configurar um produto.

O instalador usa as propriedades [públicas a seguir](public-properties.md) para gerenciar Adicionar/Remover Programas no Painel de Controle.

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
<td>URL do canal de atualização para o aplicativo. O valor que o instalador grava na Chave <a href="uninstall-registry-key.md">do Registro de Desinstalar</a>.</td>
</tr>
<tr class="even">
<td><a href="arpcomments.md"><strong>ARPCOMMENTS</strong></a></td>
<td>Fornece comentários para adicionar/remover programas no Painel de Controle. O valor que o instalador grava na Chave <a href="uninstall-registry-key.md">do Registro de Desinstalar</a>.</td>
</tr>
<tr class="odd">
<td><a href="arpcontact.md"><strong>ARPCONTACT</strong></a></td>
<td>Fornece o contato para adicionar/remover programas no Painel de Controle. O valor que o instalador grava na Chave <a href="uninstall-registry-key.md">do Registro de Desinstalar</a>.</td>
</tr>
<tr class="even">
<td><a href="arpinstalllocation.md"><strong>ARPINSTALLLOCATION</strong></a></td>
<td>Caminho totalmente qualificado para a pasta primária do aplicativo. O valor que o instalador grava na Chave <a href="uninstall-registry-key.md">do Registro de Desinstalar</a>.</td>
</tr>
<tr class="odd">
<td><a href="arphelplink.md"><strong>ARPHELPLINK</strong></a></td>
<td>Endereço da Internet ou URL para suporte técnico. O valor que o instalador grava na Chave <a href="uninstall-registry-key.md">do Registro de Desinstalar</a>.</td>
</tr>
<tr class="even">
<td><a href="arphelptelephone.md"><strong>ARPHELPTELEPHONE</strong></a></td>
<td>Números de telefone de suporte técnico. O valor que o instalador grava na Chave <a href="uninstall-registry-key.md">do Registro de Desinstalar</a>.</td>
</tr>
<tr class="odd">
<td><a href="arpnomodify.md"><strong>ARPNOMODIFY</strong></a></td>
<td>Impede a exibição de um botão Alterar para o produto em Adicionar/Remover Programas no Painel de Controle.
<blockquote>
<b>Observação:</b> Isso afeta apenas a exibição no ARP. O Windows instalador do Windows ainda é capaz de reparar, instalar sob demanda e desinstalar aplicativos por meio de uma linha de comando ou da interface de programação.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a></td>
<td>Impede a exibição de um botão Remover para o produto no botão Adicionar/Remover Programas no Painel de Controle. O produto ainda poderá ser removido selecionando o botão Alterar se o pacote de instalação tiver sido autor com uma interface do usuário que fornece a remoção do produto como uma opção.
<blockquote>
<b>Observação:</b> Isso afeta apenas a exibição no ARP. O Windows instalador do Windows ainda é capaz de reparar, instalar sob demanda e desinstalar aplicativos por meio de uma linha de comando ou da interface de programação.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="arpnorepair.md"><strong>ARPNOREPAIR</strong></a></td>
<td>Desabilita o botão Reparar no botão Adicionar/Remover Programas no Painel de Controle.
<blockquote>
<b>Observação:</b> Isso afeta apenas a exibição no ARP. O Windows instalador do Windows ainda é capaz de reparar, instalar sob demanda e desinstalar aplicativos por meio de uma linha de comando ou da interface de programação.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpproducticon.md"><strong>ARPPRODUCTICON</strong></a></td>
<td>Identifica o ícone exibido em Adicionar/Remover Programas. Se essa propriedade não estiver definida, Adicionar/Remover Programas especificará o ícone de exibição.</td>
</tr>
<tr class="odd">
<td><a href="arpreadme.md"><strong>ARPREADME</strong></a></td>
<td>Fornece o LeiaMe para Adicionar/Remover Programas Painel de Controle. O valor que o instalador grava na Chave <a href="uninstall-registry-key.md">do Registro de Desinstalar</a>.</td>
</tr>
<tr class="even">
<td><a href="arpsize.md"><strong>ARPSIZE</strong></a></td>
<td>Tamanho estimado do aplicativo em KB.</td>
</tr>
<tr class="odd">
<td><a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a></td>
<td>Impede a exibição do aplicativo na Lista de Programas da lista Adicionar/Remover Programas no Painel de Controle.
<blockquote>
<b>Observação:</b> Isso afeta apenas a exibição no ARP. O Windows instalador do Windows ainda é capaz de reparar, instalar sob demanda e desinstalar aplicativos por meio de uma linha de comando ou da interface de programação.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpurlinfoabout.md"><strong>ARPURLINFOABOUT</strong></a></td>
<td>URL para a configuração home page. O valor que o instalador grava na Chave <a href="uninstall-registry-key.md">do Registro de Desinstalar</a>.</td>
</tr>
<tr class="odd">
<td><a href="arpurlupdateinfo.md"><strong>ARPURLUPDATEINFO</strong></a></td>
<td>URL para informações de atualização do aplicativo. O valor que o instalador grava na Chave <a href="uninstall-registry-key.md">do Registro de Desinstalar</a>.</td>
</tr>
</tbody>
</table>

> [!Note]  
> Para obter informações sobre a ferramenta Definir Programa e Padrões, consulte a seção Trabalhando com Definir Acesso ao [Programa e Padrões do Computador](/previous-versions//bb776877(v=vs.85)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desinstalar a chave do Registro](uninstall-registry-key.md)
</dt> </dl>
