---
title: Associação com ADsOpenObject e IADsOpenDSObject OpenDSObject
description: A função ADsOpenObject e o método IADsOpenDSObject OpenDSObject são usados para associar a objetos de serviço de diretório quando credenciais alternativas devem ser especificadas e quando a criptografia de dados é necessária.
ms.assetid: 7b8ded11-e04f-40f5-a82a-5972c4df9dea
ms.tgt_platform: multiple
keywords:
- Associação com ADsOpenObject e IADsOpenDSObject OpenDSObject ADSI
- ADSI da ADSI, usando, associação com ADsOpenObject e IADsOpenDSObject OpenDSObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a249aa3d51520d0d345b5a098f84480e5b5016
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008358"
---
# <a name="binding-with-adsopenobject-and-iadsopendsobjectopendsobject"></a>Associação com ADsOpenObject e IADsOpenDSObject:: OpenDSObject

A função [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) e o método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) são usados para associar a objetos de serviço de diretório quando credenciais alternativas devem ser especificadas e quando a criptografia de dados é necessária.

As credenciais do thread de chamada devem ser usadas quando possível. No entanto, se credenciais alternativas precisarem ser usadas, a função [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou o método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) deverá ser usado. Se forem usadas credenciais alternativas, será importante não armazenar a senha em cache. Várias operações de ligação podem ser executadas especificando o nome de usuário e a senha para a primeira operação de ligação e, em seguida, especificando apenas o nome de usuário em associações subsequentes. O sistema configura uma sessão na primeira chamada e usa a mesma sessão em chamadas de ligação subsequentes, desde que as seguintes condições sejam atendidas:

-   O mesmo nome de usuário em cada operação de ligação.
-   Implemente a associação sem servidor ou associe-se ao mesmo servidor em cada operação de ligação.
-   Mantenha uma sessão aberta mantendo uma referência de objeto de uma das operações de ligação. A sessão é fechada quando a última referência de objeto é liberada.

[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) e [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) usam as interfaces do [provedor de suporte de segurança (SSPI)](/windows/desktop/SecAuthN/sspi) do Windows NT para permitir a flexibilidade nas opções de autenticação. A principal vantagem de usar essas interfaces é fornecer tipos diferentes de autenticação para Active Directory clientes e para criptografar a sessão. Atualmente, a ADSI não permite que certificados sejam passados. Portanto, você pode usar SSL para criptografia e, em seguida, Kerberos, NTLM ou autenticação simples, dependendo de como os sinalizadores são definidos no parâmetro *dwReserved* .

Você não pode solicitar um provedor SSPI específico em ADSI, embora sempre obtenha o protocolo de preferência mais alto. No caso de uma associação de cliente Windows a um computador que executa o Windows, o protocolo é Kerberos. Não permitir um certificado para autenticação é aceitável no caso de uma página da Web, pois a autenticação ocorre antes da execução da página da Web.

Embora as operações abertas permitam que você especifique um usuário e uma senha, você não deve fazê-lo. Em vez disso, não especifique nenhuma credencial e use implicitamente as credenciais do contexto de segurança do chamador. Para associar a um objeto de diretório usando as credenciais do chamador com [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject), especifique **NULL** para o nome de usuário e a senha.

Por fim, para associar sem autenticação, use o sinalizador **anúncios \_ sem \_ autenticação** . Nenhuma autenticação indica que o ADSI tenta ligar como um usuário anônimo ao objeto de destino e não executa nenhuma autenticação. Isso é equivalente a solicitar a associação anônima no LDAP e indica que todos os usuários estão incluídos no contexto de segurança.

Se os sinalizadores de autenticação estiverem definidos como zero, a ADSI executará uma associação simples, enviada como texto sem formatação.

> [!Caution]  
> Se um nome de usuário e senha forem especificados sem especificar sinalizadores de autenticação, o nome de usuário e a senha serão transmitidos pela rede em texto não criptografado, o que representa um risco de segurança. Não especifique um nome de usuário e uma senha sem especificar sinalizadores de autenticação.

 

## <a name="examples"></a>Exemplos

O exemplo de código a seguir Visual Basic mostra como usar o método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) .


```VB
Dim openDS As IADsOpenDSObject
Dim usr As IADsUser
 
Set openDS = GetObject("LDAP:")
 
openDS.OpenDSObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION)
```



O exemplo de código C++ a seguir mostra como usar a função [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .


```C++
IADs *pObject;
HRESULT hr;

hr = ADsOpenObject(L"LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION, 
    IID_IADs,
    (void**)&pObject);
if(SUCCEEDED(hr))
{
    // Use the object.

    // Release the object.
    pObject->Release()
}
```



A interface [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) também pode ser usada em C++, mas ela duplica a função [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .

O exemplo de código C++ a seguir mostra como usar a interface [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) para executar a mesma operação de associação que no exemplo de código acima.


```C++
IADsOpenDSObject *pDSO;
HRESULT hr;
 
hr = ADsGetObject(L"LDAP:", IID_IADsOpenDSObject, (void**)&pDSO);
if(SUCCEEDED(hr))
{
    IDispatch *pDisp;

    hr = pDSO->OpenDSObject(CComBSTR("LDAP://CN=jeffsmith,DC=fabrikam,DC=com"),
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION, 
        &pDisp);
    if(SUCCEEDED(hr))
    {
        IADs *pObject;

        hr = pDisp->QueryInterface(IID_IADs, (void**) &pObject);
        if(SUCCEEDED(hr))
        {
            // Use the object.

            // Release the object.
            pObject->Release();
        }

        pDisp->Release();
    }
    
    pDSO->Release();
}
```



 

 