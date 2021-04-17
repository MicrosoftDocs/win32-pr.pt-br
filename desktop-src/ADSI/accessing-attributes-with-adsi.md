---
title: Acessando atributos com ADSI
description: Os métodos IADs. Get e IADs. GetEx são usados para recuperar valores de atributo nomeados.
ms.assetid: 8aa139e1-6b20-4745-92f1-d2f352071f33
ms.tgt_platform: multiple
keywords:
- Atributos, acessando com ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ee6990483b45e335bb6b830cef85e482f30e00
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105749124"
---
# <a name="accessing-attributes-with-adsi"></a>Acessando atributos com ADSI

Os métodos [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) são usados para recuperar valores de atributo nomeados. Os dois métodos retornam um valor de [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) . Esses métodos estão disponíveis apenas para diretórios que dão suporte a um esquema. Ao acessar objetos em um diretório sem um esquema, as interfaces [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) e [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) devem ser usadas para manipular valores de atributo.

Os métodos [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) retornam uma [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) que pode ou não ser uma matriz **Variant** , dependendo do número de valores retornados pelo servidor. Por exemplo, se apenas um valor for retornado do servidor, independentemente de ser um atributo único ou com vários valores, o método retornará uma única **variante**. Por outro lado, se vários valores forem retornados, uma matriz **Variant** será retornada. Se uma **matriz Variant** for retornada, o membro **VT** da estrutura **Variant** conterá os sinalizadores **VT \_ Variant/vbVariant** e **VT \_ array/VBArray** .

Os métodos [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) também podem retornar um objeto com usando a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Nesse caso, o membro **VT** da estrutura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) contém o sinalizador de **\_ expedição/vbObject do VT** . Para acessar o objeto COM, chame o método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) na interface **IDispatch** para obter a interface desejada.

Outro tipo de dados retornado pelos métodos [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) são dados binários. Nesse caso, os dados são fornecidos como uma matriz contígua de bytes e o membro **VT** da estrutura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) conterá os sinalizadores **VT \_ UI1/vbByte** e **VT \_ array/VBArray** .

> [!Note]  
> O Microsoft Visual Basic, Scripting Edition, só dá suporte a matrizes [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) e **Variant** . Por isso, o VBScript não pode ser usado para ler valores de propriedade binária.

 

Muitas interfaces ADSI definem propriedades específicas de interface. Por exemplo, a interface [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) define a propriedade [**Location**](iadscomputer-property-methods.md) . Essas propriedades definidas pela interface podem conter dados idênticos a um dos atributos nomeados, mas as propriedades são específicas ao tipo de objeto ao qual a interface se refere. Em idiomas que dão suporte à automação, essas propriedades definidas pela interface podem ser acessadas usando a notação de ponto, conforme mostrado no exemplo de código a seguir.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra como acessar a propriedade ADsPath na interface IADs.


```VB
Dim oUser as IADs
Dim Path as String
 
' Bind to a specific user object.
set oUser = GetObject(
            "LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
Path = MyUser.ADsPath
```



Em linguagens que não são de automação, os métodos de acesso à propriedade devem ser usados para acessar as propriedades definidas pela interface. Por exemplo, o método de [**\_ localização IADsComputer:: Get**](iadscomputer-property-methods.md) é usado para recuperar a propriedade **IADsComputer. Location** .

O exemplo de código C++ a seguir demonstra como usar o método de acesso de propriedade em C++ para recuperar o ADsPath de um usuário.


```C++
HRESULT hr;
IADs *pUser; 
 
// Bind to user object.
hr = ADsGetObject(
     L"LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com", 
     IID_IADs, 
     (void**)&pUser);
if(SUCCEEDED(hr)) 
{
    BSTR bstrName;

    // Get property.
    hr = pUser->get_Name(&bstrName);
    if(SUCCEEDED(hr)) 
    {
        wprintf(bstrName);
 
        SysFreeString(bstrName);
    }

    pUser->Release();
}
```



Para obter mais informações sobre como acessar atributos com ADSI, consulte:

-   [O método Get](the-get-method.md)
-   [O método GetEx](the-getex-method.md)
-   [O método GetInfo](the-getinfo-method.md)
-   [Otimização usando GetInfoEx](optimization-using-getinfoex.md)
-   [Acessando atributos com a interface IDirectoryObject](accessing-attributes-with-the-idirectoryobject-interface.md)
-   [Exemplo de código para ler atributos](example-code-for-reading-attributes.md)

 

 