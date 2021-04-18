---
title: Método getint32property da classe Win32_RDMSVirtualDesktopCollection (Microsoft. Diagnostics. appanalysis. h)
description: Recupera uma propriedade de número inteiro de uma coleção de áreas de trabalho virtuais.
ms.assetid: 18ffca65-e7c0-4b17-902f-d74b2a81aba2
ms.tgt_platform: multiple
keywords:
- Método getint32property Serviços de Área de Trabalho Remota
- Método getint32property Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Serviços de Área de Trabalho Remota, método getint32property
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e8e5518590bece8e8b904ea56bf7572b436b66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764745"
---
# <a name="getint32property-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="178d8-106">Método getint32property da classe Win32 \_ RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="178d8-106">GetInt32Property method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="178d8-107">Recupera uma propriedade de número inteiro de uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="178d8-107">Retrieves an integer property from a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="178d8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="178d8-108">Syntax</span></span>


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="178d8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="178d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="178d8-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="178d8-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="178d8-111">Uma chave que identifica a propriedade a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="178d8-111">A key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="178d8-112">*Valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="178d8-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="178d8-113">Um inteiro que recebe o valor recuperado.</span><span class="sxs-lookup"><span data-stu-id="178d8-113">An integer that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="178d8-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="178d8-114">Return value</span></span>

<span data-ttu-id="178d8-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="178d8-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="178d8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="178d8-116">Requirements</span></span>



| <span data-ttu-id="178d8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="178d8-117">Requirement</span></span> | <span data-ttu-id="178d8-118">Valor</span><span class="sxs-lookup"><span data-stu-id="178d8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="178d8-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="178d8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="178d8-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="178d8-120">None supported</span></span><br/>                                                                                      |
| <span data-ttu-id="178d8-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="178d8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="178d8-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="178d8-122">Windows Server 2012</span></span><br/>                                                                                 |
| <span data-ttu-id="178d8-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="178d8-123">Namespace</span></span><br/>                | <span data-ttu-id="178d8-124">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="178d8-124">Root\\CIMv2\\rdms</span></span><br/>                                                                                   |
| <span data-ttu-id="178d8-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="178d8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="178d8-126"><dt>Microsoft. Diagnostics. appanalysis. h</dt></span><span class="sxs-lookup"><span data-stu-id="178d8-126"><dt>Microsoft.diagnostics.appanalysis.h</dt></span></span> </dl> |
| <span data-ttu-id="178d8-127">MOF</span><span class="sxs-lookup"><span data-stu-id="178d8-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="178d8-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="178d8-128"><dt>RDManagement.mof</dt></span></span> </dl>                    |
| <span data-ttu-id="178d8-129">DLL</span><span class="sxs-lookup"><span data-stu-id="178d8-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="178d8-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="178d8-130"><dt>RDMS.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="178d8-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="178d8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="178d8-132">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="178d8-132">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





