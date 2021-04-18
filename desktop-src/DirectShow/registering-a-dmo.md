---
description: Registrando um DMO
ms.assetid: 9f74fc1c-b903-4725-b667-3c56a2726dbc
title: Registrando um DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c5364304fd5f6a9557c84a4b27c86d29fa4e84
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105757871"
---
# <a name="registering-a-dmo"></a>Registrando um DMO

Para que os clientes usem o DMO, o CLSID deve ser registrado no sistema do usuário. Isso é feito por meio da função **DllRegisterServer** da dll. Se você estiver usando o Active Template Library (ATL), o assistente ATL gerará automaticamente essa função.

Você também pode registrar o DMO em uma ou mais categorias de DMO padrão. Isso permite que os clientes descubram o DMO usando a função [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) . As categorias são definidas por GUID e são listadas na seção [GUIDs de DMO](dmo-guids.md).

O registro de um DMO em uma categoria é opcional. Para fazer isso, chame a função [**DMORegister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) e especifique o nome amigável do DMO, CLSID e a categoria. Opcionalmente, você também pode registrar um conjunto de tipos de mídia aos quais seu DMOs dá suporte. Para obter mais informações, consulte [tipos de mídia DMO](dmo-media-types.md).

O exemplo a seguir mostra como registrar um efeito de áudio DMO que dá suporte a entrada e saída de áudio PCM. Nesse caso, os tipos de entrada e os tipos de saída são os mesmos.


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



Este exemplo supõe que a ATL foi usada para criar o projeto; a última linha da função chama o método ATL padrão para registrar o servidor COM. Se você não estiver usando a ATL, sua função terá uma aparência diferente.

**Cancelando o registro de um DMO**

Sua função **DllUnregisterServer** deve remover todas as entradas do registro que a função **DllRegisterServer** cria. Se você chamar **DMORegister** ao registrar o DMO, deverá [**DMOUnregister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister) com a mesma categoria ao cancelar o registro do DMO.

O exemplo a seguir remove as entradas do registro criadas no exemplo anterior:


```C++
STDAPI DllUnregisterServer(void)
{
    DMOUnregister(CLSID_MyDMO, DMOCATEGORY_AUDIO_EFFECT);
    return _Module.UnregisterServer(TRUE);
}
```



**Valores de mérito do DirectShow**

Para fins de criação de gráficos de filtro, o DirectShow atribui um valor de mérito padrão a DMOs. Você pode substituir esse valor adicionando uma entrada de registro à chave do registro do DMO em \_ classe HKEY \_ raiz \\ CLSID. Inclua um valor **DWORD** chamado `Merit` cujo valor especifique o mérito.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Escrevendo um DMO](writing-a-dmo.md)
</dt> </dl>

 

 



