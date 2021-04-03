---
title: Solicitando um objeto para uma interface
description: Solicitando um objeto para uma interface
ms.assetid: 04296372-4897-426e-9be3-e6862a530ac6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3fa740f0ef770e069ee03b644bbfcb9b2c5e0eb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007557"
---
# <a name="asking-an-object-for-an-interface"></a>Solicitando um objeto para uma interface

Vimos anteriormente que um objeto pode implementar mais de uma interface. O objeto de caixa de diálogo de item comum é um exemplo do mundo real disso. Para dar suporte aos usos mais comuns, o objeto implementa a interface [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) . Essa interface define métodos básicos para exibir a caixa de diálogo e obter informações sobre o arquivo selecionado. No entanto, para uso mais avançado, o objeto também implementa uma interface chamada [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize). Um programa pode usar essa interface para personalizar a aparência e o comportamento da caixa de diálogo, adicionando novos controles de interface do usuário.

Lembre-se de que cada interface COM deve herdar, direta ou indiretamente, da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . O diagrama a seguir mostra a herança do objeto de caixa de diálogo de item comum.

![diagrama que mostra interfaces expostas pelo objeto de caixa de diálogo de item comum](images/com06.png)

Como você pode ver no diagrama, o ancestral direto de [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) é a interface [**IFileDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog) , que por sua vez herda [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow). À medida que você passa a cadeia de herança de **IFileOpenDialog** para **IModalWindow**, as interfaces definem a funcionalidade de janela cada vez mais generalizada. Por fim, a interface **IModalWindow** herda [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown). O objeto de caixa de diálogo de item comum também implementa [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize), que existe em uma cadeia de herança separada.

Agora suponha que você tenha um ponteiro para a interface [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) . Como você obteria um ponteiro para a interface [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) ?

![diagrama que mostra dois ponteiros de interface para interfaces no mesmo objeto](images/com07.png)

Simplesmente converter o ponteiro [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) para um ponteiro [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) não funcionará. Não há uma maneira confiável de "conversão cruzada" em uma hierarquia de herança, sem alguma forma de RTTI (informações de tipo em tempo de execução), que é um recurso dependente de linguagem.

A abordagem COM é *pedir* ao objeto que lhe dê um ponteiro [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) , usando a primeira interface como um canal no objeto. Isso é feito chamando o método [**IUnknown:: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) do primeiro ponteiro de interface. Você pode considerar **QueryInterface** como uma versão independente de idioma da palavra-chave **Dynamic \_ Cast** em C++.

O método [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) tem a seguinte assinatura:

``` syntax
HRESULT QueryInterface(REFIID riid, void **ppvObject);
```

Com base no que você já conhece sobre [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance), talvez seja possível adivinhar o funcionamento de [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .

-   O parâmetro *riid* é o GUID que identifica a interface que você está solicitando. O tipo de dados **REFIID** é um **typedef** para `const GUID&` . Observe que o CLSID (identificador de classe) não é necessário, pois o objeto já foi criado. Somente o identificador de interface é necessário.
-   O parâmetro *ppvObject* recebe um ponteiro para a interface. O tipo de dados desse parâmetro é **void \* \***, pelo mesmo motivo que [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) usa este tipo de dados: [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pode ser usado para consultar qualquer interface com, portanto, o parâmetro não pode ser fortemente tipado.

Aqui está como você chamaria [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter um ponteiro [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) :


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



Como sempre, verifique o valor de retorno **HRESULT** , caso o método falhe. Se o método tiver sucesso, você deverá chamar [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) quando terminar de usar o ponteiro, conforme descrito em [Gerenciando o tempo de vida de um objeto](managing-the-lifetime-of-an-object.md).

## <a name="next"></a>Avançar

[Alocação de memória em COM](memory-allocation-in-com.md)

 

 