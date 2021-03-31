---
description: Exibir caixas de diálogo de captura do VFW
ms.assetid: 708212ca-d148-4079-8052-3bf6696a33ab
title: Exibir caixas de diálogo de captura do VFW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45b8b51b164630a8fa6e91b2e68ca8a9a3a875b6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645687"
---
# <a name="display-vfw-capture-dialog-boxes"></a>Exibir caixas de diálogo de captura do VFW

Um dispositivo de captura que ainda usa um driver de vídeo para Windows (VFW) pode dar suporte a qualquer uma das três caixas de diálogo a seguir, que são usadas para configurar o dispositivo.



| Caixa de diálogo    | Descrição                                                                                           |
|---------------|-------------------------------------------------------------------------------------------------------|
| Fonte de vídeo  | Usado para selecionar a entrada de vídeo e ajustar as configurações do dispositivo, como o brilho ou o contraste da imagem. |
| Formato de vídeo  | Usado para selecionar as dimensões da imagem e a profundidade de bits.                                                    |
| Vídeo | Usado para controlar a aparência do vídeo renderizado.                                                 |



 

Para mostrar uma dessas caixas de diálogo, faça o seguinte:

1.  Pare o gráfico de filtro.
2.  Consulte o filtro de captura para a interface [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) . Se **QueryInterface** for bem-sucedidos, isso significa que o dispositivo de captura é um dispositivo VFW.
3.  Chame [**IAMVfwCaptureDialogs:: HasDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-hasdialog) para verificar se o driver dá suporte à caixa de diálogo que você deseja exibir. A enumeração [**VfwCaptureDialogs**](/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs) define sinalizadores para cada uma das caixas de diálogo VFW. **HasDialog** retornará S \_ OK se a caixa de diálogo tiver suporte. \_Caso contrário, retornará s false, portanto, verifique o valor s \_ OK diretamente, em vez de usar a macro **Succeeded** .
4.  Se a caixa de diálogo tiver suporte, chame [**IAMVfwCaptureDialogs:: ShowDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-showdialog) para exibir a caixa de diálogo.
5.  Reinicie o grafo.

O código a seguir mostra estas etapas para a caixa de diálogo fonte de vídeo:


```C++
pControl->Stop(); // Stop the graph.

// Query the capture filter for the IAMVfwCaptureDialogs interface.
IAMVfwCaptureDialogs *pVfw = 0;
hr = pCap->QueryInterface(IID_IAMVfwCaptureDialogs, (void**)&pVfw);
if (SUCCEEDED(hr))
{
    // Check if the device supports this dialog box.
    if (S_OK == pVfw->HasDialog(VfwCaptureDialog_Source))
    {
        // Show the dialog box.
        hr = pVfw->ShowDialog(VfwCaptureDialog_Source, hwndParent);
    }
}
pControl->Run();
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando um dispositivo de captura de vídeo](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



