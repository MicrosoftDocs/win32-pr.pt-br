---
title: Parâmetro de animação da área do cliente
description: O sinalizador de animação da área de cliente indica se o usuário deseja desabilitar animações em elementos da interface do usuário.
ms.assetid: 4a3ec9da-d5ae-4cd9-8222-f02143895ce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab4d451424da0a02fa55efaead05ab285b3f07936167bb6e4376de4fd25ae11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325955"
---
# <a name="client-area-animation-parameter"></a>Parâmetro de animação da área do cliente

O parâmetro de animação da área de cliente indica se o usuário deseja desabilitar animações em elementos de interface do usuário. Os recursos de exibição, como Flash, intermitência, cintilação e movimentação de conteúdo, podem causar capturas de usuários com Epilepsias sensíveis a fotos. Esse parâmetro permite que você habilite ou desabilite todas essas animações.

Os aplicativos usam os sinalizadores **SPI \_ GETCLIENTAREAANIMATION** e **SPI \_ SETCLIENTAREAANIMATION** com a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para ativar ou desativar animações da área do cliente.

 

 