---
description: ICE81 valida a tabela MsiDigitalCertificate, a tabela MsiDigitalSignature, a tabela MsiPatchCertificate e a tabela MsiPackageCertificate.
ms.assetid: 83d8bc62-679e-410f-a95c-ffe13952b710
title: ICE81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2fef8da1027fc739ce8e6e979ca998a1cd053a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647472"
---
# <a name="ice81"></a><span data-ttu-id="5a51c-103">ICE81</span><span class="sxs-lookup"><span data-stu-id="5a51c-103">ICE81</span></span>

<span data-ttu-id="5a51c-104">ICE81 valida a tabela [MsiDigitalCertificate](msidigitalcertificate-table.md), a [tabela MsiDigitalSignature](msidigitalsignature-table.md), a tabela [MsiPatchCertificate](msipatchcertificate-table.md)e a [tabela MsiPackageCertificate](msipackagecertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="5a51c-104">ICE81 validates the [MsiDigitalCertificate table](msidigitalcertificate-table.md), [MsiDigitalSignature table](msidigitalsignature-table.md), [MsiPatchCertificate table](msipatchcertificate-table.md), and [MsiPackageCertificate Table](msipackagecertificate-table.md).</span></span> <span data-ttu-id="5a51c-105">Essa ação personalizada de ICE posta avisos para certificados digitais que não são usados ou não referenciados e posta um erro quando o objeto assinado não existe ou quando o gabinete do objeto assinado não aponta para dados externos.</span><span class="sxs-lookup"><span data-stu-id="5a51c-105">This ICE custom action posts warnings for digital certificates that are unused or unreferenced, and it posts an error when the signed object does not exist or when the signed object's cabinet does not point to external data.</span></span>

<span data-ttu-id="5a51c-106">Observe que ICE03 verifica se a entrada na coluna Table na tabela MsiDigitalSignature é "Media".</span><span class="sxs-lookup"><span data-stu-id="5a51c-106">Note that ICE03 verifies that the entry in the Table column in the MsiDigitalSignature table is "Media."</span></span>

## <a name="result"></a><span data-ttu-id="5a51c-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="5a51c-107">Result</span></span>

<span data-ttu-id="5a51c-108">ICE81 posta os seguintes avisos para certificados digitais não utilizados ou não referenciados.</span><span class="sxs-lookup"><span data-stu-id="5a51c-108">ICE81 posts the following warnings for unused or unreferenced Digital Certificates.</span></span>



| <span data-ttu-id="5a51c-109">Aviso de ICE81</span><span class="sxs-lookup"><span data-stu-id="5a51c-109">ICE81 warning</span></span>                                                                                                                                                      | <span data-ttu-id="5a51c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a51c-110">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="5a51c-111">Nenhuma referência a nenhum dos registros na tabela MsiDigitalCertificate foi encontrada nas tabelas MsiDigitalSignature, MsiPackageCertificate ou MsiPatchCertificate.</span><span class="sxs-lookup"><span data-stu-id="5a51c-111">No reference to any of the records in the MsiDigitalCertificate table could be found in MsiDigitalSignature, MsiPackageCertificate, or MsiPatchCertificate tables.</span></span> | <span data-ttu-id="5a51c-112">Esse aviso será retornado se todos os registros estiverem inutilizados.</span><span class="sxs-lookup"><span data-stu-id="5a51c-112">This warning is returned if all records are unused.</span></span>                |
| <span data-ttu-id="5a51c-113">Nenhuma referência ao certificado digital \[ 1 \] foi encontrada nas tabelas MsiDigitalSignature, MsiPackageCertificate ou MsiPatchCertificate.</span><span class="sxs-lookup"><span data-stu-id="5a51c-113">No reference to the Digital Certificate \[1\] could be found in MsiDigitalSignature, MsiPackageCertificate, or MsiPatchCertificate tables.</span></span>                         | <span data-ttu-id="5a51c-114">Esse aviso será retornado se alguns registros, mas não todos, não forem usados.</span><span class="sxs-lookup"><span data-stu-id="5a51c-114">This warning is returned if some records, but not all, are unused.</span></span> |



 

<span data-ttu-id="5a51c-115">ICE81 posta os erros a seguir.</span><span class="sxs-lookup"><span data-stu-id="5a51c-115">ICE81 posts the following errors.</span></span>



| <span data-ttu-id="5a51c-116">Erro de ICE81</span><span class="sxs-lookup"><span data-stu-id="5a51c-116">ICE81 error</span></span>                                                                                                                                                              | <span data-ttu-id="5a51c-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a51c-117">Description</span></span>                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a51c-118">A tabela de mídia não existe.</span><span class="sxs-lookup"><span data-stu-id="5a51c-118">Media Table does not exist.</span></span> <span data-ttu-id="5a51c-119">Portanto, todas as entradas em MsiDigitalSignature estão incorretas</span><span class="sxs-lookup"><span data-stu-id="5a51c-119">Hence all the entries in MsiDigitalSignature are incorrect</span></span>                                                                                   | <span data-ttu-id="5a51c-120">O objeto assinado não existe.</span><span class="sxs-lookup"><span data-stu-id="5a51c-120">The signed object does not exist.</span></span> <span data-ttu-id="5a51c-121">Esse erro será retornado se a tabela de mídia não existir, mas MsiDigitalSignature tiver entradas.</span><span class="sxs-lookup"><span data-stu-id="5a51c-121">This error is returned if the Media table does not exist but MsiDigitalSignature has entries.</span></span>                                |
| <span data-ttu-id="5a51c-122">Objeto assinado \[ 2 ausente \] na tabela de mídia</span><span class="sxs-lookup"><span data-stu-id="5a51c-122">Missing signed object \[2\] in Media Table</span></span>                                                                                                                               | <span data-ttu-id="5a51c-123">O objeto assinado \[ 2 \] não existe.</span><span class="sxs-lookup"><span data-stu-id="5a51c-123">The signed object \[2\] does not exist.</span></span> <span data-ttu-id="5a51c-124">Esse erro será retornado se a tabela de mídia existir, mas essa entrada em MsiDigitalSignature não estiver presente na tabela de mídia.</span><span class="sxs-lookup"><span data-stu-id="5a51c-124">This error is returned if the Media table exists, but this entry in MsiDigitalSignature is not present in Media table.</span></span> |
| <span data-ttu-id="5a51c-125">A entrada na tabela \[ 1 \] com a chave \[ 2 \] é assinada.</span><span class="sxs-lookup"><span data-stu-id="5a51c-125">The entry in table \[1\] with key \[2\] is signed.</span></span> <span data-ttu-id="5a51c-126">Portanto, o gabinete deve apontar para um objeto fora do pacote (o valor do gabinete não deve ser prefixado \# )</span><span class="sxs-lookup"><span data-stu-id="5a51c-126">Hence the cabinet should point to an object outside the package (the value of Cabinet should NOT be prefixed with \#)</span></span> | <span data-ttu-id="5a51c-127">O gabinete do objeto assinado não aponta para dados externos.</span><span class="sxs-lookup"><span data-stu-id="5a51c-127">The signed object's cabinet does not point to external data.</span></span> <span data-ttu-id="5a51c-128">\[1 \] é o nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="5a51c-128">\[1\] is table name.</span></span> <span data-ttu-id="5a51c-129">\[2 \] é a chave na tabela de mídia.</span><span class="sxs-lookup"><span data-stu-id="5a51c-129">\[2\] is key in the Media table.</span></span>                                             |



 

## <a name="related-topics"></a><span data-ttu-id="5a51c-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5a51c-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a51c-131">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="5a51c-131">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



