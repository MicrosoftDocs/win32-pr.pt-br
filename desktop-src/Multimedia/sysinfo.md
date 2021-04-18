---
title: comando sysinfo
description: O comando sysinfo recupera informações do sistema MCI. O comando sysinfo é um comando do sistema MCI; Ele é interpretado diretamente pelo MCI.
ms.assetid: 494e8976-aac3-4d9f-b14b-3d3fd1917b45
keywords:
- Multimídia do Windows de comando do sysinfo
topic_type:
- apiref
api_name:
- sysinfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4751a5633462afe1ca8e8cd9abee1afeb16ac242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758300"
---
# <a name="sysinfo-command"></a><span data-ttu-id="7d989-105">comando sysinfo</span><span class="sxs-lookup"><span data-stu-id="7d989-105">sysinfo command</span></span>

<span data-ttu-id="7d989-106">O comando sysinfo recupera informações do sistema MCI.</span><span class="sxs-lookup"><span data-stu-id="7d989-106">The sysinfo command retrieves MCI system information.</span></span> <span data-ttu-id="7d989-107">O comando sysinfo é um comando do sistema MCI; Ele é interpretado diretamente pelo MCI.</span><span class="sxs-lookup"><span data-stu-id="7d989-107">The sysinfo command is an MCI system command; it is interpreted directly by MCI.</span></span>

<span data-ttu-id="7d989-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="7d989-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("sysinfo %s %s %s"), 
  lpszDeviceID, 
  lpszRequest, 
  lpszFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7d989-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d989-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d989-110">*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="7d989-110">*lpszDeviceID*</span></span> 
</dt> <dd>

<span data-ttu-id="7d989-111">Identificador de um dispositivo ou tipo de dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="7d989-111">Identifier of an MCI device or device type.</span></span> <span data-ttu-id="7d989-112">Se um tipo de dispositivo for especificado, ele deverá ser um nome de tipo de dispositivo MCI padrão, conforme listado no material de referência para o comando de [**capacidade**](capability.md) .</span><span class="sxs-lookup"><span data-stu-id="7d989-112">If a device type is specified, it must be a standard MCI device-type name, as listed in the reference material for the [**capability**](capability.md) command.</span></span> <span data-ttu-id="7d989-113">Você pode especificar "All" quando o sinalizador especificado em *lpszRequest* permite essa possibilidade.</span><span class="sxs-lookup"><span data-stu-id="7d989-113">You can specify "all" when the flag specified in *lpszRequest* allows that possibility.</span></span>

</dd> <dt>

<span data-ttu-id="7d989-114">*lpszRequest*</span><span class="sxs-lookup"><span data-stu-id="7d989-114">*lpszRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="7d989-115">Um dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="7d989-115">One of the following flags.</span></span>



| <span data-ttu-id="7d989-116">Valor</span><span class="sxs-lookup"><span data-stu-id="7d989-116">Value</span></span>                                                                                                                                                                | <span data-ttu-id="7d989-117">Significado</span><span class="sxs-lookup"><span data-stu-id="7d989-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="installname"></span><span id="INSTALLNAME"></span><dl> <span data-ttu-id="7d989-118"><dt>**instalar o**</dt></span><span class="sxs-lookup"><span data-stu-id="7d989-118"><dt>**installname**</dt></span></span> </dl>               | <span data-ttu-id="7d989-119">Retorna o nome listado no registro ou o arquivo de SYSTEM.INI usado para instalar o dispositivo aberto com o identificador de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="7d989-119">Returns the name listed in the registry or the SYSTEM.INI file used to install the open device with the specified device identifier.</span></span><br/>                                                                                                                                                                                                            |
| <span id="quantity"></span><span id="QUANTITY"></span><dl> <span data-ttu-id="7d989-120"><dt>**quantidade**</dt></span><span class="sxs-lookup"><span data-stu-id="7d989-120"><dt>**quantity**</dt></span></span> </dl>                        | <span data-ttu-id="7d989-121">Retorna o número de dispositivos MCI listados no registro ou o arquivo de SYSTEM.INI do tipo especificado no parâmetro *lpszDeviceID* .</span><span class="sxs-lookup"><span data-stu-id="7d989-121">Returns the number of MCI devices listed in the registry or the SYSTEM.INI file of the type specified in the *lpszDeviceID* parameter.</span></span> <span data-ttu-id="7d989-122">Esse identificador de dispositivo deve ser um nome de tipo de dispositivo MCI padrão.</span><span class="sxs-lookup"><span data-stu-id="7d989-122">This device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="7d989-123">Quaisquer dígitos após o tipo de dispositivo são ignorados.</span><span class="sxs-lookup"><span data-stu-id="7d989-123">Any digits after the device type are ignored.</span></span> <span data-ttu-id="7d989-124">A especificação de "All" para *lpszDeviceID* retorna o número total de dispositivos MCI no sistema.</span><span class="sxs-lookup"><span data-stu-id="7d989-124">Specifying "all" for *lpszDeviceID* returns the total number of MCI devices in the system.</span></span><br/> |
| <span id="quantity_open"></span><span id="QUANTITY_OPEN"></span><dl> <span data-ttu-id="7d989-125"><dt>**quantidade aberta**</dt></span><span class="sxs-lookup"><span data-stu-id="7d989-125"><dt>**quantity open**</dt></span></span> </dl>         | <span data-ttu-id="7d989-126">Retorna o número de dispositivos MCI abertos do tipo especificado em *lpszDeviceID*.</span><span class="sxs-lookup"><span data-stu-id="7d989-126">Returns the number of open MCI devices of the type specified in *lpszDeviceID*.</span></span> <span data-ttu-id="7d989-127">Esse identificador de dispositivo deve ser um nome de tipo de dispositivo MCI padrão.</span><span class="sxs-lookup"><span data-stu-id="7d989-127">This device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="7d989-128">A especificação de "All" para *lpszDeviceID* retorna o número total de dispositivos MCI abertos no sistema.</span><span class="sxs-lookup"><span data-stu-id="7d989-128">Specifying "all" for *lpszDeviceID* returns the total number of open MCI devices in the system.</span></span><br/>                                                                                                 |
| <span id="name_index"></span><span id="NAME_INDEX"></span><dl> <span data-ttu-id="7d989-129"><dt>\* \* nome \* índice \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="7d989-129"><dt>\*\*name \*index\*\*\*</dt></span></span> </dl>                | <span data-ttu-id="7d989-130">Retorna o nome de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="7d989-130">Returns the name of an MCI device.</span></span> <span data-ttu-id="7d989-131">O identificador do dispositivo deve ser um nome de tipo de dispositivo MCI padrão.</span><span class="sxs-lookup"><span data-stu-id="7d989-131">The device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="7d989-132">O *índice* varia de 1 até o número de dispositivos desse tipo.</span><span class="sxs-lookup"><span data-stu-id="7d989-132">The *index* ranges from 1 to the number of devices of that type.</span></span> <span data-ttu-id="7d989-133">Se "All" for especificado para *lpszDeviceID*, os intervalos de *índice* de 1 para o número total de dispositivos no sistema.</span><span class="sxs-lookup"><span data-stu-id="7d989-133">If "all" is specified for *lpszDeviceID*, *index* ranges from 1 to the total number of devices in the system.</span></span><br/>                                                                |
| <span id="name_index_open"></span><span id="NAME_INDEX_OPEN"></span><dl> <span data-ttu-id="7d989-134"><dt>***índice* de nome aberto**</dt></span><span class="sxs-lookup"><span data-stu-id="7d989-134"><dt>**name *index* open**</dt></span></span> </dl> | <span data-ttu-id="7d989-135">Retorna o nome de um dispositivo MCI aberto.</span><span class="sxs-lookup"><span data-stu-id="7d989-135">Returns the name of an open MCI device.</span></span> <span data-ttu-id="7d989-136">O identificador do dispositivo deve ser um nome de tipo de dispositivo MCI padrão.</span><span class="sxs-lookup"><span data-stu-id="7d989-136">The device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="7d989-137">O *índice* varia de 1 até o número de dispositivos abertos desse tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7d989-137">The *index* ranges from 1 to the number of open devices of that device type.</span></span> <span data-ttu-id="7d989-138">Se "All" for especificado para *lpszDeviceID*, os intervalos de *índice* de 1 para o número total de dispositivos abertos no sistema.</span><span class="sxs-lookup"><span data-stu-id="7d989-138">If "all" is specified for *lpszDeviceID*, *index* ranges from 1 to the total number of open devices in the system.</span></span><br/>                                          |



 

</dd> <dt>

<span data-ttu-id="7d989-139">*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="7d989-139">*lpszFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="7d989-140">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="7d989-140">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="7d989-141">Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="7d989-141">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="7d989-142">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="7d989-142">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="7d989-143">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7d989-143">Examples</span></span>

<span data-ttu-id="7d989-144">O comando a seguir retorna o número de dispositivos Open Wave-Audio.</span><span class="sxs-lookup"><span data-stu-id="7d989-144">The following command returns the number of open waveform-audio devices.</span></span>

``` syntax
sysinfo waveaudio quantity open
```

<span data-ttu-id="7d989-145">O comando a seguir retorna o nome (alias do dispositivo) do primeiro dispositivo Open Wave-Audio.</span><span class="sxs-lookup"><span data-stu-id="7d989-145">The following command returns the name (device alias) of the first open waveform-audio device.</span></span>

``` syntax
sysinfo waveaudio name 1 open
```

## <a name="requirements"></a><span data-ttu-id="7d989-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d989-146">Requirements</span></span>



| <span data-ttu-id="7d989-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d989-147">Requirement</span></span> | <span data-ttu-id="7d989-148">Valor</span><span class="sxs-lookup"><span data-stu-id="7d989-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="7d989-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d989-149">Minimum supported client</span></span><br/> | <span data-ttu-id="7d989-150">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7d989-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7d989-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d989-151">Minimum supported server</span></span><br/> | <span data-ttu-id="7d989-152">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7d989-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="7d989-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d989-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d989-154">MCI</span><span class="sxs-lookup"><span data-stu-id="7d989-154">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="7d989-155">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="7d989-155">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="7d989-156">**recursos**</span><span class="sxs-lookup"><span data-stu-id="7d989-156">**capability**</span></span>](capability.md)
</dt> </dl>

 

