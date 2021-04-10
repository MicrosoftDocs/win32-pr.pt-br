---
description: Um objeto instalador deve ser criado inicialmente para carregar o suporte de automação necessário para acessar os componentes do instalador por meio de COM.
ms.assetid: 113ed443-a866-43d4-86bd-fc3b244f2edb
title: Sobre a interface de automação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655a01a4daccb805bec4a858337c1dce48f0fb82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169220"
---
# <a name="about-the-automation-interface"></a>Sobre a interface de automação

Um [**objeto instalador**](installer-object.md) deve ser criado inicialmente para carregar o suporte de automação necessário para acessar os componentes do instalador por meio de com. Esse objeto fornece wrappers para criar os objetos de nível superior e acessar seus métodos. Esses wrappers simplesmente fornecem conversões de parâmetro para expor as funções do instalador de uma maneira consistente com o Microsoft Visual Basic sem alterar o comportamento dos métodos.

Sempre que possível, um par de métodos get e set do C++ é exposto a Visual Basic como uma única propriedade. Em alguns casos, os métodos do C++ que levam um argumento de índice são expostos como uma propriedade indexada. Muitos métodos C++ retornam o resultado por meio de um parâmetro porque o valor de retorno é usado para o retorno de erro. No entanto, no Visual Basic, os erros são tratados por um mecanismo separado e o resultado é sempre passado no valor de retorno.

Para obter informações sobre como usar a automação e criar o objeto do instalador, consulte [usando a interface de automação](using-the-automation-interface.md).

Para obter material de referência para os objetos Windows Installer, consulte [referência da interface de automação](automation-interface-reference.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de script de Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 



