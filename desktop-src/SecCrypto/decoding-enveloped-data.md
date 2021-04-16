---
description: Tarefas gerais necessárias para decodificar uma mensagem envelopada.
ms.assetid: cb71ea3a-0edd-4d46-8088-a395fab89d2b
title: Decodificando dados envelopado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1a0ba12e967f5a0cd56347c0839ce9fca40f02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104563039"
---
# <a name="decoding-enveloped-data"></a><span data-ttu-id="06112-103">Decodificando dados envelopado</span><span class="sxs-lookup"><span data-stu-id="06112-103">Decoding Enveloped Data</span></span>

<span data-ttu-id="06112-104">As tarefas gerais necessárias para decodificar uma mensagem envelopada são descritas na ilustração a seguir e descritas na lista que a segue.</span><span class="sxs-lookup"><span data-stu-id="06112-104">The general tasks required to decode an enveloped message are depicted in the following illustration and described in the list that follows it.</span></span>

![decodificando dados envelopado](images/decemsg.png)

<span data-ttu-id="06112-106">A sequência de eventos para decodificar dados envelopos usando o gerenciamento de chaves de transporte de chaves, conforme descrito na ilustração anterior, é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="06112-106">The sequence of events for decoding enveloped data using key transport key management, as depicted in the previous illustration, is as follows:</span></span>

-   <span data-ttu-id="06112-107">Um ponteiro para a mensagem [*digitalmente envelopada*](../secgloss/d-gly.md) é recuperado.</span><span class="sxs-lookup"><span data-stu-id="06112-107">A pointer to the [*digitally enveloped*](../secgloss/d-gly.md) message is retrieved.</span></span>
-   <span data-ttu-id="06112-108">Um [*repositório de certificados*](../secgloss/c-gly.md) é aberto.</span><span class="sxs-lookup"><span data-stu-id="06112-108">A [*certificate store*](../secgloss/c-gly.md) is opened.</span></span>
-   <span data-ttu-id="06112-109">A partir da mensagem, a ID do destinatário (My ID) é recuperada.</span><span class="sxs-lookup"><span data-stu-id="06112-109">From the message, the recipient ID (My ID) is retrieved.</span></span>
-   <span data-ttu-id="06112-110">A ID do destinatário é usada para recuperar o certificado.</span><span class="sxs-lookup"><span data-stu-id="06112-110">The recipient ID is used to retrieve the certificate.</span></span>
-   <span data-ttu-id="06112-111">A [*chave privada*](../secgloss/p-gly.md) associada a esse certificado é recuperada.</span><span class="sxs-lookup"><span data-stu-id="06112-111">The [*private key*](../secgloss/p-gly.md) associated with that certificate is retrieved.</span></span>
-   <span data-ttu-id="06112-112">A chave privada é usada para descriptografar a chave [*simétrica*](../secgloss/s-gly.md) ([*sessão*](../secgloss/s-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="06112-112">The private key is used to decrypt the [*symmetric*](../secgloss/s-gly.md) ([*session*](../secgloss/s-gly.md)) key.</span></span>
-   <span data-ttu-id="06112-113">O algoritmo de criptografia é recuperado da mensagem.</span><span class="sxs-lookup"><span data-stu-id="06112-113">The encryption algorithm is retrieved from the message.</span></span>
-   <span data-ttu-id="06112-114">Usando a chave privada e o algoritmo de criptografia, os dados são descriptografados.</span><span class="sxs-lookup"><span data-stu-id="06112-114">Using the private key and encryption algorithm, the data is decrypted.</span></span>

<span data-ttu-id="06112-115">O procedimento a seguir usa funções de mensagem de nível baixo para realizar as tarefas que você acabou de listar.</span><span class="sxs-lookup"><span data-stu-id="06112-115">The following procedure uses low-level message functions to accomplish the tasks just listed.</span></span>

<span data-ttu-id="06112-116">**Para decodificar uma mensagem envelopada**</span><span class="sxs-lookup"><span data-stu-id="06112-116">**To decode an enveloped message**</span></span>

1.  <span data-ttu-id="06112-117">Obtenha um ponteiro para o BLOB codificado.</span><span class="sxs-lookup"><span data-stu-id="06112-117">Get a pointer to the encoded BLOB.</span></span>
2.  <span data-ttu-id="06112-118">Chame [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passando os argumentos necessários.</span><span class="sxs-lookup"><span data-stu-id="06112-118">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passing the necessary arguments.</span></span>
3.  <span data-ttu-id="06112-119">Chame [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) uma vez, passando o identificador recuperado na etapa 2 e um ponteiro para os dados que serão decodificados.</span><span class="sxs-lookup"><span data-stu-id="06112-119">Call [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) once, passing in the handle retrieved in step 2 and a pointer to the data that is to be decoded.</span></span> <span data-ttu-id="06112-120">Isso faz com que as ações apropriadas sejam executadas na mensagem, dependendo do tipo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="06112-120">This causes the appropriate actions to be taken on the message, depending on the message type.</span></span>
4.  <span data-ttu-id="06112-121">Chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando o identificador recuperado na etapa 2 e CMSG \_ tipo \_ param para verificar se a mensagem é do tipo de dados Envelopado.</span><span class="sxs-lookup"><span data-stu-id="06112-121">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in the handle retrieved in step 2 and CMSG\_TYPE\_PARAM to verify that the message is of the enveloped data type.</span></span>
5.  <span data-ttu-id="06112-122">Novamente, chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando \_ o parâmetro de tipo de conteúdo interno CMSG \_ \_ \_ para obter o tipo de dados do [*conteúdo interno*](../secgloss/i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="06112-122">Again call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in CMSG\_INNER\_CONTENT\_TYPE\_PARAM to get the data type of the [*inner content*](../secgloss/i-gly.md).</span></span>
6.  <span data-ttu-id="06112-123">Se o tipo de dados de conteúdo interno for **dado**, continue a descriptografar e decodificar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="06112-123">If the inner content data type is **data**, proceed to decrypt and decode the content.</span></span> <span data-ttu-id="06112-124">Caso contrário, execute um procedimento de decodificação apropriado para o tipo de dados Content.</span><span class="sxs-lookup"><span data-stu-id="06112-124">Otherwise, run a decoding procedure appropriate for the content data type.</span></span>
7.  <span data-ttu-id="06112-125">Supondo que o tipo de conteúdo interno seja "data", inicialize a estrutura [**CMSG \_ Ctrl \_ Decrypt \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para) dados e chame [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passando CMSG \_ Ctrl \_ Decrypt e o endereço da estrutura.</span><span class="sxs-lookup"><span data-stu-id="06112-125">Assuming the inner content type is "data", initialize the [**CMSG\_CTRL\_DECRYPT\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para) data structure, and call [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passing in CMSG\_CTRL\_DECRYPT and the address of the structure.</span></span> <span data-ttu-id="06112-126">O conteúdo será descriptografado.</span><span class="sxs-lookup"><span data-stu-id="06112-126">The content will be decrypted.</span></span>
8.  <span data-ttu-id="06112-127">Chame [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando no \_ parâmetro de conteúdo CMSG \_ para obter um ponteiro para o blob de dados de conteúdo decodificado (cadeia de caracteres de **byte** ).</span><span class="sxs-lookup"><span data-stu-id="06112-127">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in CMSG\_CONTENT\_PARAM to get a pointer to the decoded content data BLOB (**BYTE** string).</span></span>
9.  <span data-ttu-id="06112-128">Chame [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) para fechar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="06112-128">Call [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) to close the message.</span></span>

<span data-ttu-id="06112-129">O resultado desse procedimento é que a mensagem é decodificada e descriptografada e um ponteiro é recuperado para o BLOB de dados de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="06112-129">The result of this procedure is that the message is decoded and decrypted and a pointer is retrieved to the content data BLOB.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06112-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="06112-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06112-131">Programa C de exemplo: codificando uma mensagem envelopada e assinada</span><span class="sxs-lookup"><span data-stu-id="06112-131">Example C Program: Encoding an Enveloped, Signed Message</span></span>](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
