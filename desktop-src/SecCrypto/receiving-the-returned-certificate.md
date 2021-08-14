---
description: Explica como um aplicativo recebe um certificado.
ms.assetid: 7f87dcf5-b434-4f63-abcd-6873831d22bc
title: Recebendo o certificado retornado
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cb2efe504e2d09b3fae2b6d6293772bf67a3f038a5f9c43330707f541e2ba8f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900962"
---
# <a name="receiving-the-returned-certificate"></a>Recebendo o certificado retornado

Quando a autoridade de certificação (CA) verificou as informações de identidade do solicitante e está satisfeita de que o solicitante é o proprietário da chave privada e que os dados sobre esse solicitante são precisos, a autoridade de certificação constrói um certificado X. 509, o assina, empacota com quaisquer outros certificados necessários (como o próprio certificado da autoridade de certificação) em uma mensagem,  e envia a mensagem para o solicitante. A mensagem pode ser uma \# mensagem PKCS 7 ou uma resposta CMC (os modelos v2 resultam em uma resposta CMC).

O aplicativo receptor passa a mensagem para o controle de registro de certificado. O controle de registro de certificado abre a mensagem e extrai os certificados. O usuário receberá uma solicitação com uma caixa de diálogo perguntando se o usuário aceitará certificados autoassinados no repositório "raiz". Se o usuário aceitar o certificado raiz, o restante dos certificados (exceto para o certificado do solicitante) será colocado no repositório "CA". O certificado do solicitante é colocado no repositório de certificados especificado pelo solicitante na propriedade [**Mystorename**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename) .

o exemplo a seguir mostra como usar o Visual Basic scripting Edition (VBScript) e HTML em uma página da web para receber e armazenar os certificados retornados.


```VB
<HTML>
<TITLE>Certificate Enrollment Acceptance HTML Page
</TITLE>

<OBJECT  classid="clsid:127698E4-E730-4E5C-A2b1-21490A70C8A1"
    CODEBASE="xenroll.dll"
    id=IControl >
</OBJECT>

<SCRIPT language="VBScript">

<!--

Option Explicit 

'Accept the certificate subroutine.

Sub AcceptCertSub

On Error Resume Next

' Get the issued certificate.
' The following value, "PKCS7", represents the received message. 
' Actually, this value must be supplied through the design of
' the receiving application.
' A possible implementation is as follows: after using 
' ICertRequest.Submit to submit the PKCS #10, call 
' ICertRequest.GetLastStatus to confirm successful certificate 
' creation, and then call ICertRequest.GetCertificate to retrieve 
' the certificate.

document.result.result.value = "PKCS7"

    Call IControl.AcceptPKCS7(document.result.result.value)

    If err.Number = 0 Then
        navigate "..\done.htm"
    Else
        Alert "Error: " & Hex(err)
    End If

    End sub

    ' Decline the certificate sub-routine.
    Sub NoAcceptCertSub
    navigate "..\notdone.htm"
    End sub
-->
</SCRIPT>
</BODY>
</HTML>
```



 

 
