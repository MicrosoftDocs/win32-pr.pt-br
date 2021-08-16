---
title: Como usar GUIDs do TOM
description: GUIDs do TOM (Text Object Model) são fornecidas em Tom.h dentro das instruções MIDL \_ INTERFACE. Para usar as interfaces associadas, primeiro você deve declarar a interface usando o GUID.
ms.assetid: 48FF98C9-D42E-4E7F-874F-8E56F730E24E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c5c892ecac4b13a6e74aedad6c2a373908d2173c105ab0dbb0ec49c1439c36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828527"
---
# <a name="how-to-use-tom-guids"></a>Como usar GUIDs do TOM

GUIDs do TOM (Text Object Model) são fornecidas em Tom.h dentro das instruções MIDL \_ INTERFACE. Para usar as interfaces associadas, primeiro você deve declarar a interface usando o GUID.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções

### <a name="use-a-tom-guid"></a>Usar um GUID do TOM

O código de exemplo a seguir demonstra como usar a interface [**ITextDocument.**](/windows/desktop/api/Tom/nn-tom-itextdocument)


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

[Usando controles de edição rich](using-rich-edit-controls.md)
</dt> <dt>

[Windows demonstração de controles comuns (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




