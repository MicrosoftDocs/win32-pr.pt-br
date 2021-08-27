---
title: Como implementar dicas de ferramenta multilinha
description: Dicas de ferramenta multilinha permitem que o texto seja exibido em mais de uma linha.
ms.assetid: 62B10B44-C1C2-4C86-8648-AE6B606BACBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd0d9f4172b256d2e6b72fb59ace4dc377fa3a0061e3ee0e6c0f234a74aad06
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085617"
---
# <a name="how-to-implement-multiline-tooltips"></a>Como implementar dicas de ferramenta multilinha

Dicas de ferramenta multilinha permitem que o texto seja exibido em mais de uma linha.

Eles têm suporte na [versão 4.70](common-control-versions.md) e posterior dos controles comuns. Seu aplicativo cria uma dica de ferramenta multilinha enviando uma mensagem [**TTM \_ SETMAXTIPWIDTH,**](ttm-setmaxtipwidth.md) especificando a largura do retângulo de exibição. O texto que excede essa largura é wraps para a próxima linha em vez de ampliar a região de exibição. A altura do retângulo é aumentada conforme necessário para acomodar as linhas adicionais. O controle de dica de ferramenta envolve as linhas automaticamente ou você pode usar uma combinação de retorno de carro/alimentação de linha, r n, para forçar quebras de linha \\ \\ em locais específicos.

A exibição resultante é mostrada na ilustração a seguir.

![captura de tela de uma caixa de diálogo com uma dica de ferramenta que contém texto organizado como um parágrafo de várias linhas](images/tt-multiline.png)

> [!Note]  
> O buffer de texto especificado pelo **membro szText** da [**estrutura NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) pode acomodar apenas 80 caracteres. Se você precisar usar uma cadeia de caracteres mais longa, aponte o membro **lpszText** **de NMTTDISPINFO** para um buffer que contém o texto desejado.

 

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções

### <a name="implement-multiline-tooltips"></a>Implementar dicas de ferramenta multilinha

O fragmento de código a seguir é um exemplo de um manipulador de notificação [ \_ GETDISPINFO TTN](ttn-getdispinfo.md) simples. Ele habilita uma dica de ferramenta multilinha definindo o retângulo de exibição como 150 pixels. Uma quebra de linha manual é inserida após a primeira palavra para mostrar que as quebras de linha podem ser duras, bem como suaves.


```C++
    case WM_NOTIFY:
    {
        switch (((LPNMHDR)lParam)->code)
        {
        case TTN_GETDISPINFO:
            LPNMTTDISPINFO pInfo = (LPNMTTDISPINFO)lParam;
            SendMessage(pInfo->hdr.hwndFrom, TTM_SETMAXTIPWIDTH, 0, 150);
            wcscpy_s(pInfo->szText, ARRAYSIZE(pInfo->szText), 
                L"This\nis a very long text string " \
                L"that must be broken into several lines.");
            break;
        }
        break;
    }
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de dica de ferramenta](using-tooltip-contro.md)
</dt> </dl>

 

 




