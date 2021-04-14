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
# <a name="customizing-the-math-input-control"></a><span data-ttu-id="8af0e-103">Personalizando o controle de entrada matemática</span><span class="sxs-lookup"><span data-stu-id="8af0e-103">Customizing the Math Input Control</span></span>

<span data-ttu-id="8af0e-104">É possível alterar a aparência do controle de entrada matemática para que ele seja mais adequado ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8af0e-104">It is possible to change the look and feel of the math input control so that it is better suited to your application.</span></span> <span data-ttu-id="8af0e-105">Este tópico explica as várias maneiras pelas quais os desenvolvedores podem personalizar o controle de entrada matemática.</span><span class="sxs-lookup"><span data-stu-id="8af0e-105">This topic explains the various ways that developers can customize the math input control.</span></span>

<span data-ttu-id="8af0e-106">As seguintes personalizações são possíveis:</span><span class="sxs-lookup"><span data-stu-id="8af0e-106">The following customizations are possible:</span></span>

-   [<span data-ttu-id="8af0e-107">Alterando os botões exibidos</span><span class="sxs-lookup"><span data-stu-id="8af0e-107">Changing the Displayed Buttons</span></span>](#changing-the-displayed-buttons)
-   [<span data-ttu-id="8af0e-108">Alterando a legenda do controle</span><span class="sxs-lookup"><span data-stu-id="8af0e-108">Changing the Control Caption</span></span>](#changing-the-control-caption)
-   [<span data-ttu-id="8af0e-109">Alterando o tamanho da área de visualização do controle</span><span class="sxs-lookup"><span data-stu-id="8af0e-109">Changing the Control's Preview Area Size</span></span>](#changing-the-controls-preview-area-size)

## <a name="changing-the-displayed-buttons"></a><span data-ttu-id="8af0e-110">Alterando os botões exibidos</span><span class="sxs-lookup"><span data-stu-id="8af0e-110">Changing the Displayed Buttons</span></span>

<span data-ttu-id="8af0e-111">Você pode alterar os botões que são exibidos no controle de entrada de matemática para que o controle tenha funcionalidade estendida ou pareça menor na tela.</span><span class="sxs-lookup"><span data-stu-id="8af0e-111">You can change the buttons that are displayed on the math input control so that the control has extended functionality or appears smaller on the screen.</span></span> <span data-ttu-id="8af0e-112">Habilitar o conjunto de botões estendidos mostrará os botões **refazer** e **desfazer** .</span><span class="sxs-lookup"><span data-stu-id="8af0e-112">Enabling the extended button set will show the **Redo** and **Undo** buttons.</span></span> <span data-ttu-id="8af0e-113">O código a seguir mostra como habilitar o conjunto de botões estendidos.</span><span class="sxs-lookup"><span data-stu-id="8af0e-113">The following code shows how to enable the extended button set.</span></span>


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



<span data-ttu-id="8af0e-114">A imagem a seguir mostra o controle com o conjunto estendido de botões.</span><span class="sxs-lookup"><span data-stu-id="8af0e-114">The following image shows the control with the extended set of buttons.</span></span>

![controle de entrada matemática com um conjunto estendido de botões](images/mic.png)

<span data-ttu-id="8af0e-116">A imagem a seguir mostra o controle sem o conjunto estendido de botões.</span><span class="sxs-lookup"><span data-stu-id="8af0e-116">The following image shows the control without the extended set of buttons.</span></span>

![controle de entrada matemática sem um conjunto estendido de botões](images/mic-no-extended.png)

## <a name="changing-the-control-caption"></a><span data-ttu-id="8af0e-118">Alterando a legenda do controle</span><span class="sxs-lookup"><span data-stu-id="8af0e-118">Changing the Control Caption</span></span>

<span data-ttu-id="8af0e-119">Você pode alterar a legenda do controle para o controle de entrada matemática a fim de definir a legenda na janela do controle de entrada de matemática.</span><span class="sxs-lookup"><span data-stu-id="8af0e-119">You can change the control caption for the math input control in order to set the caption on the math input control's window.</span></span> <span data-ttu-id="8af0e-120">O código a seguir mostra como definir a legenda.</span><span class="sxs-lookup"><span data-stu-id="8af0e-120">The following code shows how to set the caption.</span></span>


```
  void CMath_Input_Control_testDlg::OnBnClickedSetCaption()
  {     
    g_spMIC->Hide();
    CComBSTR cap1(L"Some Caption Text");    
    g_spMIC->SetCaptionText((BSTR)cap1);
    g_spMIC->Show();
  }  
  
```



<span data-ttu-id="8af0e-121">A imagem a seguir mostra o controle após a definição da legenda.</span><span class="sxs-lookup"><span data-stu-id="8af0e-121">The following image shows the control after the caption has been set.</span></span>

![controle de entrada matemática com um conjunto de legendas](images/mic-caption.png)

## <a name="changing-the-controls-preview-area-size"></a><span data-ttu-id="8af0e-123">Alterando o tamanho da área de visualização do controle</span><span class="sxs-lookup"><span data-stu-id="8af0e-123">Changing the Control's Preview Area Size</span></span>

<span data-ttu-id="8af0e-124">Você pode personalizar o controle de entrada matemática para que o controle defina explicitamente o tamanho da área de visualização.</span><span class="sxs-lookup"><span data-stu-id="8af0e-124">You can customize the math input control so that the control explicitly sets its preview-area size.</span></span> <span data-ttu-id="8af0e-125">Isso cria uma área maior na qual as fórmulas matemáticas são exibidas.</span><span class="sxs-lookup"><span data-stu-id="8af0e-125">This creates a larger area in which the math formulas are displayed.</span></span> <span data-ttu-id="8af0e-126">O código a seguir mostra como definir o tamanho da área de visualização.</span><span class="sxs-lookup"><span data-stu-id="8af0e-126">The following code shows how to set the preview area size.</span></span>


```
  void CMath_Input_Control_testDlg::OnBnClickedSetPreviewAreaSize()
  {
    LONG height = 200;
    HRESULT hr = S_OK;
    hr = g_spMIC->SetPreviewHeight(height);
  }  
  
```



<span data-ttu-id="8af0e-127">As imagens a seguir mostram um controle com áreas de visualização de tamanhos diferentes.</span><span class="sxs-lookup"><span data-stu-id="8af0e-127">The following images show a control with differently sized preview areas.</span></span>

![controle de entrada matemática com o tamanho da área de visualização padrão](images/mic.png)![controle de entrada matemática com área de visualização maior](images/mic-big-preview.png)

 

 



