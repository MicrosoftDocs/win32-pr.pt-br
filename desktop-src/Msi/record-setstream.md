---
description: O método SetStream do objeto Record copia o conteúdo do arquivo especificado no campo registro designado como dados de fluxo. Os dados de fluxo não podem ser inseridos em campos temporários.
ms.assetid: feb79371-d0c4-4bb0-b539-2f431ee1051b
title: Método record. SetStream
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.SetStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 94ec3d63b3dcd75a13c2c0ff62b624b89979d641
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758617"
---
# <a name="recordsetstream-method"></a><span data-ttu-id="90015-104">Método record. SetStream</span><span class="sxs-lookup"><span data-stu-id="90015-104">Record.SetStream method</span></span>

<span data-ttu-id="90015-105">O método **SetStream** do objeto [**Record**](record-object.md) copia o conteúdo do arquivo especificado no campo registro designado como dados de fluxo.</span><span class="sxs-lookup"><span data-stu-id="90015-105">The **SetStream** method of the [**Record**](record-object.md) object copies the content of the specified file into the designated record field as stream data.</span></span> <span data-ttu-id="90015-106">Os dados de fluxo não podem ser inseridos em campos temporários.</span><span class="sxs-lookup"><span data-stu-id="90015-106">Stream data cannot be inserted into temporary fields.</span></span>

## <a name="syntax"></a><span data-ttu-id="90015-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90015-107">Syntax</span></span>


```JScript
Record.SetStream(
  field,
  filePath
)
```



## <a name="parameters"></a><span data-ttu-id="90015-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90015-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90015-109">*campo*</span><span class="sxs-lookup"><span data-stu-id="90015-109">*field*</span></span> 
</dt> <dd>

<span data-ttu-id="90015-110">Campo obrigatório número do valor dentro do registro, baseado em 1.</span><span class="sxs-lookup"><span data-stu-id="90015-110">Required field number of the value within the record, 1-based.</span></span>

</dd> <dt>

<span data-ttu-id="90015-111">*filePath*</span><span class="sxs-lookup"><span data-stu-id="90015-111">*filePath*</span></span> 
</dt> <dd>

<span data-ttu-id="90015-112">O local do arquivo a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="90015-112">The location of the file to copy.</span></span> <span data-ttu-id="90015-113">Nenhuma tradução de qualquer tipo é executada.</span><span class="sxs-lookup"><span data-stu-id="90015-113">No translation of any type is performed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90015-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="90015-114">Return value</span></span>

<span data-ttu-id="90015-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="90015-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="90015-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="90015-116">Remarks</span></span>

<span data-ttu-id="90015-117">Se o método falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="90015-117">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="90015-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90015-118">Requirements</span></span>



| <span data-ttu-id="90015-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="90015-119">Requirement</span></span> | <span data-ttu-id="90015-120">Valor</span><span class="sxs-lookup"><span data-stu-id="90015-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90015-121">Versão</span><span class="sxs-lookup"><span data-stu-id="90015-121">Version</span></span><br/> | <span data-ttu-id="90015-122">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="90015-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="90015-123">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="90015-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="90015-124">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="90015-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="90015-125">DLL</span><span class="sxs-lookup"><span data-stu-id="90015-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="90015-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90015-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="90015-127">IID</span><span class="sxs-lookup"><span data-stu-id="90015-127">IID</span></span><br/>     | <span data-ttu-id="90015-128">IID \_ IRecord é definido como 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="90015-128">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




