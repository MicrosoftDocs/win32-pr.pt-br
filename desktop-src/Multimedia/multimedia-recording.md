---
title: Gravação de multimídia
description: Gravação de multimídia
ms.assetid: e37aaac2-be89-4907-b1a8-f2c64ab2f39e
keywords:
- Função MCIWndCreate
- Macro MCIWndNew
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b1793ff7653e87a631ce1a4599345ec78f4015
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363967"
---
# <a name="multimedia-recording"></a>Gravação de multimídia

Você pode implementar recursos de gravação em seu aplicativo usando a interface do usuário interna no MCIWnd. Você pode usar a função [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) e a macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) para fornecer controles para iniciar e interromper a gravação e salvar as informações gravadas. Usando **MCIWndCreate**, você pode especificar estilos de janela para exibir uma janela MCIWnd e incluir o botão **gravar** na barra de ferramentas. Usando o **MCIWndNew**, você pode especificar o tipo de dispositivo que está sendo registrado e especificar que as informações serão capturadas em um novo arquivo.

Se seu aplicativo precisar de mais sofisticação, você poderá automatizar e personalizar a gravação usando a macro [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) . Para obter mais informações, consulte [Personalizando o processo de gravação](customizing-the-recording-process.md).

> [!Note]  
> Alguns dispositivos, como CD Audio e MCIAVI, são usados somente para reprodução. Outros dispositivos, como, por exemplo, dispositivos de áudio de forma de onda, podem ser usados para gravação. Se você especificar um dispositivo que não pode gravar, MCIWnd omitirá o botão **gravar** da barra de ferramentas.

 

 

 




