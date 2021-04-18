---
description: A \_ mensagem de endereço de linha de TAPI é enviada quando o status de um endereço é alterado em uma linha que está aberta no momento pelo aplicativo. O aplicativo pode invocar lineGetAddressStatus para determinar o status atual do endereço.
ms.assetid: af211fa1-79f8-49ac-a1d8-b62981f50519
title: Mensagem de LINE_ADDRESSSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d85b42f6957487ff24706485bd09d1d47880fe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759465"
---
# <a name="line_addressstate-message"></a><span data-ttu-id="1f391-104">\_Mensagem addressstate de linha</span><span class="sxs-lookup"><span data-stu-id="1f391-104">LINE\_ADDRESSSTATE message</span></span>

<span data-ttu-id="1f391-105">A mensagem **de \_ endereço de linha** de TAPI é enviada quando o status de um endereço é alterado em uma linha que está aberta no momento pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1f391-105">The TAPI **LINE\_ADDRESSSTATE** message is sent when the status of an address changes on a line that is currently open by the application.</span></span> <span data-ttu-id="1f391-106">O aplicativo pode invocar [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) para determinar o status atual do endereço.</span><span class="sxs-lookup"><span data-stu-id="1f391-106">The application can invoke [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) to determine the current status of the address.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="1f391-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f391-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f391-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="1f391-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="1f391-109">Um identificador para o dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="1f391-109">A handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="1f391-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="1f391-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="1f391-111">A instância de retorno de chamada fornecida ao abrir a linha.</span><span class="sxs-lookup"><span data-stu-id="1f391-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="1f391-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="1f391-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="1f391-113">O identificador de endereço do endereço que alterou o status.</span><span class="sxs-lookup"><span data-stu-id="1f391-113">The address identifier of the address that changed status.</span></span>

</dd> <dt>

<span data-ttu-id="1f391-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="1f391-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="1f391-115">O estado do endereço que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="1f391-115">The address state that changed.</span></span> <span data-ttu-id="1f391-116">Pode ser uma ou mais das [**\_ constantes LINEADDRESSSTATE**](lineaddressstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="1f391-116">Can be one or more of the [**LINEADDRESSSTATE\_ constants**](lineaddressstate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f391-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="1f391-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="1f391-118">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="1f391-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f391-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1f391-119">Return value</span></span>

<span data-ttu-id="1f391-120">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="1f391-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f391-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f391-121">Remarks</span></span>

<span data-ttu-id="1f391-122">A **mensagem \_ Addressstate de linha** é enviada para qualquer aplicativo que tenha aberto o dispositivo de linha e que tenha habilitado esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="1f391-122">The **LINE\_ADDRESSSTATE** message is sent to any application that has opened the line device and that has enabled this message.</span></span> <span data-ttu-id="1f391-123">O envio dessa mensagem para os vários itens de status pode ser controlado e consultado usando [**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) e [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span><span class="sxs-lookup"><span data-stu-id="1f391-123">The sending of this message for the various status items can be controlled and queried using [**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) and [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span></span> <span data-ttu-id="1f391-124">Por padrão, o relatório de status de endereço é desabilitado.</span><span class="sxs-lookup"><span data-stu-id="1f391-124">By default, address status reporting is disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f391-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f391-125">Requirements</span></span>



| <span data-ttu-id="1f391-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f391-126">Requirement</span></span> | <span data-ttu-id="1f391-127">Valor</span><span class="sxs-lookup"><span data-stu-id="1f391-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1f391-128">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="1f391-128">TAPI version</span></span><br/> | <span data-ttu-id="1f391-129">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="1f391-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="1f391-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f391-130">Header</span></span><br/>       | <dl> <span data-ttu-id="1f391-131"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f391-131"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f391-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f391-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f391-133">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="1f391-133">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="1f391-134">**lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="1f391-134">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[<span data-ttu-id="1f391-135">**lineGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="1f391-135">**lineGetAddressStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[<span data-ttu-id="1f391-136">**lineGetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="1f391-136">**lineGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages)
</dt> <dt>

[<span data-ttu-id="1f391-137">**lineSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="1f391-137">**lineSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> </dl>

 

 




