---
description: Ignora o número especificado de itens durante uma enumeração de objetos IWiaItem2 disponíveis.
ms.assetid: 7a5e9e1c-1e6e-4de0-9499-bf89e35c19aa
title: 'Método IEnumWiaItem2:: Skip (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Skip
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7618aad923136a9a32d8b7fb935050fefe07bff1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921073"
---
# <a name="ienumwiaitem2skip-method"></a><span data-ttu-id="085af-103">Método IEnumWiaItem2:: Skip</span><span class="sxs-lookup"><span data-stu-id="085af-103">IEnumWiaItem2::Skip method</span></span>

<span data-ttu-id="085af-104">Ignora o número especificado de itens durante uma enumeração de objetos [**IWiaItem2**](-wia-iwiaitem2.md) disponíveis.</span><span class="sxs-lookup"><span data-stu-id="085af-104">Skips the specified number of items during an enumeration of available [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="085af-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="085af-105">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG cElt
);
```



## <a name="parameters"></a><span data-ttu-id="085af-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="085af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="085af-107">*cElt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="085af-107">*cElt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="085af-108">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="085af-108">Type: **ULONG**</span></span>

<span data-ttu-id="085af-109">Especifica o número de itens a serem ignorados.</span><span class="sxs-lookup"><span data-stu-id="085af-109">Specifies the number of items to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="085af-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="085af-110">Return value</span></span>

<span data-ttu-id="085af-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="085af-111">Type: **HRESULT**</span></span>

<span data-ttu-id="085af-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="085af-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="085af-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="085af-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="085af-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="085af-114">Requirements</span></span>



| <span data-ttu-id="085af-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="085af-115">Requirement</span></span> | <span data-ttu-id="085af-116">Valor</span><span class="sxs-lookup"><span data-stu-id="085af-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="085af-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="085af-117">Minimum supported client</span></span><br/> | <span data-ttu-id="085af-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="085af-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="085af-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="085af-119">Minimum supported server</span></span><br/> | <span data-ttu-id="085af-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="085af-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="085af-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="085af-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="085af-122"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="085af-122"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="085af-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="085af-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="085af-124"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="085af-124"><dt>Wia.idl</dt></span></span> </dl> |



 

 




