---
description: Alguns dos itens do sistema encontrados no painel de controle são extensíveis. Para instalar uma extensão do painel de controle, registre a extensão do Shell da seguinte maneira, em que nome é o nome predefinido do item do sistema (consulte a tabela abaixo).
title: Estendendo itens do painel de controle do sistema
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b8b18b71-c95f-4c71-8df4-fe9342ce0165
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9b0f6628d7bc75378915c1d9f3e20327478742df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988780"
---
# <a name="extending-system-control-panel-items"></a>Estendendo itens do painel de controle do sistema

Alguns dos itens do sistema encontrados no painel de controle são extensíveis. Para instalar uma extensão do painel de controle, registre a extensão do Shell da seguinte maneira, em que *nome* é o nome predefinido do item do sistema (consulte a tabela abaixo).

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Controls Folder
                  name
                     shellex
                        PropertySheetHandlers
```

Isso é semelhante à maneira como você registraria uma extensão para um objeto de shell predefinido. Como as únicas extensões do Shell suportadas pelos itens do painel de controle são folhas de propriedades, o registro deve estar na subchave **shellex** \\ **PropertySheetHandlers** .



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Item do painel de controle</th>
<th><em>name</em></th>
<th>Comentários</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Monitor</td>
<td>Escritório</td>
<td>Também dá suporte à substituição da página <strong>da área de trabalho</strong> .
<blockquote>
[!Note]<br />
Não há mais suporte para isso no Windows Vista.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Configurações de exibição avançadas</td>
<td>Dispositivo</td>
<td>Propriedades avançadas específicas de não-difíceis.
<blockquote>
[!Note]<br />
Não há mais suporte para isso no Windows Vista.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Configurações de exibição avançadas</td>
<td>Monitor</td>
<td>Propriedades avançadas específicas de hardware.
<blockquote>
[!Note]<br />
Não há mais suporte para isso no Windows Vista.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Opções da Internet</td>
<td>Internet</td>
<td>O número máximo de páginas de extensão é 18.</td>
</tr>
<tr class="odd">
<td>Teclado</td>
<td>Teclado</td>
<td>O número máximo de páginas de extensão é 30.</td>
</tr>
<tr class="even">
<td>Mouse</td>
<td>Mouse</td>
<td>Também dá suporte à substituição de páginas padrão. O número máximo de páginas de extensão é 8.</td>
</tr>
<tr class="odd">
<td>Opções de Energia</td>
<td>Energia</td>
<td>O número máximo de páginas, incluindo páginas padrão, é 18.</td>
</tr>
<tr class="even">
<td>Sistema</td>
<td>Sistema</td>
<td>O número máximo de páginas de extensão é 8.
<blockquote>
[!Note]<br />
Não há mais suporte para isso no Windows Vista.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

O item **Adicionar ou remover programas** no painel de controle do Windows XP não é uma folha de propriedades e, portanto, não pode ser estendido pelos métodos discutidos aqui. Em vez disso, seu conteúdo é obtido de Publicadores de aplicativos. Para obter mais informações sobre como adicionar conteúdo para **Adicionar ou remover programas**, consulte [**IAppPublisher**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher), [**IEnumPublishedApps**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps)e [**IPublishedApp**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Itens do painel de controle](control-panel-applications.md)
</dt> <dt>

[Diretrizes da Experiência do Usuário](user-experience-guidelines.md)
</dt> <dt>

[Registrando itens do painel de controle](registering-control-panel-items.md)
</dt> <dt>

[Usando CPLApplet](using-cplapplet.md)
</dt> <dt>

[Processamento de mensagens do painel de controle](message-processing.md)
</dt> <dt>

[Executando itens do painel de controle](executing-control-panel-items.md)
</dt> <dt>

[Atribuindo categorias do painel de controle](assigning-control-panel-categories.md)
</dt> <dt>

[Criando links de tarefas pesquisáveis para um item do painel de controle](creating-searchable-task-links.md)
</dt> <dt>

[Acessando o painel de controle no modo de segurança no Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




