---
title: Elemento THEME
description: Elemento THEME
ms.assetid: fe7e793e-1774-412c-aed2-721ed2cf1bb3
keywords:
- Capas do Windows Media Player, elemento THEME
- capas, elemento THEME
- Elemento THEME
- referência para capas, elemento THEME
- elementos, tema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8cd0d40b4b020cf5416569417401af9e4f3a33b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822440"
---
# <a name="theme-element"></a>Elemento THEME

O elemento **Theme** é o elemento de nível pai de uma capa e contém um ou mais elementos **View** que, por sua vez, contêm todos os outros elementos em uma capa. No código do script, o elemento **Theme** é acessado por meio do atributo global **Theme** , em vez de um nome especificado por um atributo **ID** , que não tem suporte do elemento **Theme** .

O elemento **Theme** dá suporte aos seguintes atributos.



| Atributo                                | Descrição                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [autorização](theme-author.md)               | Especifica ou recupera o nome do autor da capa.                                                                      |
| [authorVersion](theme-authorversion.md) | Especifica ou recupera o número de versão da capa, conforme atribuído pelo autor.                                                |
| [internacionais](theme-copyright.md)         | Especifica ou recupera a cadeia de caracteres de direitos autorais para a capa.                                                                       |
| [currentViewID](theme-currentviewid.md) | Especifica ou recupera a **exibição** exibida no momento.                                                                        |
| [title](theme-title.md)                 | Especifica ou recupera o título da capa.                                                                                   |
| [version](theme-version.md)             | Especifica ou recupera o número de versão do Windows Media Player para o qual a capa foi criada. Só pode ser definido em tempo de design. |



 

O elemento **Theme** dá suporte aos métodos a seguir.



| Método                                         | Descrição                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [closeView](theme-closeview.md)               | Fecha um **modo de exibição** aberto.                                                                                        |
| [loadpreference](theme-loadpreference.md)     | Carrega uma preferência do registro.                                                                           |
| [logString](theme-logstring.md)               | Registra uma cadeia de caracteres definida pelo usuário no arquivo de erro, se o registro em log estiver habilitado.                                            |
| [openDialog](theme-opendialog.md)             | Abre uma caixa de diálogo de arquivo.                                                                                        |
| [AbrirModoDeExibição](theme-openview.md)                 | Abre uma **exibição** em uma nova janela.                                                                               |
| [openViewRelative](theme-openviewrelative.md) | Abre uma **exibição** em uma nova janela em uma posição inicial especificada em relação ao canto superior esquerdo da capa. |
| [playSound](theme-playsound.md)               | Reproduz o arquivo de som especificado.                                                                                 |
| [savePreference](theme-savepreference.md)     | Salva uma preferência no registro.                                                                             |
| [showErrorDialog](theme-showerrordialog.md)   | Exibe a caixa de diálogo de erro padrão.                                                                         |



 

O elemento **Theme** não dá suporte a manipuladores de eventos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação de capa**](skin-programming-reference.md)
</dt> </dl>

 

 




