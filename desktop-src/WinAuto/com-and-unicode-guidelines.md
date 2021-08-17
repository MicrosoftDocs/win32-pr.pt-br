---
title: Diretrizes COM e Unicode
description: Como Microsoft Active Accessibility baseia-se no COM (Component Object Model), os desenvolvedores precisam de um nível moderado de compreensão sobre objetos e interfaces COM e devem saber como executar tarefas básicas (por exemplo, como inicializar a biblioteca COM).
ms.assetid: ed4bbef9-676a-4f4e-926a-044f71399c56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023b1d58a1a31997142097d02d8fc7d80881111e08f0020d967c1984d9946c57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133899"
---
# <a name="com-and-unicode-guidelines"></a>Diretrizes COM e Unicode

Como Microsoft Active Accessibility baseia-se no COM (Component Object Model), os desenvolvedores precisam de um nível moderado de compreensão sobre objetos e interfaces COM e devem saber como executar tarefas básicas (por exemplo, como inicializar a biblioteca COM). Os desenvolvedores de servidores precisam entender como criar classes que implementam a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e como criar objetos acessíveis.

Você também precisa de um nível moderado de compreensão sobre Unicode para usar muitas das funções Microsoft Active Accessibility que retornam cadeias de caracteres.

Para usar Microsoft Active Accessibility, você deve entender as seguintes funções, estruturas, tipos de dados e interfaces COM e Unicode a seguir. Informações limitadas sobre alguns desses itens são fornecidas nesta documentação.

### <a name="functions"></a>Funções:

-   [**Oleinitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize)
-   [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [ **CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)
-   [**IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) e [ **IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)
-   [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) e [ **VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)
-   [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) e [ **WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)
-   [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) e [ **SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)

### <a name="structures-and-data-types"></a>Estruturas e tipos de dados:

-   [**Variante**](variant-structure.md)
-   [**Hresult**](/windows/desktop/com/structure-of-com-error-codes)
-   [**BSTR**](/previous-versions/windows/desktop/automat/bstr)

### <a name="com-interfaces"></a>Interfaces COM:

-   [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)
-   [**IDispatch**](idispatch-interface.md)
-   [**Ienumvariant**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant)

## <a name="in-this-section"></a>Nesta seção

-   [Estrutura VARIANT](variant-structure.md)
-   [IDispatch Interface](idispatch-interface.md)
-   [Convertendo cadeias de caracteres Unicode e ANSI](converting-unicode-and-ansi-strings.md)

 

 