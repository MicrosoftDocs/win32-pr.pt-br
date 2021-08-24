---
description: Por padrão, desde Windows vista Painel de Controle itens não são mostrados quando Windows é executado no modo de segurança.
title: Acessando o Painel de Controle no modo Cofre
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f37bcb0f-9417-4cc4-a57d-4f67a9ccda19
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 777a44c7fe30b0481096a1c5d62c98410277a3bc76169925aff4ae5e59e549d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710786"
---
# <a name="accessing-the-control-panel-in-safe-mode"></a>Acessando o Painel de Controle no modo Cofre

Por padrão, desde Windows vista Painel de Controle itens não são mostrados quando Windows é executado no modo de segurança. Para permitir que um novo Painel de Controle seja exibido no modo de segurança, os valores do Registro apropriados para o tipo de item podem ser definidos. Os valores são interpretados da seguinte maneira:



| Valor | Significado                                                            |
|-------|--------------------------------------------------------------------|
| 1     | O item deve aparecer apenas no modo de segurança mínimo.                  |
| 2     | O item deverá aparecer no modo de segurança somente se a rede estiver habilitada. |
| 3     | O item sempre deve aparecer em qualquer forma de modo de segurança.            |



 

Este exemplo mostra as entradas necessárias para um item implementado como um .cpl ou .dll arquivo. Especifica que o item deve aparecer no modo de segurança com rede.

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

Este exemplo mostra as entradas necessárias para um item implementado como um .exe arquivo. Especifica que o item deve aparecer em qualquer forma de modo de segurança.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         System.ControlPanel.EnableInSafeMode = [REG_DWORD] 3
```

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

[Estendendo itens Painel de Controle sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Atribuindo Painel de Controle categorias](assigning-control-panel-categories.md)
</dt> <dt>

[Criando links de tarefa pesquisáveis para um Painel de Controle item](creating-searchable-task-links.md)
</dt> </dl>

 

 



