---
description: A ferramenta SetReg define o valor das chaves do registro que controlam o comportamento do processo de verificação do certificado Authenticode.
ms.assetid: c34c00fe-da99-4c2e-9e9a-0ef6406ae5ae
title: Usando SetReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706463f86d38a03bc3416713be7427df55424d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090915"
---
# <a name="using-setreg"></a><span data-ttu-id="69d34-103">Usando SetReg</span><span class="sxs-lookup"><span data-stu-id="69d34-103">Using SetReg</span></span>

<span data-ttu-id="69d34-104">A ferramenta SetReg define o valor das chaves do registro que controlam o comportamento do processo de verificação do certificado Authenticode.</span><span class="sxs-lookup"><span data-stu-id="69d34-104">The SetReg tool sets the value of the registry keys controlling the behavior of the Authenticode certificate verification process.</span></span> <span data-ttu-id="69d34-105">Essas chaves, chamadas de chaves de estado de publicação de software, controlam se deve confiar em uma raiz de teste, permitir a aprovação offline de certificados, testar as datas de validade do certificado e executar verificações de revogação.</span><span class="sxs-lookup"><span data-stu-id="69d34-105">These keys, called the Software Publishing State Keys, control whether to trust a test root, allow offline approval of certificates, test certificate expiration dates, and perform revocation checks.</span></span>

<span data-ttu-id="69d34-106">O comando a seguir lista a sintaxe e as opções para usar o SetReg.</span><span class="sxs-lookup"><span data-stu-id="69d34-106">The following command lists the syntax and options for using SetReg.</span></span>

<span data-ttu-id="69d34-107">**setreg-?**</span><span class="sxs-lookup"><span data-stu-id="69d34-107">**setreg -?**</span></span>

<span data-ttu-id="69d34-108">O comando a seguir torna uma raiz de teste confiável.</span><span class="sxs-lookup"><span data-stu-id="69d34-108">The following command makes a test root trusted.</span></span> <span data-ttu-id="69d34-109">Por padrão, uma raiz de teste não é confiável.</span><span class="sxs-lookup"><span data-stu-id="69d34-109">By default, a test root is not trusted.</span></span> <span data-ttu-id="69d34-110">Depois que qualquer alteração nos valores de chave for feita, uma lista do valor atual de todos os valores de chave será exibida.</span><span class="sxs-lookup"><span data-stu-id="69d34-110">After any changes in the key values are made, a list of the current value of all of the key values is displayed.</span></span> <span data-ttu-id="69d34-111">Se a opção **-q** for usada, os valores de chave não serão exibidos.</span><span class="sxs-lookup"><span data-stu-id="69d34-111">If the **-q** option is used, the key values are not displayed.</span></span>

<span data-ttu-id="69d34-112">**setreg 1 verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="69d34-112">**setreg 1 TRUE**</span></span>

<span data-ttu-id="69d34-113">O comando a seguir torna uma raiz de teste não confiável e faz com que toda a verificação Verifique a revogação.</span><span class="sxs-lookup"><span data-stu-id="69d34-113">The following command makes a test root untrusted and causes all verification to check for revocation.</span></span> <span data-ttu-id="69d34-114">A opção **-q** é usada para que a lista de valores de chave não seja exibida</span><span class="sxs-lookup"><span data-stu-id="69d34-114">The **-q** option is used so that the list of key values is not displayed</span></span>

<span data-ttu-id="69d34-115">**setreg-q 1 FALSE 3 TRUE**</span><span class="sxs-lookup"><span data-stu-id="69d34-115">**setreg -q 1 FALSE 3 TRUE**</span></span>

> [!Note]  
> <span data-ttu-id="69d34-116">Comandos, opções e argumentos não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="69d34-116">Commands, options, and arguments are not case sensitive.</span></span>

 

 

 



