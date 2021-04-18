---
title: Diretrizes de COM e Unicode
description: Como o Microsoft Acessibilidade Ativa se baseia em Component Object Model (COM), os desenvolvedores precisam de um nível moderado de compreensão sobre objetos e interfaces COM e devem saber como executar tarefas básicas (por exemplo, como inicializar a biblioteca COM).
ms.assetid: ed4bbef9-676a-4f4e-926a-044f71399c56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2312b6177891c31c0987b846f7adfc1aa08abc7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105772610"
---
# <a name="com-and-unicode-guidelines"></a>Diretrizes de COM e Unicode

Como o Microsoft Acessibilidade Ativa se baseia em Component Object Model (COM), os desenvolvedores precisam de um nível moderado de compreensão sobre objetos e interfaces COM e devem saber como executar tarefas básicas (por exemplo, como inicializar a biblioteca COM). Os desenvolvedores de servidor precisam entender como projetar classes que implementam a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e como criar objetos acessíveis.

Você também precisa de um nível moderado de compreensão sobre o Unicode para usar muitas das funções do Microsoft Acessibilidade Ativa que retornam cadeias de caracteres.

Para usar o Microsoft Acessibilidade Ativa com eficiência, você deve entender as seguintes funções e estruturas de COM e Unicode, estrutura, tipos de dados e interfaces. Informações limitadas sobre alguns desses itens são fornecidas nesta documentação.

### <a name="functions"></a>Funções:

-   [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize)
-   [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [ **CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)
-   [**IUnknown:: AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) e [ **IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)
-   [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) e [ **VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)
-   [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) e [ **WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)
-   [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) e [ **SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)

### <a name="structures-and-data-types"></a>Estruturas e tipos de dados:

-   [**VARIANTE**](variant-structure.md)
-   [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)
-   [**BSTR**](/previous-versions/windows/desktop/automat/bstr)

### <a name="com-interfaces"></a>Interfaces COM:

-   [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)
-   [**IDispatch**](idispatch-interface.md)
-   [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant)

## <a name="in-this-section"></a>Nesta seção

-   [Estrutura de variante](variant-structure.md)
-   [Interface IDispatch](idispatch-interface.md)
-   [Convertendo cadeias de caracteres Unicode e ANSI](converting-unicode-and-ansi-strings.md)

 

 