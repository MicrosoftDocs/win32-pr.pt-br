---
title: Solicitando uma interface a um objeto
description: Solicitando uma interface a um objeto
ms.assetid: 04296372-4897-426e-9be3-e6862a530ac6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a173342c7dba59c09cdef05c6b20d9d4d37da9d6971e6a7c26c1787b708121bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680727"
---
# <a name="asking-an-object-for-an-interface"></a>Solicitando uma interface a um objeto

Vimos anteriormente que um objeto pode implementar mais de uma interface. O objeto Common Item Dialog é um exemplo do mundo real. Para dar suporte aos usos mais típicos, o objeto implementa a interface [**IFileOpenDialog.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) Essa interface define métodos básicos para exibir a caixa de diálogo e obter informações sobre o arquivo selecionado. Para uso mais avançado, no entanto, o objeto também implementa uma interface chamada [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize). Um programa pode usar essa interface para personalizar a aparência e o comportamento da caixa de diálogo, adicionando novos controles de interface do usuário.

Lembre-se de que cada interface COM deve herdar, direta ou indiretamente, da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) O diagrama a seguir mostra a herança do objeto Common Item Dialog.

![diagrama que mostra interfaces expostas pelo objeto de diálogo de item comum](images/com06.png)

Como você pode ver no diagrama, o ancestral direto de [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) é a interface [**IFileDialog,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog) que, por sua vez, herda [**IModalWindow.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow) Conforme você aumenta a cadeia de herança de **IFileOpenDialog para** **IModalWindow,** as interfaces definem a funcionalidade de janela cada vez mais generalizada. Por fim, a interface **IModalWindow** herda [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown). O objeto Common Item Dialog também implementa [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize), que existe em uma cadeia de herança separada.

Agora suponha que você tenha um ponteiro para a interface [**IFileOpenDialog.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) Como obter um ponteiro para a interface [**IFileDialogCustomize?**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize)

![diagrama que mostra dois ponteiros de interface para interfaces no mesmo objeto](images/com07.png)

Simplesmente a seleção [**do ponteiro IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) em [**um ponteiro IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) não funcionará. Não há nenhuma maneira confiável de "translagem cruzada" em uma hierarquia de herança, sem alguma forma de RTTI (informações de tipo de tempo de run-time), que é um recurso altamente dependente de idioma.

A abordagem COM é *solicitar* que o objeto lhe dê um ponteiro [**IFileDialogCustomize,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) usando a primeira interface como um canal para o objeto. Isso é feito chamando o [**método IUnknown::QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) do primeiro ponteiro de interface. Você pode pensar em **QueryInterface** como uma versão independente de linguagem da palavra-chave **de \_ cast** dinâmica em C++.

O [**método QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) tem a seguinte assinatura:

``` syntax
HRESULT QueryInterface(REFIID riid, void **ppvObject);
```

Com base no que você já sabe sobre [**CoCreateInstance,**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)talvez seja possível adivinhar como [**o QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) funciona.

-   O *parâmetro riid* é o GUID que identifica a interface que você está solicitando. O tipo de **dados REFIID** é **um typedef** para `const GUID&` . Observe que o CLSID (identificador de classe) não é necessário, porque o objeto já foi criado. Somente o identificador de interface é necessário.
-   O *parâmetro ppvObject* recebe um ponteiro para a interface . O tipo de dados desse parâmetro é nulo , pelo mesmo motivo pelo qual [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) usa esse tipo de dados: [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pode ser usado para consultar qualquer interface COM, portanto, o parâmetro não pode ser fortemente digitado. **\* \***

Veja como você chamaria [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter um [**ponteiro IFileDialogCustomize:**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize)


```C++
hr = pFileOpen->QueryInterface(IID_IFileDialogCustomize, 
    reinterpret_cast<void**>(&pCustom));
if (SUCCEEDED(hr))
{
    // Use the interface. (Not shown.)
    // ...

    pCustom->Release();
}
else
{
    // Handle the error.
}
```



Como sempre, verifique o **valor de retorno HRESULT,** caso o método falhe. Se o método for bem-sucedido, você deverá chamar Release quando terminar de usar o ponteiro , conforme descrito em Gerenciando o tempo de vida [de um objeto](managing-the-lifetime-of-an-object.md). [](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)

## <a name="next"></a>Avançar

[Alocação de memória em COM](memory-allocation-in-com.md)

 

 