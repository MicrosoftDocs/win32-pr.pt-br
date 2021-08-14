---
description: Exibir caixas de diálogo Captura do VFW
ms.assetid: 708212ca-d148-4079-8052-3bf6696a33ab
title: Exibir caixas de diálogo Captura do VFW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2713cc4d2eba52626c66974eed23f2c1752a1268fea78a30ca2bc9d7babc3a27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821134"
---
# <a name="display-vfw-capture-dialog-boxes"></a>Exibir caixas de diálogo Captura do VFW

Um dispositivo de captura que ainda usa um driver VFW (Video for Windows) pode dar suporte a qualquer uma das três caixas de diálogo a seguir, que são usadas para configurar o dispositivo.



| Caixa de diálogo    | Descrição                                                                                           |
|---------------|-------------------------------------------------------------------------------------------------------|
| Origem do vídeo  | Usado para selecionar a entrada de vídeo e ajustar as configurações do dispositivo, como brilho ou contraste da imagem. |
| Formato de vídeo  | Usado para selecionar as dimensões de imagem e a profundidade de bits.                                                    |
| Vídeo exibido | Usado para controlar a aparência do vídeo renderizado.                                                 |



 

Para mostrar uma dessas caixas de diálogo, faça o seguinte:

1.  Pare o grafo de filtro.
2.  Consulte o filtro de captura para a interface [**IAMVfwCaptureDialogs.**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) Se **QueryInterface for** bem-sucedido, isso significará que o dispositivo de captura é um dispositivo VFW.
3.  Chame [**IAMVfwCaptureDialogs::HasDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-hasdialog) para verificar se o driver dá suporte à caixa de diálogo que você deseja exibir. A [**enumeração VfwCaptureDialogs**](/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs) define sinalizadores para cada uma das caixas de diálogo do VFW. **HasDialog** retornará S \_ OK se a caixa de diálogo tiver suporte. Ele retorna S \_ FALSE caso contrário, verifique o valor S \_ OK diretamente, em vez de usar a **macro SUCCEEDED.**
4.  Se a caixa de diálogo tiver suporte, chame [**IAMVfwCaptureDialogs::ShowDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-showdialog) para exibir a caixa de diálogo.
5.  Reinicie o grafo.

O código a seguir mostra estas etapas para a caixa de diálogo Origem do Vídeo:


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

 

 



