---
description: Para obter controle mais detalhado sobre o comportamento de preenchimento automático ou para adicionar uma fonte personalizada de cadeias de caracteres de preenchimento automático, você deve gerenciar o objeto de AutoCompletar por conta própria.
ms.assetid: E1A7B1B0-2879-452E-9EBB-73F02B932200
title: Como habilitar o preenchimento automático manualmente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee4b327c6ccdd62fd921c56cfb046edb8527bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967905"
---
# <a name="how-to-enable-autocomplete-manually"></a>Como habilitar o preenchimento automático manualmente

Para obter controle mais detalhado sobre o comportamento de preenchimento automático ou para adicionar uma fonte personalizada de cadeias de caracteres de preenchimento automático, você deve gerenciar o objeto de AutoCompletar por conta própria. Você pode habilitar o preenchimento automático manualmente das seguintes maneiras.

## <a name="instructions"></a>Instruções

### <a name="creating-a-simple-autocomplete-object"></a>Criando um objeto de preenchimento automático simples

As etapas a seguir mostram como criar e inicializar um objeto de preenchimento automático simples. Um objeto de preenchimento automático simples conclui as cadeias de caracteres de uma única fonte. A verificação de erros foi omitida intencionalmente neste exemplo.

1.  Crie o objeto de preenchimento automático.

    ```C++
    IAutoComplete *pac;

    HRESULT hr = CoCreateInstance(CLSID_AutoComplete, 
                                    NULL, 
                                  CLSCTX_INPROC_SERVER,
                                  IID_PPV_ARGS(&pac));
    ```

    

2.  Crie a origem de AutoCompletar. Você pode usar uma [fonte de preenchimento automático predefinida](ac-ovw.md) ou pode escrever sua própria fonte personalizada.

    O código a seguir usa uma das fontes de preenchimento automático predefinidas.

    ```C++
    IUnknown *punkSource;

    hr = CoCreateInstance(CLSID_ACListISF, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&punkSource));
    ```

    

    O código a seguir usa uma fonte de preenchimento automático personalizada. Você pode escrever sua própria fonte de preenchimento automático implementando um objeto que expõe a interface [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring) . O objeto também pode implementar, opcionalmente, as interfaces [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) e [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) .

    ```C++
    CCustomAutoCompleteSource *pcacs = new CCustomAutoCompleteSource();

    hr = pcacs->QueryInterface(IID_PPV_ARGS(&punkSource));
    if(SUCCEEDED(hr))
    {
        // ...
    }

    pcacs->Release();
    ```

    

3.  Defina as opções na fonte de preenchimento automático (opcional).

    Você pode personalizar o comportamento da fonte de preenchimento automático definindo suas opções se a origem expõe a interface [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) . Ao usar as fontes de preenchimento automático predefinidas, somente o CLSID \_ ACListISF exporta **IACList2**. Para obter uma lista completa de opções e seus valores, consulte [**IACList2:: SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).

    ```C++
    IACList2 *pal2;

    hr = punkSource->QueryInterface(IID_PPV_ARGS(&pal2));
    if (SUCCEEDED(hr))
    {
        hr = pal2->SetOptions(ACLO_FILESYSONLY);
        pal2->Release();
    }
    ```

    

4.  Inicialize o objeto de preenchimento automático.

    Neste exemplo, **hwndEdit** é o identificador da janela de controle de edição para a qual o preenchimento automático deve ser habilitado. Consulte [**IAutoComplete:: init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init) para obter uma descrição dos dois parâmetros finais não utilizados.

    ```C++
    hr = pac->Init(hwndEdit, punkSource, NULL, NULL);
    ```

    

5.  Defina as opções do objeto preenchimento automático (opcional).

    Você pode personalizar o comportamento do objeto de preenchimento automático definindo suas opções. Para obter uma lista completa de opções e seus valores, consulte a documentação para [**IACList2:: SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).

    ```C++
    IAutoComplete2 *pac2;

    hr = pac->QueryInterface(IID_PPV_ARGS(&pac2));

    if (SUCCEEDED(hr))
    {
        hr = pac2->SetOptions(ACO_AUTOSUGGEST);
        pac2->Release();
    }
    ```

    

6.  Libere os objetos.

    > [!Note]  
    > O objeto de preenchimento automático permanece anexado ao controle de edição mesmo depois que você o libera. Se você pretender ter a necessidade de acessar esses objetos mais tarde — se quiser alterar as opções de preenchimento automático posteriormente, por exemplo, não é necessário liberá-las neste ponto.

     

    ```C++
    punkSource->Release();
    pac->Release();
    ```

    

### <a name="creating-a-compound-autocomplete-object"></a>Criando um objeto de preenchimento automático composto

Um objeto de preenchimento automático composto corresponde A cadeias de caracteres de várias fontes. Por exemplo, a barra de endereços do Windows Internet Explorer usa um objeto de preenchimento automático composto, pois o usuário pode começar a digitar o nome de um arquivo ou uma URL. A maioria das etapas envolvidas na criação de um objeto de preenchimento automático composto é idêntica às etapas em "criando um objeto de AutoCompletamento simples". Essas etapas são indicadas como tal.

1.  Crie o objeto de preenchimento automático. Isso é o mesmo que a etapa 1 acima.

2.  Crie o Gerenciador de objetos de fonte composta de preenchimento automático.

    O objeto de fonte composta de preenchimento automático permite que várias fontes de preenchimento automático sejam combinadas em uma única origem de AutoCompletar.

    ```C++
    IObjMgr *pom;

    hr = CoCreateInstance(CLSID_ACLMulti, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&pom));
    ```

    

3.  Crie e defina opções para cada uma das fontes de preenchimento automático. Repita as etapas 2 e 3 acima para cada fonte.

4.  Anexe cada fonte de preenchimento automático ao Gerenciador de objetos de origem.

    ```C++
    hr = pom->Append(punkSource1);
    hr = pom->Append(punkSource2);
    ```

    

5.  Inicialize o objeto de preenchimento automático.

    Isso é o mesmo que a etapa 4 acima, exceto que, em vez de passar a fonte de AutoCompletar simples para [**IAutoComplete:: init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init), você passa o Gerenciador de objetos de origem composto.

    ```C++
    hr = pac->Init(hwndEdit, pom, NULL, NULL);
    ```

    

6.  Defina as opções do objeto preenchimento automático. Isso é o mesmo que a etapa 5 acima.

7.  Libere os objetos.

    Como no caso simples, você pode liberar os objetos assim que terminar de usá-los, mas também poderá mantê-los para alterar as opções posteriormente.

    ```C++
    pac->Release();
    pom->Release();

    // Release each individual source.
    punkSource1->Release(); 
    punkSource2->Release();
    ```

    

 

 
