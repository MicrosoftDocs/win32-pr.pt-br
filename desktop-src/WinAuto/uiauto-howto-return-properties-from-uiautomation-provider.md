---
title: Como retornar propriedades de um provedor de automação de interface do usuário
description: Este tópico contém um código de exemplo que mostra como um provedor de automação de interface do usuário da Microsoft retorna propriedades de um elemento de interface do usuário para aplicativos cliente.
ms.assetid: 6932de16-5548-4aa3-9f29-5daa57bb202b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4133a53df3c59e6d5c93b1c9cd8e6aa942b4bd56
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366071"
---
# <a name="how-to-return-properties-from-a-ui-automation-provider"></a>Como retornar propriedades de um provedor de automação de interface do usuário

Este tópico contém um código de exemplo que mostra como um provedor de automação de interface do usuário da Microsoft retorna propriedades de um elemento de interface do usuário para aplicativos cliente.

Para recuperar um valor de Propriedade do provedor, a automação da interface do usuário chama a implementação de um provedor do método [**IRawElementProviderSimple:: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) , passando a ID da propriedade a ser recuperada e um ponteiro para uma estrutura de [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) . Se o provedor oferecer suporte à propriedade especificada, ele copiará o tipo de dados e o valor da propriedade na estrutura de **variantes** . Se a propriedade não for suportada, o provedor definirá o membro **VT** da estrutura **Variant** como VT \_ vazio.


```C++
IFACEMETHODIMP Provider::GetPropertyValue(PROPERTYID propertyId, VARIANT* pRetVal)
{
    // The Name property is typically the same as the Caption property of the 
    // control window, if it has one. Here, the Name is overridden for the 
    // sake of illustration. 
    if (propertyId == UIA_NamePropertyId) 
    {
        pRetVal->vt = VT_BSTR;
        pRetVal->bstrVal = SysAllocString(L"Custom button");
    }
    
    else if (propertyId == UIA_ControlTypePropertyId) 
    {
        pRetVal->vt = VT_I4;
        pRetVal->lVal = UIA_ButtonControlTypeId; 
    }

    else if (propertyId == UIA_IsContentElementPropertyId) 
    {
        pRetVal->vt = VT_BOOL;
        pRetVal->lVal = TRUE; 
    }

    else if (propertyId == UIA_IsControlElementPropertyId) 
    {
        pRetVal->vt = VT_BOOL;
        pRetVal->lVal = TRUE; 
    }

    //
    // Return other properties as appropriate for the control type. 
    //

    else
    {
        pRetVal->vt = VT_EMPTY;
        // UI Automation will attempt to get the property from the  
        // provider for window that hosts the control.
    }
    return S_OK;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão geral das propriedades de automação da interface do usuário](uiauto-propertiesoverview.md)
</dt> <dt>

[Tópicos de instruções para provedores de automação de interface do usuário](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 