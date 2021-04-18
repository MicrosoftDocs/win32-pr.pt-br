---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de informações comuns.
ms.assetid: eaae7431-d53d-42a1-9286-001c6f5b1641
title: Propriedades de informações comuns (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Common
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: b773d8404997da20b4196c802ba12286679af683
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787642"
---
# <a name="common-information-properties"></a><span data-ttu-id="18642-103">Propriedades de informações comuns</span><span class="sxs-lookup"><span data-stu-id="18642-103">Common Information Properties</span></span>

<span data-ttu-id="18642-104">Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de informações comuns.</span><span class="sxs-lookup"><span data-stu-id="18642-104">Windows Portable Devices supports the following common information properties.</span></span>



| <span data-ttu-id="18642-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="18642-105">Property</span></span>                                      | <span data-ttu-id="18642-106">VarType</span><span class="sxs-lookup"><span data-stu-id="18642-106">VarType</span></span>        | <span data-ttu-id="18642-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="18642-107">Description</span></span>                                                                                              |
|-----------------------------------------------|----------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18642-108">**\_observações de \_ informações \_ comuns do WPD**</span><span class="sxs-lookup"><span data-stu-id="18642-108">**WPD\_COMMON\_INFORMATION\_NOTES**</span></span>           | <span data-ttu-id="18642-109">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="18642-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="18642-110">Para compromissos, tarefas e objetos semelhantes, essa propriedade contém todas as anotações para o objeto fornecido.</span><span class="sxs-lookup"><span data-stu-id="18642-110">For appointments, tasks, and similar objects, this property contains any notes for the given object.</span></span>     |
| <span data-ttu-id="18642-111">**\_assunto de \_ informações \_ comuns do WPD**</span><span class="sxs-lookup"><span data-stu-id="18642-111">**WPD\_COMMON\_INFORMATION\_SUBJECT**</span></span>         | <span data-ttu-id="18642-112">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="18642-112">**VT\_LPWSTR**</span></span> | <span data-ttu-id="18642-113">Um valor que especifica o campo de assunto deste objeto.</span><span class="sxs-lookup"><span data-stu-id="18642-113">A value that specifies the subject field of this object.</span></span>                                                 |
| <span data-ttu-id="18642-114">**\_texto de \_ corpo de informações comuns \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="18642-114">**WPD\_COMMON\_INFORMATION\_BODY\_TEXT**</span></span>      | <span data-ttu-id="18642-115">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="18642-115">**VT\_LPWSTR**</span></span> | <span data-ttu-id="18642-116">Essa propriedade contém o texto do corpo de um objeto, em formato HTML ou de texto não criptografado.</span><span class="sxs-lookup"><span data-stu-id="18642-116">This property contains the body text of an object, in plaintext or HTML format.</span></span>                          |
| <span data-ttu-id="18642-117">**\_prioridade de \_ informações \_ comuns WPD**</span><span class="sxs-lookup"><span data-stu-id="18642-117">**WPD\_COMMON\_INFORMATION\_PRIORITY**</span></span>        | <span data-ttu-id="18642-118">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="18642-118">**VT\_UI4**</span></span>    | <span data-ttu-id="18642-119">Um valor que especifica a prioridade deste objeto.</span><span class="sxs-lookup"><span data-stu-id="18642-119">A value that specifies the priority of this object.</span></span> <span data-ttu-id="18642-120">0 indica a prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="18642-120">0 indicates the highest priority.</span></span>                    |
| <span data-ttu-id="18642-121">**\_DateTime de \_ início de informações comuns \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="18642-121">**WPD\_COMMON\_INFORMATION\_START\_DATETIME**</span></span> | <span data-ttu-id="18642-122">**Data de VT \_**</span><span class="sxs-lookup"><span data-stu-id="18642-122">**VT\_DATE**</span></span>   | <span data-ttu-id="18642-123">Um valor que especifica a data/hora em que um compromisso, uma tarefa ou um objeto semelhante está agendado para iniciar.</span><span class="sxs-lookup"><span data-stu-id="18642-123">A value that specifies the date/time that an appointment, task, or similar object is scheduled to start.</span></span> |
| <span data-ttu-id="18642-124">**\_data de \_ término de informações comuns \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="18642-124">**WPD\_COMMON\_INFORMATION\_END\_DATETIME**</span></span>   | <span data-ttu-id="18642-125">**Data de VT \_**</span><span class="sxs-lookup"><span data-stu-id="18642-125">**VT\_DATE**</span></span>   | <span data-ttu-id="18642-126">Um valor que especifica a data/hora em que um compromisso, uma tarefa ou um objeto semelhante está agendado para terminar.</span><span class="sxs-lookup"><span data-stu-id="18642-126">A value that specifies the date/time that an appointment, task, or similar object is scheduled to end.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="18642-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18642-127">Requirements</span></span>



| <span data-ttu-id="18642-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="18642-128">Requirement</span></span> | <span data-ttu-id="18642-129">Valor</span><span class="sxs-lookup"><span data-stu-id="18642-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="18642-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="18642-130">Header</span></span><br/> | <dl> <span data-ttu-id="18642-131"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="18642-131"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18642-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="18642-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18642-133">**Propriedades e atributos WPD**</span><span class="sxs-lookup"><span data-stu-id="18642-133">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




