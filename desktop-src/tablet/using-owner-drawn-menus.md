---
description: Usando os menus desenhados pelo proprietário para dar suporte à funcionalidade de fala para o Tablet PC.
ms.assetid: fbe2d420-f667-416b-bff3-0fee9ae22203
title: Usando Owner-Drawn menus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42f16f9328fadfedccee2c730678fc4cd2d8ab3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647092"
---
# <a name="using-owner-drawn-menus"></a>Usando Owner-Drawn menus

Ao usar menus desenhados pelo proprietário, você deve disponibilizar os nomes de menu para dar suporte à funcionalidade de fala. Há duas maneiras de fazer isso:

-   Expor o nome do item de menu usando a estrutura MSAAMENUINFO.
-   Forneça uma opção para substituir os menus gráficos por menus de texto padrão quando um auxílio de acessibilidade estiver ativo. Se a função [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) retornar **true** com seu parâmetro *uiAction* definido como SPI \_ GETSCREENREADER, use os menus padrão. O aplicativo deve observar a \_ mensagem SETTINGSCHANGE do WM e responder consultando o estado dessa opção e ajustando sua exibição adequadamente. Por exemplo, Microsoft Visual Studio fornece uma opção para usar menus padrão em vez dos menus personalizados que são exibidos por padrão.

 

 
