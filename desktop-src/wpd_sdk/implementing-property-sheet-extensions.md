---
description: Implementando extensões de folha de propriedades
ms.assetid: 5d1f9d91-e8a1-4cbb-b1de-4262a61e3cb7
title: Implementando extensões de folha de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a351678c2377aacdd73ec750841a32a81ad973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768350"
---
# <a name="implementing-property-sheet-extensions"></a>Implementando extensões de folha de propriedades

A extensão do namespace WPD dá suporte a folhas de propriedades extensíveis. Essas são as caixas de diálogo de propriedade que aparecem quando um usuário clica com o botão direito do mouse em um objeto, como um arquivo ou uma pasta, e seleciona **Propriedades**. Alguns aplicativos WPD aproveitam essas folhas de propriedades extensível para exibir propriedades de conteúdo do lado do dispositivo (ou objetos que residem no dispositivo).

As interfaces de propriedades extensíveis são suportadas pela interface descrita na tabela a seguir. Para obter mais informações sobre qualquer uma dessas interfaces, consulte a SDK do Windows.



| Interface           | Descrição                                                                  |
|---------------------|------------------------------------------------------------------------------|
| IDataObject         | Usado para passar a matriz PIDL do menu de contexto para o manipulador de menu de contexto.      |
| IPropertySetStorage | Essa interface é usada para recuperar as propriedades de WPD para o objeto fornecido.      |
| IPropertyStorage    | Essa interface também é usada para recuperar as propriedades de WPD para o objeto fornecido. |
| IShellExtInit       | Inicializa as extensões do shell do Windows Vista para o menu de contexto.         |
| IShellPropSheetExt  | Dá suporte à adição de extensões de folha de propriedades.                              |



 

Folhas de propriedades para WPD são implementadas como qualquer outra folha de propriedades no Windows Vista. Se você já tiver implementado um manipulador de folha de propriedades, poderá modificar o código existente para que ele dê suporte ao conteúdo do lado do dispositivo. Se você nunca criou um manipulador de menu de contexto, consulte o tópico Criando manipuladores de folha de propriedades na SDK do Windows.

Os dois pontos em que um manipulador de folha de propriedades WPD difere de qualquer outro manipulador está no registro do manipulador e no suporte ao conteúdo do lado do dispositivo.

 

 



