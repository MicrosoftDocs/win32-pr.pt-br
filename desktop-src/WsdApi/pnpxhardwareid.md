---
description: Especifica o identificador de hardware PnP-X do serviço.
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: Elemento PnPXHardwareId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0ffc389ca6df363439dd6463b3f86ca756359e8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996523"
---
# <a name="pnpxhardwareid-element"></a><span data-ttu-id="9ea3e-103">Elemento PnPXHardwareId</span><span class="sxs-lookup"><span data-stu-id="9ea3e-103">PnPXHardwareId element</span></span>

<span data-ttu-id="9ea3e-104">Especifica o identificador de hardware PnP-X do serviço.</span><span class="sxs-lookup"><span data-stu-id="9ea3e-104">Specifies the PnP-X Hardware Identifier of the service.</span></span> <span data-ttu-id="9ea3e-105">O PnP corresponde a esse elemento com as descrições de hardware fornecidas na \[ seção PnpxDevice \] do arquivo inf do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ea3e-105">PnP matches this element with the hardware description(s) provided in the \[PnpxDevice\] section of the device's INF file.</span></span> <span data-ttu-id="9ea3e-106">Com base nessas informações, o serviço PnP seleciona e carrega o driver de dispositivo mais apropriado.</span><span class="sxs-lookup"><span data-stu-id="9ea3e-106">Based on this information, the PnP service selects and loads the most appropriate device driver.</span></span>

## <a name="usage"></a><span data-ttu-id="9ea3e-107">Uso</span><span class="sxs-lookup"><span data-stu-id="9ea3e-107">Usage</span></span>

``` syntax
<PnPXHardwareId/>
```

## <a name="attributes"></a><span data-ttu-id="9ea3e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9ea3e-108">Attributes</span></span>

<span data-ttu-id="9ea3e-109">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="9ea3e-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9ea3e-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="9ea3e-110">Child elements</span></span>

<span data-ttu-id="9ea3e-111">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="9ea3e-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="9ea3e-112">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="9ea3e-112">Parent elements</span></span>



| <span data-ttu-id="9ea3e-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="9ea3e-113">Element</span></span>                             | <span data-ttu-id="9ea3e-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="9ea3e-114">Description</span></span>                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ea3e-115">**hospedado**</span><span class="sxs-lookup"><span data-stu-id="9ea3e-115">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="9ea3e-116">Define elementos para os serviços definidos pelo host de serviço.</span><span class="sxs-lookup"><span data-stu-id="9ea3e-116">Defines elements for the services defined by the service host.</span></span> <br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="9ea3e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ea3e-117">Remarks</span></span>

<span data-ttu-id="9ea3e-118">Para especificar mais de uma ID de hardware, separe os identificadores com um caractere de espaço, por exemplo, "PnPX \_ SampleService \_ HWID \_ 1 PnPX \_ SampleService \_ HWID \_ 2 PnPX \_ SampleService1 \_ HWID \_ 3".</span><span class="sxs-lookup"><span data-stu-id="9ea3e-118">To specify more than one hardware ID, separate the identifiers with a space character, for example, "PnPX\_SampleService\_HWID\_1 PnPX\_SampleService\_HWID\_2 PnPX\_SampleService1\_HWID\_3".</span></span>

## <a name="element-information"></a><span data-ttu-id="9ea3e-119">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="9ea3e-119">Element information</span></span>



| <span data-ttu-id="9ea3e-120">Label</span><span class="sxs-lookup"><span data-stu-id="9ea3e-120">Label</span></span> | <span data-ttu-id="9ea3e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="9ea3e-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="9ea3e-122">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ea3e-122">Minimum supported system</span></span><br/> | <span data-ttu-id="9ea3e-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ea3e-123">Windows Vista</span></span> |
| <span data-ttu-id="9ea3e-124">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="9ea3e-124">Can be empty</span></span>                        | <span data-ttu-id="9ea3e-125">Sim</span><span class="sxs-lookup"><span data-stu-id="9ea3e-125">Yes</span></span>           |



 

 




