---
title: Detectando se um computador remoto dá suporte ao protocolo WS-Management
description: Você pode usar os métodos Session. Identify ou IWSManSession. Identify para determinar se o computador remoto tem um serviço que dá suporte ao protocolo WS-Management.
ms.assetid: 4d11ac02-fa8b-45d7-bceb-a18f561bc928
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af82284b38b2a101c767766d44eb975ff7e1dadc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105810865"
---
# <a name="detecting-whether-a-remote-computer-supports-ws-management-protocol"></a>Detectando se um computador remoto dá suporte ao protocolo WS-Management

Você pode usar os métodos [**Session. Identify**](session-identify.md) ou [**IWSManSession. Identify**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify) para determinar se o computador remoto tem um serviço que dá suporte ao protocolo WS-Management.

Se um serviço de protocolo WS-Management estiver configurado no computador remoto e estiver ouvindo solicitações, o serviço poderá detectar uma solicitação de identificação pelo seguinte XML no cabeçalho.


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



O serviço de protocolo WS-Management que recebe a solicitação retorna as informações contidas na lista a seguir, no corpo da mensagem:

-   A versão do protocolo WS-Management. Por exemplo, "https://schemas.dmtf.org/wbem/wsman/1/wsman".
-   O fornecedor do produto, por exemplo, "Microsoft Corporation".
-   A versão do produto. Se a solicitação for enviada com **WSManFlagUseNoAuthentication** no parâmetro *flags* , nenhuma informação de versão do produto será retornada. Se a solicitação for enviada com a autenticação padrão em vigor ou com outro modo de autenticação especificado, as informações de versão do produto poderão ser retornadas.

A solicitação para detectar se o computador remoto tem um serviço de protocolo configurado e de escuta WS-Management pode ser executado no início de um script com outras operações. Isso verificará se o computador de destino ou os computadores podem responder a outras solicitações de protocolo de WS-Management. A verificação também pode ser feita em um script separado.

**Para detectar um serviço de protocolo WS-Management**

1.  Crie um objeto [**WSMan**](wsman.md) .

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  Determine se a solicitação deve ser enviada autenticada ou não autenticada e defina o parâmetro *flags* adequadamente na chamada para [**WSMan. CreateSession**](wsman-createsession.md).

    ```VB
    set objSession = objWsman.CreateSession("Remote1", _
       objWsman.SessionFlagUseNoAuthentication)
    ```

    

3.  Chame [**Session. Identify**](session-identify.md).

    ```VB
    objSession.Identify
    ```

    

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir envia uma solicitação de identificação não autenticada para o computador remoto chamado "Remote1" no mesmo domínio.


```VB
set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession("Remote1", _
  objWsman.SessionFlagUseNoAuthentication)
WScript.Echo objSession.Identify
```



A resposta a seguir mostra o XML retornado pelo computador remoto. A versão do protocolo de WS-Management (" https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd ") e o fornecedor do sistema operacional ("Microsoft Corporation") são especificados no XML retornado. Como a mensagem é enviada não autenticada, a versão do produto não é retornada pelo serviço de Gerenciamento Remoto do Windows.


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 0.0.0 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



O exemplo de código VBScript a seguir envia uma solicitação de identificação autenticada para o computador remoto.


```VB
set ObjWSMan = CreateObject("Wsman.Automation")
set objSession = WSMan.CreateSession("Remote1", _
  objWSMan.SessionFlagUseKerberos)
WScript.Echo objSession.Identify
```



Como a solicitação foi enviada com a autenticação, as informações de versão são retornadas.


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

[Sobre Gerenciamento Remoto do Windows](about-windows-remote-management.md)
</dt> <dt>

[Usando Gerenciamento Remoto do Windows](using-windows-remote-management.md)
</dt> <dt>

[Referência de Gerenciamento Remoto do Windows](windows-remote-management-reference.md)
</dt> </dl>

 

 




