---
title: Usando uma interface de vários documentos
description: Usando uma interface de vários documentos
ms.assetid: bc59f19c-1064-4df8-8864-38e6d188f92f
keywords:
- Função MCIWndRegisterClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b75d337c5375b66974161c1c983c1aeec5bed7805457186139771d879132b6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941051"
---
# <a name="using-a-multiple-document-interface"></a>Usando uma interface de vários documentos

Os aplicativos que usam uma MDI (interface de vários documentos) podem precisar especificar estilos de janela que não estão disponíveis por meio da função [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) . Para esses aplicativos, você pode registrar e criar uma janela MCIWnd usando a função [**MCIWndRegisterClass**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass) com a função [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) . A função **MCIWndRegisterClass** registra a classe da janela da \_ classe MCIWND Window \_ e, em seguida, **CreateWindowEx** cria uma instância de uma janela MCIWND.

 

 