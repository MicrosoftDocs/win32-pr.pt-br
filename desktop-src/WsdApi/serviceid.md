---
description: Um URI que representa o identificador de serviço.
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: Elemento ServiceId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305e97250b0b33d276dced4b5d454aec9298387c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814156"
---
# <a name="serviceid-element"></a><span data-ttu-id="ab234-103">Elemento ServiceId</span><span class="sxs-lookup"><span data-stu-id="ab234-103">ServiceID element</span></span>

<span data-ttu-id="ab234-104">Um URI que representa o identificador de serviço.</span><span class="sxs-lookup"><span data-stu-id="ab234-104">A URI that represents the service identifier.</span></span>

## <a name="usage"></a><span data-ttu-id="ab234-105">Uso</span><span class="sxs-lookup"><span data-stu-id="ab234-105">Usage</span></span>

``` syntax
<ServiceID/>
```

## <a name="attributes"></a><span data-ttu-id="ab234-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="ab234-106">Attributes</span></span>

<span data-ttu-id="ab234-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="ab234-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ab234-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ab234-108">Child elements</span></span>

<span data-ttu-id="ab234-109">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="ab234-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="ab234-110">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="ab234-110">Parent elements</span></span>



| <span data-ttu-id="ab234-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="ab234-111">Element</span></span>                             | <span data-ttu-id="ab234-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab234-112">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab234-113">**hospedeira**</span><span class="sxs-lookup"><span data-stu-id="ab234-113">**host**</span></span>](host.md)<br/>     | <span data-ttu-id="ab234-114">Define os elementos **ServiceId** e [**Types**](types.md) para o host de serviço.</span><span class="sxs-lookup"><span data-stu-id="ab234-114">Defines the **ServiceID** and [**Types**](types.md) elements for the service host.</span></span> <span data-ttu-id="ab234-115">Se não for fornecido explicitamente, o WSDAPI não fornecerá nenhum dado padrão em resposta a solicitações de metadados.</span><span class="sxs-lookup"><span data-stu-id="ab234-115">If not provided explicitly, WSDAPI will not supply any default data in response to metadata requests.</span></span><br/> <br/>                                                                                                                     |
| [<span data-ttu-id="ab234-116">**hospedado**</span><span class="sxs-lookup"><span data-stu-id="ab234-116">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="ab234-117">Define os elementos **ServiceId** e [**Types**](types.md) para os serviços fornecidos por esse host de serviço.</span><span class="sxs-lookup"><span data-stu-id="ab234-117">Defines the **ServiceID** and [**Types**](types.md) elements for the services provided by this service host.</span></span> <span data-ttu-id="ab234-118">Cada serviço fornecido por esse host de serviço deve ter suas próprias informações de elemento [**hospedado**](hosted.md) para garantir que o serviço seja publicado corretamente em respostas a solicitações de metadados.</span><span class="sxs-lookup"><span data-stu-id="ab234-118">Each service provided by this service host should have its own [**hosted**](hosted.md) element information to ensure that the service is published properly in responses to metadata requests.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="ab234-119">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="ab234-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="ab234-120">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab234-120">Minimum supported system</span></span><br/> | <span data-ttu-id="ab234-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab234-121">Windows Vista</span></span> |
| <span data-ttu-id="ab234-122">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="ab234-122">Can be empty</span></span>                        | <span data-ttu-id="ab234-123">Sim</span><span class="sxs-lookup"><span data-stu-id="ab234-123">Yes</span></span>           |



 

 




