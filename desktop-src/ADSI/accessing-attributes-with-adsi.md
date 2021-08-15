---
title: Acessando atributos com ADSI
description: Os métodos IADs.Get e IADs.GetEx são usados para recuperar valores de atributo nomeados.
ms.assetid: 8aa139e1-6b20-4745-92f1-d2f352071f33
ms.tgt_platform: multiple
keywords:
- Atributos, acessando com ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e37c63b61986a56e7b22f114b5956d9e047f1ae45b5dc2e653074ea35440f10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024124"
---
# <a name="accessing-attributes-with-adsi"></a>Acessando atributos com ADSI

Os [**métodos IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) [**e IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) são usados para recuperar valores de atributo nomeados. Ambos os métodos retornam um [**valor VARIANT.**](/windows/win32/api/oaidl/ns-oaidl-variant) Esses métodos estão disponíveis apenas para diretórios que suportam um esquema. Ao acessar objetos em um diretório sem um esquema, as interfaces [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) e [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) devem ser usadas para manipular valores de atributo.

Os [**métodos IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) retornam uma [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) que pode ou não ser uma matriz **VARIANT,** dependendo do número de valores retornados pelo servidor. Por exemplo, se apenas um valor for retornado do servidor, independentemente de ser um atributo único ou com vários valores, o método retornará uma **única VARIANT.** Por outro lado, se vários valores são retornados, uma **matriz VARIANT** é retornada. Se uma **matriz VARIANT** for retornada, o membro **vt** da estrutura **VARIANT** conterá os sinalizadores **VT \_ VARIANT/vbVariant** e **VT \_ ARRAY/vbArray.**

Os [**métodos IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) também podem retornar um objeto COM usando a interface [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) Nesse caso, o **membro vt** da estrutura [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) contém o **sinalizador VT \_ DISPATCH/vbObject.** Para acessar o objeto COM, chame o [**método QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) na interface **IDispatch** para obter a interface desejada.

Outro tipo de dados retornado pelos [**métodos IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) são dados binários. Nesse caso, os dados são fornecidos como uma matriz contígua de bytes e o membro **vt** da estrutura [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) conterá os sinalizadores **VT \_ UI1/vbByte** e **VT \_ ARRAY/vbArray.**

> [!Note]  
> Microsoft Visual Basic, o Scripting Edition dá suporte apenas [**a matrizes VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) e **VARIANT.** Por isso, o VBScript não pode ser usado para ler valores de propriedade binária.

 

Muitas interfaces ADSI definem propriedades específicas da interface. Por exemplo, a [**interface IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) define a [**propriedade Location.**](iadscomputer-property-methods.md) Essas propriedades definidas pela interface podem conter dados idênticos a um dos atributos nomeados, mas as propriedades são específicas ao tipo de objeto ao qual a interface se refere. Em linguagens que suportam automação, essas propriedades definidas pela interface podem ser acessadas usando a notação de ponto, conforme mostrado no exemplo de código a seguir.

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



Em linguagens que não são de automação, os métodos de acesso à propriedade devem ser usados para acessar as propriedades definidas pela interface. Por exemplo, o [**método IADsComputer::get \_ Location**](iadscomputer-property-methods.md) é usado para recuperar a **propriedade IADsComputer.Location.**

O exemplo de código C++ a seguir demonstra como usar o método de acesso à propriedade em C++ para recuperar o ADsPath de um usuário.


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
-   [Código de exemplo para ler atributos](example-code-for-reading-attributes.md)

 

 