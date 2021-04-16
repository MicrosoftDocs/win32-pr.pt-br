---
description: Converte o tempo universal coordenado (hora de Greenwich) na hora local do computador.
ms.assetid: 4085d7cb-d346-477d-a043-e96fb951c35a
title: Método Utilities. UTCTimeToLocalTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.UTCTimeToLocalTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fe41cf8d9ec92c0c71be5130aded0b7db539b9b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757995"
---
# <a name="utilitiesutctimetolocaltime-method"></a><span data-ttu-id="074c0-103">Método Utilities. UTCTimeToLocalTime</span><span class="sxs-lookup"><span data-stu-id="074c0-103">Utilities.UTCTimeToLocalTime method</span></span>

<span data-ttu-id="074c0-104">\[O método **UTCTimeToLocalTime** está disponível para uso nos sistemas operacionais especificados na seção requisitos.\]</span><span class="sxs-lookup"><span data-stu-id="074c0-104">\[The **UTCTimeToLocalTime** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="074c0-105">O método **UTCTimeToLocalTime** converte o tempo universal coordenado (hora de Greenwich) na hora local do computador.</span><span class="sxs-lookup"><span data-stu-id="074c0-105">The **UTCTimeToLocalTime** method converts Coordinated Universal Time (Greenwich Mean Time) to the computer's local time.</span></span>

## <a name="syntax"></a><span data-ttu-id="074c0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="074c0-106">Syntax</span></span>


```VB
Utilities.UTCTimeToLocalTime( _
  ByVal UTCTime _
)
```



## <a name="parameters"></a><span data-ttu-id="074c0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="074c0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="074c0-108">*UTCTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="074c0-108">*UTCTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="074c0-109">O tempo universal coordenado a ser convertido na hora local do computador.</span><span class="sxs-lookup"><span data-stu-id="074c0-109">The Coordinated Universal Time to be converted to the computer's local time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="074c0-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="074c0-110">Return value</span></span>

<span data-ttu-id="074c0-111">A hora local que corresponde ao tempo universal coordenado especificado.</span><span class="sxs-lookup"><span data-stu-id="074c0-111">The local time that corresponds to the specified Coordinated Universal Time.</span></span>

## <a name="remarks"></a><span data-ttu-id="074c0-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="074c0-112">Remarks</span></span>

<span data-ttu-id="074c0-113">Enquanto o sistema usa o tempo universal coordenado internamente, os aplicativos geralmente exibem a hora local, que é a data e a hora do dia para o fuso horário local do computador.</span><span class="sxs-lookup"><span data-stu-id="074c0-113">While the system uses Coordinated Universal Time internally, applications generally display the local time, which is the date and time of day for the computer's local time zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="074c0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="074c0-114">Requirements</span></span>



| <span data-ttu-id="074c0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="074c0-115">Requirement</span></span> | <span data-ttu-id="074c0-116">Valor</span><span class="sxs-lookup"><span data-stu-id="074c0-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="074c0-117">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="074c0-117">Redistributable</span></span><br/> | <span data-ttu-id="074c0-118">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="074c0-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="074c0-119">DLL</span><span class="sxs-lookup"><span data-stu-id="074c0-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="074c0-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="074c0-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="074c0-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="074c0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="074c0-122">**Utilitários**</span><span class="sxs-lookup"><span data-stu-id="074c0-122">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 




