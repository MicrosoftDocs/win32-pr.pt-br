---
description: O processo de criação de uma caixa de diálogo no Windows Installer é semelhante ao processo de criação de uma caixa de diálogo de forma programática usando um modelo de caixa de diálogo da API do Microsoft Windows.
ms.assetid: c46f6b7b-e78c-4dd8-a4ff-7da5465391f9
title: Visão geral da caixa de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884c85f06bc06588084311aee370700d5b2a5290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296916"
---
# <a name="dialog-box-overview"></a>Visão geral da caixa de diálogo

O processo de criação de uma caixa de diálogo no Windows Installer é semelhante ao processo de criação de uma caixa de diálogo de forma programática usando um modelo de caixa de diálogo da API do Microsoft Windows. Embora um modelo de caixa de diálogo do Windows seja armazenado em uma cadeia de caracteres terminada como nula, Windows Installer armazena os parâmetros da caixa de diálogo na tabela de diálogo. A tabela de diálogo contém uma coluna atributos que é análoga aos estilos de janela na API da interface do usuário do Microsoft Windows. No entanto, o número de bits de estilo de caixa de diálogo no Windows Installer é um conjunto especializado e reduzido.

Para criar fisicamente a caixa de diálogo usando a API da interface do usuário do Windows, [**caixa**](/windows/win32/api/winuser/nf-winuser-dialogboxa) é chamado e passa um ponteiro para o modelo. No Windows Installer, a caixa de diálogo é criada durante a execução de uma das três tabelas de sequência da interface do usuário.

Windows Installer não contém uma interface do usuário padrão que os autores de pacotes podem utilizar para seus pacotes. Ele contém um conjunto limitado de caixas de diálogo padrão que exibem mensagens de erro e informações, mas elas são exibidas somente se Windows Installer consulta a caixa de diálogo e as tabelas de sequência da interface do usuário e descobre que não há caixas de diálogo personalizadas disponíveis.

O SDK do instalador inclui um banco de dados mínimo chamado Uisample.msi que contém as tabelas preenchidas da interface do usuário e da sequência de execução e uma interface do usuário completa. Esse banco de dados é facilmente personalizado e mesclado em qualquer pacote.

Algumas ações padrão e as condições de erro internas de Windows Installer retornam um conjunto específico de dados da interface do usuário e, portanto, exigem uma caixa de diálogo com um conjunto específico de controles para acomodar esses dados. Windows Installer verifica dois locais separados para os identificadores dessas caixas de diálogo.

-   Windows Installer contém um conjunto de nomes de caixas de diálogo inseridas. A ação personalizada consulta a tabela de diálogo para obter esses nomes reservados.
-   Em cada uma das três tabelas de sequência de interface do usuário, os nomes de caixa de diálogo com um número de sequência de-1,-2 ou-3 são exibidos em resposta a sair, saída solicitada pelo usuário e mensagens de erro fatal de Windows Installer.

Uma lista completa de nomes da caixa de diálogo de chave primária reservada está disponível nas [caixas de diálogo](dialog-boxes.md). Observe que o nome da caixa de diálogo de chave primária é reservado apenas pelo instalador e não há nenhuma implementação específica da caixa de diálogo dentro de Windows Installer. Os autores de pacote ainda devem preencher todos os campos no banco de dados que especificam os atributos e os controles dessas caixas de diálogo reservadas.

 

 
