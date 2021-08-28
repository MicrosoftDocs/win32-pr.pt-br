---
title: Detectando se um computador remoto dá suporte WS-Management protocolo
description: Você pode usar os métodos Session.Identify ou IWSManSession.Identify para determinar se o computador remoto tem um serviço que dá suporte ao protocolo WS-Management.
ms.assetid: 4d11ac02-fa8b-45d7-bceb-a18f561bc928
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49a7ebeb25f7f3af69a03c55499dd53a890e540c1a1ed677e7d48e5b11b82b1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643226"
---
# <a name="detecting-whether-a-remote-computer-supports-ws-management-protocol"></a>Detectando se um computador remoto dá suporte WS-Management protocolo

Você pode usar os métodos [**Session.Identify**](session-identify.md) ou [**IWSManSession.Identify**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify) para determinar se o computador remoto tem um serviço que dá suporte ao protocolo WS-Management.

Se um WS-Management de protocolo estiver configurado no computador remoto e estiver escutando solicitações, o serviço poderá detectar uma solicitação Identificar pelo XML a seguir no header.


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



O WS-Management protocolo que recebe a solicitação retorna as informações, contidas na lista a seguir, no corpo da mensagem:

-   A versão WS-Management protocolo. Por exemplo, "https://schemas.dmtf.org/wbem/wsman/1/wsman".
-   O fornecedor do produto, por exemplo, "Microsoft Corporation".
-   A versão do produto. Se a solicitação for enviada **com WSManFlagUseNoAuthentication** no parâmetro *flags,* nenhuma informação de versão do produto será retornada. Se a solicitação for enviada com a autenticação padrão em vigor ou com outro modo de autenticação especificado, as informações de versão do produto poderão ser retornadas.

A solicitação para detectar se o computador remoto tem um serviço de protocolo WS-Management configurado e de escuta pode ser executada no início de um script com outras operações. Isso verificará se os computadores ou computadores de destino podem responder a solicitações WS-Management protocolo. A verificação também pode ser feita em um script separado.

**Para detectar um serviço WS-Management protocolo**

1.  Crie um [**objeto WSMan.**](wsman.md)

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  Determine se a solicitação deve ser enviada autenticada ou não autenticada e de acordo com o parâmetro *flags* na chamada para [**WSMan.CreateSession**](wsman-createsession.md).

    ```VB
    set objSession = objWsman.CreateSession("Remote1", _
       objWsman.SessionFlagUseNoAuthentication)
    ```

    

3.  Chame [**Session.Identify**](session-identify.md).

    ```VB
    objSession.Identify
    ```

    

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir envia uma solicitação de Identificação não autenticada para o computador remoto chamado "Remote1" no mesmo domínio.


```VB
set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession("Remote1", _
  objWsman.SessionFlagUseNoAuthentication)
WScript.Echo objSession.Identify
```



A resposta a seguir mostra o XML retornado pelo computador remoto. A WS-Management do protocolo (" ") e o fornecedor do sistema operacional https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd ("Microsoft Corporation") são especificados no XML retornado. Como a mensagem é enviada sem autenticação, a versão do produto não é retornada pelo serviço Windows Gerenciamento Remoto.


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 0.0.0 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



O exemplo de código VBScript a seguir envia uma solicitação de Identificação autenticada para o computador remoto.


```VB
set ObjWSMan = CreateObject("Wsman.Automation")
set objSession = WSMan.CreateSession("Remote1", _
  objWSMan.SessionFlagUseKerberos)
WScript.Echo objSession.Identify
```



Como a solicitação foi enviada com autenticação, as informações de versão são retornadas.


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 6.0.5384 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre Windows gerenciamento remoto](about-windows-remote-management.md)
</dt> <dt>

[Usando Windows gerenciamento remoto](using-windows-remote-management.md)
</dt> <dt>

[Windows Referência de gerenciamento remoto](windows-remote-management-reference.md)
</dt> </dl>

 

 




