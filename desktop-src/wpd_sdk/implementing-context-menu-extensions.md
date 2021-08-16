---
description: Implementando extensões do menu de contexto
ms.assetid: b8bea667-b9ea-476d-942f-281cb2e9636c
title: Implementando extensões do menu de contexto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090f37b4cf77f9508e8c149ef6389297c561e1a4e574ef767f3a5e5c7e07fe05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194679"
---
# <a name="implementing-context-menu-extensions"></a>Implementando extensões do menu de contexto

A extensão de namespace WPD dá suporte a menus de contexto extensível (ou atalho). Esses são os menus que aparecem quando um usuário clica com o botão direito do mouse em um objeto, como um arquivo ou uma pasta. Alguns aplicativos WPD aproveitam esses menus extensíveis para dar suporte a operações no conteúdo do lado do dispositivo (ou objetos que residem no dispositivo).

Os menus de contexto extensível têm suporte nas interfaces descritas na tabela a seguir. para obter mais informações sobre qualquer uma dessas interfaces, consulte a SDK do Windows.



| Interface           | Descrição                                                                                                                |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| IContextMenu        | o Shell do Windows Vista chama os métodos nesta interface para criar ou mesclar o novo menu de contexto com o objeto fornecido. |
| IDataObject         | Usado para passar a matriz PIDL do menu de contexto para o manipulador de menu de contexto.                                                    |
| IPropertySetStorage | Essa interface é usada para recuperar as propriedades de WPD para o objeto fornecido.                                                    |
| IPropertyStorage    | Essa interface também é usada para recuperar as propriedades de WPD para o objeto fornecido.                                               |
| IShellExtInit       | inicializa as extensões do Shell do Windows Vista para o menu de contexto.                                                       |
| IStream             | A ser fornecido.                                                                                                            |



 

os menus de contexto para WPD são implementados como qualquer outro menu de contexto no Windows Vista. Se você já tiver implementado um manipulador de menu de contexto, poderá modificar o código existente para que ele dê suporte ao conteúdo do lado do dispositivo. se você nunca criou um manipulador de menu de contexto, consulte o tópico criando manipuladores de menu de contexto na SDK do Windows.

Os dois pontos em que um manipulador de menu de contexto WPD difere de qualquer outro manipulador está no registro do manipulador e no suporte ao conteúdo do lado do dispositivo.

 

 



