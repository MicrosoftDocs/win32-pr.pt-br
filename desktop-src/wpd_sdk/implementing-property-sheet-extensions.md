---
description: Implementando extensões de folha de propriedades
ms.assetid: 5d1f9d91-e8a1-4cbb-b1de-4262a61e3cb7
title: Implementando extensões de folha de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23b4f74559176ecc0c411f75e7ca630db152a51109f09ecdca47a62d0113e70c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590276"
---
# <a name="implementing-property-sheet-extensions"></a>Implementando extensões de folha de propriedades

A Extensão de Namespace WPD dá suporte a folhas de propriedades extensíveis. Essas são as caixas de diálogo de propriedade que aparecem quando um usuário clica com o botão direito do mouse em um objeto, como um arquivo ou uma pasta, e seleciona **Propriedades**. Alguns aplicativos WPD aproveitarão essas folhas de propriedades extensíveis para exibir propriedades para conteúdo do lado do dispositivo (ou objetos que residem no dispositivo).

As folhas de propriedades extensíveis têm suporte nas interfaces descritas na tabela a seguir. Para obter mais informações sobre qualquer uma dessas interfaces, consulte o Windows SDK.



| Interface           | Descrição                                                                  |
|---------------------|------------------------------------------------------------------------------|
| Idataobject         | Usado para passar a matriz PIDL do menu de contexto para o manipulador de menu de contexto.      |
| IPropertySetStorage | Essa interface é usada para recuperar propriedades WPD para o objeto determinado.      |
| IPropertyStorage    | Essa interface também é usada para recuperar propriedades WPD para o objeto determinado. |
| IShellExtInit       | Inicializa o Windows extensões do Vista Shell para o menu de contexto.         |
| IShellPropSheetExt  | Dá suporte à adição de extensões de folha de propriedades.                              |



 

As folhas de propriedades para WPD são implementadas como qualquer outra folha de propriedades no Windows Vista. Se você já tiver implementado um manipulador de folha de propriedades, poderá modificar seu código existente para que ele seja compatível com o conteúdo do lado do dispositivo. Se você nunca criou um manipulador de menu de contexto, consulte o tópico Creating Property Sheet Handlers no SDK Windows.

Os dois pontos em que um manipulador de folha de propriedades WPD difere de qualquer outro manipulador está no registro do manipulador e o suporte do conteúdo do lado do dispositivo.

 

 



