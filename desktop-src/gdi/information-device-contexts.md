---
description: O controlador de domínio de informações é usado para recuperar dados de dispositivo padrão.
ms.assetid: 8fd05c17-e8c9-4747-9a66-ce7d958edeb9
title: Contextos de dispositivo de informações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002e9d5ebb6831f9e2251e76049e586ac3e84056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502413"
---
# <a name="information-device-contexts"></a>Contextos de dispositivo de informações

O controlador de domínio de informações é usado para recuperar dados de dispositivo padrão. Por exemplo, um aplicativo pode chamar a função [**createy**](/windows/desktop/api/Wingdi/nf-wingdi-createica) para criar um controlador de domínio de informações para um modelo específico de impressora e, em seguida, chamar as funções [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) e [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) para recuperar os atributos padrão da caneta ou do pincel. Como o sistema pode recuperar informações do dispositivo sem criar as estruturas normalmente associadas a outros tipos de contextos de dispositivo, um controlador de domínio de informações envolve muito menos sobrecarga e é criado significativamente mais rápido do que qualquer um dos outros tipos. Depois que um aplicativo termina de recuperar dados usando um controlador de domínio de informações, ele deve chamar a função [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) .

 

 



