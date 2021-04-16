---
description: O comando a seguir encapsula um certificado X. 509, MyCert. cer, em um \# SPC (certificado de editor de software) PKCS 7, chamado MyCert. SPC.
ms.assetid: c3287289-d2bf-4d1d-80f0-e7dd41a3cbe3
title: Usando Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca10b0ab121e283a181c84b056b63ce10ece385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502178"
---
# <a name="using-cert2spc"></a><span data-ttu-id="3b88f-103">Usando Cert2SPC</span><span class="sxs-lookup"><span data-stu-id="3b88f-103">Using Cert2SPC</span></span>

<span data-ttu-id="3b88f-104">O comando a seguir encapsula um certificado [*X. 509*](../secgloss/x-gly.md) , *MyCert*. cer, em um \# SPC ( [*certificado de editor de software*](../secgloss/s-gly.md) ) PKCS 7, chamado *MyCert*. SPC.</span><span class="sxs-lookup"><span data-stu-id="3b88f-104">The following command wraps an [*X.509*](../secgloss/x-gly.md) certificate, *MyCert*.cer, into a test PKCS \#7 [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC), called *MyCert*.spc.</span></span> <span data-ttu-id="3b88f-105">O SPC criado deve ser usado apenas para fins de teste.</span><span class="sxs-lookup"><span data-stu-id="3b88f-105">The SPC created is to be used for test purposes only.</span></span> <span data-ttu-id="3b88f-106">Um SPC usado para realmente assinar o código a ser distribuído para o público deve ser obtido em GTE, VeriSign, Inc. ou outra [*autoridade de certificação*](../secgloss/c-gly.md) (CA) confiável.</span><span class="sxs-lookup"><span data-stu-id="3b88f-106">An SPC used to actually sign code to be distributed to the public must be obtained from GTE, VeriSign, Inc., or another trusted [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="3b88f-107">**Cert2SPC** \*MyCert \* \* *. cer* \*  *MyCert \* \* *. SPC**</span><span class="sxs-lookup"><span data-stu-id="3b88f-107">**Cert2SPC** *MyCert\*\*\*.cer*\* *MyCert\*\*\*.spc*\*</span></span>

 

 
