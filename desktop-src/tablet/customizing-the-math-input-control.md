---
description: Explica como alterar a aparência do controle de entrada de matemática.
ms.assetid: 922562be-4d5b-45b6-ad0b-49176f893c8e
title: Personalizando o controle de entrada matemática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c3cab7c6efe003738c46a89d07866fcc9302ec5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565274"
---
# <a name="customizing-the-math-input-control"></a>Personalizando o controle de entrada matemática

É possível alterar a aparência do controle de entrada matemática para que ele seja mais adequado ao seu aplicativo. Este tópico explica as várias maneiras pelas quais os desenvolvedores podem personalizar o controle de entrada matemática.

As seguintes personalizações são possíveis:

-   [Alterando os botões exibidos](#changing-the-displayed-buttons)
-   [Alterando a legenda do controle](#changing-the-control-caption)
-   [Alterando o tamanho da área de visualização do controle](#changing-the-controls-preview-area-size)

## <a name="changing-the-displayed-buttons"></a>Alterando os botões exibidos

Você pode alterar os botões que são exibidos no controle de entrada de matemática para que o controle tenha funcionalidade estendida ou pareça menor na tela. Habilitar o conjunto de botões estendidos mostrará os botões **refazer** e **desfazer** . O código a seguir mostra como habilitar o conjunto de botões estendidos.


```
  void CMath_Input_Control_testDlg::OnBnClickedToggleBtns()
  {
    static bool enabled = true;
    HRESULT hr = S_OK;

    hr = g_spMIC->Hide();    
    if(!enabled){
      if (SUCCEEDED(hr)){
        hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
        enabled = true;
      }
    }else{
      if (SUCCEEDED(hr)){
        hr = g_spMIC->EnableExtendedButtons(VARIANT_FALSE);
        enabled = false;
      }
    }
    if (SUCCEEDED(hr)){
      hr = g_spMIC->Show();
    }
  }
  
```



A imagem a seguir mostra o controle com o conjunto estendido de botões.

![controle de entrada matemática com um conjunto estendido de botões](images/mic.png)

A imagem a seguir mostra o controle sem o conjunto estendido de botões.

![controle de entrada matemática sem um conjunto estendido de botões](images/mic-no-extended.png)

## <a name="changing-the-control-caption"></a>Alterando a legenda do controle

Você pode alterar a legenda do controle para o controle de entrada matemática a fim de definir a legenda na janela do controle de entrada de matemática. O código a seguir mostra como definir a legenda.


```
  void CMath_Input_Control_testDlg::OnBnClickedSetCaption()
  {     
    g_spMIC->Hide();
    CComBSTR cap1(L"Some Caption Text");    
    g_spMIC->SetCaptionText((BSTR)cap1);
    g_spMIC->Show();
  }  
  
```



A imagem a seguir mostra o controle após a definição da legenda.

![controle de entrada matemática com um conjunto de legendas](images/mic-caption.png)

## <a name="changing-the-controls-preview-area-size"></a>Alterando o tamanho da área de visualização do controle

Você pode personalizar o controle de entrada matemática para que o controle defina explicitamente o tamanho da área de visualização. Isso cria uma área maior na qual as fórmulas matemáticas são exibidas. O código a seguir mostra como definir o tamanho da área de visualização.


```
  void CMath_Input_Control_testDlg::OnBnClickedSetPreviewAreaSize()
  {
    LONG height = 200;
    HRESULT hr = S_OK;
    hr = g_spMIC->SetPreviewHeight(height);
  }  
  
```



As imagens a seguir mostram um controle com áreas de visualização de tamanhos diferentes.

![controle de entrada matemática com o tamanho da área de visualização padrão](images/mic.png)![controle de entrada matemática com área de visualização maior](images/mic-big-preview.png)

 

 



