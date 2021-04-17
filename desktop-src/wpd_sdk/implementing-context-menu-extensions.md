---
description: Implementando extensões do menu de contexto
ms.assetid: b8bea667-b9ea-476d-942f-281cb2e9636c
title: Implementando extensões do menu de contexto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65918f385984355490456cccb626ba297bd3368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812346"
---
# <a name="implementing-context-menu-extensions"></a>Implementando extensões do menu de contexto

A extensão de namespace WPD dá suporte a menus de contexto extensível (ou atalho). Esses são os menus que aparecem quando um usuário clica com o botão direito do mouse em um objeto, como um arquivo ou uma pasta. Alguns aplicativos WPD aproveitam esses menus extensíveis para dar suporte a operações no conteúdo do lado do dispositivo (ou objetos que residem no dispositivo).

Os menus de contexto extensível têm suporte nas interfaces descritas na tabela a seguir. Para obter mais informações sobre qualquer uma dessas interfaces, consulte a SDK do Windows.



| Interface           | Descrição                                                                                                                |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| IContextMenu        | O Shell do Windows Vista chama os métodos nesta interface para criar ou mesclar o novo menu de contexto com o objeto fornecido. |
| IDataObject         | Usado para passar a matriz PIDL do menu de contexto para o manipulador de menu de contexto.                                                    |
| IPropertySetStorage | Essa interface é usada para recuperar as propriedades de WPD para o objeto fornecido.                                                    |
| IPropertyStorage    | Essa interface também é usada para recuperar as propriedades de WPD para o objeto fornecido.                                               |
| IShellExtInit       | Inicializa as extensões do shell do Windows Vista para o menu de contexto.                                                       |
| IStream             | A ser fornecido.                                                                                                            |



 

Os menus de contexto para WPD são implementados como qualquer outro menu de contexto no Windows Vista. Se você já tiver implementado um manipulador de menu de contexto, poderá modificar o código existente para que ele dê suporte ao conteúdo do lado do dispositivo. Se você nunca criou um manipulador de menu de contexto, consulte o tópico Criando manipuladores de menu de contexto na SDK do Windows.

Os dois pontos em que um manipulador de menu de contexto WPD difere de qualquer outro manipulador está no registro do manipulador e no suporte ao conteúdo do lado do dispositivo.

 

 



