---
title: Autenticação (Windows Media Format 11 SDK)
description: Autenticação
ms.assetid: 9c181615-e864-4588-846f-d04d73824f5f
keywords:
- SDK do Windows Media Format, autenticação
- SDK do Windows Media Format, autenticação de rede
- ASF (Advanced Systems Format), autenticação
- ASF (formato de sistemas avançados), autenticação
- ASF (Advanced Systems Format), autenticação de rede
- ASF (formato de sistemas avançados), autenticação de rede
- autenticação
- autenticação de rede, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf815881ac7beb354fffbfdb9b5475d040e9e83
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105798390"
---
# <a name="authentication-windows-media-format-11-sdk"></a>Autenticação (Windows Media Format 11 SDK)

O objeto leitor pode lidar com desafios de autenticação de rede, incluindo autenticação Digest e autenticação NTLM. Em alguns casos, o aplicativo deve fornecer as credenciais do usuário por meio de uma interface de retorno de chamada:

-   Autenticação Digest: o aplicativo deve implementar a interface **IWMCredentialCallback** , conforme descrito posteriormente neste tópico.
-   Autenticação NTLM: o leitor responde automaticamente com as credenciais de logon do usuário. Se o usuário atual estiver autorizado a fazer logon no servidor, o aplicativo não precisará fazer nada. Se o usuário não tiver autorização, o aplicativo deverá implementar a interface **IWMCredentialCallback** .

    > [!Note]  
    > O Windows Media Services versão 4,1 não oferece suporte à autenticação NTLM por meio de um servidor proxy. A autenticação NTLM requer várias trocas de cliente/servidor na mesma conexão, e a versão 4,1 não mantém uma conexão persistente com o proxy. O Windows Media Services 9 Series no Microsoft Windows Server 2003 dá suporte à autenticação NTLM por meio de um servidor proxy, desde que o proxy dê suporte a conexões Keep-Alive.

     

Como observado, em alguns casos, o aplicativo deve fornecer as credenciais do usuário. Isso ocorre por meio da interface **IWMCredentialCallback** , que tem um único método, **AcquireCredentials**. Para dar suporte à autenticação, implemente essa interface em seu aplicativo. O objeto de leitor consulta essa interface chamando **QueryInterface** no ponteiro [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) recebido do aplicativo no método [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) . Se o objeto do leitor precisar obter as credenciais do usuário, ele chamará o método **AcquireCredentials** do aplicativo.

Se as credenciais forem enviadas pela rede sem criptografia, o leitor definirá o sinalizador de \_ texto não criptografado da credencial WMT \_ \_ no parâmetro *pdwFlags* . Isso dá ao aplicativo uma oportunidade de avisar ao usuário que suas credenciais serão enviadas em texto sem formatação.

Caso contrário, o objeto leitor criptografará automaticamente as credenciais antes de enviá-las pela rede. O aplicativo pode retorná-los ao objeto leitor em texto sem formatação. Além disso, se o objeto do leitor definir o \_ sinalizador de criptografia de credencial WMT \_ , isso significará que o leitor dá suporte a obter credenciais criptografadas do aplicativo. Nesse caso, o aplicativo pode retornar as credenciais em texto sem formatação ou, caso contrário, criptografá-las usando a função **CryptProtectData** , que é descrita na documentação do Platform SDK. Se o aplicativo criptografar as credenciais, ele deverá definir o \_ sinalizador de criptografia de credencial WMT \_ no parâmetro *pdwFlags* antes que o método retorne.

Em geral, não é necessário criptografar os dados, pois o objeto leitor criptografa os dados, se necessário. No entanto, a criptografia poderá ser útil se o aplicativo mantiver o nome de usuário e a senha na memória, pois impede que um invasor Inspecione um despejo de memória do processo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> <dt>

[**Interface IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> </dl>

 

 




