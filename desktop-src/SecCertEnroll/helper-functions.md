---
description: Cada uma das seções a seguir discute uma função exportada por Xenroll.dll. Cada seção também aborda como usar CertEnroll.dll para substituir a função ou indica que não existe nenhum mapeamento entre as duas bibliotecas.
ms.assetid: 06d8dd6f-7a8d-4da5-a99d-9c9d8fb90cfa
title: Funções auxiliares (API de registro de certificado)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ee272e7b11c3fccf7975c5356302a2961b32ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297198"
---
# <a name="helper-functions-certificate-enrollment-api"></a><span data-ttu-id="b6a8c-104">Funções auxiliares (API de registro de certificado)</span><span class="sxs-lookup"><span data-stu-id="b6a8c-104">Helper Functions (Certificate Enrollment API)</span></span>

<span data-ttu-id="b6a8c-105">Cada uma das seções a seguir discute uma função exportada por Xenroll.dll.</span><span class="sxs-lookup"><span data-stu-id="b6a8c-105">Each of the following sections discusses a function exported by Xenroll.dll.</span></span> <span data-ttu-id="b6a8c-106">Cada seção também aborda como usar CertEnroll.dll para substituir a função ou indica que não existe nenhum mapeamento entre as duas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="b6a8c-106">Each section also discusses how to use CertEnroll.dll to replace the function or indicates that no mapping between the two libraries exists.</span></span>

## <a name="binaryblobtostring"></a><span data-ttu-id="b6a8c-107">binaryBlobToString</span><span class="sxs-lookup"><span data-stu-id="b6a8c-107">binaryBlobToString</span></span>

<span data-ttu-id="b6a8c-108">A função [**binaryBlobToString**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-binaryblobtostring) no Xenroll.dll converte uma matriz de bytes em uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b6a8c-108">The [**binaryBlobToString**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-binaryblobtostring) function in Xenroll.dll converts a byte array to a string.</span></span>

<span data-ttu-id="b6a8c-109">Usando CertEnroll.dll, você pode chamar o método [**VariantByteArrayToString**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-variantbytearraytostring) na interface [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) .</span><span class="sxs-lookup"><span data-stu-id="b6a8c-109">Using CertEnroll.dll, you can call the [**VariantByteArrayToString**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-variantbytearraytostring) method on the [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) interface.</span></span>

## <a name="stringtobinaryblob"></a><span data-ttu-id="b6a8c-110">stringToBinaryBlob</span><span class="sxs-lookup"><span data-stu-id="b6a8c-110">stringToBinaryBlob</span></span>

<span data-ttu-id="b6a8c-111">A função [**stringToBinaryBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-stringtobinaryblob) no Xenroll.dll converte uma cadeia de caracteres em uma matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="b6a8c-111">The [**stringToBinaryBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-stringtobinaryblob) function in Xenroll.dll converts a string to a byte array.</span></span>

<span data-ttu-id="b6a8c-112">Usando CertEnroll.dll, você pode chamar o método [**StringToVariantByteArray**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-stringtovariantbytearray) na interface [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) .</span><span class="sxs-lookup"><span data-stu-id="b6a8c-112">Using CertEnroll.dll, you can call the [**StringToVariantByteArray**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-stringtovariantbytearray) method on the [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6a8c-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b6a8c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6a8c-114">Mapeando Xenroll.dll para CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="b6a8c-114">Mapping Xenroll.dll to CertEnroll.dll</span></span>](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[<span data-ttu-id="b6a8c-115">**IBinaryConverter**</span><span class="sxs-lookup"><span data-stu-id="b6a8c-115">**IBinaryConverter**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)
</dt> </dl>

 

 
