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
ms.openlocfilehash: daa86bfd9975df5cd057dd3e577f443bafa6c363061e267e67adad69b590e678
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661076"
---
# <a name="registering-control-panel-items"></a>Registrando itens do painel de controle

Os itens do painel de controle devem ser registrados para que apareçam na janela do painel de controle. Se o item do painel de controle for implementado como parte de um arquivo de .exe, ele será registrado como um objeto de comando. O registro difere se o item for implementado como um arquivo de .dll que exporta a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) .

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

[acessando o painel de controle no modo de Cofre em Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
