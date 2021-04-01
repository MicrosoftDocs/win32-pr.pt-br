---
title: Método getint32property da classe Win32_RDSHServer (Microsoft. Diagnostics. appanalysis. h)
description: Recupera um valor da propriedade Integer de um \_ objeto RDSHServer do Win32.
ms.assetid: 4601e9cb-927b-4af8-a12b-09a8ca44c2f7
ms.tgt_platform: multiple
keywords:
- Método getint32property Serviços de Área de Trabalho Remota
- Método getint32property Serviços de Área de Trabalho Remota, classe Win32_RDSHServer
- Classe Win32_RDSHServer Serviços de Área de Trabalho Remota, método getint32property
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a2427cfa19a84a8b8988cceacf3e0b836a031f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918660"
---
# <a name="getint32property-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="9ead6-106">Método getint32property da classe Win32 \_ RDSHServer</span><span class="sxs-lookup"><span data-stu-id="9ead6-106">GetInt32Property method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="9ead6-107">Recupera um valor da propriedade Integer de um objeto [**\_ RDSHServer do Win32**](win32-rdshserver.md) .</span><span class="sxs-lookup"><span data-stu-id="9ead6-107">Retrieves an integer property value of a [**Win32\_RDSHServer**](win32-rdshserver.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ead6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ead6-108">Syntax</span></span>


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="9ead6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ead6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ead6-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9ead6-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ead6-111">A chave que identifica a propriedade a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="9ead6-111">The key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="9ead6-112">*Valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="9ead6-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ead6-113">Recebe o valor da propriedade recuperada.</span><span class="sxs-lookup"><span data-stu-id="9ead6-113">Receives the retrieved property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ead6-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9ead6-114">Return value</span></span>

<span data-ttu-id="9ead6-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="9ead6-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ead6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ead6-116">Requirements</span></span>



| <span data-ttu-id="9ead6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ead6-117">Requirement</span></span> | <span data-ttu-id="9ead6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9ead6-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ead6-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ead6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9ead6-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9ead6-120">None supported</span></span><br/>                                                                                      |
| <span data-ttu-id="9ead6-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ead6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9ead6-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9ead6-122">Windows Server 2012</span></span><br/>                                                                                 |
| <span data-ttu-id="9ead6-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="9ead6-123">Namespace</span></span><br/>                | <span data-ttu-id="9ead6-124">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="9ead6-124">Root\\CIMv2\\rdms</span></span><br/>                                                                                   |
| <span data-ttu-id="9ead6-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9ead6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ead6-126"><dt>Microsoft. Diagnostics. appanalysis. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ead6-126"><dt>Microsoft.diagnostics.appanalysis.h</dt></span></span> </dl> |
| <span data-ttu-id="9ead6-127">MOF</span><span class="sxs-lookup"><span data-stu-id="9ead6-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ead6-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ead6-128"><dt>RDManagement.mof</dt></span></span> </dl>                    |
| <span data-ttu-id="9ead6-129">DLL</span><span class="sxs-lookup"><span data-stu-id="9ead6-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ead6-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ead6-130"><dt>RDMS.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="9ead6-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ead6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ead6-132">**\_RDSHServer Win32**</span><span class="sxs-lookup"><span data-stu-id="9ead6-132">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





