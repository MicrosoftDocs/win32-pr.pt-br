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
ms.openlocfilehash: 73853250c581e460360f5490defc0c94e76e5be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779353"
---
# <a name="receiving-the-returned-certificate"></a><span data-ttu-id="97432-103">Recebendo o certificado retornado</span><span class="sxs-lookup"><span data-stu-id="97432-103">Receiving the Returned Certificate</span></span>

<span data-ttu-id="97432-104">Quando a autoridade de certificação (CA) verificou as informações de identidade do solicitante e está satisfeita de que o solicitante é o proprietário da chave privada e que os dados sobre esse solicitante são precisos, a autoridade de certificação constrói um certificado X. 509, o assina, empacota com quaisquer outros certificados necessários (como o próprio certificado da autoridade de certificação) em uma mensagem e envia a mensagem para o solicitante.</span><span class="sxs-lookup"><span data-stu-id="97432-104">When the certification authority (CA) has verified the requester's identity information and is satisfied that the requester is the owner of the private key and that the data about that requester is accurate, the CA constructs an X.509 certificate, signs it, packages it with any other needed certificates (such as the CA's own certificate) in a message, and sends the message to the requester.</span></span> <span data-ttu-id="97432-105">A mensagem pode ser uma \# mensagem PKCS 7 ou uma resposta CMC (os modelos v2 resultam em uma resposta CMC).</span><span class="sxs-lookup"><span data-stu-id="97432-105">The message can be a PKCS \#7 message or a CMC response (V2 templates result in a CMC response).</span></span>

<span data-ttu-id="97432-106">O aplicativo receptor passa a mensagem para o controle de registro de certificado.</span><span class="sxs-lookup"><span data-stu-id="97432-106">The receiving application passes the message to the Certificate Enrollment Control.</span></span> <span data-ttu-id="97432-107">O controle de registro de certificado abre a mensagem e extrai os certificados.</span><span class="sxs-lookup"><span data-stu-id="97432-107">The Certificate Enrollment Control then opens the message and extracts the certificates.</span></span> <span data-ttu-id="97432-108">O usuário receberá uma solicitação com uma caixa de diálogo perguntando se o usuário aceitará certificados autoassinados no repositório "raiz".</span><span class="sxs-lookup"><span data-stu-id="97432-108">The user is prompted with a dialog box asking whether the user will accept self-signed certificates in the "Root" store.</span></span> <span data-ttu-id="97432-109">Se o usuário aceitar o certificado raiz, o restante dos certificados (exceto para o certificado do solicitante) será colocado no repositório "CA".</span><span class="sxs-lookup"><span data-stu-id="97432-109">If the user accepts the root certificate, the rest of the certificates (except for the requester's certificate) are placed in the "CA" store.</span></span> <span data-ttu-id="97432-110">O certificado do solicitante é colocado no repositório de certificados especificado pelo solicitante na propriedade [**Mystorename**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename) .</span><span class="sxs-lookup"><span data-stu-id="97432-110">The requester's certificate is placed in the certificate store specified by the requester in the [**MyStoreName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename) property.</span></span>

<span data-ttu-id="97432-111">O exemplo a seguir mostra como usar o Visual Basic Scripting Edition (VBScript) e HTML em uma página da Web para receber e armazenar os certificados retornados.</span><span class="sxs-lookup"><span data-stu-id="97432-111">The following example shows how to use the Visual Basic Scripting Edition (VBScript) and HTML in a webpage to receive and store the returned certificates.</span></span>


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



 

 
