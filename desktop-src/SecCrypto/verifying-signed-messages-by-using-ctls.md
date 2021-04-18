---
description: Uma das vantagens de usar listas de certificados confiáveis (CTLs) é que os aplicativos podem ser criados para verificar automaticamente as mensagens assinadas em relação a certificados confiáveis sem incomodarr o usuário com caixas de diálogo.
ms.assetid: e45ea3ae-52bc-49d3-8144-f3becc254f53
title: Verificando mensagens assinadas usando CTLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a660bcd7e17a168b25048e61684aabc2d3ef3124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760378"
---
# <a name="verifying-signed-messages-by-using-ctls"></a><span data-ttu-id="3b03e-103">Verificando mensagens assinadas usando CTLs</span><span class="sxs-lookup"><span data-stu-id="3b03e-103">Verifying Signed Messages by Using CTLs</span></span>

<span data-ttu-id="3b03e-104">Uma das vantagens de usar [*listas de certificados confiáveis*](../secgloss/c-gly.md) (CTLs) é que os aplicativos podem ser criados para verificar automaticamente as mensagens assinadas em relação a certificados confiáveis sem incomodarr o usuário com caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3b03e-104">One of the advantages of using [*certificate trust lists*](../secgloss/c-gly.md) (CTLs) is that applications can be designed that can automatically verify signed messages against trusted certificates without bothering the user with dialog boxes.</span></span> <span data-ttu-id="3b03e-105">Ele também fornece a confiança de fontes de controle de administrador de rede.</span><span class="sxs-lookup"><span data-stu-id="3b03e-105">It also gives a network administrator control sources to be trusted.</span></span>

<span data-ttu-id="3b03e-106">O procedimento a seguir pode ser usado para verificar a assinatura de uma mensagem assinada usando uma CTL.</span><span class="sxs-lookup"><span data-stu-id="3b03e-106">The following procedure can be used to verify the signature of a signed message by using a CTL.</span></span>

<span data-ttu-id="3b03e-107">**Para verificar uma mensagem assinada usando uma CTL**</span><span class="sxs-lookup"><span data-stu-id="3b03e-107">**To verify a signed message by using a CTL**</span></span>

1.  <span data-ttu-id="3b03e-108">Decodifique a mensagem da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="3b03e-108">Decode the message as follows:</span></span>

    1.  <span data-ttu-id="3b03e-109">Obtenha um ponteiro para a mensagem recebida (o [*blob*](../secgloss/b-gly.md)codificado).</span><span class="sxs-lookup"><span data-stu-id="3b03e-109">Get a pointer to the received message (the encoded [*BLOB*](../secgloss/b-gly.md)).</span></span>
    2.  <span data-ttu-id="3b03e-110">Chame [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passando os argumentos necessários.</span><span class="sxs-lookup"><span data-stu-id="3b03e-110">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passing the necessary arguments.</span></span>
    3.  <span data-ttu-id="3b03e-111">Chame [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) uma vez, passando o identificador recuperado na etapa b e um ponteiro para os dados que serão decodificados.</span><span class="sxs-lookup"><span data-stu-id="3b03e-111">Call [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) once, passing in the handle retrieved in step b and a pointer to the data that is to be decoded.</span></span> <span data-ttu-id="3b03e-112">Isso faz com que as ações apropriadas sejam executadas na mensagem, dependendo do tipo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="3b03e-112">This causes the appropriate actions to be taken on the message, depending on the message type.</span></span>

2.  <span data-ttu-id="3b03e-113">Verifique a assinatura da mensagem decodificada, assinada e obtenha um ponteiro para o [**\_ contexto do certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)do Assinante.</span><span class="sxs-lookup"><span data-stu-id="3b03e-113">Verify the signature of the decoded, signed message, and get a pointer to the signer's [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span></span>

    <span data-ttu-id="3b03e-114">Isso pode ser feito chamando [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), passando o identificador de mensagem recuperado na etapa 1C como o parâmetro *hCryptMsg* .</span><span class="sxs-lookup"><span data-stu-id="3b03e-114">This can be done by calling [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), passing the message handle retrieved in step 1c as the *hCryptMsg* parameter.</span></span> <span data-ttu-id="3b03e-115">Se a chamada de função retornar **true**, a assinatura foi verificada e um ponteiro para o [**\_ contexto PCCERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) do signatário será retornado no parâmetro *ppSigner* .</span><span class="sxs-lookup"><span data-stu-id="3b03e-115">If the function call returns **TRUE**, the signature was verified, and a pointer to the signer's [**PCCERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) is returned in the *ppSigner* parameter.</span></span>

3.  <span data-ttu-id="3b03e-116">Confirme se o signatário é uma fonte confiável da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="3b03e-116">Confirm that the signer is a trusted source as follows:</span></span>

    1.  <span data-ttu-id="3b03e-117">Abra o repositório de certificados que contém a CTL apropriada.</span><span class="sxs-lookup"><span data-stu-id="3b03e-117">Open the certificate store containing the appropriate CTL.</span></span>
    2.  <span data-ttu-id="3b03e-118">Obtenha um ponteiro para o [**\_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) chamando [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span><span class="sxs-lookup"><span data-stu-id="3b03e-118">Get a pointer to the [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) by calling [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span></span>
    3.  <span data-ttu-id="3b03e-119">Para confirmar que o signatário é uma fonte confiável, chame [**CertFindSubjectInCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinctl), passando o ponteiro recuperado na etapa anterior no parâmetro *pCtlContext* , o tipo de \_ \_ entidade de certificado CTL \_ no parâmetro *DwSubjectType* e o ponteiro para o [**\_ contexto de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) recuperado na etapa 2 no parâmetro *pvSubject* .</span><span class="sxs-lookup"><span data-stu-id="3b03e-119">To confirm that the signer is a trusted source, call [**CertFindSubjectInCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinctl), passing the pointer retrieved in the previous step in the *pCtlContext* parameter, CTL\_CERT\_SUBJECT\_TYPE in the *dwSubjectType* parameter, and the pointer to the [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) retrieved in step 2 in the *pvSubject* parameter.</span></span> <span data-ttu-id="3b03e-120">Se a chamada de função retornar **true**, **o \_ contexto de certificado** passado para a função será uma fonte confiável na CTL.</span><span class="sxs-lookup"><span data-stu-id="3b03e-120">If the function call returns **TRUE**, the **CERT\_CONTEXT** passed to the function is a trusted source in the CTL.</span></span>

 

 
