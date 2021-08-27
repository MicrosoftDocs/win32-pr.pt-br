---
title: Parâmetro do leitor de tela
description: O parâmetro leitor de tela indica se um aplicativo deve fornecer informações textuais em situações em que, caso contrário, apresentaria as informações graficamente.
ms.assetid: ac79c389-511c-4403-a8d5-75b2eba2b39f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 818ad36cfe833c1c9a3f39047cd88e6b4e8be55972d521ce524bb1e0618a48ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098416"
---
# <a name="screen-reader-parameter"></a>Parâmetro do leitor de tela

O parâmetro leitor de tela indica se um aplicativo deve fornecer informações textuais em situações em que, caso contrário, apresentaria as informações graficamente.

Esse parâmetro é normalmente definido por auxílios de acessibilidade, como leitores de tela. Os aplicativos usam os sinalizadores **SPI \_ GETSCREENREADER** e **SPI \_ SETSCREENREADER** com a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obter e definir o parâmetro de leitor de tela.

> [!Note]  
> o narrador, o leitor de tela que está incluído com o Windows, não define os sinalizadores **spi \_ SETSCREENREADER** ou **spi \_ GETSCREENREADER** .

 

 

 