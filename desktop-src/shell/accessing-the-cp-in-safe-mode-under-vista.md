---
description: Por padrão, os itens do painel de controle do Windows Vista não são mostrados quando o Windows é executado no modo de segurança.
title: Acessando o painel de controle no modo de segurança
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f37bcb0f-9417-4cc4-a57d-4f67a9ccda19
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 0f7a401bbc22a7f8de3618f844bfe463fa3baa50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967366"
---
# <a name="accessing-the-control-panel-in-safe-mode"></a>Acessando o painel de controle no modo de segurança

Por padrão, os itens do painel de controle do Windows Vista não são mostrados quando o Windows é executado no modo de segurança. Para permitir que um novo item do painel de controle seja exibido no modo de segurança, os valores de registro apropriados para o tipo de item podem ser definidos. Os valores são interpretados da seguinte maneira:



| Valor | Significado                                                            |
|-------|--------------------------------------------------------------------|
| 1     | O item deve aparecer apenas no modo de segurança mínimo.                  |
| 2     | O item só deverá aparecer no modo de segurança se a rede estiver habilitada. |
| 3     | O item sempre deve aparecer em qualquer forma de modo de segurança.            |



 

Este exemplo mostra as entradas necessárias para um item implementado como um arquivo. cpl ou. dll. Ele especifica que o item deve aparecer no modo de segurança com rede.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.EnableInSafeMode
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 2
```

Este exemplo mostra as entradas necessárias para um item implementado como um arquivo. exe. Ele especifica que o item deve aparecer em qualquer forma de modo de segurança.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         System.ControlPanel.EnableInSafeMode = [REG_DWORD] 3
```

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

[Estendendo itens do painel de controle do sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Atribuindo categorias do painel de controle](assigning-control-panel-categories.md)
</dt> <dt>

[Criando links de tarefas pesquisáveis para um item do painel de controle](creating-searchable-task-links.md)
</dt> </dl>

 

 



