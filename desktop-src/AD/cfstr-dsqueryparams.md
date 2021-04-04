---
title: CFSTR_DSQUERYPARAMS (DSQuery. h)
description: O \_ formato de área de transferência CFSTR DSQUERYPARAMS fornece um identificador de memória global (HGLOBAL) que contém uma estrutura DSQUERYPARAMS.
ms.assetid: bb8aea98-8309-42bf-993d-fa408bb4deb2
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSQUERYPARAMS
api_location:
- DSQuery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a330d228778f34118d232b2004e7294ab493ed77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918287"
---
# <a name="cfstr_dsqueryparams"></a><span data-ttu-id="2c5a8-103">CFSTR \_ DSQUERYPARAMS</span><span class="sxs-lookup"><span data-stu-id="2c5a8-103">CFSTR\_DSQUERYPARAMS</span></span>

<dl> <dt>

<span data-ttu-id="2c5a8-104"><span id="CFSTR_DSQUERYPARAMS"></span><span id="cfstr_dsqueryparams"></span>**CFSTR \_ DSQUERYPARAMS**</span><span class="sxs-lookup"><span data-stu-id="2c5a8-104"><span id="CFSTR_DSQUERYPARAMS"></span><span id="cfstr_dsqueryparams"></span>**CFSTR\_DSQUERYPARAMS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5a8-105">"DsQueryparameters"</span><span class="sxs-lookup"><span data-stu-id="2c5a8-105">"DsQueryParameters"</span></span>
</dt> <dt>



<span data-ttu-id="2c5a8-106">O formato de área de transferência **CFSTR \_ DSQUERYPARAMS** é suportado pelo [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) fornecido pelo método [**ICommonQuery:: OpenQueryWindow**](/windows/win32/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow) .</span><span class="sxs-lookup"><span data-stu-id="2c5a8-106">The **CFSTR\_DSQUERYPARAMS** clipboard format is supported by the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) provided by the [**ICommonQuery::OpenQueryWindow**](/windows/win32/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow) method.</span></span> <span data-ttu-id="2c5a8-107">O formato de área de transferência **CFSTR \_ DSQUERYPARAMS** fornece um identificador de memória global (**HGLOBAL**) que contém uma estrutura [**DSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) .</span><span class="sxs-lookup"><span data-stu-id="2c5a8-107">The **CFSTR\_DSQUERYPARAMS** clipboard format provides a global memory handle (**HGLOBAL**) that contains a [**DSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) structure.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c5a8-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c5a8-108">Requirements</span></span>



| <span data-ttu-id="2c5a8-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c5a8-109">Requirement</span></span> | <span data-ttu-id="2c5a8-110">Valor</span><span class="sxs-lookup"><span data-stu-id="2c5a8-110">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2c5a8-111">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c5a8-111">Minimum supported client</span></span><br/> | <span data-ttu-id="2c5a8-112">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c5a8-112">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="2c5a8-113">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c5a8-113">Minimum supported server</span></span><br/> | <span data-ttu-id="2c5a8-114">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c5a8-114">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="2c5a8-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2c5a8-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c5a8-116"><dt>DSQuery. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c5a8-116"><dt>DSQuery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c5a8-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c5a8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c5a8-118">**IDataObject**</span><span class="sxs-lookup"><span data-stu-id="2c5a8-118">**IDataObject**</span></span>](/windows/win32/api/objidl/nn-objidl-idataobject)
</dt> <dt>

[<span data-ttu-id="2c5a8-119">**ICommonQuery::OpenQueryWindow**</span><span class="sxs-lookup"><span data-stu-id="2c5a8-119">**ICommonQuery::OpenQueryWindow**</span></span>](/windows/win32/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow)
</dt> <dt>

[<span data-ttu-id="2c5a8-120">**DSQUERYPARAMS**</span><span class="sxs-lookup"><span data-stu-id="2c5a8-120">**DSQUERYPARAMS**</span></span>](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams)
</dt> </dl>

 

