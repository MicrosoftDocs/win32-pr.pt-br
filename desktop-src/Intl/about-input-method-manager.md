---
description: O uso da funcionalidade do IMM em seu aplicativo com reconhecimento de IME alivia os usuários da necessidade de se lembrar de todos os valores de caractere possíveis.
ms.assetid: 43b3e561-b844-4688-ab3d-d99f92ed140e
title: Sobre o Gerenciador de métodos de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7b96c64eba5ddfb6966c96d88792fd657f94aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105800050"
---
# <a name="about-input-method-manager"></a>Sobre o Gerenciador de métodos de entrada

O uso da funcionalidade do IMM em seu aplicativo com reconhecimento de IME alivia os usuários da necessidade de se lembrar de todos os valores de caractere possíveis. Em vez disso, ele permite que o IME monitore os pressionamentos de tecla de um usuário, prevê os caracteres que o usuário pode desejar e apresenta uma lista de caracteres candidatos a partir dos quais escolher.

> [!Note]  
> O IMM executa operações semelhantes às da estrutura de [serviços de texto](../tsf/text-services-framework.md), usada por aplicativos que se comunicam com serviços de texto.

 

Por padrão, o IMM fornece uma janela IME por meio da qual o usuário insere pressionamentos de teclas e exibições e seleciona candidatos. Os aplicativos podem usar as funções e mensagens do IMM para criar e gerenciar suas próprias janelas do IME, fornecendo uma interface personalizada ao usar os recursos de conversão do IME.

O IMM é habilitado somente no Leste Asiático (chinês, japonês, coreano) sistemas operacionais Windows localizados. Nesses sistemas, o aplicativo chama [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) com SM \_ DBCSENABLED para determinar se o IMM está habilitado.

**Windows 2000:** O suporte completo a IMM é fornecido em todas as versões de idiomas localizadas. No entanto, o IMM é habilitado somente quando um pacote de idiomas asiático é instalado. Um aplicativo com reconhecimento de IME pode chamar [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) com SM \_ IMMENABLED para determinar se o IMM está habilitado.

Este tópico inclui as seções a seguir.

-   [Listas de candidatos](candidate-lists.md)
-   [Cadeia de caracteres de composição](composition-string.md)
-   [HexToUnicode IME](hextounicode-ime.md)
-   [Teclas de Atalho](hot-keys.md)
-   [Mensagens do IME](ime-messages.md)
-   [Classe da janela do IME](ime-window-class.md)
-   [Contexto de entrada](input-context.md)
-   [Janelas de status, composição e candidatos](status--composition--and-candidates-windows.md)

 

 
