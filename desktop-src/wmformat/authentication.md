---
title: Autenticação (Windows SDK de Formato de Mídia 11)
description: Autenticação
ms.assetid: 9c181615-e864-4588-846f-d04d73824f5f
keywords:
- Windows SDK de Formato de Mídia, autenticação
- Windows SDK de Formato de Mídia, autenticação de rede
- ASF (Advanced Systems Format), autenticação
- ASF (Formato de Sistemas Avançados), autenticação
- ASF (Advanced Systems Format), autenticação de rede
- ASF (Formato de Sistemas Avançados), autenticação de rede
- autenticação
- autenticação de rede,sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee276bc2800ad7f2d5fa94f00e282dc7d4f5402396d69eb7e3b240fd4303f4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007116"
---
# <a name="authentication-windows-media-format-11-sdk"></a>Autenticação (Windows SDK de Formato de Mídia 11)

O objeto leitor pode lidar com desafios de autenticação de rede, incluindo autenticação digest e autenticação NTLM. Em alguns casos, o aplicativo deve fornecer as credenciais do usuário por meio de uma interface de retorno de chamada:

-   Autenticação digest: o aplicativo deve implementar a interface **IWMCredentialCallback,** conforme descrito posteriormente neste tópico.
-   Autenticação NTLM: o leitor responde automaticamente com as credenciais de logon do usuário. Se o usuário atual estiver autorizado a fazer logoff no servidor, o aplicativo não precisa fazer nada. Se o usuário não tiver autorização, o aplicativo deverá implementar a interface **IWMCredentialCallback.**

    > [!Note]  
    > Windows Media Services versão 4.1 não dá suporte à autenticação NTLM por meio de um servidor proxy. A autenticação NTLM requer várias trocas cliente-servidor na mesma conexão e a versão 4.1 não mantém uma conexão persistente com o proxy. Windows Media Services Série 9 no Microsoft Windows Server 2003 dá suporte à autenticação NTLM por meio de um servidor proxy, desde que o proxy seja compatível com conexões keep alive.

     

Como é possível lembrar, em alguns casos, o aplicativo deve fornecer as credenciais do usuário. Isso ocorre por meio da interface **IWMCredentialCallback,** que tem um único método, **AcquireCredentials.** Para dar suporte à autenticação, implemente essa interface em seu aplicativo. O objeto de leitor consulta essa interface chamando **QueryInterface** no ponteiro [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) que ele recebeu do aplicativo no método [**IWMReader::Open.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) Se o objeto de leitor precisar obter as credenciais do usuário, ele chamará o **método AcquireCredentials do** aplicativo.

Se as credenciais serão enviadas pela rede sem criptografia, o leitor define o sinalizador WMT CREDENTIAL CLEAR TEXT no \_ \_ parâmetro \_ *pdwFlags.* Isso dá ao aplicativo a oportunidade de avisar o usuário de que suas credenciais serão enviadas em texto sem-texto.

Caso contrário, o objeto leitor criptografa automaticamente as credenciais antes de enviá-las pela rede. O aplicativo pode devolvê-los ao objeto de leitor em texto sem-texto. Além disso, se o objeto leitor define o sinalizador WMT CREDENTIAL ENCRYPT, isso significa que o leitor dá suporte à obter credenciais criptografadas \_ \_ do aplicativo. Nesse caso, o aplicativo pode retornar as credenciais em texto sem-texto ou criptografá-las usando a função **CryptProtectData,** que é descrita na documentação do SDK da Plataforma. Se o aplicativo criptografar as credenciais, ele deverá definir o sinalizador WMT CREDENTIAL ENCRYPT no parâmetro \_ \_ *pdwFlags* antes que o método retorne.

Em geral, não é necessário criptografar os dados, pois o objeto leitor criptografa os dados, se necessário. No entanto, a criptografia poderá ser útil se o aplicativo mantiver o nome de usuário e a senha na memória, pois impede que um invasor inspecione um despejo de memória do processo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMCredentialCallback Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> <dt>

[**IWMReader Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> </dl>

 

 




