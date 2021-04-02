---
description: Exporta uma coleção de instantâneos de sistemas de computador virtual para um arquivo. A coleção de instantâneos, suas definições de configuração associadas e suas configurações de recurso associadas serão preservadas no arquivo resultante.
ms.assetid: 61fbc81c-c3e8-4058-b11a-4ed69481207c
title: Método ExportSnapshot da classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ExportSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f4dd29e001c8335477451e86151d950c25edb9b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165254"
---
# <a name="exportsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="f83b9-104">Método ExportSnapshot da \_ classe CollectionSnapshotService Msvm</span><span class="sxs-lookup"><span data-stu-id="f83b9-104">ExportSnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="f83b9-105">Exporta uma coleção de instantâneos de sistemas de computador virtual para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="f83b9-105">Exports a snapshot collection of virtual computer systems to a file.</span></span> <span data-ttu-id="f83b9-106">A coleção de instantâneos, suas definições de configuração associadas e suas configurações de recurso associadas serão preservadas no arquivo resultante.</span><span class="sxs-lookup"><span data-stu-id="f83b9-106">The snapshot collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f83b9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f83b9-107">Syntax</span></span>


```mof
uint32 ExportSnapshot(
  [in]  CIM_Collection  REF SnapshotCollection,
  [in]  string              ExportDirectory,
  [in]  string              ExportSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f83b9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f83b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f83b9-109">*Instantâneocollection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f83b9-109">*SnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f83b9-110">Uma referência a uma [**\_ coleção CIM**](cim-collection.md) que representa a coleção de instantâneos a ser exportada.</span><span class="sxs-lookup"><span data-stu-id="f83b9-110">A reference to a [**CIM\_Collection**](cim-collection.md) that represents the snapshot collection to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="f83b9-111">*ExportDirectory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f83b9-111">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f83b9-112">O caminho totalmente qualificado do diretório para o qual a coleção do sistema virtual deve ser exportada.</span><span class="sxs-lookup"><span data-stu-id="f83b9-112">The fully-qualified path of the directory to which the virtual system collection is to be exported.</span></span> <span data-ttu-id="f83b9-113">Se a propriedade **CreateVmExportSubdirectory** no parâmetro *ExportSettingData* for definida como **true** , esse diretório poderá ser reutilizado para exportar várias coleções de sistema virtual e esse método colocará cada definição de coleção do sistema virtual em um subdiretório separado sob esse caminho.</span><span class="sxs-lookup"><span data-stu-id="f83b9-113">If the **CreateVmExportSubdirectory** property in the *ExportSettingData* parameter is set to **True** then this directory can be reused for exporting multiple virtual system collections and this method places each virtual system collection definition in a separate subdirectory under this path.</span></span>

</dd> <dt>

<span data-ttu-id="f83b9-114">*ExportSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f83b9-114">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f83b9-115">Uma instância de [**Msvm \_ CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md) que representa as configurações da operação de exportação.</span><span class="sxs-lookup"><span data-stu-id="f83b9-115">An instance of [**Msvm\_CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md) that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="f83b9-116">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="f83b9-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f83b9-117">Uma referência opcional que será retornada se a operação for executada de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="f83b9-117">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="f83b9-118">Se estiver presente, a referência retornada a uma instância de [**CIM \_ ConcreteJob**](cim-concretejob.md) poderá ser usada para monitorar o progresso e obter o resultado do método.</span><span class="sxs-lookup"><span data-stu-id="f83b9-118">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f83b9-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f83b9-119">Return value</span></span>

<span data-ttu-id="f83b9-120">Se esse método for executado de forma síncrona, ele retornará 0 se tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="f83b9-120">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="f83b9-121">Se esse método for executado de forma assíncrona, ele retornará 4096 e o parâmetro de saída do trabalho poderá ser usado para acompanhar o progresso da operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="f83b9-121">If this method is executed asynchronously, it returns 4096 and the Job output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="f83b9-122">Qualquer outro valor de retorno indica um erro.</span><span class="sxs-lookup"><span data-stu-id="f83b9-122">Any other return value indicates an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="f83b9-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f83b9-123">Requirements</span></span>



| <span data-ttu-id="f83b9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f83b9-124">Requirement</span></span> | <span data-ttu-id="f83b9-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f83b9-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f83b9-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f83b9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f83b9-127">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f83b9-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f83b9-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f83b9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f83b9-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f83b9-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f83b9-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="f83b9-130">Namespace</span></span><br/>                | <span data-ttu-id="f83b9-131">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f83b9-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f83b9-132">MOF</span><span class="sxs-lookup"><span data-stu-id="f83b9-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f83b9-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f83b9-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f83b9-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f83b9-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f83b9-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f83b9-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f83b9-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="f83b9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f83b9-137">**Msvm \_ CollectionSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="f83b9-137">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




