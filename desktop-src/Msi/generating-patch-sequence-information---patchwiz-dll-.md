---
description: A versão do PATCHWIZ.DLL lançada com Windows Installer&\# 160; 3.0 pode gerar automaticamente informações de sequenciamento de patch e adicionar à tabela MsiPatchSequence um novo patch.
ms.assetid: 03e7eea6-1a37-4c86-a9da-109fbaf20728
title: Gerando informações de sequência de patch (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff82166f33266a58cd3ef299b2546b04a94ebb14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922029"
---
# <a name="generating-patch-sequence-information-patchwizdll"></a><span data-ttu-id="0e6e0-103">Gerando informações de sequência de patch (PATCHWIZ.DLL)</span><span class="sxs-lookup"><span data-stu-id="0e6e0-103">Generating Patch Sequence Information (PATCHWIZ.DLL)</span></span>

<span data-ttu-id="0e6e0-104">A versão do [PATCHWIZ.DLL](patchwiz-dll.md) lançada com Windows Installer 3,0 pode gerar automaticamente informações de sequenciamento de patch e adicionar à [tabela MsiPatchSequence](msipatchsequence-table.md) um novo patch.</span><span class="sxs-lookup"><span data-stu-id="0e6e0-104">The version of [PATCHWIZ.DLL](patchwiz-dll.md) released with Windows Installer 3.0 can automatically generate patch sequencing information and add to the [MsiPatchSequence Table](msipatchsequence-table.md) a new patch.</span></span>

<span data-ttu-id="0e6e0-105">Defina a propriedade de geração de dados de sequência \_ \_ \_ desabilitada como 1 (uma) na [tabela Propriedades](properties-table-patchwiz-dll-.md) do arquivo. PCP para evitar a geração automática de informações de sequenciamento de patch.</span><span class="sxs-lookup"><span data-stu-id="0e6e0-105">Set the SEQUENCE\_DATA\_GENERATION\_DISABLED property to 1 (one) in the [Properties Table](properties-table-patchwiz-dll-.md) of the .pcp file to prevent the automatic generation of patch sequencing information.</span></span> <span data-ttu-id="0e6e0-106">Se essa propriedade estiver ausente, as informações serão geradas e adicionadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="0e6e0-106">If this property is absent, the information is automatically generated and added.</span></span>

<span data-ttu-id="0e6e0-107">Quando o [PATCHWIZ.DLL](patchwiz-dll.md) liberado com Windows Installer 3,0 é usado para gerar automaticamente as informações de sequenciamento de patch, ocorre o seguinte:</span><span class="sxs-lookup"><span data-stu-id="0e6e0-107">When the [PATCHWIZ.DLL](patchwiz-dll.md) released with Windows Installer 3.0 is used to automatically generate the patch sequencing information, the following occurs:</span></span>

-   <span data-ttu-id="0e6e0-108">Uma nova linha é adicionada à [tabela MsiPatchSequence](msipatchsequence-table.md) para cada código de produto de uma imagem de destino listada na [tabela TargetImages](targetimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="0e6e0-108">A new row is added to the [MsiPatchSequence Table](msipatchsequence-table.md) for each product code of a target image that is listed in the [TargetImages Table](targetimages-table-patchwiz-dll-.md).</span></span>
-   <span data-ttu-id="0e6e0-109">Os valores adicionados à coluna PatchFamily nas novas linhas correspondem aos códigos de produto de destino das imagens de destino listadas na [tabela TargetImages](targetimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="0e6e0-109">The values added to the PatchFamily column in the new rows correspond to the target product codes of the target images that are listed in the [TargetImages Table](targetimages-table-patchwiz-dll-.md).</span></span>
-   <span data-ttu-id="0e6e0-110">Os valores adicionados às colunas de sequência nas novas linhas são gerados usando a versão de produto mais alta direcionada pelo patch e a hora UTC quando o patch é gerado.</span><span class="sxs-lookup"><span data-stu-id="0e6e0-110">The values added to the Sequence columns in the new rows are generated using the highest product version targeted by the patch and the UTC time when the patch is generated.</span></span> <span data-ttu-id="0e6e0-111">O número de sequência é <Product Minor Version> . <Build Major Number> . <carimbo de data/hora 1>. <carimbo de data/hora 2>.</span><span class="sxs-lookup"><span data-stu-id="0e6e0-111">The sequence number is <Product Minor Version>.<Build Major Number>.<Time Stamp 1>.<Time Stamp 2>.</span></span>
    -   <span data-ttu-id="0e6e0-112">O primeiro campo é a versão do produto da versão mais recente do produto que é alvo do patch.</span><span class="sxs-lookup"><span data-stu-id="0e6e0-112">The first field is the product version of the highest version of the product that is targeted by the patch.</span></span>
    -   <span data-ttu-id="0e6e0-113">O segundo campo é o número principal de compilação da versão mais recente do produto que é alvo do patch.</span><span class="sxs-lookup"><span data-stu-id="0e6e0-113">The second field is the build major number of the highest version of the product that is targeted by the patch.</span></span>

    <span data-ttu-id="0e6e0-114">Os dois campos de carimbo de data/hora contam com o carimbo de data/hora de 32 bits necessário para contar os segundos em UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="0e6e0-114">The two time stamp fields account for the 32 bit time stamp that is needed to count the seconds in Coordinated Universal Time (UTC).</span></span>
    > [!Note]  
    > <span data-ttu-id="0e6e0-115">As versões do produto têm o seguinte formato: <Product Major Version> . <Product Minor Version> . <Build Major Number> <Build Minor Number> e um produto com um número de versão 2.1.0.0 é uma versão superior à de um produto com o número de versão 1.2.0.0</span><span class="sxs-lookup"><span data-stu-id="0e6e0-115">Product versions have the following format: <Product Major Version>.<Product Minor Version>.<Build Major Number>.<Build Minor Number> and a product with a version number 2.1.0.0 is a higher version than a product with version number 1.2.0.0</span></span>

     

-   <span data-ttu-id="0e6e0-116">O atributo msidbPatchSequenceSupersedeEarlier é inserido na coluna de atributo de novas linhas que são geradas para Service Packs (SP) ou patches de atualização secundária.</span><span class="sxs-lookup"><span data-stu-id="0e6e0-116">The msidbPatchSequenceSupersedeEarlier attribute is entered into the Attribute column of new rows that are generated for service packs (SP) or minor upgrade patches.</span></span> <span data-ttu-id="0e6e0-117">O atributo msidbPatchSequenceSupersedeEarlier não é adicionado a um QFE ou um patch de atualização pequeno.</span><span class="sxs-lookup"><span data-stu-id="0e6e0-117">The msidbPatchSequenceSupersedeEarlier attribute is not added to a QFE or small update patch.</span></span>
    > [!Note]  
    > <span data-ttu-id="0e6e0-118">Um service pack (SP) deve conter as correções de todos os QFEs que foram lançados antes dele.</span><span class="sxs-lookup"><span data-stu-id="0e6e0-118">A service pack (SP) should contain the fixes of all the QFEs that were released prior to it.</span></span> <span data-ttu-id="0e6e0-119">No entanto, se um autor de patch definir a propriedade de substituição de dados de sequência \_ \_ como 0 (zero) ou 1 (um) no arquivo. PCP, a coluna atributos de todas as linhas na tabela MsiPatchSequence será definida como o valor especificado para substituição de dados de sequência \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0e6e0-119">However, if a patch author sets the SEQUENCE\_DATA\_SUPERSEDENCE property to 0 (zero) or 1 (one) in the .pcp file, the Attributes column of all rows in the MsiPatchSequence table is set to the value that is specified for SEQUENCE\_DATA\_SUPERSEDENCE.</span></span> <span data-ttu-id="0e6e0-120">Os autores de patches que exigem mais controle devem criar a coluna atributos manualmente.</span><span class="sxs-lookup"><span data-stu-id="0e6e0-120">Patch authors who require more control must author the Attributes column manually.</span></span>

     

<span data-ttu-id="0e6e0-121">Se você incluir uma [tabela PatchSequence](patchsequence-table--patchwiz-dll-.md) no arquivo. PCP, a propriedade de \_ geração de dados de sequência \_ \_ desabilitada será ignorada e as informações fornecidas na tabela PatchSequence poderão ser adicionadas à [tabela MsiPatchSequence](msipatchsequence-table.md) do patch.</span><span class="sxs-lookup"><span data-stu-id="0e6e0-121">If you include a [PatchSequence Table](patchsequence-table--patchwiz-dll-.md) in the .pcp file, the SEQUENCE\_DATA\_GENERATION\_DISABLED property is ignored and the information provided in the PatchSequence Table can be added to the [MsiPatchSequence Table](msipatchsequence-table.md) of the patch.</span></span>

 

 



