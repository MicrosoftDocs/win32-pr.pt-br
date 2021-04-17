---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de tarefa.
ms.assetid: 9bd6c2e1-740a-453d-b390-120700af7c93
title: Propriedades da tarefa (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Task
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 829685ac3fa5737356c172ed9e66303b3d6115ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762416"
---
# <a name="task-properties"></a><span data-ttu-id="ee8c7-103">Propriedades da tarefa</span><span class="sxs-lookup"><span data-stu-id="ee8c7-103">Task Properties</span></span>

<span data-ttu-id="ee8c7-104">Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de tarefa.</span><span class="sxs-lookup"><span data-stu-id="ee8c7-104">Windows Portable Devices supports the following task properties.</span></span>



| <span data-ttu-id="ee8c7-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ee8c7-105">Property</span></span>                         | <span data-ttu-id="ee8c7-106">VarType</span><span class="sxs-lookup"><span data-stu-id="ee8c7-106">VarType</span></span>        | <span data-ttu-id="ee8c7-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee8c7-107">Description</span></span>                                                                                 |
|----------------------------------|----------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee8c7-108">**\_proprietário da tarefa WPD \_**</span><span class="sxs-lookup"><span data-stu-id="ee8c7-108">**WPD\_TASK\_OWNER**</span></span>             | <span data-ttu-id="ee8c7-109">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="ee8c7-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="ee8c7-110">O proprietário da tarefa.</span><span class="sxs-lookup"><span data-stu-id="ee8c7-110">The owner of the task.</span></span>                                                                      |
| <span data-ttu-id="ee8c7-111">**\_porcentagem de tarefa WPD \_ \_ concluída**</span><span class="sxs-lookup"><span data-stu-id="ee8c7-111">**WPD\_TASK\_PERCENT\_COMPLETE**</span></span> | <span data-ttu-id="ee8c7-112">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="ee8c7-112">**VT\_UI4**</span></span>    | <span data-ttu-id="ee8c7-113">Um número entre 0 e 100 que especifica como concluir a tarefa.</span><span class="sxs-lookup"><span data-stu-id="ee8c7-113">A number between 0 and 100 that specifies how complete the task is.</span></span>                         |
| <span data-ttu-id="ee8c7-114">**\_data do \_ lembrete da tarefa WPD \_**</span><span class="sxs-lookup"><span data-stu-id="ee8c7-114">**WPD\_TASK\_REMINDER\_DATE**</span></span>    | <span data-ttu-id="ee8c7-115">**Data de VT \_**</span><span class="sxs-lookup"><span data-stu-id="ee8c7-115">**VT\_DATE**</span></span>   | <span data-ttu-id="ee8c7-116">Um valor que especifica quando um lembrete deve ser enviado para executar a tarefa, se não for concluído.</span><span class="sxs-lookup"><span data-stu-id="ee8c7-116">A value that specifies when a reminder should be sent to perform the task, if not complete.</span></span> |
| <span data-ttu-id="ee8c7-117">**\_status da tarefa WPD \_**</span><span class="sxs-lookup"><span data-stu-id="ee8c7-117">**WPD\_TASK\_STATUS**</span></span>            | <span data-ttu-id="ee8c7-118">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="ee8c7-118">**VT\_LPWSTR**</span></span> | <span data-ttu-id="ee8c7-119">Uma descrição da cadeia de caracteres do status da tarefa, por exemplo, "em andamento".</span><span class="sxs-lookup"><span data-stu-id="ee8c7-119">A string description of the status of the task, for example, "In Progress".</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="ee8c7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee8c7-120">Requirements</span></span>



| <span data-ttu-id="ee8c7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee8c7-121">Requirement</span></span> | <span data-ttu-id="ee8c7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ee8c7-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee8c7-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ee8c7-123">Header</span></span><br/> | <dl> <span data-ttu-id="ee8c7-124"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee8c7-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee8c7-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee8c7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee8c7-126">**Propriedades e atributos WPD**</span><span class="sxs-lookup"><span data-stu-id="ee8c7-126">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




