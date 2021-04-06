---
description: Identifica os possíveis certificados de signatário usados para assinar digitalmente patches.
ms.assetid: 8f76c27d-92f1-4de7-a69c-fba877e0325d
title: Tabela MsiPatchCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01648e792931fd856a1231a5d876c7db843479df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011148"
---
# <a name="msipatchcertificate-table"></a><span data-ttu-id="19a51-103">Tabela MsiPatchCertificate</span><span class="sxs-lookup"><span data-stu-id="19a51-103">MsiPatchCertificate Table</span></span>

<span data-ttu-id="19a51-104">A tabela MsiPatchCertificate identifica os possíveis certificados de signatário usados para assinar digitalmente patches.</span><span class="sxs-lookup"><span data-stu-id="19a51-104">The MsiPatchCertificate Table identifies the possible signer certificates used to digitally sign patches.</span></span> <span data-ttu-id="19a51-105">A tabela MsiPatchCertificate contém as informações necessárias para habilitar a [aplicação de patches de controle de conta de usuário (UAC)](user-account-control--uac--patching.md) para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="19a51-105">The MsiPatchCertificate Table contains the information that is needed to enable [User Account Control (UAC) Patching](user-account-control--uac--patching.md) for an application.</span></span>

<span data-ttu-id="19a51-106">A tabela MsiPatchCertificate tem as seguintes colunas:</span><span class="sxs-lookup"><span data-stu-id="19a51-106">The MsiPatchCertificate Table has the following columns:</span></span>



| <span data-ttu-id="19a51-107">Coluna</span><span class="sxs-lookup"><span data-stu-id="19a51-107">Column</span></span>               | <span data-ttu-id="19a51-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="19a51-108">Type</span></span>                         | <span data-ttu-id="19a51-109">Chave</span><span class="sxs-lookup"><span data-stu-id="19a51-109">Key</span></span> | <span data-ttu-id="19a51-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="19a51-110">Nullable</span></span> |
|----------------------|------------------------------|-----|----------|
| <span data-ttu-id="19a51-111">PatchCertificate</span><span class="sxs-lookup"><span data-stu-id="19a51-111">PatchCertificate</span></span>     | [<span data-ttu-id="19a51-112">Identificador</span><span class="sxs-lookup"><span data-stu-id="19a51-112">Identifier</span></span>](identifier.md) | <span data-ttu-id="19a51-113">S</span><span class="sxs-lookup"><span data-stu-id="19a51-113">Y</span></span>   | <span data-ttu-id="19a51-114">N</span><span class="sxs-lookup"><span data-stu-id="19a51-114">N</span></span>        |
| <span data-ttu-id="19a51-115">DigitalCertificate\_</span><span class="sxs-lookup"><span data-stu-id="19a51-115">DigitalCertificate\_</span></span> | [<span data-ttu-id="19a51-116">Identificador</span><span class="sxs-lookup"><span data-stu-id="19a51-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="19a51-117">N</span><span class="sxs-lookup"><span data-stu-id="19a51-117">N</span></span>   | <span data-ttu-id="19a51-118">N</span><span class="sxs-lookup"><span data-stu-id="19a51-118">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="19a51-119">Colunas</span><span class="sxs-lookup"><span data-stu-id="19a51-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="19a51-120"><span id="PatchCertificate"></span><span id="patchcertificate"></span><span id="PATCHCERTIFICATE"></span>PatchCertificate</span><span class="sxs-lookup"><span data-stu-id="19a51-120"><span id="PatchCertificate"></span><span id="patchcertificate"></span><span id="PATCHCERTIFICATE"></span>PatchCertificate</span></span>
</dt> <dd>

<span data-ttu-id="19a51-121">O identificador exclusivo para esta linha na tabela MsiPatchCertificate.</span><span class="sxs-lookup"><span data-stu-id="19a51-121">The unique identifier for this row in the MsiPatchCertificate Table.</span></span>

</dd> <dt>

<span data-ttu-id="19a51-122"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="19a51-122"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span></span>
</dt> <dd>

<span data-ttu-id="19a51-123">Uma chave externa na primeira coluna da [tabela MsiDigitalCertificate](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="19a51-123">An external key into the first column of the [MsiDigitalCertificate Table](msidigitalcertificate-table.md).</span></span> <span data-ttu-id="19a51-124">A linha indicada na tabela MsiDigitalCertificate contém a representação binária do certificado de signatário.</span><span class="sxs-lookup"><span data-stu-id="19a51-124">The row indicated in the MsiDigitalCertificate Table contains the binary representation of the signer certificate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19a51-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="19a51-125">Remarks</span></span>

<span data-ttu-id="19a51-126">Os patches são sempre avaliados em relação à tabela MsiPatchCertificate que é atual no momento em que o patch é aplicado.</span><span class="sxs-lookup"><span data-stu-id="19a51-126">Patches are always evaluated against the MsiPatchCertificate Table that is current at the time the patch is applied.</span></span> <span data-ttu-id="19a51-127">Um patch pode modificar a tabela MsiPatchCertificate adicionando ou removendo entradas.</span><span class="sxs-lookup"><span data-stu-id="19a51-127">A patch can modify the MsiPatchCertificate Table by adding or removing entries.</span></span> <span data-ttu-id="19a51-128">Isso permite que um patch modifique a avaliação de patches futuros que são aplicados posteriormente na sequência de aplicação de patches.</span><span class="sxs-lookup"><span data-stu-id="19a51-128">This enables a patch to modify the evaluation of future patches that are applied later in the patching sequence.</span></span> <span data-ttu-id="19a51-129">Vários certificados podem existir na tabela e o patch deve corresponder a pelo menos um certificado a ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="19a51-129">Multiple certificates can exist in the table, and the patch must match at least one certificate to be applied.</span></span>

## <a name="validation"></a><span data-ttu-id="19a51-130">Validação</span><span class="sxs-lookup"><span data-stu-id="19a51-130">Validation</span></span>

<dl>

[<span data-ttu-id="19a51-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="19a51-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="19a51-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="19a51-132">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="19a51-133">ICE32</span><span class="sxs-lookup"><span data-stu-id="19a51-133">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="19a51-134">ICE81</span><span class="sxs-lookup"><span data-stu-id="19a51-134">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="19a51-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="19a51-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19a51-136">DisableLUAPatching</span><span class="sxs-lookup"><span data-stu-id="19a51-136">DisableLUAPatching</span></span>](disableluapatching.md)
</dt> <dt>

[<span data-ttu-id="19a51-137">Aplicação de patch de UAC (controle de conta de usuário)</span><span class="sxs-lookup"><span data-stu-id="19a51-137">User Account Control (UAC) Patching</span></span>](user-account-control--uac--patching.md)
</dt> <dt>

[<span data-ttu-id="19a51-138">**MSIDISABLELUAPATCHING**</span><span class="sxs-lookup"><span data-stu-id="19a51-138">**MSIDISABLELUAPATCHING**</span></span>](msidisableluapatching.md)
</dt> <dt>

[<span data-ttu-id="19a51-139">Assinaturas digitais e Windows Installer</span><span class="sxs-lookup"><span data-stu-id="19a51-139">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> <dt>

[<span data-ttu-id="19a51-140">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="19a51-140">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



