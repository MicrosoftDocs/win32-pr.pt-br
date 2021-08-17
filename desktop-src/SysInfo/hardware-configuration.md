---
description: As funções de configuração de hardware recuperam informações como processador, perfil de hardware e informações de teclado.
ms.assetid: c6245571-428a-4965-b58c-24645ddca70d
title: Configuração de hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e396b2d08b489e92c7a407ca892250135fdd3d174d16de50d0c2d75428a88dce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764414"
---
# <a name="hardware-configuration"></a>Configuração de hardware

As funções de configuração de hardware recuperam informações como processador, perfil de hardware e informações de teclado.

A [**função GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) recupera informações de processador e memória, como o tamanho da página, o identificador OEM (fabricante original de equipamentos), o número e o tipo de processadores, o intervalo de endereços do aplicativo e assim por diante. A [**função IsProcessorFeaturePresent**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent) recupera informações sobre as operações de ponto flutuante e conjuntos de instruções com suporte pelo processador.

A [**função GetCurrentHwProfile**](/windows/desktop/api/Winbase/nf-winbase-getcurrenthwprofilea) recupera informações sobre o perfil de hardware. O perfil de hardware inclui informações como o estado de encaixe, o GUID (identificador global exclusivo) e o nome de exibição do perfil. A [**função GetKeyboardType**](/windows/desktop/api/winuser/nf-winuser-getkeyboardtype) recupera informações como o tipo de teclado e o número de teclas de função no teclado atual.

 

 
