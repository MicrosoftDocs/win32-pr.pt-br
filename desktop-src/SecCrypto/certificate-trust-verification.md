---
description: Deve existir uma relação de confiança entre o destinatário de uma mensagem assinada e o signatário da mensagem.
ms.assetid: 770e4674-8896-4062-a93a-a17bd30a9129
title: Verificação de confiança de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b711e0a86dcc5ae9cdedea278d6a3a698dfd633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758020"
---
# <a name="certificate-trust-verification"></a><span data-ttu-id="6f176-103">Verificação de confiança de certificado</span><span class="sxs-lookup"><span data-stu-id="6f176-103">Certificate Trust Verification</span></span>

<span data-ttu-id="6f176-104">Deve existir uma relação de confiança entre o destinatário de uma mensagem assinada e o signatário da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6f176-104">A trust must exist between the recipient of a signed message and the signer of the message.</span></span> <span data-ttu-id="6f176-105">Um método de estabelecer essa confiança é por meio de um [*certificado*](../secgloss/c-gly.md), um documento eletrônico que verifica se as entidades ou as pessoas são quem afirma ser.</span><span class="sxs-lookup"><span data-stu-id="6f176-105">One method of establishing this trust is through a [*certificate*](../secgloss/c-gly.md), an electronic document verifying that entities or persons are who they claim to be.</span></span> <span data-ttu-id="6f176-106">Um certificado é emitido para uma entidade por terceiros que é confiável para ambas as partes.</span><span class="sxs-lookup"><span data-stu-id="6f176-106">A certificate is issued to an entity by a third party that is trusted by both of the other parties.</span></span> <span data-ttu-id="6f176-107">Portanto, cada destinatário de uma mensagem assinada decide se o emissor do certificado do signatário é confiável.</span><span class="sxs-lookup"><span data-stu-id="6f176-107">So, each recipient of a signed message decides if the issuer of the signer's certificate is trustworthy.</span></span> <span data-ttu-id="6f176-108">O [*CryptoAPI*](../secgloss/c-gly.md) implementou uma metodologia para permitir que os desenvolvedores de aplicativos criem aplicativos que verificam automaticamente os certificados em relação a uma lista predefinida de certificados ou [*raízes*](../secgloss/r-gly.md)confiáveis.</span><span class="sxs-lookup"><span data-stu-id="6f176-108">[*CryptoAPI*](../secgloss/c-gly.md) has implemented a methodology to allow application developers to create applications that automatically verify certificates against a predefined list of trusted certificates or [*roots*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="6f176-109">Essa lista de entidades confiáveis (chamadas de entidades) é chamada de [*lista de certificados confiáveis*](../secgloss/c-gly.md) (CTL).</span><span class="sxs-lookup"><span data-stu-id="6f176-109">This list of trusted entities (called subjects) is called a [*certificate trust list*](../secgloss/c-gly.md) (CTL).</span></span>

<span data-ttu-id="6f176-110">O exemplo a seguir de como usar uma CTL envolve um administrador de intranet (rede intra-empresa) que deseja controlar apenas quais fontes externas são confiáveis.</span><span class="sxs-lookup"><span data-stu-id="6f176-110">The following example of using a CTL involves an intranet (intra-company network) administrator who wants to control just which outside sources are trusted.</span></span> <span data-ttu-id="6f176-111">Nesse caso, o administrador pode criar uma lista de certificados ou raízes confiáveis, assinar e tornar a lista disponível para todos os clientes na rede na forma de uma CTL.</span><span class="sxs-lookup"><span data-stu-id="6f176-111">In this case, the administrator can create a list of trusted certificates or roots, sign it, and make the list available to all clients on the network in the form of a CTL.</span></span> <span data-ttu-id="6f176-112">Um aplicativo criado para usar essa funcionalidade de CryptoAPI aceitará apenas mensagens assinadas ou um software baixado que foi assinado por entidades na lista.</span><span class="sxs-lookup"><span data-stu-id="6f176-112">An application designed to use this CryptoAPI functionality would then only accept signed messages or downloaded software that was signed by entities on the list.</span></span>

<span data-ttu-id="6f176-113">Para obter uma lista dessas funções, consulte [funções de verificação de certificado](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6f176-113">For a list of these functions, see [Certificate Verification Functions](cryptography-functions.md).</span></span>

 

 
