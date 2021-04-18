---
description: Impede comportamentos de gestos de borda quando uma janela de aplicativo está ativa e no modo de tela inteira (ou uma janela de propriedade está ativa).
ms.assetid: F4242C05-181B-44FC-BE6C-8ABB76079981
title: System. EdgeGesture. DisableTouchWhenFullscreen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 208962f11b96420a8e0ef771ada846a3f802e815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756499"
---
# <a name="systemedgegesturedisabletouchwhenfullscreen"></a><span data-ttu-id="10af2-103">System. EdgeGesture. DisableTouchWhenFullscreen</span><span class="sxs-lookup"><span data-stu-id="10af2-103">System.EdgeGesture.DisableTouchWhenFullscreen</span></span>

<span data-ttu-id="10af2-104">Impede comportamentos de gestos de borda quando uma janela de aplicativo está ativa e no modo de tela inteira (ou uma janela de propriedade está ativa).</span><span class="sxs-lookup"><span data-stu-id="10af2-104">Prevents edge gesture behaviors when an application window is active and in full-screen mode (or an owned window is active).</span></span>

> [!Note]  
> <span data-ttu-id="10af2-105">No modo de tela inteira, o tamanho da janela do aplicativo corresponde à resolução da tela.</span><span class="sxs-lookup"><span data-stu-id="10af2-105">In full-screen mode, the size of the application window matches the screen resolution.</span></span>

 

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="10af2-106">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="10af2-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.EdgeGesture.DisableTouchWhenFullscreen
   shellPKey = PKEY_EdgeGesture_DisableTouchWhenFullscreen
   formatID = 32CE38B2-2C9A-41B1-9BC5-B3784394AA44
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a><span data-ttu-id="10af2-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="10af2-107">Remarks</span></span>

<span data-ttu-id="10af2-108">No Windows 8, as interações de usuário com as bordas da tela exibem a interface do usuário do sistema, como barras de aplicativo, botões e aplicativos em execução.</span><span class="sxs-lookup"><span data-stu-id="10af2-108">In Windows 8, user interactions with the edges of the screen display system UI such as app bars, charms, and running apps.</span></span>

<span data-ttu-id="10af2-109">Para aplicativos remotos de tela inteira, esse comportamento de interface do usuário no computador local pode substituir e interferir na interface do usuário da sessão remota.</span><span class="sxs-lookup"><span data-stu-id="10af2-109">For full-screen, remote applications, this UI behavior on the local machine might override and interfere with the UI of the remote session.</span></span> <span data-ttu-id="10af2-110">Essa propriedade permite que um aplicativo desabilite a interface do usuário do Edge no computador local.</span><span class="sxs-lookup"><span data-stu-id="10af2-110">This property enables an application to disable the edge UI on the local machine.</span></span>

<span data-ttu-id="10af2-111">Para desabilitar a interface do usuário do Edge, defina essa propriedade como VARIANT \_ true.</span><span class="sxs-lookup"><span data-stu-id="10af2-111">To disable edge UI, set this property to VARIANT\_TRUE.</span></span> <span data-ttu-id="10af2-112">O valor padrão é VARIANT \_ false.</span><span class="sxs-lookup"><span data-stu-id="10af2-112">The default value is VARIANT\_FALSE.</span></span>

<span data-ttu-id="10af2-113">Esta propriedade não tem nenhum efeito nos aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="10af2-113">This property has no effect on Windows Store apps.</span></span>

<span data-ttu-id="10af2-114">O exemplo a seguir mostra como definir os comportamentos da interface do usuário do Edge.</span><span class="sxs-lookup"><span data-stu-id="10af2-114">The following example shows how to set edge UI behaviors.</span></span>


```
HRESULT SetTouchDisableProperty(HWND hwnd, BOOL fDisableTouch)
{
    IPropertyStore* pPropStore;
    HRESULT hrReturnValue = SHGetPropertyStoreForWindow(hwnd, IID_PPV_ARGS(&pPropStore));
    if (SUCCEEDED(hrReturnValue))
    {
        PROPVARIANT var;
        var.vt = VT_BOOL;
        var.boolVal = fDisableTouch ? VARIANT_TRUE : VARIANT_FALSE;
        hrReturnValue = pPropStore->SetValue(PKEY_EdgeGesture_DisableTouchWhenFullscreen, var);
        pPropStore->Release();
    }
    return hrReturnValue;
}
```



## <a name="related-topics"></a><span data-ttu-id="10af2-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="10af2-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10af2-116">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="10af2-116">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="10af2-117">searchInfo</span><span class="sxs-lookup"><span data-stu-id="10af2-117">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="10af2-118">typeInfo</span><span class="sxs-lookup"><span data-stu-id="10af2-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> </dl>

 

 
