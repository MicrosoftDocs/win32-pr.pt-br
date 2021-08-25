---
description: A TAPI modela botões e lâmpadas de telefones como pares de lâmpada de botão.
ms.assetid: e4c50bd6-a256-407f-af3b-b24383a30ea0
title: Telefone Botões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e72288133615b19e622434b8727608aaec9a9136dd58eaa03e339708c42a13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774156"
---
# <a name="phone-buttons"></a>Telefone Botões

A TAPI modela botões e lâmpadas de um telefone como pares de lâmpada de botão. Um botão sem nenhuma lâmpada ao lado dela ou uma lâmpada sem botão é especificado usando um indicador "fictício" para a lâmpada ou botão ausente. Um botão com várias lâmpadas é modelado usando vários pares de lâmpada de botão.

As informações associadas a um botão de telefone podem ser definidas e recuperadas. Quando um botão é pressionado, uma [**mensagem PHONE \_ BUTTON**](phone-button.md) é enviada para a função de aplicativo. Os parâmetros dessa mensagem são um identificador para o dispositivo de telefone e o identificador de lâmpada de botão do botão que foi pressionado. Os botões de teclado '0' a '9', ' ' e ' são atribuídos aos identificadores fixos de lâmpada de botão \* \# 0 a 11.

As funções associadas aos botões são [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo), que define as informações associadas a um botão em um dispositivo de telefone e [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo), que retorna informações associadas a um botão em um dispositivo de telefone. A mensagem \_ PHONE BUTTON é enviada a um aplicativo quando um botão no telefone é pressionado.

As informações associadas a um botão não têm nenhum significado semântico no que diz respeito à TAPI. É útil para aplicativos específicos do dispositivo que entendem o significado dessas informações para um determinado dispositivo de telefone ou para exibição para o usuário, como ajuda online.

 

 



