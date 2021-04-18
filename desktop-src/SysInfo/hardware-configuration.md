---
description: As funções de configuração de hardware recuperam informações como processador, perfil de hardware e informações de teclado.
ms.assetid: c6245571-428a-4965-b58c-24645ddca70d
title: Configuração de hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee4abe543f0603ab6cf80ef395fe56e4e3300c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756351"
---
# <a name="hardware-configuration"></a>Configuração de hardware

As funções de configuração de hardware recuperam informações como processador, perfil de hardware e informações de teclado.

A função [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) recupera informações de processador e memória, como o tamanho da página, o identificador OEM (fabricante original do equipamento), o número e o tipo de processadores, o intervalo de endereços do aplicativo e assim por diante. A função [**IsProcessorFeaturePresent**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent) recupera informações sobre as operações de ponto flutuante e os conjuntos de instruções com suporte do processador.

A função [**GetCurrentHwProfile**](/windows/desktop/api/Winbase/nf-winbase-getcurrenthwprofilea) recupera informações sobre o perfil de hardware. O perfil de hardware inclui informações como o estado de encaixe, o GUID (identificador global exclusivo) e o nome de exibição do perfil. A função [**Getkeyboardtype**](/windows/desktop/api/winuser/nf-winuser-getkeyboardtype) recupera informações como o tipo de teclado e o número de teclas de função no teclado atual.

 

 
