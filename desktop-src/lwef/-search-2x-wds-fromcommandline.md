---
title: Chamando o WDS por meio da linha de comando
description: Você pode iniciar a interface do usuário do Microsoft Windows Desktop Search (WDS) com um filtro, uma loja e uma consulta específicos de outro aplicativo ou uma página da Web que usa o BHO (objeto auxiliar do navegador) usando a sintaxe de linha de comando windowssearch.exe.
ms.assetid: fd62f7c9-08a9-4e05-b0bc-e2215cfff59e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efae7aebc13f578e9c5c32542b451d3600a93a2b
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/19/2020
ms.locfileid: "103640278"
---
# <a name="calling-wds-from-the-command-line"></a>Chamando o WDS por meio da linha de comando

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use o [Windows Search](../search/-search-3x-wds-overview.md) em vez disso.

Você pode iniciar a interface do usuário do Microsoft Windows Desktop Search (WDS) com um filtro, uma loja e uma consulta específicos de outro aplicativo ou uma página da Web que usa o BHO (objeto auxiliar do navegador) usando a sintaxe de linha de comando windowssearch.exe. Ao chamar o WDS na linha de comando, nenhuma informação sobre as ações ou a seleção do usuário na janela do WDS é retornada para o aplicativo de chamada ou para a página da Web.

O caminho de instalação do WDS é especificado na configuração do registro InstallDir em HKEY_LOCAL_MACHINE \\ software \\ Microsoft \\ Windows Desktop Search. O caminho padrão em que o windowssearch.exe é instalado é arquivos de programas \\ Windows Desktop Search.

## <a name="command-line-syntax"></a>Sintaxe da linha de comando

A sintaxe a seguir se aplica à interface de linha de comando do Windows Desktop Search 2. x.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Opções</th>
<th>Parâmetro</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>/startup</td>

<td>Inicializa o Windows Desktop Search</td>
</tr>
<tr class="even">
<td>/indexnow</td>

<td>Desativa o desligamento da indexação e examina novamente todos os locais de índice</td>
</tr>
<tr class="odd">
<td>/showstatus</td>

<td>Mostra a janela de status de indexação</td>
</tr>
<tr class="even">
<td>/launchsearchwindow ou/URL</td>

<td>Abre uma janela do WDS com uma consulta vazia</td>
</tr>
<tr class="odd">
<td>/url</td>
<td>pesquisa: [Store | mostrar | consulta] cadeia de caracteres de consulta</td>
<td>Abre uma janela do WDS com uma consulta e um filtro com base nos seguintes parâmetros:
<ul>
<li><p>Store-especifica a fonte de dados para consultar: arquivos, Outlook, OutlookExpress. Se não for especificado, todos os repositórios serão pesquisados. <br/></p>
<blockquote>
[!Note]<br />
Embora a sintaxe de consulta avançada ofereça suporte à referência do Microsoft Outlook como ' OE ', o parâmetro Store na linha de comando deve ser ' OutlookExpress '.
</blockquote>
<p><br/></p></li>
<li><p>Mostrar-especifica qual tipo percebido de resultados deve ser retornado. Consulte <a href="-search-2x-wds-perceivedtype.md">tipos observados</a> para obter uma lista completa de tipos. Se não for especificado, todos os tipos serão retornados. <br/></p>
<blockquote>
[!Note]<br />
Há três diferenças entre os valores de tipo percebido e os valores para show. Para <code>show</code> , use ' documentos ' em vez de ' Doc ', ' imagens ' em vez de ' pics ' e ' textdocuments ' em vez de ' texto '.
</blockquote>
<p><br/></p></li>
<li>consulta-especifica os critérios de pesquisa. Esse valor dá suporte a parâmetros de <a href="-search-2x-wds-aqsreference.md">sintaxe de consulta avançada</a> para refinar os resultados. O parâmetro de consulta deve ser o último parâmetro na URL.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="example"></a>Exemplo

Por exemplo, para pesquisar todos os arquivos de imagens que correspondem aos critérios de ' wallpaper ', use o seguinte comando:

`WindowsSearch.exe /url search:store=files&show=pictures&query=wallpaper`

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Sintaxe de consulta avançada](-search-2x-wds-aqsreference.md)
</dt> <dt>

[Tipos observados](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[Chamando o WDS de páginas da Web](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

 





