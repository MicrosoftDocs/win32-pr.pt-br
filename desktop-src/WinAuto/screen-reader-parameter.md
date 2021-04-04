---
title: Parâmetro do leitor de tela
description: O parâmetro leitor de tela indica se um aplicativo deve fornecer informações textuais em situações em que, caso contrário, apresentaria as informações graficamente.
ms.assetid: ac79c389-511c-4403-a8d5-75b2eba2b39f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c237f3d945b9782884ffc655cf87a203159a16
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007820"
---
# <a name="screen-reader-parameter"></a>Parâmetro do leitor de tela

O parâmetro leitor de tela indica se um aplicativo deve fornecer informações textuais em situações em que, caso contrário, apresentaria as informações graficamente.

Esse parâmetro é normalmente definido por auxílios de acessibilidade, como leitores de tela. Os aplicativos usam os sinalizadores **SPI \_ GETSCREENREADER** e **SPI \_ SETSCREENREADER** com a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obter e definir o parâmetro de leitor de tela.

> [!Note]  
> O narrador, o leitor de tela que está incluído no Windows, não define os sinalizadores **SPI \_ SETSCREENREADER** ou **SPI \_ GETSCREENREADER** .

 

 

 