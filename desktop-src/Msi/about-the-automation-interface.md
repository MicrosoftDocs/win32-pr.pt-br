---
description: Um objeto instalador deve ser criado inicialmente para carregar o suporte de automação necessário para acessar os componentes do instalador por meio de COM.
ms.assetid: 113ed443-a866-43d4-86bd-fc3b244f2edb
title: Sobre a interface de automação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c51469240ad684d6fd32ffbc5466007e73f4e4ff7a870b6878b18f25f54d32c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382063"
---
# <a name="about-the-automation-interface"></a>Sobre a interface de automação

Um [**objeto instalador**](installer-object.md) deve ser criado inicialmente para carregar o suporte de automação necessário para acessar os componentes do instalador por meio de com. Esse objeto fornece wrappers para criar os objetos de nível superior e acessar seus métodos. esses wrappers simplesmente fornecem conversões de parâmetro para expor as funções do instalador de uma maneira consistente com o Microsoft Visual Basic sem alterar o comportamento dos métodos.

sempre que possível, um par de métodos Get e Set do C++ é exposto a Visual Basic como uma única propriedade. Em alguns casos, os métodos do C++ que levam um argumento de índice são expostos como uma propriedade indexada. Muitos métodos C++ retornam o resultado por meio de um parâmetro porque o valor de retorno é usado para o retorno de erro. no entanto, no Visual Basic, os erros são tratados por um mecanismo separado e o resultado é sempre passado no valor de retorno.

Para obter informações sobre como usar a automação e criar o objeto do instalador, consulte [usando a interface de automação](using-the-automation-interface.md).

para obter material de referência para os objetos Windows Installer, consulte [referência da Interface de automação](automation-interface-reference.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Exemplos de script do instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 



