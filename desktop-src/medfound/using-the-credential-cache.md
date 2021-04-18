---
description: Usando o cache de credenciais
ms.assetid: b58d0a6e-ecae-48a1-a3af-d4246caa272b
title: Usando o cache de credenciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d512d0bab8f45f50a587e3c8eda2a73c4832685f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790415"
---
# <a name="using-the-credential-cache"></a>Usando o cache de credenciais

Media Foundation fornece uma implementação padrão da interface [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) . Um aplicativo que implementa a interface [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) pode usar o objeto de cache de credencial padrão para armazenar as credenciais do usuário.

Para criar o objeto de cache de credencial padrão, chame a função [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) .


```C++
HRESULT hr = S_OK;
IMFNetCredentialCache *pCredentialCache = NULL;
hr = MFCreateCredentialCache(&pCredentialCache);
```



Depois que o cache de credenciais é criado, o aplicativo pode usar os métodos a seguir para obter um objeto de credencial, definir as credenciais do usuário e especificar as opções de cache.

-   Para obter o objeto de credencial para uma URL, chame [**IMFNetCredentialCache:: GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).

    ```C++
    hr = pCredentialCache-> GetCredential(
            pszUrl,
            pszRealm,
            dwAuthenticationFlags,
            &pCredential,
            &dwRequirementsFlags);
    ```

    

    Se as credenciais para a URL especificada não existirem no cache de credenciais, [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) criará um novo objeto de credencial com valores de senha e nome de usuário vazios.

-   Para definir o nome de usuário e a senha no objeto Credential, chame [**IMFNetCredential:: SETUSER**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) e [**IMFNetCredential:: SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword).
-   Para definir as opções de cache no objeto Credential, chame [**IMFNetCredentialCache:: Setuseroptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions).

    ```C++
    hr = pCredentialCache-> SetUserOptions( 
            pCredentialCache,
            MFNET_CREDENTIAL_SAVE);
    ```

    

    Os valores de parâmetro *dwOptionsFlags* são definidos na enumeração [**MFNetCredentialOptions**](/windows/desktop/api/mfidl/ne-mfidl-mfnetcredentialoptions) . Para salvar as credenciais do usuário de uma URL em um armazenamento persistente, defina o \_ sinalizador de salvamento da credencial MFNET \_ . Se a chamada [**Setuseroptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) for concluída com êxito, a chamada subsequente para [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) pesquisará as credenciais no armazenamento persistente. Se uma correspondência for encontrada, esse método retornará um ponteiro para o objeto de credencial que contém as informações.

    Por padrão, as credenciais de usuário enviadas pela rede são criptografadas. Para alterar isso para texto não criptografado, defina o sinalizador de MFNET \_ credencial \_ permitir \_ texto não criptografado \_ .

    Para remover informações do registro, chame [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) para obter o objeto de credencial e, em seguida, chame [**SetUserOption**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) e defina *dwOptionsFlags* para MFNET \_ Credential não \_ \_ cache.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Autenticação de origem da rede](network-source-authentication.md)
</dt> </dl>

 

 



