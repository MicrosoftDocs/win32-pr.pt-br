---
description: Lidando com Unicode em um aplicativo IME-Aware
ms.assetid: fa202c1e-d0af-441f-b878-ed98205a880c
title: Lidando com Unicode em um aplicativo IME-Aware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78174776eb608c3e494fd5967acba41609e436a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761832"
---
# <a name="handling-unicode-in-an-ime-aware-application"></a>Lidando com Unicode em um aplicativo IME-Aware

Dois problemas estão envolvidos no IMM e seu manuseio de Unicode. O primeiro problema é que as versões Unicode das funções do IMM recuperam o tamanho de um buffer em bytes em vez de caracteres Unicode de 16 bits. O segundo problema é que o IMM normalmente recupera caracteres Unicode (em vez de caracteres DBCS) nas mensagens de caracteres do [**WM \_ Char**](../inputdev/wm-char.md) e do [**\_ \_ IME do WM**](wm-ime-char.md) .

O Windows dá suporte a uma interface Unicode para o IMM, além da interface ANSI com suporte originalmente.

Seus aplicativos devem usar [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) para fazer com que as mensagens de caracteres do [**WM \_ Char**](../inputdev/wm-char.md) e do [**\_ IME \_ do WM**](wm-ime-char.md) recuperem caracteres Unicode em vez de caracteres DBCS no parâmetro *wParam* .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Gerenciador de métodos de entrada](using-input-method-manager.md)
</dt> </dl>

 

 
