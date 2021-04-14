---
title: Como usar as GUIDs de TOM
description: Os GUIDs de TOM (modelo de objeto de texto) são fornecidos em Tom. h dentro das \_ instruções da interface MIDL. Para usar as interfaces associadas, primeiro você deve declarar a interface usando o GUID.
ms.assetid: 48FF98C9-D42E-4E7F-874F-8E56F730E24E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9c937d8b3c3612a3a49f27f18ac7c392b7a596
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "104453898"
---
# <a name="how-to-use-tom-guids"></a>Como usar as GUIDs de TOM

Os GUIDs de TOM (modelo de objeto de texto) são fornecidos em Tom. h dentro das \_ instruções da interface MIDL. Para usar as interfaces associadas, primeiro você deve declarar a interface usando o GUID.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="use-a-tom-guid"></a>Usar uma GUID de TOM

O código de exemplo a seguir demonstra como usar a interface [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) .


```C++
#define DEFINE_GUIDXXX(name, l, w1, w2, b1, b2, b3, b4, b5, b6, b7, b8) \
        EXTERN_C const GUID CDECL name \
                = { l, w1, w2, { b1, b2,  b3,  b4,  b5,  b6,  b7,  b8 } }

DEFINE_GUIDXXX(IID_ITextDocument,0x8CC497C0,0xA1DF,0x11CE,0x80,0x98,
                0x00,0xAA,0x00,0x47,0xBE,0x5D);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o modelo de objeto de texto](using-the-text-object-model.md)
</dt> <dt>

[Usando controles de edição avançados](using-rich-edit-controls.md)
</dt> <dt>

[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




