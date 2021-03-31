---
description: As ferramentas de CryptoAPI são ferramentas para executar tarefas comuns de gerenciamento de certificados.
ms.assetid: 29146de8-adae-444b-bc75-fa43a19ab8f9
title: Ferramentas para criar, exibir e gerenciar certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2fb4595b7c7711b10271bd97a447a77f3a01c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663196"
---
# <a name="tools-to-create-view-and-manage-certificates"></a><span data-ttu-id="1ac4e-103">Ferramentas para criar, exibir e gerenciar certificados</span><span class="sxs-lookup"><span data-stu-id="1ac4e-103">Tools to Create, View, and Manage Certificates</span></span>

<span data-ttu-id="1ac4e-104">As ferramentas de CryptoAPI são ferramentas para executar tarefas comuns de gerenciamento de certificados.</span><span class="sxs-lookup"><span data-stu-id="1ac4e-104">CryptoAPI Tools are tools to perform common certificate management tasks.</span></span>



| <span data-ttu-id="1ac4e-105">Ferramenta</span><span class="sxs-lookup"><span data-stu-id="1ac4e-105">Tool</span></span>                                | <span data-ttu-id="1ac4e-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ac4e-106">Remarks</span></span>                                                                                                                                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ac4e-107">MakeCert</span><span class="sxs-lookup"><span data-stu-id="1ac4e-107">MakeCert</span></span>](makecert.md)<br/> | <span data-ttu-id="1ac4e-108">Cria um certificado [*X. 509*](../secgloss/x-gly.md) de teste.</span><span class="sxs-lookup"><span data-stu-id="1ac4e-108">Creates a test [*X.509*](../secgloss/x-gly.md) certificate.</span></span><br/>                                                                                |
| [<span data-ttu-id="1ac4e-109">Cert2SPC</span><span class="sxs-lookup"><span data-stu-id="1ac4e-109">Cert2SPC</span></span>](cert2spc.md)<br/> | <span data-ttu-id="1ac4e-110">Cria um [*certificado do Publicador de software*](../secgloss/s-gly.md) de teste (SPC).</span><span class="sxs-lookup"><span data-stu-id="1ac4e-110">Creates a test [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC).</span></span><br/>           |
| [<span data-ttu-id="1ac4e-111">CertMgr</span><span class="sxs-lookup"><span data-stu-id="1ac4e-111">CertMgr</span></span>](certmgr.md)<br/>   | <span data-ttu-id="1ac4e-112">Gerencia certificados, CTLs e listas de certificados [*revogados*](../secgloss/c-gly.md) (CRLs).</span><span class="sxs-lookup"><span data-stu-id="1ac4e-112">Manages certificates, CTLs, and [*certificate revocation lists*](../secgloss/c-gly.md) (CRLs).</span></span><br/> |



 

<span data-ttu-id="1ac4e-113">Todas as entradas do usuário para essas ferramentas não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1ac4e-113">All user input to these tools is case insensitive.</span></span> <span data-ttu-id="1ac4e-114">As opções separadas agora existem para o nome do [*par de chaves*](../secgloss/k-gly.md) e o arquivo de [*chave privada*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="1ac4e-114">Separate options now exist for the [*key pair*](../secgloss/k-gly.md) name and the [*private key*](../secgloss/p-gly.md) file.</span></span>

## <a name="additional-tools"></a><span data-ttu-id="1ac4e-115">Ferramentas adicionais</span><span class="sxs-lookup"><span data-stu-id="1ac4e-115">Additional Tools</span></span>

<span data-ttu-id="1ac4e-116">Certutil.exe é uma ferramenta de linha de comando instalada como parte dos serviços de certificados.</span><span class="sxs-lookup"><span data-stu-id="1ac4e-116">Certutil.exe is a command-line tool that is installed as part of Certificate Services.</span></span> <span data-ttu-id="1ac4e-117">Você pode usar Certutil.exe para despejar e exibir informações de configuração da AC ( [*autoridade de certificação*](../secgloss/c-gly.md) ), configurar os serviços de certificados, fazer backup e restaurar os componentes da AC e verificar [*certificados*](../secgloss/c-gly.md), [*pares de chaves*](../secgloss/k-gly.md)e cadeias de certificados.</span><span class="sxs-lookup"><span data-stu-id="1ac4e-117">You can use Certutil.exe to dump and display [*certification authority*](../secgloss/c-gly.md) (CA) configuration information, configure Certificate Services, back up and restore CA components, and verify [*certificates*](../secgloss/c-gly.md), [*key pairs*](../secgloss/k-gly.md), and certificate chains.</span></span> <span data-ttu-id="1ac4e-118">Para obter mais informações sobre o Certutil, consulte o tópico [certutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732443(v=ws.11)) no Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="1ac4e-118">For more information about Certutil, see the [Certutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732443(v=ws.11)) topic on Microsoft TechNet.</span></span>

 

 
