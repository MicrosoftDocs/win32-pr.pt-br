---
description: Cert2SPC
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 419f0e6dc6f1183252f138029dadc7817ac3b5ed
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581974"
---
# <a name="cert2spc"></a><span data-ttu-id="2c1a2-103">Cert2SPC</span><span class="sxs-lookup"><span data-stu-id="2c1a2-103">Cert2SPC</span></span>

<span data-ttu-id="2c1a2-104">A ferramenta Cert2SPC cria um SPC [*(Certificado*](../secgloss/s-gly.md) Publisher software) de teste usando certificados [*X.509*](../secgloss/x-gly.md) [*existentes.*](../secgloss/c-gly.md)</span><span class="sxs-lookup"><span data-stu-id="2c1a2-104">The Cert2SPC tool creates a test [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) by using existing [*X.509*](../secgloss/x-gly.md) [*certificates*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="2c1a2-105">Cert2SPC pode envolver vários certificados X.509 em um objeto de dados assinados [*PKCS \# 7.*](../secgloss/p-gly.md)</span><span class="sxs-lookup"><span data-stu-id="2c1a2-105">Cert2SPC can wrap multiple X.509 certificates into a [*PKCS \#7*](../secgloss/p-gly.md) signed-data object.</span></span> <span data-ttu-id="2c1a2-106">A ferramenta é instalada na pasta Bin do caminho de instalação do \\ SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2c1a2-106">The tool is installed in the \\Bin folder of the Microsoft Windows Software Development Kit (SDK) installation path.</span></span>

<span data-ttu-id="2c1a2-107">O Cert2SPC está disponível como parte do SDK do Windows, que você pode baixar do <https://go.microsoft.com/fwlink/p/?linkid=84091> .</span><span class="sxs-lookup"><span data-stu-id="2c1a2-107">Cert2SPC is available as part of the Windows SDK, which you can download from <https://go.microsoft.com/fwlink/p/?linkid=84091>.</span></span>

> [!Note]
> <span data-ttu-id="2c1a2-108">Essa ferramenta é apenas para fins de teste.</span><span class="sxs-lookup"><span data-stu-id="2c1a2-108">This tool is for test purposes only.</span></span> <span data-ttu-id="2c1a2-109">Um SPC válido é obtido de uma autoridade de [*certificação*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2c1a2-109">A valid SPC is obtained from a [*certification authority*](../secgloss/c-gly.md).</span></span>


<span data-ttu-id="2c1a2-110">**Cert2SPC** *Cert1.cer Cert2.cer...*</span><span class="sxs-lookup"><span data-stu-id="2c1a2-110">**Cert2SPC** *Cert1.cer Cert2.cer* …</span></span> <span data-ttu-id="2c1a2-111">*Output.spc*</span><span class="sxs-lookup"><span data-stu-id="2c1a2-111">*Output.spc*</span></span>

 



| <span data-ttu-id="2c1a2-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c1a2-112">Parameters</span></span>              | <span data-ttu-id="2c1a2-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="2c1a2-113">Description</span></span>                                                                                                                        |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c1a2-114">*Cert1.cer Cert2.cer...*</span><span class="sxs-lookup"><span data-stu-id="2c1a2-114">*Cert1.cer Cert2.cer* …</span></span> | <span data-ttu-id="2c1a2-115">Nomes dos certificados X.509 a incluir no SPC.</span><span class="sxs-lookup"><span data-stu-id="2c1a2-115">Names of the X.509 certificates to include in the SPC.</span></span> <span data-ttu-id="2c1a2-116">Cada nome de certificado termina com a extensão .cer.</span><span class="sxs-lookup"><span data-stu-id="2c1a2-116">Each certificate name ends with the .cer extension.</span></span>                         |
| <span data-ttu-id="2c1a2-117">*Output.spc*</span><span class="sxs-lookup"><span data-stu-id="2c1a2-117">*Output.spc*</span></span>            | <span data-ttu-id="2c1a2-118">Nome do objeto PKCS \# 7 que contém os certificados X.509 a serem criados.</span><span class="sxs-lookup"><span data-stu-id="2c1a2-118">Name of the PKCS \#7 object that contains the X.509 certificates to be created.</span></span> <span data-ttu-id="2c1a2-119">O nome do arquivo de saída termina com a extensão .spc.</span><span class="sxs-lookup"><span data-stu-id="2c1a2-119">The output file name ends with the .spc extension.</span></span> |



 

 

 
