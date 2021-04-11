---
title: Estrutura de WINBIO_UNIT_SCHEMA (WinBio \_ Types. h)
description: Descreve os recursos de uma unidade biométrica.
ms.assetid: b20adf18-2948-481f-9d12-8da17aa152f7
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_UNIT_SCHEMA
- Ponteiro de estrutura de PWINBIO_UNIT_SCHEMA Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_UNIT_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c217be1e0c6bde740c815f5a990509a6a87ef0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919136"
---
# <a name="winbio_unit_schema-structure"></a><span data-ttu-id="35ccc-105">Estrutura de esquema de \_ unidade WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="35ccc-105">WINBIO\_UNIT\_SCHEMA structure</span></span>

<span data-ttu-id="35ccc-106">A estrutura de **\_ \_ esquema de unidade WINBIO** descreve os recursos de uma unidade biométrica.</span><span class="sxs-lookup"><span data-stu-id="35ccc-106">The **WINBIO\_UNIT\_SCHEMA** structure describes the capabilities of a biometric unit.</span></span> <span data-ttu-id="35ccc-107">Ele é usado pela função [**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits) .</span><span class="sxs-lookup"><span data-stu-id="35ccc-107">It is used by the [**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="35ccc-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35ccc-108">Syntax</span></span>


```C++
typedef struct _WINBIO_UNIT_SCHEMA {
  WINBIO_UNIT_ID                  UnitId;
  WINBIO_POOL_TYPE                PoolType;
  WINBIO_BIOMETRIC_TYPE           BiometricFactor;
  WINBIO_BIOMETRIC_SENSOR_SUBTYPE SensorSubType;
  WINBIO_CAPABILITIES             Capabilities;
  WINBIO_STRING                   DeviceInstanceId;
  WINBIO_STRING                   Description;
  WINBIO_STRING                   Manufacturer;
  WINBIO_STRING                   Model;
  WINBIO_STRING                   SerialNumber;
  WINBIO_VERSION                  FirmwareVersion;
} WINBIO_UNIT_SCHEMA, *PWINBIO_UNIT_SCHEMA;
```



## <a name="members"></a><span data-ttu-id="35ccc-109">Membros</span><span class="sxs-lookup"><span data-stu-id="35ccc-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="35ccc-110">**Unidadeid**</span><span class="sxs-lookup"><span data-stu-id="35ccc-110">**UnitId**</span></span>
</dt> <dd>

<span data-ttu-id="35ccc-111">Um valor que identifica a unidade biométrica.</span><span class="sxs-lookup"><span data-stu-id="35ccc-111">A value that identifies the biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="35ccc-112">**Pooltype**</span><span class="sxs-lookup"><span data-stu-id="35ccc-112">**PoolType**</span></span>
</dt> <dd>

<span data-ttu-id="35ccc-113">Um valor **ULONG** que especifica o tipo da unidade biométrica.</span><span class="sxs-lookup"><span data-stu-id="35ccc-113">A **ULONG** value that specifies the type of the biometric unit.</span></span> <span data-ttu-id="35ccc-114">Esse valor pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="35ccc-114">This can be one of the following values:</span></span>



| <span data-ttu-id="35ccc-115">Valor</span><span class="sxs-lookup"><span data-stu-id="35ccc-115">Value</span></span>                                                                                                                                                                            | <span data-ttu-id="35ccc-116">Significado</span><span class="sxs-lookup"><span data-stu-id="35ccc-116">Meaning</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <span data-ttu-id="35ccc-117"><dt>**\_pool WINBIO \_ desconhecido**</dt></span><span class="sxs-lookup"><span data-stu-id="35ccc-117"><dt>**WINBIO\_POOL\_UNKNOWN**</dt></span></span> </dl> | <span data-ttu-id="35ccc-118">O tipo é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="35ccc-118">The type is unknown.</span></span><br/>                                                                            |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <span data-ttu-id="35ccc-119"><dt>**\_sistema de pool WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="35ccc-119"><dt>**WINBIO\_POOL\_SYSTEM**</dt></span></span> </dl>    | <span data-ttu-id="35ccc-120">A sessão se conecta a uma coleção compartilhada de unidades biométricas gerenciadas pelo provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="35ccc-120">The session connects to a shared collection of biometric units managed by the service provider.</span></span><br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <span data-ttu-id="35ccc-121"><dt>**WINBIO \_ pool \_ privado**</dt></span><span class="sxs-lookup"><span data-stu-id="35ccc-121"><dt>**WINBIO\_POOL\_PRIVATE**</dt></span></span> </dl> | <span data-ttu-id="35ccc-122">A sessão se conecta a uma coleção de unidades biométricas que são gerenciadas pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="35ccc-122">The session connects to a collection of biometric units that are managed by the caller.</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="35ccc-123">**BiometricFactor**</span><span class="sxs-lookup"><span data-stu-id="35ccc-123">**BiometricFactor**</span></span>
</dt> <dd>

<span data-ttu-id="35ccc-124">Um valor que especifica o tipo da unidade biométrica.</span><span class="sxs-lookup"><span data-stu-id="35ccc-124">A value that specifies the type of the biometric unit.</span></span> <span data-ttu-id="35ccc-125">No momento, somente a **\_ \_ impressão digital do tipo WINBIO** é suportada.</span><span class="sxs-lookup"><span data-stu-id="35ccc-125">Only **WINBIO\_TYPE\_FINGERPRINT** is currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="35ccc-126">**SensorSubType**</span><span class="sxs-lookup"><span data-stu-id="35ccc-126">**SensorSubType**</span></span>
</dt> <dd>

<span data-ttu-id="35ccc-127">Um subtipo de sensor definido para o tipo biométrico especificado pelo membro **BiometricFactor** .</span><span class="sxs-lookup"><span data-stu-id="35ccc-127">A sensor subtype defined for the biometric type specified by the **BiometricFactor** member.</span></span> <span data-ttu-id="35ccc-128">Atualmente, há suporte apenas para tipos de impressão digital (**\_ \_ impressão digital do tipo WINBIO**).</span><span class="sxs-lookup"><span data-stu-id="35ccc-128">Only fingerprint types (**WINBIO\_TYPE\_FINGERPRINT**) are currently supported.</span></span> <span data-ttu-id="35ccc-129">Os seguintes subtipos estão atualmente definidos para impressões digitais:</span><span class="sxs-lookup"><span data-stu-id="35ccc-129">The following subtypes are currently defined for fingerprints:</span></span>

-   <span data-ttu-id="35ccc-130">subtipo de \_ sensor WINBIO \_ \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="35ccc-130">WINBIO\_SENSOR\_SUBTYPE\_UNKNOWN</span></span>
-   <span data-ttu-id="35ccc-131">\_deslize o \_ \_ subtipo do \_ sensor de WINBIO FP</span><span class="sxs-lookup"><span data-stu-id="35ccc-131">WINBIO\_FP\_SENSOR\_SUBTYPE\_SWIPE</span></span>
-   <span data-ttu-id="35ccc-132">\_toque de \_ \_ subtipo de \_ sensor de WINBIO FP</span><span class="sxs-lookup"><span data-stu-id="35ccc-132">WINBIO\_FP\_SENSOR\_SUBTYPE\_TOUCH</span></span>

</dd> <dt>

<span data-ttu-id="35ccc-133">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="35ccc-133">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="35ccc-134">Um bitmask dos recursos do sensor biométrico.</span><span class="sxs-lookup"><span data-stu-id="35ccc-134">A bitmask of the biometric sensor capabilities.</span></span> <span data-ttu-id="35ccc-135">Isso pode ser um valor de bits **ou** um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="35ccc-135">This can be a bitwise **OR** of the following values:</span></span>

-   <span data-ttu-id="35ccc-136">\_sensor de capacidade de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="35ccc-136">WINBIO\_CAPABILITY\_SENSOR</span></span>
-   <span data-ttu-id="35ccc-137">\_correspondência de capacidade de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="35ccc-137">WINBIO\_CAPABILITY\_MATCHING</span></span>
-   <span data-ttu-id="35ccc-138">banco de dados de \_ funcionalidades WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="35ccc-138">WINBIO\_CAPABILITY\_DATABASE</span></span>
-   <span data-ttu-id="35ccc-139">\_processamento de recursos WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="35ccc-139">WINBIO\_CAPABILITY\_PROCESSING</span></span>
-   <span data-ttu-id="35ccc-140">\_criptografia de recurso WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="35ccc-140">WINBIO\_CAPABILITY\_ENCRYPTION</span></span>
-   <span data-ttu-id="35ccc-141">\_navegação de capacidade do WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="35ccc-141">WINBIO\_CAPABILITY\_NAVIGATION</span></span>
-   <span data-ttu-id="35ccc-142">\_indicador de funcionalidade de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="35ccc-142">WINBIO\_CAPABILITY\_INDICATOR</span></span>
-   <span data-ttu-id="35ccc-143">\_ \_ sensor virtual de funcionalidade de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="35ccc-143">WINBIO\_CAPABILITY\_VIRTUAL\_SENSOR</span></span>
    > [!Note]  
    > <span data-ttu-id="35ccc-144">A constante do **\_ \_ \_ sensor virtual de funcionalidade do WINBIO** se aplica somente ao Windows 10 e posterior.</span><span class="sxs-lookup"><span data-stu-id="35ccc-144">The **WINBIO\_CAPABILITY\_VIRTUAL\_SENSOR** constant applies only for Windows 10 and later.</span></span>

     

</dd> <dt>

<span data-ttu-id="35ccc-145">**DeviceInstanceId**</span><span class="sxs-lookup"><span data-stu-id="35ccc-145">**DeviceInstanceId**</span></span>
</dt> <dd>

<span data-ttu-id="35ccc-146">Um valor de cadeia de caracteres que contém a ID do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="35ccc-146">A string value that contains the device ID.</span></span> <span data-ttu-id="35ccc-147">A cadeia de caracteres pode conter até 256 caracteres Unicode, incluindo um caractere **nulo** de terminação.</span><span class="sxs-lookup"><span data-stu-id="35ccc-147">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="35ccc-148">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="35ccc-148">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="35ccc-149">Um valor de cadeia de caracteres que contém uma descrição da unidade biométrica.</span><span class="sxs-lookup"><span data-stu-id="35ccc-149">A string value that contains a description of the biometric unit.</span></span> <span data-ttu-id="35ccc-150">A cadeia de caracteres pode conter até 256 caracteres Unicode, incluindo um caractere **nulo** de terminação.</span><span class="sxs-lookup"><span data-stu-id="35ccc-150">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="35ccc-151">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="35ccc-151">**Manufacturer**</span></span>
</dt> <dd>

<span data-ttu-id="35ccc-152">Um valor de cadeia de caracteres que contém o nome do fabricante.</span><span class="sxs-lookup"><span data-stu-id="35ccc-152">A string value that contains the name of the manufacturer.</span></span> <span data-ttu-id="35ccc-153">A cadeia de caracteres pode conter até 256 caracteres Unicode, incluindo um caractere **nulo** de terminação.</span><span class="sxs-lookup"><span data-stu-id="35ccc-153">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="35ccc-154">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="35ccc-154">**Model**</span></span>
</dt> <dd>

<span data-ttu-id="35ccc-155">Um valor de cadeia de caracteres que contém o número do modelo da unidade biométrica.</span><span class="sxs-lookup"><span data-stu-id="35ccc-155">A string value that contains the model number of the biometric unit.</span></span> <span data-ttu-id="35ccc-156">A cadeia de caracteres pode conter até 256 caracteres Unicode, incluindo um caractere **nulo** de terminação.</span><span class="sxs-lookup"><span data-stu-id="35ccc-156">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="35ccc-157">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="35ccc-157">**SerialNumber**</span></span>
</dt> <dd>

<span data-ttu-id="35ccc-158">Uma cadeia de caracteres Unicode terminada em **nulo** que contém o número de série da unidade biométrica.</span><span class="sxs-lookup"><span data-stu-id="35ccc-158">A **NULL**-terminated Unicode string that contains the serial number of the biometric unit.</span></span> <span data-ttu-id="35ccc-159">A cadeia de caracteres pode conter até 256 caracteres Unicode, incluindo um caractere **nulo** de terminação.</span><span class="sxs-lookup"><span data-stu-id="35ccc-159">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="35ccc-160">**FirmwareVersion**</span><span class="sxs-lookup"><span data-stu-id="35ccc-160">**FirmwareVersion**</span></span>
</dt> <dd>

<span data-ttu-id="35ccc-161">Uma estrutura de [**\_ versão do WINBIO**](winbio-version.md) que contém os números de versão principal e secundária para a unidade biométrica.</span><span class="sxs-lookup"><span data-stu-id="35ccc-161">A [**WINBIO\_VERSION**](winbio-version.md) structure that contains the major and minor version numbers for the biometric unit.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35ccc-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35ccc-162">Requirements</span></span>



| <span data-ttu-id="35ccc-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="35ccc-163">Requirement</span></span> | <span data-ttu-id="35ccc-164">Valor</span><span class="sxs-lookup"><span data-stu-id="35ccc-164">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35ccc-165">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35ccc-165">Minimum supported client</span></span><br/> | <span data-ttu-id="35ccc-166">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="35ccc-166">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="35ccc-167">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35ccc-167">Minimum supported server</span></span><br/> | <span data-ttu-id="35ccc-168">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="35ccc-168">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="35ccc-169">parâmetro</span><span class="sxs-lookup"><span data-stu-id="35ccc-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="35ccc-170"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35ccc-170"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35ccc-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="35ccc-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ccc-172">Estruturas de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="35ccc-172">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="35ccc-173">**WinBioEnumBiometricUnits**</span><span class="sxs-lookup"><span data-stu-id="35ccc-173">**WinBioEnumBiometricUnits**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits)
</dt> </dl>

 

 





