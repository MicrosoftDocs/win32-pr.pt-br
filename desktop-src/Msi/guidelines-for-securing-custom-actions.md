---
description: para ajudar a manter uma instalação de software segura, siga estas diretrizes ao criar uma Windows Installer ação personalizada.
ms.assetid: f7081b0c-bfa2-47a1-840b-28881ad97071
title: Diretrizes para proteger ações personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b5ea12bd8d38025587cb09fd7a17d3e87739acedf31d85f72ff4b1b76b0432
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649286"
---
# <a name="guidelines-for-securing-custom-actions"></a>Diretrizes para proteger ações personalizadas

a adesão às seguintes diretrizes ao criar um pacote de Windows Installer com ações personalizadas ajuda a manter um ambiente seguro durante a instalação:

-   Proteja todos os arquivos adicionais gravados por sua ação personalizada.
-   Verifique os comprimentos do buffer e a validade de todos os dados lidos por sua ação personalizada. Isso inclui propriedades que podem fornecer dados para sua ação personalizada, particularmente aquelas que usam propriedades públicas fornecidas por um usuário.
-   Não confie em DLLs externas que não são confiáveis pelo sistema em todas as plataformas nas quais o pacote de instalação deve ser executado.
-   Considere atentamente se as ações personalizadas que usam privilégios [*elevados*](e-gly.md) ou representação devem ser usadas. As ações personalizadas, como "abrir uma URL após a instalação, são concluídas", "iniciar o software após a instalação concluída" ou "iniciar o Leiame após a instalação concluída", normalmente, não exigiria privilégios elevados para funcionar. Se a ação personalizada deve ser executada com privilégios *elevados* , certifique-se de que o código de ação personalizado protege contra estouros de buffer e carregamento inadvertido de código não seguro. Observe que durante a fase de execução da instalação, o instalador passa informações para um processo com privilégios *elevados* e executa o script. Todas as ações personalizadas executadas durante a fase de execução podem ser executadas com privilégios *elevados* .
-   Reúna todas as informações fornecidas pelo usuário durante a sequência de interface Não solicite ao usuário nenhuma informação que não possa ser definida usando uma propriedade pública.
-   Se a ação personalizada do script expandir as propriedades, tome precauções de que a ação personalizada é protegida contra a possibilidade de injeção de script. O script pode ser registrado em texto não criptografado.

Consulte também [segurança de ação personalizada](custom-action-security.md).

 

 



