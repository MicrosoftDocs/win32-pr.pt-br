---
description: A TAPI modela os botões e as lâmpadas dos telefones como os pares de luzes de botão.
ms.assetid: e4c50bd6-a256-407f-af3b-b24383a30ea0
title: Botões de telefone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3e65c34096c0cf043b85d80c9c726c6bef982d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661784"
---
# <a name="phone-buttons"></a>Botões de telefone

A TAPI modela os botões e as lâmpadas de um telefone como pares de luzes de botão. Um botão sem nenhuma lâmpada ao lado dele ou uma lâmpada sem nenhum botão é especificado usando um indicador "fictício" para a lâmpada ou o botão ausente. Um botão com várias lâmpadas é modelado usando vários pares de botões de lâmpada.

As informações associadas a um botão de telefone podem ser definidas e recuperadas. Quando um botão é pressionado, uma mensagem de [**\_ botão de telefone**](phone-button.md) é enviada para a função do aplicativo. Os parâmetros dessa mensagem são um identificador para o dispositivo de telefone e o identificador de lâmpada de botão do botão que foi pressionado. Os botões de teclado ' 0 ' a ' 9 ', ' \* ' e ' \# ' são atribuídos ao botão fixo – identificadores de lâmpada de 0 a 11.

As funções associadas aos botões são [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo), que define as informações associadas a um botão em um dispositivo de telefone e [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo), que retorna informações associadas a um botão em um dispositivo de telefone. A \_ mensagem do botão telefone é enviada a um aplicativo quando um botão no telefone é pressionado.

As informações associadas a um botão não têm nenhum significado semântico no que diz respeito à TAPI. Ele é útil para aplicativos específicos do dispositivo que entendem o significado dessas informações para um determinado dispositivo de telefone, ou para exibição para o usuário, como a ajuda online.

 

 



