---
description: Converte a hora local do computador em tempo universal coordenado (Greenwich Mean Time).
ms.assetid: ff5d40ba-7d94-4f11-9c18-e41752d1d7b9
title: Método Utilities. LocalTimeToUTCTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.LocalTimeToUTCTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2691e3306a84ce4eff3d73df4b070ba4b65671f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767815"
---
# <a name="utilitieslocaltimetoutctime-method"></a><span data-ttu-id="aa576-103">Método Utilities. LocalTimeToUTCTime</span><span class="sxs-lookup"><span data-stu-id="aa576-103">Utilities.LocalTimeToUTCTime method</span></span>

<span data-ttu-id="aa576-104">\[O método **LocalTimeToUTCTime** está disponível para uso nos sistemas operacionais especificados na seção requisitos.\]</span><span class="sxs-lookup"><span data-stu-id="aa576-104">\[The **LocalTimeToUTCTime** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="aa576-105">O método **LocalTimeToUTCTime** converte a hora local do computador em tempo universal coordenado (Greenwich Mean Time).</span><span class="sxs-lookup"><span data-stu-id="aa576-105">The **LocalTimeToUTCTime** method converts the computer's local time to Coordinated Universal Time (Greenwich Mean Time).</span></span>

## <a name="syntax"></a><span data-ttu-id="aa576-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa576-106">Syntax</span></span>


```VB
Utilities.LocalTimeToUTCTime( _
  ByVal LocalTime _
)
```



## <a name="parameters"></a><span data-ttu-id="aa576-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa576-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa576-108">*Localtime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa576-108">*LocalTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa576-109">A hora local a ser convertida em tempo universal coordenado.</span><span class="sxs-lookup"><span data-stu-id="aa576-109">The local time to be converted to Coordinated Universal Time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa576-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa576-110">Return value</span></span>

<span data-ttu-id="aa576-111">O tempo universal coordenado que corresponde à hora local especificada.</span><span class="sxs-lookup"><span data-stu-id="aa576-111">The Coordinated Universal Time that corresponds to the specified local time.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa576-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa576-112">Remarks</span></span>

<span data-ttu-id="aa576-113">Enquanto o sistema usa o tempo universal coordenado internamente, os aplicativos geralmente exibem a hora local, que é a data e a hora do dia para o fuso horário local do computador.</span><span class="sxs-lookup"><span data-stu-id="aa576-113">While the system uses Coordinated Universal Time internally, applications generally display the local time, which is the date and time of day for the computer's local time zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa576-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa576-114">Requirements</span></span>



| <span data-ttu-id="aa576-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa576-115">Requirement</span></span> | <span data-ttu-id="aa576-116">Valor</span><span class="sxs-lookup"><span data-stu-id="aa576-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa576-117">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="aa576-117">Redistributable</span></span><br/> | <span data-ttu-id="aa576-118">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="aa576-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="aa576-119">DLL</span><span class="sxs-lookup"><span data-stu-id="aa576-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="aa576-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa576-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa576-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa576-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa576-122">**Utilitários**</span><span class="sxs-lookup"><span data-stu-id="aa576-122">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 




