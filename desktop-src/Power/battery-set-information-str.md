---
description: Contém as informações da bateria a serem definidas.
ms.assetid: 535e56cb-2bab-458a-84a8-2d9a4d96412b
title: Estrutura de BATTERY_SET_INFORMATION (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 0b23489bc5a7608e2e8afb297bb4be7ba35cecb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091633"
---
# <a name="battery_set_information-structure"></a><span data-ttu-id="66a35-103">Estrutura de informações de \_ conjunto de bateria \_</span><span class="sxs-lookup"><span data-stu-id="66a35-103">BATTERY\_SET\_INFORMATION structure</span></span>

<span data-ttu-id="66a35-104">Contém as informações da bateria a serem definidas.</span><span class="sxs-lookup"><span data-stu-id="66a35-104">Contains battery information to be set.</span></span> <span data-ttu-id="66a35-105">Essa estrutura é usada com o código de controle de [**informações do conjunto de baterias do IOCTL \_ \_ \_**](ioctl-battery-set-information.md) .</span><span class="sxs-lookup"><span data-stu-id="66a35-105">This structure is used with the [**IOCTL\_BATTERY\_SET\_INFORMATION**](ioctl-battery-set-information.md) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="66a35-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66a35-106">Syntax</span></span>


```C++
typedef struct _BATTERY_SET_INFORMATION {
  ULONG                         BatteryTag;
  BATTERY_SET_INFORMATION_LEVEL InformationLevel;
  UCHAR                         Buffer[1];
} BATTERY_SET_INFORMATION, *PBATTERY_SET_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="66a35-107">Membros</span><span class="sxs-lookup"><span data-stu-id="66a35-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="66a35-108">**BatteryTag**</span><span class="sxs-lookup"><span data-stu-id="66a35-108">**BatteryTag**</span></span>
</dt> <dd>

<span data-ttu-id="66a35-109">A marca de bateria atual para a bateria.</span><span class="sxs-lookup"><span data-stu-id="66a35-109">The current battery tag for the battery.</span></span> <span data-ttu-id="66a35-110">As informações para uma bateria que correspondem à marca só podem ser retornadas.</span><span class="sxs-lookup"><span data-stu-id="66a35-110">Information for a battery matching the tag can only be returned.</span></span> <span data-ttu-id="66a35-111">Sempre que esse valor não corresponder à marca atual da bateria, a solicitação de IOCTL será concluída com o \_ arquivo \_ de erro não \_ encontrado, que indica ao chamador que a bateria para a qual ela tem uma marca não existe mais.</span><span class="sxs-lookup"><span data-stu-id="66a35-111">Whenever this value does not match the battery's current tag, the IOCTL request will be completed with ERROR\_FILE\_NOT\_FOUND, which indicates to the caller that the battery for which it has a tag for no longer exists.</span></span> <span data-ttu-id="66a35-112">O chamador pode optar por usar a operação de [**\_ \_ \_ marca de consulta da bateria do IOCTL**](ioctl-battery-query-tag.md) para determinar a marca da bateria recém-instalada, se existir uma.</span><span class="sxs-lookup"><span data-stu-id="66a35-112">The caller may opt to use the [**IOCTL\_BATTERY\_QUERY\_TAG**](ioctl-battery-query-tag.md) operation to determine the tag of the newly installed battery, if one exists.</span></span> <span data-ttu-id="66a35-113">(Consulte [marcas de bateria](battery-information.md) para obter mais informações.)</span><span class="sxs-lookup"><span data-stu-id="66a35-113">(See [Battery Tags](battery-information.md) for more information.)</span></span>

<span data-ttu-id="66a35-114">Quando uma solicitação de informações de consulta é feita, esse valor é verificado.</span><span class="sxs-lookup"><span data-stu-id="66a35-114">When a query information request is made, this value is verified.</span></span> <span data-ttu-id="66a35-115">Além disso, se a solicitação estiver em andamento enquanto esse valor for alterado, a solicitação será anulada com o status do \_ arquivo de erro \_ não \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="66a35-115">In addition, if the request is in progress while this value changes, the request is aborted with the status of ERROR\_FILE\_NOT\_FOUND.</span></span>

</dd> <dt>

<span data-ttu-id="66a35-116">**InformationLevel**</span><span class="sxs-lookup"><span data-stu-id="66a35-116">**InformationLevel**</span></span>
</dt> <dd>

<span data-ttu-id="66a35-117">As informações da bateria a serem definidas.</span><span class="sxs-lookup"><span data-stu-id="66a35-117">The battery information to be set.</span></span> <span data-ttu-id="66a35-118">O tipo de dados no membro do **buffer** depende do valor desse membro.</span><span class="sxs-lookup"><span data-stu-id="66a35-118">The type of data in the **Buffer** member depends on the value of this member.</span></span> <span data-ttu-id="66a35-119">Esse membro pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="66a35-119">This member can be one of the following values.</span></span>



| <span data-ttu-id="66a35-120">Valor</span><span class="sxs-lookup"><span data-stu-id="66a35-120">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="66a35-121">Significado</span><span class="sxs-lookup"><span data-stu-id="66a35-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryCharge"></span><span id="batterycharge"></span><span id="BATTERYCHARGE"></span><dl> <span data-ttu-id="66a35-122"><dt>**BatteryCharge**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="66a35-122"><dt>**BatteryCharge**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="66a35-123">Informa ao dispositivo de bateria que o usuário solicitou que a bateria deve cobrar no momento.</span><span class="sxs-lookup"><span data-stu-id="66a35-123">Informs the battery device that the user has requested that the battery should be charging at this time.</span></span> <span data-ttu-id="66a35-124">Por exemplo, com uma bateria/carregador/seletor inteligente, o aplicativo pode cobrar uma bateria por vez.</span><span class="sxs-lookup"><span data-stu-id="66a35-124">For example, with a smart battery/charger/selector, the application could charge one battery at a time.</span></span> <span data-ttu-id="66a35-125">O membro de **buffer** dessa estrutura é ignorado.</span><span class="sxs-lookup"><span data-stu-id="66a35-125">The **Buffer** member of this structure is ignored.</span></span><br/>                                                                      |
| <span id="BatteryCriticalBias"></span><span id="batterycriticalbias"></span><span id="BATTERYCRITICALBIAS"></span><dl> <span data-ttu-id="66a35-126"><dt>**BatteryCriticalBias**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="66a35-126"><dt>**BatteryCriticalBias**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="66a35-127">Define o ajuste de tendência crítica da bateria.</span><span class="sxs-lookup"><span data-stu-id="66a35-127">Sets the battery's critical bias adjustment.</span></span> <span data-ttu-id="66a35-128">Observe que esse valor normalmente seria alterado pelo software, e está presente no recurso interfaces somente como uma manutenção de recursos.</span><span class="sxs-lookup"><span data-stu-id="66a35-128">Note it is not envisioned that this value would normally be changed by software, and is present in the interfaces only as a maintenance feature.</span></span> <span data-ttu-id="66a35-129">Nem todas as baterias podem manter essa configuração, e as informações da bateria devem ser lidas para confirmar que a bateria aceitou a configuração.</span><span class="sxs-lookup"><span data-stu-id="66a35-129">Not all batteries can maintain such a setting, and the battery information should be read to confirm that the battery accepted the setting.</span></span><br/> |
| <span id="BatteryDischarge"></span><span id="batterydischarge"></span><span id="BATTERYDISCHARGE"></span><dl> <span data-ttu-id="66a35-130"><dt>**BatteryDischarge**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="66a35-130"><dt>**BatteryDischarge**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="66a35-131">Informa ao dispositivo de bateria que o usuário solicitou que a bateria está sendo descarregada no momento.</span><span class="sxs-lookup"><span data-stu-id="66a35-131">Informs the battery device that the user has requested that the battery be discharging at this time.</span></span> <span data-ttu-id="66a35-132">Por exemplo, isso pode ser usado para indicar a bateria que o usuário deseja para ligar o sistema no momento.</span><span class="sxs-lookup"><span data-stu-id="66a35-132">For example, this could be used to indicate which battery the user currently wants to power the system.</span></span> <span data-ttu-id="66a35-133">O membro de **buffer** dessa estrutura é ignorado.</span><span class="sxs-lookup"><span data-stu-id="66a35-133">The **Buffer** member of this structure is ignored.</span></span><br/>                                                                          |



 

</dd> <dt>

<span data-ttu-id="66a35-134">**Buffer**</span><span class="sxs-lookup"><span data-stu-id="66a35-134">**Buffer**</span></span>
</dt> <dd>

<span data-ttu-id="66a35-135">As informações da bateria a serem definidas.</span><span class="sxs-lookup"><span data-stu-id="66a35-135">The battery information to be set.</span></span> <span data-ttu-id="66a35-136">Os dados dependem do valor de **InformationLevel**.</span><span class="sxs-lookup"><span data-stu-id="66a35-136">The data depends on the value of **InformationLevel**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66a35-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="66a35-137">Remarks</span></span>

<span data-ttu-id="66a35-138">A estrutura de **\_ \_ informações do conjunto de bateria** é uma estrutura de comprimento variável e você deve alocar um buffer de tamanho adequado para que as informações sejam incluídas na estrutura.</span><span class="sxs-lookup"><span data-stu-id="66a35-138">The **BATTERY\_SET\_INFORMATION** structure is a variable-length structure, and you must allocate a buffer of suitable size for the information to be included in the structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="66a35-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66a35-139">Requirements</span></span>



| <span data-ttu-id="66a35-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="66a35-140">Requirement</span></span> | <span data-ttu-id="66a35-141">Valor</span><span class="sxs-lookup"><span data-stu-id="66a35-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66a35-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66a35-142">Minimum supported client</span></span><br/> | <span data-ttu-id="66a35-143">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="66a35-143">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="66a35-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66a35-144">Minimum supported server</span></span><br/> | <span data-ttu-id="66a35-145">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="66a35-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="66a35-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66a35-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="66a35-147"><dt>Poclass. h; </dt> <dt>Batclass. h no Windows server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="66a35-147"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66a35-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="66a35-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66a35-149">**\_informações do \_ conjunto de baterias do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="66a35-149">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

 




