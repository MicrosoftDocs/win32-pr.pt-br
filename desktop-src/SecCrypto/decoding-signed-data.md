---
description: Processo para decodificar dados assinados.
ms.assetid: 803220d0-7963-4fc4-8451-a979e54a9cc3
title: Decodificando dados assinados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdfd327746c5d0ba8e7089e1c273817b76c16370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754948"
---
# <a name="decoding-signed-data"></a><span data-ttu-id="b158d-103">Decodificando dados assinados</span><span class="sxs-lookup"><span data-stu-id="b158d-103">Decoding Signed Data</span></span>

<span data-ttu-id="b158d-104">O processo geral a seguir Decodifica um tipo de [*dados assinado*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b158d-104">The following general process decodes a [*signed data*](../secgloss/s-gly.md) type.</span></span>

<span data-ttu-id="b158d-105">**Para decodificar uma mensagem assinada**</span><span class="sxs-lookup"><span data-stu-id="b158d-105">**To decode a signed message**</span></span>

1.  <span data-ttu-id="b158d-106">Obtenha um ponteiro para o BLOB codificado.</span><span class="sxs-lookup"><span data-stu-id="b158d-106">Get a pointer to the encoded BLOB.</span></span>
2.  <span data-ttu-id="b158d-107">Chame [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passando os argumentos necessários.</span><span class="sxs-lookup"><span data-stu-id="b158d-107">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passing the necessary arguments.</span></span>
3.  <span data-ttu-id="b158d-108">Chame [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) uma vez, passando o identificador recuperado na etapa 2 e um ponteiro para os dados que serão decodificados.</span><span class="sxs-lookup"><span data-stu-id="b158d-108">Call [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) once, passing in the handle retrieved in step 2 and a pointer to the data that is to be decoded.</span></span> <span data-ttu-id="b158d-109">Isso faz com que as ações apropriadas sejam executadas na mensagem, dependendo do tipo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="b158d-109">This causes the appropriate actions to be taken on the message, depending on the message type.</span></span>
4.  <span data-ttu-id="b158d-110">Chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando o identificador recuperado na etapa 2 e os tipos de parâmetro apropriados para acessar os dados decodificados.</span><span class="sxs-lookup"><span data-stu-id="b158d-110">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in the handle retrieved in step 2 and the appropriate parameter types to access the decoded data.</span></span> <span data-ttu-id="b158d-111">Por exemplo, passe \_ o parâmetro de conteúdo CMSG \_ para obter um ponteiro para o conteúdo decodificado.</span><span class="sxs-lookup"><span data-stu-id="b158d-111">For example, pass in CMSG\_CONTENT\_PARAM to get a pointer to the decoded content.</span></span>

<span data-ttu-id="b158d-112">O processo geral a seguir verifica a assinatura de uma mensagem decodificada e assinada.</span><span class="sxs-lookup"><span data-stu-id="b158d-112">The following general process verifies the signature of a decoded, signed message.</span></span>

<span data-ttu-id="b158d-113">**Para verificar a assinatura de uma mensagem decodificada e assinada**</span><span class="sxs-lookup"><span data-stu-id="b158d-113">**To verify the signature of a decoded, signed message**</span></span>

1.  <span data-ttu-id="b158d-114">Chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando o identificador de mensagem e o \_ parâmetro de informações de certificado do assinante CMSG \_ \_ \_ para obter as [**\_ informações de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) do assinante da mensagem.</span><span class="sxs-lookup"><span data-stu-id="b158d-114">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in the message handle and CMSG\_SIGNER\_CERT\_INFO\_PARAM to get the signer's [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) from the message.</span></span>
2.  <span data-ttu-id="b158d-115">Chame [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) para abrir um repositório temporário que é inicializado com os certificados da mensagem.</span><span class="sxs-lookup"><span data-stu-id="b158d-115">Call [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) to open a temporary store that is initialized with the certificates from the message.</span></span>
3.  <span data-ttu-id="b158d-116">Chame [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) para obter as informações de [**certificado \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) do assinante dos certificados incluídos na mensagem.</span><span class="sxs-lookup"><span data-stu-id="b158d-116">Call [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) to get the signer's [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) from the certificates included in the message.</span></span>
4.  <span data-ttu-id="b158d-117">Chame [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passando na CMSG \_ Ctrl de \_ verificação de \_ assinatura para verificar as assinaturas.</span><span class="sxs-lookup"><span data-stu-id="b158d-117">Call [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passing in CMSG\_CTRL\_VERIFY\_SIGNATURE to verify the signatures.</span></span>
5.  <span data-ttu-id="b158d-118">Chame [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) para fechar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="b158d-118">Call [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) to close the message.</span></span>

<span data-ttu-id="b158d-119">O resultado desses procedimentos é que a assinatura é verificada e um ponteiro é recuperado para o conteúdo da mensagem decodificada obtido na etapa 4 do procedimento para decodificar uma mensagem assinada.</span><span class="sxs-lookup"><span data-stu-id="b158d-119">The result of these procedures is that the signature is verified and a pointer is retrieved to the decoded message content obtained in step 4 of the procedure for decoding a signed message.</span></span>

<span data-ttu-id="b158d-120">Para obter detalhes de codificação C, consulte [exemplo c programa: assinatura, codificação, decodificação e verificação de uma mensagem](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).</span><span class="sxs-lookup"><span data-stu-id="b158d-120">For C coding details, see [Example C Program: Signing, Encoding, Decoding, and Verifying a Message](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).</span></span>

 

 
