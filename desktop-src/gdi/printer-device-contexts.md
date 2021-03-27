---
description: O controlador de domínio da impressora pode ser usado ao imprimir em uma impressora matricial, impressora jato de tinta, impressora laser ou plotadora.
ms.assetid: c53f15d8-5a02-4095-8f05-ae309d4553ff
title: Contextos de dispositivo de impressora (GDI do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7475776a3d13394b210f8289b458b8e99c474c93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967609"
---
# <a name="printer-device-contexts-windows-gdi"></a>Contextos de dispositivo de impressora (GDI do Windows)

O controlador de domínio da impressora pode ser usado ao imprimir em uma impressora matricial, impressora jato de tinta, impressora laser ou plotadora. Um aplicativo cria um DC de impressora chamando a função [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) e fornecendo os argumentos apropriados (o nome do driver de impressora, o nome da impressora, o nome do arquivo ou do dispositivo para a mídia de saída física e outros dados de inicialização). Quando um aplicativo termina de imprimir, ele exclui o controlador de domínio da impressora chamando a função [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) . Um aplicativo deve excluir (em vez de liberar) um controlador de domínio de impressora; a função [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) falha quando um aplicativo tenta usá-lo para liberar um controlador de domínio de impressora.

Para obter mais informações, consulte [saída da impressora](../printdocs/printer-output.md).

 

 
