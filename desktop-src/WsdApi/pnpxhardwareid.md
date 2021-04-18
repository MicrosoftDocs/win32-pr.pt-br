---
description: Especifica o identificador de hardware PnP-X do serviço.
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: Elemento PnPXHardwareId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55e5e38b669a289545225df96fad05e55069b474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781578"
---
# <a name="pnpxhardwareid-element"></a><span data-ttu-id="4b9e6-103">Elemento PnPXHardwareId</span><span class="sxs-lookup"><span data-stu-id="4b9e6-103">PnPXHardwareId element</span></span>

<span data-ttu-id="4b9e6-104">Especifica o identificador de hardware PnP-X do serviço.</span><span class="sxs-lookup"><span data-stu-id="4b9e6-104">Specifies the PnP-X Hardware Identifier of the service.</span></span> <span data-ttu-id="4b9e6-105">O PnP corresponde a esse elemento com as descrições de hardware fornecidas na \[ seção PnpxDevice \] do arquivo inf do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4b9e6-105">PnP matches this element with the hardware description(s) provided in the \[PnpxDevice\] section of the device's INF file.</span></span> <span data-ttu-id="4b9e6-106">Com base nessas informações, o serviço PnP seleciona e carrega o driver de dispositivo mais apropriado.</span><span class="sxs-lookup"><span data-stu-id="4b9e6-106">Based on this information, the PnP service selects and loads the most appropriate device driver.</span></span>

## <a name="usage"></a><span data-ttu-id="4b9e6-107">Uso</span><span class="sxs-lookup"><span data-stu-id="4b9e6-107">Usage</span></span>

``` syntax
<PnPXHardwareId/>
```

## <a name="attributes"></a><span data-ttu-id="4b9e6-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4b9e6-108">Attributes</span></span>

<span data-ttu-id="4b9e6-109">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="4b9e6-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4b9e6-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4b9e6-110">Child elements</span></span>

<span data-ttu-id="4b9e6-111">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="4b9e6-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="4b9e6-112">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="4b9e6-112">Parent elements</span></span>



| <span data-ttu-id="4b9e6-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="4b9e6-113">Element</span></span>                             | <span data-ttu-id="4b9e6-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b9e6-114">Description</span></span>                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b9e6-115">**hospedado**</span><span class="sxs-lookup"><span data-stu-id="4b9e6-115">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="4b9e6-116">Define elementos para os serviços definidos pelo host de serviço.</span><span class="sxs-lookup"><span data-stu-id="4b9e6-116">Defines elements for the services defined by the service host.</span></span> <br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="4b9e6-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b9e6-117">Remarks</span></span>

<span data-ttu-id="4b9e6-118">Para especificar mais de uma ID de hardware, separe os identificadores com um caractere de espaço, por exemplo, "PnPX \_ SampleService \_ HWID \_ 1 PnPX \_ SampleService \_ HWID \_ 2 PnPX \_ SampleService1 \_ HWID \_ 3".</span><span class="sxs-lookup"><span data-stu-id="4b9e6-118">To specify more than one hardware ID, separate the identifiers with a space character, for example, "PnPX\_SampleService\_HWID\_1 PnPX\_SampleService\_HWID\_2 PnPX\_SampleService1\_HWID\_3".</span></span>

## <a name="element-information"></a><span data-ttu-id="4b9e6-119">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="4b9e6-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="4b9e6-120">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b9e6-120">Minimum supported system</span></span><br/> | <span data-ttu-id="4b9e6-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b9e6-121">Windows Vista</span></span> |
| <span data-ttu-id="4b9e6-122">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="4b9e6-122">Can be empty</span></span>                        | <span data-ttu-id="4b9e6-123">Sim</span><span class="sxs-lookup"><span data-stu-id="4b9e6-123">Yes</span></span>           |



 

 




