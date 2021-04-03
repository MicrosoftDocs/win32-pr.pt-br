---
title: Constantes de WINBIO_SENSOR_MODE (WinBio \_ Types. h)
description: Defina o modo do adaptador do sensor.
ms.assetid: fceaed5c-de59-4da7-9d7a-adeef353292f
topic_type:
- apiref
api_name:
- WINBIO_SENSOR_UNKNOWN_MODE
- WINBIO_SENSOR_BASIC_MODE
- WINBIO_SENSOR_ADVANCED_MODE
- WINBIO_SENSOR_NAVIGATION_MODE
- WINBIO_SENSOR_SLEEP_MODE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fedf419a64b3629d0cccbcb3d56de31a4adf383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645192"
---
# <a name="winbio_sensor_mode-constants"></a><span data-ttu-id="f97fe-103">Constantes do modo de \_ sensor WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="f97fe-103">WINBIO\_SENSOR\_MODE Constants</span></span>

<span data-ttu-id="f97fe-104">Os valores a seguir são usados na função [**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) para definir o modo do adaptador do sensor.</span><span class="sxs-lookup"><span data-stu-id="f97fe-104">The following values are used in the [**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) function to set the sensor adapter mode.</span></span>



| <span data-ttu-id="f97fe-105">Constante</span><span class="sxs-lookup"><span data-stu-id="f97fe-105">Constant</span></span>                                                                                                                                                                                                        | <span data-ttu-id="f97fe-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f97fe-106">Description</span></span>                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_SENSOR_UNKNOWN_MODE"></span><span id="winbio_sensor_unknown_mode"></span><dl> <span data-ttu-id="f97fe-107"><dt>**\_ \_ modo desconhecido do sensor de WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f97fe-107"><dt>**WINBIO\_SENSOR\_UNKNOWN\_MODE**</dt></span></span> </dl>          | <span data-ttu-id="f97fe-108">O modo de operação não é conhecido.</span><span class="sxs-lookup"><span data-stu-id="f97fe-108">The operating mode is not known.</span></span><br/>                                                                                                                    |
| <span id="WINBIO_SENSOR_BASIC_MODE"></span><span id="winbio_sensor_basic_mode"></span><dl> <span data-ttu-id="f97fe-109"><dt>**\_ \_ modo básico do sensor WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f97fe-109"><dt>**WINBIO\_SENSOR\_BASIC\_MODE**</dt></span></span> </dl>                | <span data-ttu-id="f97fe-110">Opere o sensor no modo básico.</span><span class="sxs-lookup"><span data-stu-id="f97fe-110">Operate the sensor in basic mode.</span></span> <span data-ttu-id="f97fe-111">O sensor atua apenas como um dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="f97fe-111">The sensor acts only as a capture device.</span></span> <span data-ttu-id="f97fe-112">Qualquer recurso integrado de processamento ou armazenamento que não exista não será usado.</span><span class="sxs-lookup"><span data-stu-id="f97fe-112">Any onboard processing or storage capabilities that exist are not used.</span></span><br/> |
| <span id="WINBIO_SENSOR_ADVANCED_MODE"></span><span id="winbio_sensor_advanced_mode"></span><dl> <span data-ttu-id="f97fe-113"><dt>**\_ \_ modo avançado do sensor WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f97fe-113"><dt>**WINBIO\_SENSOR\_ADVANCED\_MODE**</dt></span></span> </dl>       | <span data-ttu-id="f97fe-114">Opere o sensor no modo avançado.</span><span class="sxs-lookup"><span data-stu-id="f97fe-114">Operate the sensor in advanced mode.</span></span> <span data-ttu-id="f97fe-115">O sensor pode capturar amostras e executar funções de correspondência e armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f97fe-115">The sensor can capture samples and perform matching and storage functions.</span></span><br/>                                     |
| <span id="WINBIO_SENSOR_NAVIGATION_MODE"></span><span id="winbio_sensor_navigation_mode"></span><dl> <span data-ttu-id="f97fe-116"><dt>**\_modo de \_ navegação do sensor WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f97fe-116"><dt>**WINBIO\_SENSOR\_NAVIGATION\_MODE**</dt></span></span> </dl> | <span data-ttu-id="f97fe-117">Operar o sensor como um mouse pad.</span><span class="sxs-lookup"><span data-stu-id="f97fe-117">Operate the sensor as a mouse pad.</span></span> <span data-ttu-id="f97fe-118">Atualmente, não há suporte para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="f97fe-118">This is not currently supported.</span></span><br/>                                                                                 |
| <span id="WINBIO_SENSOR_SLEEP_MODE"></span><span id="winbio_sensor_sleep_mode"></span><dl> <span data-ttu-id="f97fe-119"><dt>**\_modo de \_ suspensão do sensor WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f97fe-119"><dt>**WINBIO\_SENSOR\_SLEEP\_MODE**</dt></span></span> </dl>                | <span data-ttu-id="f97fe-120">Opere o sensor no modo de suspensão.</span><span class="sxs-lookup"><span data-stu-id="f97fe-120">Operate the sensor in sleep mode.</span></span><br/>                                                                                                                   |



## <a name="requirements"></a><span data-ttu-id="f97fe-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f97fe-121">Requirements</span></span>



| <span data-ttu-id="f97fe-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f97fe-122">Requirement</span></span> | <span data-ttu-id="f97fe-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f97fe-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f97fe-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f97fe-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f97fe-125">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f97fe-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="f97fe-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f97fe-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f97fe-127">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="f97fe-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f97fe-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f97fe-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f97fe-129"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f97fe-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f97fe-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="f97fe-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f97fe-131">Constantes de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="f97fe-131">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





