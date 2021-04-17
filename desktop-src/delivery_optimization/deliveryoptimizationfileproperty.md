---
title: Enumeração DeliveryOptimizationFileProperty (Deliveryoptimization. h)
description: A enumeração DeliveryOptimizationFileProperty especifica a ID de uma propriedade opcional para o arquivo do.
keywords:
- Enumeração DeliveryOptimizationFileProperty
topic_type:
- apiref
api_name:
- DeliveryOptimizationFileProperty
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 238ad815149f7d40dd1902b991608e0a3005eb35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105766512"
---
# <a name="deliveryoptimizationfileproperty-enumeration"></a><span data-ttu-id="e77f7-104">Enumeração DeliveryOptimizationFileProperty</span><span class="sxs-lookup"><span data-stu-id="e77f7-104">DeliveryOptimizationFileProperty enumeration</span></span>

<span data-ttu-id="e77f7-105">A enumeração DeliveryOptimizationFileProperty especifica a ID de uma propriedade opcional para o arquivo do.</span><span class="sxs-lookup"><span data-stu-id="e77f7-105">The DeliveryOptimizationFileProperty enumeration specifies the ID of an optional property for the DO file.</span></span> <span data-ttu-id="e77f7-106">Essa enumeração é usada na interface IDeliveryOptimizationFile2 em que o valor da Propriedade do tipo VARIANT é passado</span><span class="sxs-lookup"><span data-stu-id="e77f7-106">This enumeration is used in the IDeliveryOptimizationFile2 interface where the property value of type VARIANT is passed</span></span>

## <a name="syntax"></a><span data-ttu-id="e77f7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e77f7-107">Syntax</span></span>

```C++
typedef enum _DeliveryOptimizationFileProperty {  
  DOFilePropertyId_DecryptionInfo,
  DOFilePropertyId_IntegrityCheckInfo,
  DOFilePropertyId_IntegrityCheckMandatory,
  DOFilePropertyId_DownloadSinkInterface,
  DOFilePropertyId_DownloadSinkFilePath,
  DOFilePropertyId_DownloadSinkMemoryStream,
  DOFilePropertyId_TotalSizeBytes
} DOFilePropertyId;
```

## <a name="constants"></a><span data-ttu-id="e77f7-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="e77f7-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e77f7-109">DOFilePropertyId_DecryptionInfo</span><span class="sxs-lookup"><span data-stu-id="e77f7-109">DOFilePropertyId_DecryptionInfo</span></span>
</dt> <dd>

<span data-ttu-id="e77f7-110">A ID de propriedade DOFilePropertyId_DecryptionInfo define informações de descriptografia na forma de uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="e77f7-110">The DOFilePropertyId_DecryptionInfo property ID sets decryption information in the form of a JSON string.</span></span> <span data-ttu-id="e77f7-111">DOFilePropertyId_DecryptionInfo é uma propriedade somente gravação do tipo VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="e77f7-111">DOFilePropertyId_DecryptionInfo is a Write only property of type VT_BSTR.</span></span>

</dd> <dt>

<span data-ttu-id="e77f7-112">DOFilePropertyId_IntegrityCheckInfo</span><span class="sxs-lookup"><span data-stu-id="e77f7-112">DOFilePropertyId_IntegrityCheckInfo</span></span>
</dt> <dd>

<span data-ttu-id="e77f7-113">A ID da propriedade DOFilePropertyId_IntegrityCheckInfo define o local do arquivo de hash da parte (PHF), que é usado pelo DO para executar verificações de integridade de tempo de execução no conteúdo baixado.</span><span class="sxs-lookup"><span data-stu-id="e77f7-113">The DOFilePropertyId_IntegrityCheckInfo property ID sets the piece hash file (PHF) location, which is used by DO to perform runtime integrity checks on the downloaded content.</span></span> <span data-ttu-id="e77f7-114">DOFilePropertyId_IntegrityCheckInfo é uma propriedade somente gravação do tipo VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="e77f7-114">DOFilePropertyId_IntegrityCheckInfo is a Write only property of type VT_BSTR.</span></span>

</dd> <dt>

<span data-ttu-id="e77f7-115">DOFilePropertyId_IntegrityCheckMandatory</span><span class="sxs-lookup"><span data-stu-id="e77f7-115">DOFilePropertyId_IntegrityCheckMandatory</span></span>
</dt> <dd>

<span data-ttu-id="e77f7-116">A ID de propriedade DOFilePropertyId_IntegrityCheckMandatory define um sinalizador booliano que indica se o uso de PHF é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="e77f7-116">The DOFilePropertyId_IntegrityCheckMandatory property ID sets a boolean flag indicating whether usage of the PHF is mandatory.</span></span> <span data-ttu-id="e77f7-117">Se for TRUE, o download será anulado quando a verificação de integridade falhar.</span><span class="sxs-lookup"><span data-stu-id="e77f7-117">If TRUE, the download will be aborted once the integrity check is failed.</span></span> <span data-ttu-id="e77f7-118">DOFilePropertyId_IntegrityCheckMandatory é uma propriedade de leitura/gravação do tipo VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="e77f7-118">DOFilePropertyId_IntegrityCheckMandatory is a Read/Write property of type VT_BOOL.</span></span>

</dd> <dt>

<span data-ttu-id="e77f7-119">DOFilePropertyId_DownloadSinkFilePath</span><span class="sxs-lookup"><span data-stu-id="e77f7-119">DOFilePropertyId_DownloadSinkFilePath</span></span>
</dt> <dd>

<span data-ttu-id="e77f7-120">A ID de propriedade de DOFilePropertyId_DownloadSinkFilePath define um local DO sistema de arquivos totalmente qualificado onde o deve armazenar as partes baixadas.</span><span class="sxs-lookup"><span data-stu-id="e77f7-120">The DOFilePropertyId_DownloadSinkFilePath property ID sets a fully qualified file system location where DO should store the downloaded pieces.</span></span> <span data-ttu-id="e77f7-121">DOFilePropertyId_DownloadSinkFilePath é do tipo VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="e77f7-121">DOFilePropertyId_DownloadSinkFilePath is of type VT_BSTR.</span></span>

</dd> <dt>

<span data-ttu-id="e77f7-122">DOFilePropertyId_DownloadSinkMemoryStream</span><span class="sxs-lookup"><span data-stu-id="e77f7-122">DOFilePropertyId_DownloadSinkMemoryStream</span></span>
</dt> <dd>

<span data-ttu-id="e77f7-123">A ID da propriedade de DOFilePropertyId_DownloadSinkMemoryStream foi preterida.</span><span class="sxs-lookup"><span data-stu-id="e77f7-123">The DOFilePropertyId_DownloadSinkMemoryStream property ID is deprecated.</span></span> <span data-ttu-id="e77f7-124">Não use.</span><span class="sxs-lookup"><span data-stu-id="e77f7-124">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="e77f7-125">DOFilePropertyId_TotalSizeBytes</span><span class="sxs-lookup"><span data-stu-id="e77f7-125">DOFilePropertyId_TotalSizeBytes</span></span>
</dt> <dd>

<span data-ttu-id="e77f7-126">A ID da propriedade DOFilePropertyId_TotalSizeBytes especifica o tamanho total do download.</span><span class="sxs-lookup"><span data-stu-id="e77f7-126">The DOFilePropertyId_TotalSizeBytes property ID specifies the total download size.</span></span> <span data-ttu-id="e77f7-127">DOFilePropertyId_TotalSizeBytes é do tipo VT_UI8.</span><span class="sxs-lookup"><span data-stu-id="e77f7-127">DOFilePropertyId_TotalSizeBytes is of type VT_UI8.</span></span>
</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e77f7-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e77f7-128">Requirements</span></span>

| <span data-ttu-id="e77f7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e77f7-129">Requirement</span></span> | <span data-ttu-id="e77f7-130">Valor</span><span class="sxs-lookup"><span data-stu-id="e77f7-130">Value</span></span> |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="e77f7-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e77f7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e77f7-132">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="e77f7-132">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="e77f7-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e77f7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e77f7-134">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="e77f7-134">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>  |
| <span data-ttu-id="e77f7-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e77f7-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e77f7-136"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="e77f7-136"><dt>Deliveryoptimization.h</dt></span></span> </dl>               |
