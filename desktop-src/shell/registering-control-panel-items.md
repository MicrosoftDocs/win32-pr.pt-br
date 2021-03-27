---
description: Os itens do painel de controle devem ser registrados para que apareçam na janela do painel de controle.
title: Registrando itens do painel de controle
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6f21f223-a293-47b5-95e9-06b7a4ff1652
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05c2a652314babc212e17b48198e9441f4d3465d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091718"
---
# <a name="registering-control-panel-items"></a>Registrando itens do painel de controle

Os itens do painel de controle devem ser registrados para que apareçam na janela do painel de controle. Se o item do painel de controle for implementado como parte de um arquivo. exe, ele será registrado como um objeto de comando. O registro difere se o item for implementado como um arquivo. dll que exporta a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) .

Requisitos específicos são discutidos nestes tópicos:

-   [Como registrar itens do painel de controle executável](how-to-register-an-executable-control-panel-item-registration-.md)
-   [Como registrar itens do painel de controle da DLL](how-to-register-dll-control-panel-item-registration-.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Itens do painel de controle](control-panel-applications.md)
</dt> <dt>

[Diretrizes da Experiência do Usuário](user-experience-guidelines.md)
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
</dt> <dt>

[Acessando o painel de controle no modo de segurança no Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
