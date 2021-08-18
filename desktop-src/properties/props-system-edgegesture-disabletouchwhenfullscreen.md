---
description: Impede comportamentos de gesto de borda quando uma janela do aplicativo está ativa e no modo de tela inteira (ou uma janela de propriedade está ativa).
ms.assetid: F4242C05-181B-44FC-BE6C-8ABB76079981
title: System.EdgeGesture.DisableTouchWhenFullscreen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13132ba30fd3f1e594ec54966dfe2268ce66d570b66ca6d34b1c63b03bfc0c75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119845116"
---
# <a name="systemedgegesturedisabletouchwhenfullscreen"></a>System.EdgeGesture.DisableTouchWhenFullscreen

Impede comportamentos de gesto de borda quando uma janela do aplicativo está ativa e no modo de tela inteira (ou uma janela de propriedade está ativa).

> [!Note]  
> No modo de tela inteira, o tamanho da janela do aplicativo corresponde à resolução da tela.

 

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8

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

## <a name="remarks"></a>Comentários

No Windows 8, as interações do usuário com as bordas da tela exibem a interface do usuário do sistema, como barras de aplicativo, charms e aplicativos em execução.

Para aplicativos remotos de tela inteira, esse comportamento de interface do usuário no computador local pode substituir e interferir na interface do usuário da sessão remota. Essa propriedade permite que um aplicativo desabilite a interface do usuário de borda no computador local.

Para desabilitar a interface do usuário de borda, de definir essa propriedade como VARIANT \_ TRUE. O valor padrão é VARIANT \_ FALSE.

Essa propriedade não tem nenhum efeito sobre os Windows Store.

O exemplo a seguir mostra como definir comportamentos de interface do usuário de borda.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propertydescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[Typeinfo](./propdesc-schema-typeinfo.md)
</dt> </dl>

 

 
