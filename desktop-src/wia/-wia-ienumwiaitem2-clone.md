---
description: Cria uma instância adicional da interface IEnumWiaItem2 e envia de volta um ponteiro para ela.
ms.assetid: 0d36d555-d0d9-4a1c-ac54-de611850449c
title: 'Método IEnumWiaItem2:: clone (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Clone
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3279e7db3efe66e940adbcb9677204e5df7867f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647492"
---
# <a name="ienumwiaitem2clone-method"></a><span data-ttu-id="c9a0d-103">Método IEnumWiaItem2:: clone</span><span class="sxs-lookup"><span data-stu-id="c9a0d-103">IEnumWiaItem2::Clone method</span></span>

<span data-ttu-id="c9a0d-104">Cria uma instância adicional da interface [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) e envia de volta um ponteiro para ela.</span><span class="sxs-lookup"><span data-stu-id="c9a0d-104">Creates an additional instance of the [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface and sends back a pointer to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9a0d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9a0d-105">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumWiaItem2 **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="c9a0d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9a0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9a0d-107">*ppIEnum* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c9a0d-107">*ppIEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a0d-108">Tipo: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c9a0d-108">Type: **[**IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span></span>

<span data-ttu-id="c9a0d-109">Recebe o endereço da instância de interface [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) que **IEnumWiaItem2:: clone** cria.</span><span class="sxs-lookup"><span data-stu-id="c9a0d-109">Receives the address of the [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface instance that **IEnumWiaItem2::Clone** creates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9a0d-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c9a0d-110">Return value</span></span>

<span data-ttu-id="c9a0d-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c9a0d-111">Type: **HRESULT**</span></span>

<span data-ttu-id="c9a0d-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c9a0d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c9a0d-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c9a0d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9a0d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9a0d-114">Remarks</span></span>

<span data-ttu-id="c9a0d-115">Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *ppIEnum* .</span><span class="sxs-lookup"><span data-stu-id="c9a0d-115">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9a0d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9a0d-116">Requirements</span></span>



| <span data-ttu-id="c9a0d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9a0d-117">Requirement</span></span> | <span data-ttu-id="c9a0d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c9a0d-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c9a0d-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9a0d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c9a0d-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c9a0d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c9a0d-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9a0d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c9a0d-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c9a0d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c9a0d-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c9a0d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9a0d-124"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9a0d-124"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="c9a0d-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="c9a0d-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c9a0d-126"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c9a0d-126"><dt>Wia.idl</dt></span></span> </dl> |



 

 
