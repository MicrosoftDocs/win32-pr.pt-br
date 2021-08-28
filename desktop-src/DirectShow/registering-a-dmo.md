---
description: Registrando um DMO
ms.assetid: 9f74fc1c-b903-4725-b667-3c56a2726dbc
title: Registrando um DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab5635f7b05edb13da80adb62104db5c412fa55608ec2f9b5214380b7d9a095e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904536"
---
# <a name="registering-a-dmo"></a>Registrando um DMO

Para que os clientes usem seu DMO, o CLSID deve ser registrado no sistema do usuário. Isso é feito por meio da função **DllRegisterServer da DLL.** Se você estiver usando o Active Template Library (ATL), o assistente da ATL gerará automaticamente essa função.

Você também pode registrar seu DMO em uma ou mais categorias DMO padrão. Isso permite que os clientes descubram sua DMO usando a [**função DMOEnum.**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) As categorias são definidas por GUID e são listadas na seção [DMO GUIDs](dmo-guids.md).

Registrar um DMO em uma categoria é opcional. Para fazer isso, chame a [**função DMORegister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) e especifique o nome amigável do DMO, o CLSID e a categoria. Opcionalmente, você também pode registrar um conjunto de tipos de mídia aos quais seus DMOs são compatíveis. Para obter mais informações, consulte [DMO tipos de mídia](dmo-media-types.md).

O exemplo a seguir mostra como registrar um efeito de áudio DMO que dá suporte à entrada e à saída de áudio PCM. Nesse caso, os tipos de entrada e os tipos de saída são os mesmos.


```C++
STDAPI DllRegisterServer(void)
{
    // Register the DMO as a PCM audio effect DMO
    DMO_PARTIAL_MEDIATYPE mt;
    mt.type    = MEDIATYPE_Audio;
    mt.subtype = MEDIASUBTYPE_PCM;
    HRESULT hr = DMORegister(
        L"MyDMO",                  // Friendly name
        CLSID_MyDMO,               // CLSID
        DMOCATEGORY_AUDIO_EFFECT,  // Category
        0,                         // Flags 
        1,                         // Number of input types
        &mt,                       // Array of input types
        1,                         // Number of output types
        &mt);                      // Array of output types

    if (FAILED(hr)) return hr;

    // Registers the object, with no typelib.
    return _Module.RegisterServer(FALSE);
}
```



Este exemplo pressu que a ATL foi usada para criar o projeto; a última linha da função chama o método ATL padrão para registrar o servidor COM. Se você não estiver usando a ATL, sua função terá uma aparência diferente.

**Não registro de um DMO**

Sua **função DllUnregisterServer** deve remover as entradas do Registro criadas pela função **DllRegisterServer.** Se você chamar **DMORegister** ao registrar o DMO, deverá [**DMOUnregister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister) com a mesma categoria quando você não registrar o DMO.

O exemplo a seguir remove as entradas do Registro criadas no exemplo anterior:


```C++
STDAPI DllUnregisterServer(void)
{
    DMOUnregister(CLSID_MyDMO, DMOCATEGORY_AUDIO_EFFECT);
    return _Module.UnregisterServer(TRUE);
}
```



**DirectShow Valores de Valores de Valor**

Para fins de criação de grafos de filtro, DirectShow atribui um valor de valor de valor padrão a DMOs. Você pode substituir esse valor adicionando uma entrada do Registro à chave do registro DMO do usuário em CLSID RAIZ de \_ CLASSES \_ \\ HKEY. Inclua um **valor DWORD** chamado `Merit` cujo valor especifica o valor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Escrevendo um DMO](writing-a-dmo.md)
</dt> </dl>

 

 



