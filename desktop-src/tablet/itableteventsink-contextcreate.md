---
description: Ocorre quando um novo contexto do Tablet é criado.
ms.assetid: 64e1f778-90c1-417d-a80b-37aeecffd411
title: 'Método ITabletEventSink:: ContextCreate'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.ContextCreate
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: e622a246c7c317cf9e3373cbd3791108ed071e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297531"
---
# <a name="itableteventsinkcontextcreate-method"></a><span data-ttu-id="20dee-103">Método ITabletEventSink:: ContextCreate</span><span class="sxs-lookup"><span data-stu-id="20dee-103">ITabletEventSink::ContextCreate method</span></span>

<span data-ttu-id="20dee-104">Ocorre quando um novo contexto do Tablet é criado.</span><span class="sxs-lookup"><span data-stu-id="20dee-104">Occurs when a new tablet context is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="20dee-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20dee-105">Syntax</span></span>


```C++
HRESULT ContextCreate(
  [in] TABLET_CONTEXT_ID tcid
);
```



## <a name="parameters"></a><span data-ttu-id="20dee-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20dee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20dee-107">*TCID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20dee-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20dee-108">O identificador do contexto do Tablet que está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="20dee-108">The identifier of the tablet context being created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20dee-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="20dee-109">Return value</span></span>

<span data-ttu-id="20dee-110">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="20dee-110">This method can return one of these values.</span></span>



| <span data-ttu-id="20dee-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="20dee-111">Return code</span></span>                                                                            | <span data-ttu-id="20dee-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="20dee-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="20dee-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="20dee-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="20dee-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="20dee-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="20dee-115"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="20dee-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="20dee-116">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="20dee-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="20dee-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20dee-117">Requirements</span></span>



| <span data-ttu-id="20dee-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="20dee-118">Requirement</span></span> | <span data-ttu-id="20dee-119">Valor</span><span class="sxs-lookup"><span data-stu-id="20dee-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="20dee-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20dee-120">Minimum supported client</span></span><br/> | <span data-ttu-id="20dee-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="20dee-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="20dee-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20dee-122">Minimum supported server</span></span><br/> | <span data-ttu-id="20dee-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="20dee-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="20dee-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="20dee-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="20dee-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="20dee-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20dee-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="20dee-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20dee-127">**Interface ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="20dee-127">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




