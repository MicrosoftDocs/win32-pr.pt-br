---
description: Indica um tipo de alteração de status de serviço para monitoramento e relatório.
ms.assetid: 7508526c-02ce-4ac2-8616-491390a4afad
title: Enumeração de SC_EVENT_TYPE (Winsvcp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SC_EVENT_TYPE
api_type:
- HeaderDef
api_location:
- Winsvcp.h
ms.openlocfilehash: 55853d13844d3bb255ab0e84a50e8cbbea2d76ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754114"
---
# <a name="sc_event_type-enumeration"></a><span data-ttu-id="1ccca-103">Enumeração de tipo de \_ evento SC \_</span><span class="sxs-lookup"><span data-stu-id="1ccca-103">SC\_EVENT\_TYPE enumeration</span></span>

<span data-ttu-id="1ccca-104">Indica um tipo de alteração de status de serviço para monitoramento e relatório.</span><span class="sxs-lookup"><span data-stu-id="1ccca-104">Indicates a type of service status change for monitoring and reporting.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ccca-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ccca-105">Syntax</span></span>


```C++
typedef enum _SC_EVENT_TYPE { 
  SC_EVENT_DATABASE_CHANGE  = 0,
  SC_EVENT_PROPERTY_CHANGE  = 1,
  SC_EVENT_STATUS_CHANGE    = 2
} SC_EVENT_TYPE, *PSC_EVENT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="1ccca-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="1ccca-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1ccca-107"><span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span>**\_alteração do \_ banco de dados de eventos SC \_**</span><span class="sxs-lookup"><span data-stu-id="1ccca-107"><span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span>**SC\_EVENT\_DATABASE\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="1ccca-108">Um serviço foi adicionado ou excluído.</span><span class="sxs-lookup"><span data-stu-id="1ccca-108">A service has been added or deleted.</span></span> <span data-ttu-id="1ccca-109">O parâmetro *hService* da função [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) deve ser um identificador para o SCM.</span><span class="sxs-lookup"><span data-stu-id="1ccca-109">The *hService* parameter of the [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) function must be a handle to the SCM.</span></span>

</dd> <dt>

<span data-ttu-id="1ccca-110"><span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span>**\_alteração da \_ Propriedade do evento SC \_**</span><span class="sxs-lookup"><span data-stu-id="1ccca-110"><span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span>**SC\_EVENT\_PROPERTY\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="1ccca-111">Uma ou mais propriedades de serviço foram atualizadas.</span><span class="sxs-lookup"><span data-stu-id="1ccca-111">One or more of service properties have been updated.</span></span> <span data-ttu-id="1ccca-112">O parâmetro *hService* da função [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) deve ser um identificador para o serviço.</span><span class="sxs-lookup"><span data-stu-id="1ccca-112">The *hService* parameter of the [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) function must be a handle to the service.</span></span>

</dd> <dt>

<span data-ttu-id="1ccca-113"><span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span>**\_alteração do \_ status do evento SC \_**</span><span class="sxs-lookup"><span data-stu-id="1ccca-113"><span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span>**SC\_EVENT\_STATUS\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="1ccca-114">O status de um serviço foi alterado.</span><span class="sxs-lookup"><span data-stu-id="1ccca-114">The status of a service has changed.</span></span> <span data-ttu-id="1ccca-115">O parâmetro *hService* da função [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) deve ser um identificador para o serviço.</span><span class="sxs-lookup"><span data-stu-id="1ccca-115">The *hService* parameter of the [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) function must be a handle to the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1ccca-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ccca-116">Requirements</span></span>



| <span data-ttu-id="1ccca-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ccca-117">Requirement</span></span> | <span data-ttu-id="1ccca-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1ccca-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1ccca-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ccca-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1ccca-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1ccca-120">Windows 8</span></span><br/>                                                                 |
| <span data-ttu-id="1ccca-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ccca-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1ccca-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1ccca-122">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="1ccca-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ccca-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ccca-124"><dt>Winsvcp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ccca-124"><dt>Winsvcp.h</dt></span></span> </dl> |



 

 




