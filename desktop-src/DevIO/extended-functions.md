---
description: Algumas funções de comunicação podem ser chamadas para um dispositivo usando a função EscapeCommFunction.
ms.assetid: 12b92d4b-04b5-4509-9fad-af23fcfd8857
title: Funções estendidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d0e57c316b521cbc246e5f31dcfb683238e216e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010244"
---
# <a name="extended-functions"></a>Funções estendidas

Algumas funções de comunicação podem ser chamadas para um dispositivo usando a função [**EscapeCommFunction**](/windows/desktop/api/Winbase/nf-winbase-escapecommfunction) . Essa função envia um código para direcionar o dispositivo para executar uma função estendida. Por exemplo, um aplicativo pode suspender a transmissão de caracteres com o código SETBREAK e retomar a transmissão com o código CLRBREAK. Essas operações específicas também podem ser iniciadas chamando as funções [**SetCommBreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak) e [**ClearCommBreak**](/windows/desktop/api/Winbase/nf-winbase-clearcommbreak) . O **EscapeCommFunction** também pode ser usado para implementar o controle de modem manual. Por exemplo, os códigos CLRDTR e SETDTR podem ser usados para implementar o controle de fluxo DTR (Data-Terminal-Ready) manual. Observe, no entanto, que um erro ocorrerá se um processo usar **EscapeCommFunction** para manipular a linha de DTR quando o dispositivo tiver sido configurado para habilitar o HANDSHAKE de DTR ou a linha RTS (solicitação para envio) se o HANDSHAKE de RTS estiver habilitado.

A função [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) permite que um processo envie um código de função estendido diretamente para um driver de dispositivo especificado, fazendo com que o dispositivo execute uma determinada operação. **DeviceIoControl** fornece um dispositivo associado a uma capacidade de recursos de comunicação não suportada pelas funções de comunicação serial padrão. Ele permite que um aplicativo configure um dispositivo usando parâmetros exclusivos para esse dispositivo, bem como para chamar qualquer função específica do dispositivo.

 

 
