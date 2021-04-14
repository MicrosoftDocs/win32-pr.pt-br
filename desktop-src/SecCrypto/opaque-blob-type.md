---
description: BLOBs opacos, também conhecidos como OPAQUEKEYBLOBs, são usados para armazenar chaves de sessão em um formato específico de fornecedor, como Schannel.
ms.assetid: a0756c03-0c27-41ff-9b74-8af462e09675
title: Tipo de BLOB opaco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e45cf8899d5cc63fb360a6b5e4177733de3880f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370775"
---
# <a name="opaque-blob-type"></a><span data-ttu-id="dfb35-103">Tipo de BLOB opaco</span><span class="sxs-lookup"><span data-stu-id="dfb35-103">Opaque BLOB Type</span></span>

<span data-ttu-id="dfb35-104">[*BLOBs opacos*](../secgloss/o-gly.md), também conhecidos como OPAQUEKEYBLOBs, são usados para armazenar [*chaves de sessão*](../secgloss/s-gly.md) em um formato específico de fornecedor, como [*Schannel*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="dfb35-104">[*Opaque BLOBs*](../secgloss/o-gly.md), also known as OPAQUEKEYBLOBs, are used to store [*session keys*](../secgloss/s-gly.md) in a vendor-specific format, such as [*Schannel*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="dfb35-105">Eles contêm o material de chave base e todas as informações de [*estado*](../secgloss/s-gly.md) atuais.</span><span class="sxs-lookup"><span data-stu-id="dfb35-105">They contain the base key material and all current [*state*](../secgloss/s-gly.md) information.</span></span> <span data-ttu-id="dfb35-106">Isso inclui informações como o [*valor salt*](../secgloss/s-gly.md), o [*vetor de inicialização*](../secgloss/i-gly.md)e a tabela de chave.</span><span class="sxs-lookup"><span data-stu-id="dfb35-106">This includes information such as the [*salt value*](../secgloss/s-gly.md), the [*initialization vector*](../secgloss/i-gly.md), and the key table.</span></span> <span data-ttu-id="dfb35-107">O formato dos BLOBs opacos não é publicado.</span><span class="sxs-lookup"><span data-stu-id="dfb35-107">The format of opaque BLOBs is unpublished.</span></span> <span data-ttu-id="dfb35-108">Cada fornecedor do CSP determina seu próprio formato de BLOB.</span><span class="sxs-lookup"><span data-stu-id="dfb35-108">Each CSP vendor determines its own BLOB format.</span></span>

<span data-ttu-id="dfb35-109">Como uma chave é exportada para um BLOB opaco no formato específico do CSP, ela só pode ser importada para o CSP do qual foi exportada originalmente.</span><span class="sxs-lookup"><span data-stu-id="dfb35-109">Because a key is exported into an opaque BLOB in CSP-specific format, it can only be imported into the CSP from which it was originally exported.</span></span>

<span data-ttu-id="dfb35-110">Quando dois processos estão envolvidos, cada [*processo*](../secgloss/p-gly.md) chama o [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) de forma independente.</span><span class="sxs-lookup"><span data-stu-id="dfb35-110">When two processes are involved, each [*process*](../secgloss/p-gly.md) calls [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) independently.</span></span> <span data-ttu-id="dfb35-111">Cada processo Obtém um identificador para um contêiner de chave.</span><span class="sxs-lookup"><span data-stu-id="dfb35-111">Each process gets a handle to a key container.</span></span> <span data-ttu-id="dfb35-112">É possível que ambos os processos tenham identificadores para o mesmo contêiner de chave.</span><span class="sxs-lookup"><span data-stu-id="dfb35-112">It is possible for both processes to have handles to the same key container.</span></span> <span data-ttu-id="dfb35-113">Um processo cria as chaves e as exporta em BLOBs opacos e, em seguida, passa os BLOBs para o segundo processo.</span><span class="sxs-lookup"><span data-stu-id="dfb35-113">One process creates the keys and exports them into opaque BLOBs, then passes the BLOBs to the second process.</span></span> <span data-ttu-id="dfb35-114">O segundo processo importa as chaves do BLOB para seu [*contêiner de chave*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="dfb35-114">The second process imports the keys from the BLOB into its [*key container*](../secgloss/k-gly.md).</span></span>

<span data-ttu-id="dfb35-115">Se um CSP de hardware não oferecer suporte à exportação de chaves, o BLOB poderá conter apenas o índice de um registro de chave ou algo semelhante.</span><span class="sxs-lookup"><span data-stu-id="dfb35-115">If a hardware CSP does not support exporting keys, the BLOB might only contain the index of a key register, or something similar.</span></span> <span data-ttu-id="dfb35-116">Nesse caso, o restante do procedimento é ignorado.</span><span class="sxs-lookup"><span data-stu-id="dfb35-116">In this case, the rest of the procedure is ignored.</span></span>

``` syntax
<secure process>
cbBlob = sizeof(rgbBlob);
CryptExportKey(
          hKey, 
          0, 
          OPAQUEKEYBLOB, 
          0, 
          rgbBlob, 
          &cbBlob);
hKey = 0;

<BLOB is transferred to other process>

<user process>
CryptImportKey(
            hProv, 
            pbBlob, 
            cbBlob, 
            0, 
            0, 
            &hKey);
```

 

 
