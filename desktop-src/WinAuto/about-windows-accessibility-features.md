---
title: Recursos de acessibilidade do Windows
description: Windows A acessibilidade dá suporte a duas categorias de recursos para desenvolvedores Windows – APIs do Win32 e Usuários Configurações.
ms.assetid: 823bbc5b-062b-43ef-9f3e-822dc6f55c5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fac63f4bf021888ee96cb180e423f55b07190959ad8c8b7966f1a4a7ae395119
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994416"
---
# <a name="windows-accessibility-features"></a>Recursos de acessibilidade do Windows

Windows A acessibilidade dá suporte a duas categorias de recursos para ajudar os desenvolvedores Windows a criar aplicativos acessíveis, desenvolvedores de tecnologia adaptativa criam ferramentas como leitores de tela e lupas e engenheiros de teste de software criam scripts automatizados para testar Windows aplicativos.

## <a name="settings"></a>Configurações

Há dois tipos de configurações disponíveis para os usuários (por meio do Central de Facilidade de Acesso no Painel de Controle) que também são expostos aos desenvolvedores:

- [Parâmetros de acessibilidade](accessibility-parameters.md). Quando definidos, esses parâmetros indicam que os aplicativos devem alterar seu comportamento padrão. Os aplicativos podem verificar o estado de um parâmetro de acessibilidade para determinar se o usuário deseja um comportamento especial que possa ser fornecido de maneira específica do aplicativo. Por exemplo, o parâmetro ShowSounds indica que um aplicativo que normalmente usa som para transmitir informações importantes também deve fornecer as informações visualmente.
- [Recursos de acessibilidade integrados](built-in-accessibility-features.md). Esses recursos são integrados ao sistema ou fornecidos como uma extensão para o sistema. Eles afetam como o usuário fornece entrada de teclado e mouse para o computador. Quando habilitada, sua funcionalidade está disponível, independentemente de quais aplicativos estão em execução. Um exemplo é um filtro de teclado que facilita para usuários com deficiências de movimento digitar combinações de teclas, como CTRL+ALT+DEL.

Cada parâmetro de acessibilidade e cada recurso de acessibilidade integrado corresponde a um parâmetro do sistema que pode ser definido ou consultado com a [função SystemParametersInfo.](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)

## <a name="win32-apis"></a>APIs Win32

As APIs win32 fornecem recursos de acessibilidade e automação para ajudar os desenvolvedores a criar aplicativos e estruturas de interface do usuário, fornecedores de tecnologia adaptativa a criar ferramentas, testadores garantem implementações de qualidade e pessoas com deficiências usam seus computadores e dispositivos.

## <a name="related-topics"></a>Tópicos relacionados

[Considerações sobre segurança para tecnologias adaptativas](uiauto-securityoverview.md)