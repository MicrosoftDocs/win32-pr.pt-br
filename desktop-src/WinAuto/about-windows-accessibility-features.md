---
title: Recursos de acessibilidade do Windows
description: A acessibilidade do Windows dá suporte a duas categorias de recursos para desenvolvedores do Windows – APIs do Win32 e configurações de usuário.
ms.assetid: 823bbc5b-062b-43ef-9f3e-822dc6f55c5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aabd92ed8594d711ae9b744dc7f4a2622e8cb3d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007775"
---
# <a name="windows-accessibility-features"></a>Recursos de acessibilidade do Windows

A acessibilidade do Windows dá suporte a duas categorias de recursos para ajudar os desenvolvedores do Windows a projetar aplicativos acessíveis, desenvolvedores de tecnologia assistencial criam ferramentas como leitores de tela e lupas, e engenheiros de teste de software criam scripts automatizados para testar aplicativos do Windows.

## <a name="settings"></a>Settings

Há dois tipos de configurações disponíveis para os usuários (por meio da central de facilidade de acesso no painel de controle) que também são expostas aos desenvolvedores:

- [Parâmetros de acessibilidade](accessibility-parameters.md). Quando definido, esses parâmetros indicam que os aplicativos devem alterar seu comportamento padrão. Os aplicativos podem verificar o estado de um parâmetro de acessibilidade para determinar se o usuário deseja um comportamento especial que possa ser fornecido de maneira específica ao aplicativo. Por exemplo, o parâmetro de mostrar sons indica que um aplicativo que normalmente usa o som para transmitir informações importantes também deve fornecer as informações visualmente.
- [Recursos de acessibilidade internos](built-in-accessibility-features.md). Esses recursos são incorporados ao sistema ou fornecidos como uma extensão para o sistema. Eles afetam a forma como o usuário fornece entrada de teclado e mouse para o computador. Quando habilitada, sua funcionalidade estará disponível, independentemente dos aplicativos em execução. Um exemplo é um filtro de teclado que torna mais fácil para os usuários com deficiências de movimento digitar combinações de teclas como CTRL + ALT + DEL.

Cada parâmetro de acessibilidade e cada recurso de acessibilidade interno correspondem a um parâmetro do sistema que pode ser definido ou consultado com a função [SystemParametersInfo](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) .

## <a name="win32-apis"></a>APIs Win32

As APIs do Win32 fornecem recursos de acessibilidade e automação para ajudar os desenvolvedores a criar aplicativos e estruturas de interface do usuário, fornecedores de tecnologia assistencial criam ferramentas, testadores garantem implementações de qualidade e pessoas com deficiências usam seus computadores e dispositivos.

## <a name="related-topics"></a>Tópicos relacionados

[Considerações de segurança para tecnologias assistenciais](uiauto-securityoverview.md)