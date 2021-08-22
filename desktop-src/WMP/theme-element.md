---
title: Elemento THEME
description: Elemento THEME
ms.assetid: fe7e793e-1774-412c-aed2-721ed2cf1bb3
keywords:
- Windows Media Player capas, elemento THEME
- skins, elemento THEME
- Elemento THEME
- referência para capas, elemento THEME
- elementos, THEME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c15091ffa93e3ae64a06979580931c27bdf4c1cd2e26c7acc206d76de8b0fc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507386"
---
# <a name="theme-element"></a>Elemento THEME

O **elemento THEME** é o elemento de nível pai de uma capa e contém um ou mais elementos **VIEW,** que, por sua vez, contêm todos os outros elementos dentro de uma capa. Dentro do código de script, o elemento **THEME** é acessado por meio do atributo **global** do tema, em vez de por meio de um nome especificado por um atributo de **ID,** que não é suportado pelo **elemento THEME.**

O **elemento THEME** dá suporte aos atributos a seguir.



| Atributo                                | Descrição                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [Autor](theme-author.md)               | Especifica ou recupera o nome do autor da capa.                                                                      |
| [authorVersion](theme-authorversion.md) | Especifica ou recupera o número de versão da capa atribuída pelo autor.                                                |
| [Copyright](theme-copyright.md)         | Especifica ou recupera a cadeia de caracteres de direitos autorais para a capa.                                                                       |
| [currentViewID](theme-currentviewid.md) | Especifica ou recupera a EXIBIÇÃO exibida **no momento.**                                                                        |
| [title](theme-title.md)                 | Especifica ou recupera o título da capa.                                                                                   |
| [version](theme-version.md)             | Especifica ou recupera o número Windows Media Player versão para o qual a capa foi autorizada. Só pode ser definido em tempo de design. |



 

O **elemento THEME** dá suporte aos métodos a seguir.



| Método                                         | Descrição                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [closeView](theme-closeview.md)               | Fecha um **VIEW aberto.**                                                                                        |
| [loadPreference](theme-loadpreference.md)     | Carrega uma preferência do Registro.                                                                           |
| [logString](theme-logstring.md)               | Registra uma cadeia de caracteres definida pelo usuário no arquivo de erro, se o registro em log estiver habilitado.                                            |
| [openDialog](theme-opendialog.md)             | Abre uma caixa de diálogo de arquivo.                                                                                        |
| [Openview](theme-openview.md)                 | Abre uma **VIEW** em uma nova janela.                                                                               |
| [openViewRelative](theme-openviewrelative.md) | Abre uma **VIEW** em uma nova janela em uma posição inicial especificada em relação ao canto superior esquerdo da capa. |
| [Playsound](theme-playsound.md)               | Reproduz o arquivo de som especificado.                                                                                 |
| [savePreference](theme-savepreference.md)     | Salva uma preferência no Registro.                                                                             |
| [showErrorDialog](theme-showerrordialog.md)   | Exibe a caixa de diálogo de erro padrão.                                                                         |



 

O **elemento THEME** não dá suporte a manipuladores de eventos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação de capa**](skin-programming-reference.md)
</dt> </dl>

 

 




