---
title: Registro do serviço de texto
description: Além das entradas de registro de servidor no proc padrão, um serviço de texto deve se registrar com a TSF (estrutura de serviços de texto) para que possa estar disponível para uso com um aplicativo.
ms.assetid: 95676067-ab5c-470b-a4be-117ab6810d48
keywords:
- TSF (estrutura de serviços de texto), registro
- TSF (estrutura de serviços de texto), registro
- serviços de texto, registro
- TSF (estrutura de serviços de texto), perfis de idioma
- TSF (estrutura de serviços de texto), perfis de idioma
- serviços de texto, perfis de idioma
- TSF (estrutura de serviços de texto), categorias
- TSF (estrutura de serviços de texto), categorias
- serviços de texto, categorias
- registrando serviços de texto
- registrando perfis de idioma
- registrando categorias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dc1b91ad1a3b1fde9a2e49b92950ce2db4876f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454192"
---
# <a name="text-service-registration"></a>Registro do serviço de texto

Além das entradas de registro de servidor no proc padrão, um serviço de texto deve se registrar com a TSF (estrutura de serviços de texto) para que possa estar disponível para uso com um aplicativo. O TSF fornece a interface [ITfInputProcessorProfiles](/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles) e [ITfCategoryMgr](/windows/desktop/api/msctf/nn-msctf-itfcategorymgr) para simplificar o processo de registro.

Os provedores de serviço de texto também devem fornecer assinaturas digitais com seus executáveis binários. Consulte [introdução à assinatura de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).

## <a name="registering-the-text-service"></a>Registrando o serviço de texto

Um serviço de texto se registra com o TSF chamando [ITfInputProcessorProfiles:: Register](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-register) com o identificador de classe do serviço de texto. Uma instância da interface **ITfInputProcessorProfiles** é obtida chamando **CoCreateInstance** com CLSID \_ TF \_ InputProcessorProfiles.

O exemplo a seguir demonstra como criar um objeto **ITfInputProcessorProfiles** e registrar o serviço de texto.


```C++
BOOL RegisterTextService(CLSID clsidTextService)
{
    HRESULT hr;
    ITfInputProcessorProfiles *pInputProcessProfiles;

    hr = CoCreateInstance(  CLSID_TF_InputProcessorProfiles, 
                            NULL, 
                            CLSCTX_INPROC_SERVER,
                            IID_ITfInputProcessorProfiles, 
                            (LPVOID*)&pInputProcessProfiles);

    if (hr != S_OK)
    {
        return FALSE;
    }

    hr = pInputProcessProfiles->Register(clsidTextService);

    pInputProcessProfiles->Release();
    
    return (S_OK == hr);
}
```



[ITfInputProcessorProfiles:: cancelar registro](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-unregister)

## <a name="registering-language-profiles"></a>Registrando perfis de idioma

Um serviço de texto só está disponível quando um aplicativo tem o foco e o idioma apropriado é selecionado na barra de idiomas. Para facilitar isso, o TSF requer que um serviço de texto se registre em todos os idiomas aos quais ele dá suporte. O serviço de texto registra seus perfis de idioma chamando [ITfInputProcessorProfiles:: AddLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile) com o identificador de classe de serviço de texto, esse identificador de idioma do perfil e um **GUID** de serviço de texto definido que identifica o perfil de idioma.

Um perfil de idioma pode ser removido chamando [ITfInputProcessorProfiles:: RemoveLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-removelanguageprofile). **ITfInputProcessorProfiles:: Unregister** remove todos os perfis de idioma para o serviço de texto; Quando um serviço de texto é desinstalado, ele requer a remoção dos perfis de idioma individuais.

## <a name="registering-categories"></a>Registrando categorias

Um serviço de texto também deve registrar a categoria à qual o serviço de texto se aplica. Por exemplo, se o serviço de texto fornece informações de atributo de exibição, ele deve se registrar como um provedor de atributo de exibição chamando [ITfCategoryMgr:: RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) com o identificador de classe do serviço de texto para o primeiro parâmetro, GUID \_ TFCAT \_ DISPLAYATTRIBUTEPROVIDER para o segundo parâmetro e o identificador de classe do serviço de texto novamente para o terceiro parâmetro. As categorias possíveis são listadas em [valores de categoria predefinidos](predefined-category-values.md).

Remova as categorias registradas anteriormente chamando [ITfCategoryMgr:: UnregisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-unregistercategory). ITfInputProcessorProfiles:: Unregister remove todas as categorias para o serviço de texto; Quando um serviço de texto é desinstalado, ele deve remover as categorias individuais.

 

 