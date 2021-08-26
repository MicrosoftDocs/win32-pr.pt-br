---
description: Alguns dos itens do sistema encontrados no Painel de Controle são extensíveis. Para instalar uma Painel de Controle, registre sua extensão do Shell da seguinte forma, em que name é o nome predefinido do item do sistema (consulte a tabela abaixo).
title: Estendendo itens Painel de Controle sistema
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b8b18b71-c95f-4c71-8df4-fe9342ce0165
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8c5948ad99111dc87578dfa15c5278cf03d5918e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469743"
---
# <a name="extending-system-control-panel-items"></a>Estendendo itens Painel de Controle sistema

Alguns dos itens do sistema encontrados no Painel de Controle são extensíveis. Para instalar uma Painel de Controle, registre sua extensão do Shell da seguinte forma, em que *name* é o nome predefinido do item do sistema (consulte a tabela abaixo).

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

Isso é semelhante à maneira como você registraria uma extensão para um objeto Shell predefinido. Como as únicas extensões do Shell com suporte Painel de Controle itens são folhas de propriedades, o registro deve estar na sub-chave \\ **PropertySheetHandlers** do shellex.




| Painel de Controle item | <em>name</em> | Comentários | 
|--------------------|---------------|---------|
| Exibir | Mesa | Também dá suporte à substituição da <strong>página Área de</strong> Trabalho.<blockquote>[!Note]<br />Não há mais suporte para isso no Windows Vista.</blockquote><br /> | 
| Exibir Configurações Avançado | Dispositivo | Propriedades avançadas não específicas doware.<blockquote>[!Note]<br />Não há mais suporte para isso no Windows Vista.</blockquote><br /> | 
| Exibir Configurações Avançado | Exibir | Propriedades avançadas específicas do hardware.<blockquote>[!Note]<br />Não há mais suporte para isso no Windows Vista.</blockquote><br /> | 
| Opções da Internet | Internet | O número máximo de páginas de extensão é 18. | 
| Teclado | Teclado | O número máximo de páginas de extensão é 30. | 
| Mouse | Mouse | Também dá suporte à substituição de páginas padrão. O número máximo de páginas de extensão é 8. | 
| Opções de Energia | Energia | O número máximo de páginas, incluindo páginas padrão, é 18. | 
| Sistema | Sistema | O número máximo de páginas de extensão é 8.<blockquote>[!Note]<br />Não há mais suporte para isso no Windows Vista.</blockquote><br /> | 




 

O **item Adicionar ou Remover Programas** no Windows XP Painel de Controle não é uma folha de propriedades e, portanto, não pode ser estendido pelos métodos discutidos aqui. Em vez disso, seu conteúdo é obtido de editores de aplicativos. Para obter mais informações sobre como adicionar conteúdo a Adicionar ou remover programas **,** consulte [**IAppPublisher**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher), [**IEnumPublishedApps**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps)e [**IPublishedApp**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Painel de Controle itens](control-panel-applications.md)
</dt> <dt>

[Diretrizes da Experiência do Usuário](user-experience-guidelines.md)
</dt> <dt>

[Registrando Painel de Controle itens](registering-control-panel-items.md)
</dt> <dt>

[Usando CPLApplet](using-cplapplet.md)
</dt> <dt>

[Painel de Controle processamento de mensagens](message-processing.md)
</dt> <dt>

[Executando Painel de Controle itens](executing-control-panel-items.md)
</dt> <dt>

[Atribuindo categorias Painel de Controle dados](assigning-control-panel-categories.md)
</dt> <dt>

[Criando links de tarefa pesquisáveis para um Painel de Controle item](creating-searchable-task-links.md)
</dt> <dt>

[Acessando o Painel de Controle no modo Cofre em Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




