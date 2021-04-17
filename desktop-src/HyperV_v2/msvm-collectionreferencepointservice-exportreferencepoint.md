---
description: Exporta uma coleção de pontos de referência para um arquivo. A coleção de pontos de referência, suas definições de configuração associadas e suas configurações de recursos associadas serão preservadas no arquivo resultante.
ms.assetid: 0ed61ded-b4d6-40c5-98be-e192eb934387
title: Método ExportReferencePoint da classe Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 49517da44cc7955d825792afcc475c56e37fad37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782355"
---
# <a name="exportreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="ca2b1-104">Método ExportReferencePoint da \_ classe CollectionReferencePointService Msvm</span><span class="sxs-lookup"><span data-stu-id="ca2b1-104">ExportReferencePoint method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="ca2b1-105">Exporta uma coleção de pontos de referência para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="ca2b1-105">Exports a reference point collection to a file.</span></span> <span data-ttu-id="ca2b1-106">A coleção de pontos de referência, suas definições de configuração associadas e suas configurações de recursos associadas serão preservadas no arquivo resultante.</span><span class="sxs-lookup"><span data-stu-id="ca2b1-106">The reference point collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca2b1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca2b1-107">Syntax</span></span>


```mof
uint32 ExportReferencePoint(
  [in]  CIM_Collection  REF ReferencePointCollection,
  [in]  string              ExportDirectory,
  [in]  string              ExportSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ca2b1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca2b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca2b1-109">*ReferencePointCollection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ca2b1-109">*ReferencePointCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca2b1-110">Uma referência a uma [**\_ coleção CIM**](cim-collection.md) que representa a coleção de pontos de referência a ser exportada.</span><span class="sxs-lookup"><span data-stu-id="ca2b1-110">A reference to a [**CIM\_Collection**](cim-collection.md) that represents the reference point collection to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="ca2b1-111">*ExportDirectory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ca2b1-111">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca2b1-112">O caminho totalmente qualificado do diretório para o qual a coleção de pontos de referência deve ser exportada.</span><span class="sxs-lookup"><span data-stu-id="ca2b1-112">The fully-qualified path of the directory to which the reference point collection is to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="ca2b1-113">*ExportSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ca2b1-113">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca2b1-114">Uma instância de [**Msvm \_ CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) que representa as configurações da operação de exportação.</span><span class="sxs-lookup"><span data-stu-id="ca2b1-114">An instance of [**Msvm\_CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="ca2b1-115">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="ca2b1-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca2b1-116">Uma referência opcional que será retornada se a operação for executada de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="ca2b1-116">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="ca2b1-117">Se estiver presente, a referência retornada a uma instância de [**CIM \_ ConcreteJob**](cim-concretejob.md) poderá ser usada para monitorar o progresso e obter o resultado do método.</span><span class="sxs-lookup"><span data-stu-id="ca2b1-117">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca2b1-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ca2b1-118">Return value</span></span>

<span data-ttu-id="ca2b1-119">Se esse método for executado de forma síncrona, ele retornará 0 se tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="ca2b1-119">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="ca2b1-120">Se esse método for executado de forma assíncrona, ele retornará 4096 e o parâmetro de saída do trabalho poderá ser usado para acompanhar o progresso da operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="ca2b1-120">If this method is executed asynchronously, it returns 4096 and the Job output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="ca2b1-121">Qualquer outro valor de retorno indica um erro.</span><span class="sxs-lookup"><span data-stu-id="ca2b1-121">Any other return value indicates an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca2b1-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca2b1-122">Requirements</span></span>



| <span data-ttu-id="ca2b1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca2b1-123">Requirement</span></span> | <span data-ttu-id="ca2b1-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ca2b1-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca2b1-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca2b1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ca2b1-126">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ca2b1-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="ca2b1-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca2b1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ca2b1-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ca2b1-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ca2b1-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="ca2b1-129">Namespace</span></span><br/>                | <span data-ttu-id="ca2b1-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="ca2b1-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ca2b1-131">MOF</span><span class="sxs-lookup"><span data-stu-id="ca2b1-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca2b1-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca2b1-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca2b1-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ca2b1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca2b1-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ca2b1-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ca2b1-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca2b1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca2b1-136">**Msvm \_ CollectionReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="ca2b1-136">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




