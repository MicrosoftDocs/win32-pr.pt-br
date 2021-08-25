---
description: Usar menus desenhados pelo proprietário para dar suporte à funcionalidade de fala para o Tablet PC.
ms.assetid: fbe2d420-f667-416b-bff3-0fee9ae22203
title: Usando Owner-Drawn menus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a14e63e3602e31edc506a6c9c070fa0bfcce670ec2248c73d68944a2f83a12f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842796"
---
# <a name="using-owner-drawn-menus"></a>Usando Owner-Drawn menus

Ao usar menus desenhados pelo proprietário, você deve disponibilizar os nomes de menu para dar suporte à funcionalidade de fala. Há duas maneiras de fazer isso:

-   Exponha o nome do item de menu usando a estrutura MSAAMENUINFO.
-   Forneça uma opção para substituir menus gráficos por menus de texto padrão quando um auxílio de acessibilidade estiver ativo. Se a [**função SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) retornar **TRUE com** seu parâmetro *uiAction* definido como SPI \_ GETSCREENREADER, use menus padrão. O aplicativo deve observar a mensagem WM SETTINGSCHANGE e responder consultando o estado dessa opção e ajustando \_ sua exibição adequadamente. Por exemplo, Microsoft Visual Studio fornece uma opção para usar menus padrão em vez dos menus personalizados exibidos por padrão.

 

 
