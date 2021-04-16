---
title: Visão geral da miniatura do DWM
description: Gerenciador de Janelas da Área de Trabalho (DWM) permite a exibição de representações em miniatura de janelas de aplicativos.
ms.assetid: 6d71fcda-0cf0-463c-8c60-0415109d154f
keywords:
- Gerenciador de Janelas da Área de Trabalho (DWM), miniaturas
- DWM (Gerenciador de Janelas da Área de Trabalho), miniaturas
- Gerenciador de Janelas da Área de Trabalho (DWM), relações de miniatura
- DWM (Gerenciador de Janelas da Área de Trabalho), relações de miniatura
- miniaturas
- relações de miniatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3e0f1e6875e447a18ff5e63d703460ff909b25
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104566630"
---
# <a name="dwm-thumbnail-overview"></a>Visão geral da miniatura do DWM

Gerenciador de Janelas da Área de Trabalho (DWM) permite a exibição de representações em miniatura de janelas de aplicativos. Esses não são instantâneos estáticos de uma janela, mas são dinâmicos, em vez de conexões constantes entre uma janela de origem em miniatura e um local em uma janela de destino que recebe a renderização de miniaturas ao vivo. Isso permite uma exibição rápida da execução de aplicativos passando o mouse sobre o aplicativo na barra de tarefas ou usando o gesto de tecla ALT-TAB para ver e alternar rapidamente para um aplicativo.

A imagem a seguir ilustra a miniatura do Windows Vista ao vivo vista quando você passa o mouse sobre o aplicativo na barra de tarefas.

![Captura de tela que mostra a miniatura D W M vista ao passar o mouse sobre um aplicativo na barra de tarefas.](images/dwm-livethumbnail.png)

A imagem a seguir ilustra o Windows Vista Flip (ALT-TAB) habilitado pelo DWM.

![captura de tela da guia Alt habilitada para DWM](images/dwm-flip.png)

> [!Note]  
> As miniaturas do DWM não permitem que os desenvolvedores criem aplicativos como o recurso Windows Vista Flip3D (WINKEY-TAB). As miniaturas são renderizadas diretamente para a janela de destino em 2-D.

 

## <a name="dwm-thumbnail-relationships"></a>Relações de miniatura do DWM

Para exibir miniaturas em seu aplicativo, primeiro você deve estabelecer uma relação entre uma janela de origem e uma janela de destino. Isso é feito chamando a função [**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) .

[**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) não processa uma miniatura na janela de destino, mas apenas cria a relação e fornece o identificador de miniatura. A miniatura é renderizada depois que as [**\_ \_ Propriedades de miniatura do DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) tiverem sido definidas e a função [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) tiver sido chamada. As chamadas subsequentes para **DwmUpdateThumbnailProperties** atualizam a miniatura com um novo conjunto de propriedades. O DWM também fornece a função auxiliar [**DwmQueryThumbnailSourceSize**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize) para obter o tamanho da janela de origem da miniatura.

Para encerrar uma relação de miniatura, chame a função [**DwmUnregisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail) .

O exemplo a seguir demonstra como criar um releationship com a área de trabalho do Windows e exibi-lo em um aplicativo.


```
HRESULT hr = S_OK;
HTHUMBNAIL thumbnail = NULL;

// Register the thumbnail
hr = DwmRegisterThumbnail(hwnd, FindWindow(_T("Progman"), NULL), &thumbnail);
if (SUCCEEDED(hr))
{
    // Specify the destination rectangle size
    RECT dest = {0,50,100,150};

    // Set the thumbnail properties for use
    DWM_THUMBNAIL_PROPERTIES dskThumbProps;
    dskThumbProps.dwFlags = DWM_TNP_SOURCECLIENTAREAONLY | DWM_TNP_VISIBLE | DWM_TNP_OPACITY | DWM_TNP_RECTDESTINATION;
    dskThumbProps.fSourceClientAreaOnly = FALSE; 
    dskThumbProps.fVisible = TRUE;
    dskThumbProps.opacity = (255 * 70)/100;
    dskThumbProps.rcDestination = dest;

    // Display the thumbnail
    hr = DwmUpdateThumbnailProperties(thumbnail,&dskThumbProps);
    if (SUCCEEDED(hr))
    {
        // ...
    }
}
return hr;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral do Gerenciador de Janelas da Área de Trabalho](dwm-overview.md)
</dt> <dt>

[Habilitar e controlar a composição do DWM](composition-ovw.md)
</dt> <dt>

[Considerações sobre desempenho e práticas recomendadas](bestpractices-ovw.md)
</dt> </dl>

 

 




