---
description: Os modelos de telefonia da Microsoft são botões e lâmpadas de telefones como pares de luzes de botão.
ms.assetid: 6ac912bb-8d2b-4aa3-a6e8-af86fbaabd58
title: Botões (API de telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd1fc18e02331f98f4dbb98cfea7d9df2ca7f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757001"
---
# <a name="buttons-telephony-api"></a>Botões (API de telefonia)

A telefonia da Microsoft modela os botões e as lâmpadas de um telefone como pares de luzes de botão. Um botão sem nenhuma lâmpada ao lado ou uma lâmpada sem nenhum botão é especificado usando um indicador fictício para a lâmpada ou o botão ausente. Um botão com várias lâmpadas é modelado usando vários pares de botões de lâmpada.

As informações associadas a um botão de telefone podem ser definidas e recuperadas. Quando um botão é pressionado, o provedor de serviços envia uma mensagem de [**\_ botão de telefone**](/previous-versions/windows/desktop/legacy/ms725254(v=vs.85)) para a função de retorno de chamada TAPI. Os parâmetros dessa mensagem são um identificador para o dispositivo de telefone e o identificador de botão/lâmpada do botão que foi pressionado. O botão do teclado ' 0 ' por meio de ' 9 ', ' \* ' e ' \# ' recebe identificadores de botão/lâmpada fixos de 0 a 11.

A função [**TSPI \_ phoneSetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo) define as informações associadas a um botão em um dispositivo de telefone. [**TSPI \_ phoneGetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonegetbuttoninfo) retorna informações associadas a um botão em um dispositivo de telefone. O provedor de serviços envia uma \_ mensagem de botão de telefone para a função de retorno de chamada TAPI quando um botão no telefone é pressionado.

As informações associadas a um botão não têm nenhum significado semântico no que diz respeito ao TSPI. Ele é útil para aplicativos específicos do dispositivo que interpretam essas informações para um determinado dispositivo de telefone ou para exibição para o usuário, como no sistema de ajuda de um aplicativo.

 

 
