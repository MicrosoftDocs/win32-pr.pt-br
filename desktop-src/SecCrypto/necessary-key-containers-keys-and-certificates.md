---
description: Os programas de exemplo nas seções a seguir executam operações que exigem a disponibilidade de pares de chaves pública/privada para criptografar e descriptografar arquivos, mensagens e assinaturas.
ms.assetid: b03528ff-0170-4dde-ae35-f5c3951d6b1f
title: Contêineres de chave, chaves e certificados necessários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d1f01a59c83ea21437608608e033a2ee0f8fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663143"
---
# <a name="necessary-key-containers-keys-and-certificates"></a><span data-ttu-id="27e0a-103">Contêineres de chave, chaves e certificados necessários</span><span class="sxs-lookup"><span data-stu-id="27e0a-103">Necessary Key Containers, Keys, and Certificates</span></span>

<span data-ttu-id="27e0a-104">Os programas de exemplo nas seções a seguir executam operações que exigem a disponibilidade de [*pares de chaves pública/privada*](../secgloss/p-gly.md) para criptografar e descriptografar arquivos, mensagens e assinaturas.</span><span class="sxs-lookup"><span data-stu-id="27e0a-104">Example programs in the following sections perform operations that require [*public/private key pairs*](../secgloss/p-gly.md) to be available for encrypting and decrypting files, messages, and signatures.</span></span> <span data-ttu-id="27e0a-105">Muitos desses programas serão compilados, vinculados e executados, mas falharão em tempo de execução sem a existência de [*contêineres de chave*](../secgloss/k-gly.md), chaves, [*repositórios de certificados*](../secgloss/c-gly.md)e certificados apropriados nesses armazenamentos.</span><span class="sxs-lookup"><span data-stu-id="27e0a-105">Many of these programs will compile, link, and run but fail at run time without the existence of proper [*key containers*](../secgloss/k-gly.md), keys, [*certificate stores*](../secgloss/c-gly.md), and certificates in those stores.</span></span>

<span data-ttu-id="27e0a-106">Além disso, alguns dos certificados no meu repositório devem ter algumas das suas propriedades estendidas definidas.</span><span class="sxs-lookup"><span data-stu-id="27e0a-106">In addition, some of the certificates in the MY store must have some of their extended properties set.</span></span>

<span data-ttu-id="27e0a-107">A criação do contêiner de chave padrão necessário pode ser feita executando o programa no [programa C de exemplo: Criando um contêiner de chave e gerando chaves](example-c-program-creating-a-key-container-and-generating-keys.md).</span><span class="sxs-lookup"><span data-stu-id="27e0a-107">Creating the needed default key container can be done by running the program in [Example C Program: Creating a Key Container and Generating Keys](example-c-program-creating-a-key-container-and-generating-keys.md).</span></span> <span data-ttu-id="27e0a-108">Observe que a criação de um contêiner de chave não gera automaticamente pares de chaves pública/privada.</span><span class="sxs-lookup"><span data-stu-id="27e0a-108">Note that the creation of a key container does not automatically generate public/private key pairs.</span></span> <span data-ttu-id="27e0a-109">O programa de exemplo, no entanto, cria o contêiner de chave e gera os pares de chaves pública/privada.</span><span class="sxs-lookup"><span data-stu-id="27e0a-109">The example program, however, both creates the key container and generates the public/private key pairs.</span></span>

<span data-ttu-id="27e0a-110">Após os pares de chaves pública/privada terem sido gerados, os certificados de teste usando essas chaves podem ser obtidos de uma [*autoridade de certificação*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="27e0a-110">After public/private key pairs have been generated, test certificates using those keys can be obtained from a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="27e0a-111">Vários dos programas pressupõem que os certificados com nomes de entidades específicos existam no repositório do meu sistema.</span><span class="sxs-lookup"><span data-stu-id="27e0a-111">Several of the programs assume that certificates with specific subject names exist in the MY system store.</span></span> <span data-ttu-id="27e0a-112">Em particular, vários programas procuram certificados com os nomes de assunto "certificado de teste completo" e "Hortense".</span><span class="sxs-lookup"><span data-stu-id="27e0a-112">In particular, several programs look for certificates with the subject names "Full Test Cert" and "Hortense."</span></span> <span data-ttu-id="27e0a-113">Os nomes de entidade para os certificados podem ser alterados no código para corresponder aos nomes de entidades de certificados existentes no repositório meu certificado.</span><span class="sxs-lookup"><span data-stu-id="27e0a-113">The subject names for the certificates may be changed in the code to match the subject names of certificates that exist in the MY certificate store.</span></span>

<span data-ttu-id="27e0a-114">Executando o programa de exemplo no [programa C de exemplo: listar os certificados em um repositório](example-c-program-listing-the-certificates-in-a-store.md) exibirá todos os certificados em um repositório e todas as propriedades estendidas definidas nesses certificados.</span><span class="sxs-lookup"><span data-stu-id="27e0a-114">Running the example program in [Example C Program: Listing the Certificates in a Store](example-c-program-listing-the-certificates-in-a-store.md) will display all of the certificates in a store and all of the extended properties that are set on those certificates.</span></span>

 

 
