---
title: Como implementar dicas de ferramenta para ícones da barra de status
description: Uma maneira não intrusiva de exibir uma mensagem explicativa para um ícone da barra de status é implementar uma dica de ferramenta. A dica de ferramenta desaparece quando clicada, mas você também pode especificar um valor de tempo limite.
ms.assetid: AA7F17F2-63A4-4954-9DAB-788B73984628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2bd100dc6edb2aac7b4c8c5df3781e76391ae2d9d0ad456533384ed8701f14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958575"
---
# <a name="how-to-implement-tooltips-for-status-bar-icons"></a>Como implementar dicas de ferramenta para ícones da barra de status

Uma maneira não intrusiva de exibir uma mensagem explicativa para um ícone da barra de status é implementar uma dica de ferramenta. A dica de ferramenta desaparece quando clicada, mas você também pode especificar um valor de tempo limite.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Programação de interface do usuário

## <a name="instructions"></a>Instruções

### <a name="implement-tooltips-for-status-bar-icons"></a>Implementar dicas de ferramentas para ícones da barra de status

O fragmento de código a seguir ilustra como adicionar uma dica de ferramenta de balão a um ícone de barra de status.


```C++
#define ARRAYSIZE(a) (sizeof(a)/sizeof(a[0]))

NOTIFYICONDATA IconData = {0};

IconData.cbSize = sizeof(IconData);
IconData.hWnd   = hwndNI;
IconData.uFlags = NIF_INFO;

HRESULT hr = StringCchCopy(IconData.szInfo, 
                           ARRAYSIZE(IconData.szInfo), 
                           TEXT("Your message text goes here."));

if(FAILED(hr))
{
  // TODO: Write an error handler in case the call to StringCchCopy fails.
}
IconData.uTimeout = 15000; // in milliseconds

Shell_NotifyIcon(NIM_MODIFY, &IconData);
            
```



## <a name="remarks"></a>Comentários

Para obter uma discussão detalhada sobre a barra de status, consulte [a barra de tarefas](/windows/desktop/shell/taskbar).

Para exibir uma dica de ferramenta de balão, você precisa definir o sinalizador de informações de nse \_ na estrutura [**NOTIFYICONDATA**](/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa) e usar os membros **szInfo** e **uTimeout** para especificar o texto da dica de ferramenta e a duração do tempo limite.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de dica de ferramenta](using-tooltip-contro.md)
</dt> </dl>

 

 