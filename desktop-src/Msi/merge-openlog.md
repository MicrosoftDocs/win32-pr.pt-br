---
description: O método OpenLog do objeto Merge abre um arquivo de log que recebe o progresso e as mensagens de erro. Se o arquivo de log já existir, o instalador acrescentará novas mensagens. Se o arquivo de log não existir, o instalador criará um arquivo de log.
ms.assetid: 97d01ea3-43b6-4529-9706-97b3b0132d9c
title: Método Merge. OpenLog (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenLog
- IMsmMerge.OpenLog
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 46dc029c88b44540817e93e1e559829d88b9f62b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752846"
---
# <a name="mergeopenlog-method"></a><span data-ttu-id="16a6c-105">Método Merge. OpenLog</span><span class="sxs-lookup"><span data-stu-id="16a6c-105">Merge.OpenLog method</span></span>

<span data-ttu-id="16a6c-106">O método **OpenLog** do objeto [**Merge**](merge-object.md) abre um arquivo de log que recebe o progresso e as mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="16a6c-106">The **OpenLog** method of the [**Merge**](merge-object.md) object opens a log file that receives progress and error messages.</span></span> <span data-ttu-id="16a6c-107">Se o arquivo de log já existir, o instalador acrescentará novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="16a6c-107">If the log file already exists, the installer appends new messages.</span></span> <span data-ttu-id="16a6c-108">Se o arquivo de log não existir, o instalador criará um arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="16a6c-108">If the log file does not exist, the installer creates a log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="16a6c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16a6c-109">Syntax</span></span>


```JScript
Merge.OpenLog(
  Filename
)
```



## <a name="parameters"></a><span data-ttu-id="16a6c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16a6c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16a6c-111">*Filename*</span><span class="sxs-lookup"><span data-stu-id="16a6c-111">*Filename*</span></span> 
</dt> <dd>

<span data-ttu-id="16a6c-112">Nome de arquivo totalmente qualificado que aponta para um arquivo a ser aberto ou criado.</span><span class="sxs-lookup"><span data-stu-id="16a6c-112">Fully qualified file name pointing to a file to open or create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16a6c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="16a6c-113">Return value</span></span>

<span data-ttu-id="16a6c-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="16a6c-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="16a6c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="16a6c-115">Remarks</span></span>

<span data-ttu-id="16a6c-116">Os clientes podem enviar suas próprias mensagens para esse arquivo de log por meio do método [**log**](merge-log.md) .</span><span class="sxs-lookup"><span data-stu-id="16a6c-116">Clients may send their own messages to this log file through the [**Log**](merge-log.md) method.</span></span>

### <a name="c"></a><span data-ttu-id="16a6c-117">C++</span><span class="sxs-lookup"><span data-stu-id="16a6c-117">C++</span></span>

<span data-ttu-id="16a6c-118">Consulte a função [**OpenLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog) .</span><span class="sxs-lookup"><span data-stu-id="16a6c-118">See [**OpenLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="16a6c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16a6c-119">Requirements</span></span>



| <span data-ttu-id="16a6c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="16a6c-120">Requirement</span></span> | <span data-ttu-id="16a6c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="16a6c-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16a6c-122">Versão</span><span class="sxs-lookup"><span data-stu-id="16a6c-122">Version</span></span><br/> | <span data-ttu-id="16a6c-123">Mergemod.dll 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="16a6c-123">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="16a6c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16a6c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="16a6c-125"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="16a6c-125"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="16a6c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="16a6c-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="16a6c-127"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16a6c-127"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
