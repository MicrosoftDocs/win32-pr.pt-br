---
description: Cert2SPC
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1680f8fe426c2e3a62cac0674928a1520b402357
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105756687"
---
# <a name="cert2spc"></a><span data-ttu-id="763a2-103">Cert2SPC</span><span class="sxs-lookup"><span data-stu-id="763a2-103">Cert2SPC</span></span>

<span data-ttu-id="763a2-104">A ferramenta Cert2SPC cria um certificado de teste do [*fornecedor de software*](../secgloss/s-gly.md) (SPC) usando [*certificados*](../secgloss/c-gly.md) [*X. 509*](../secgloss/x-gly.md) existentes.</span><span class="sxs-lookup"><span data-stu-id="763a2-104">The Cert2SPC tool creates a test [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) by using existing [*X.509*](../secgloss/x-gly.md) [*certificates*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="763a2-105">Cert2SPC pode encapsular vários certificados X. 509 em um objeto de dados assinado [*PKCS \# 7*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="763a2-105">Cert2SPC can wrap multiple X.509 certificates into a [*PKCS \#7*](../secgloss/p-gly.md) signed-data object.</span></span> <span data-ttu-id="763a2-106">A ferramenta é instalada na \\ pasta bin do caminho de instalação do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="763a2-106">The tool is installed in the \\Bin folder of the Microsoft Windows Software Development Kit (SDK) installation path.</span></span>

<span data-ttu-id="763a2-107">O Cert2SPC está disponível como parte do SDK do Windows, do qual você pode baixar <https://go.microsoft.com/fwlink/p/?linkid=84091> .</span><span class="sxs-lookup"><span data-stu-id="763a2-107">Cert2SPC is available as part of the Windows SDK, which you can download from <https://go.microsoft.com/fwlink/p/?linkid=84091>.</span></span>

> [!Note]
> <span data-ttu-id="763a2-108">Essa ferramenta é apenas para fins de teste.</span><span class="sxs-lookup"><span data-stu-id="763a2-108">This tool is for test purposes only.</span></span> <span data-ttu-id="763a2-109">Um SPC válido é obtido de uma [*autoridade de certificação*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="763a2-109">A valid SPC is obtained from a [*certification authority*](../secgloss/c-gly.md).</span></span>


<span data-ttu-id="763a2-110">**Cert2SPC** *Cert1. cer Cert2. cer* ...</span><span class="sxs-lookup"><span data-stu-id="763a2-110">**Cert2SPC** *Cert1.cer Cert2.cer* …</span></span> <span data-ttu-id="763a2-111">*Output. SPC*</span><span class="sxs-lookup"><span data-stu-id="763a2-111">*Output.spc*</span></span>

 



|                         |                                                                                                                                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="763a2-112">*Cert1. cer Cert2. cer* ...</span><span class="sxs-lookup"><span data-stu-id="763a2-112">*Cert1.cer Cert2.cer* …</span></span> | <span data-ttu-id="763a2-113">Nomes dos certificados X. 509 a serem incluídos no SPC.</span><span class="sxs-lookup"><span data-stu-id="763a2-113">Names of the X.509 certificates to include in the SPC.</span></span> <span data-ttu-id="763a2-114">Cada nome de certificado termina com a extensão. cer.</span><span class="sxs-lookup"><span data-stu-id="763a2-114">Each certificate name ends with the .cer extension.</span></span>                         |
| <span data-ttu-id="763a2-115">*Output. SPC*</span><span class="sxs-lookup"><span data-stu-id="763a2-115">*Output.spc*</span></span>            | <span data-ttu-id="763a2-116">Nome do objeto PKCS \# 7 que contém os certificados X. 509 a serem criados.</span><span class="sxs-lookup"><span data-stu-id="763a2-116">Name of the PKCS \#7 object that contains the X.509 certificates to be created.</span></span> <span data-ttu-id="763a2-117">O nome do arquivo de saída termina com a extensão. SPC.</span><span class="sxs-lookup"><span data-stu-id="763a2-117">The output file name ends with the .spc extension.</span></span> |



 

 

 
