---
title: Estrutura de WINBIO_BIR_HEADER (WinBio \_ Types. h)
description: Contém o cabeçalho de um BIR (registro de informações biométricas).
ms.assetid: 4b020720-42ef-4ac7-aaa3-7a0e45198890
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_BIR_HEADER
topic_type:
- apiref
api_name:
- WINBIO_BIR_HEADER
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1479c0db3ee826d79cf95a311215c8cf76f1c96b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085562"
---
# <a name="winbio_bir_header-structure"></a><span data-ttu-id="d02d8-104">\_Estrutura de \_ cabeçalho WINBIO Bir</span><span class="sxs-lookup"><span data-stu-id="d02d8-104">WINBIO\_BIR\_HEADER structure</span></span>

<span data-ttu-id="d02d8-105">A estrutura de **\_ \_ cabeçalho WINBIO Bir** contém o cabeçalho de um Bir (registro de informações biométricas).</span><span class="sxs-lookup"><span data-stu-id="d02d8-105">The **WINBIO\_BIR\_HEADER** structure contains the header of a biometric information record (BIR).</span></span>

## <a name="syntax"></a><span data-ttu-id="d02d8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d02d8-106">Syntax</span></span>


```C++
typedef struct _WINBIO_BIR_HEADER {
  USHORT                   ValidFields;
  WINBIO_BIR_VERSION       HeaderVersion;
  WINBIO_BIR_VERSION       PatronHeaderVersion;
  WINBIO_BIR_DATA_FLAGS    DataFlags;
  WINBIO_BIOMETRIC_TYPE    Type;
  WINBIO_BIOMETRIC_SUBTYPE Subtype;
  WINBIO_BIR_PURPOSE       Purpose;
  WINBIO_BIR_QUALITY       DataQuality;
  LARGE_INTEGER            CreationDate;
  struct {
    LARGE_INTEGER BeginDate;
    LARGE_INTEGER EndDate;
  } ValidityPeriod;
  WINBIO_REGISTERED_FORMAT BiometricDataFormat;
  WINBIO_REGISTERED_FORMAT ProductId;
} WINBIO_BIR_HEADER;
```



## <a name="members"></a><span data-ttu-id="d02d8-107">Membros</span><span class="sxs-lookup"><span data-stu-id="d02d8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d02d8-108">**ValidFields**</span><span class="sxs-lookup"><span data-stu-id="d02d8-108">**ValidFields**</span></span>
</dt> <dd>

<span data-ttu-id="d02d8-109">Bitmask que especifica quais campos nessa estrutura são válidos.</span><span class="sxs-lookup"><span data-stu-id="d02d8-109">Bitmask that specifies which fields in this structure are valid.</span></span> <span data-ttu-id="d02d8-110">Para obter mais informações, consulte [**WINBIO \_ Bir \_ Field Constants**](winbio-bir-field-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d02d8-110">For more information, see [**WINBIO\_BIR\_FIELD Constants**](winbio-bir-field-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="d02d8-111">**HeaderVersion**</span><span class="sxs-lookup"><span data-stu-id="d02d8-111">**HeaderVersion**</span></span>
</dt> <dd>

<span data-ttu-id="d02d8-112">Uma constante de **\_ \_ versão WINBIO Bir** que especifica a versão do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="d02d8-112">A **WINBIO\_BIR\_VERSION** constant that specifies the header version.</span></span> <span data-ttu-id="d02d8-113">Os números de versão são valores de 8 bits em que os quatro bits superiores especificam o número principal e os quatro bits baixos especificam o número de versão secundária.</span><span class="sxs-lookup"><span data-stu-id="d02d8-113">Version numbers are 8-bit values where the upper four bits specify the major number and the low four bits specify the minor version number.</span></span> <span data-ttu-id="d02d8-114">Atualmente, ele deve ser \_ WINBIO \_ \_ (versão de cabeçalho CBEFF).</span><span class="sxs-lookup"><span data-stu-id="d02d8-114">Currently this must be WINBIO\_CBEFF\_HEADER\_VERSION (0x11).</span></span>

</dd> <dt>

<span data-ttu-id="d02d8-115">**PatronHeaderVersion**</span><span class="sxs-lookup"><span data-stu-id="d02d8-115">**PatronHeaderVersion**</span></span>
</dt> <dd>

<span data-ttu-id="d02d8-116">Uma constante de **\_ \_ versão WINBIO Bir** que especifica a versão do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="d02d8-116">A **WINBIO\_BIR\_VERSION** constant that specifies the header version.</span></span> <span data-ttu-id="d02d8-117">Os números de versão são valores de 8 bits em que os quatro bits superiores especificam o número principal e os quatro bits baixos especificam o número de versão secundária.</span><span class="sxs-lookup"><span data-stu-id="d02d8-117">Version numbers are 8-bit values where the upper four bits specify the major number and the low four bits specify the minor version number.</span></span> <span data-ttu-id="d02d8-118">Atualmente, ele deve ser \_ WINBIO \_ \_ (versão de cabeçalho Patron).</span><span class="sxs-lookup"><span data-stu-id="d02d8-118">Currently this must be WINBIO\_PATRON\_HEADER\_VERSION (0x11).</span></span>

</dd> <dt>

<span data-ttu-id="d02d8-119">**Sinalizadores de**</span><span class="sxs-lookup"><span data-stu-id="d02d8-119">**DataFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d02d8-120">Um valor que especifica o formato dos dados de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="d02d8-120">A value that specifies the format of the header data.</span></span> <span data-ttu-id="d02d8-121">Isso pode ser uma **ou uma ou** mais das seguintes sinalizações de nível de segurança e de processamento.</span><span class="sxs-lookup"><span data-stu-id="d02d8-121">This can be a bitwise **OR** of the following security and processing level flags.</span></span> <span data-ttu-id="d02d8-122">Para obter mais informações, [**consulte \_ constantes \_ de \_ sinalizadores de dados do WINBIO Bir**](winbio-bir-data-flags-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d02d8-122">For more information, see [**WINBIO\_BIR\_DATA\_FLAGS Constants**](winbio-bir-data-flags-constants.md).</span></span>



| <span data-ttu-id="d02d8-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d02d8-123">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="d02d8-124">Significado</span><span class="sxs-lookup"><span data-stu-id="d02d8-124">Meaning</span></span>                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <span data-ttu-id="d02d8-125"><dt>**WINBIO \_ \_ \_ Privacidade do sinalizador de dados**</dt> <dt>((UCHAR) 0x02)</dt></span><span class="sxs-lookup"><span data-stu-id="d02d8-125"><dt>**WINBIO\_DATA\_FLAG\_PRIVACY**</dt> <dt>((UCHAR)0x02)</dt></span></span> </dl>                                       | <span data-ttu-id="d02d8-126">Os dados estão criptografados.</span><span class="sxs-lookup"><span data-stu-id="d02d8-126">The data is encrypted.</span></span><br/>                                                                                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <span data-ttu-id="d02d8-127"><dt>**WINBIO \_ \_ \_ Integridade do sinalizador de dados**</dt> <dt>((UCHAR) 0x01)</dt></span><span class="sxs-lookup"><span data-stu-id="d02d8-127"><dt>**WINBIO\_DATA\_FLAG\_INTEGRITY**</dt> <dt>((UCHAR)0x01)</dt></span></span> </dl>                                 | <span data-ttu-id="d02d8-128">Os dados são assinados digitalmente ou protegidos por um MAC (código de autenticação de mensagem).</span><span class="sxs-lookup"><span data-stu-id="d02d8-128">The data is digitally signed or protected by a message authentication code (MAC).</span></span><br/>                                                                                                                        |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <span data-ttu-id="d02d8-129"><dt>**WINBIO \_ Sinalizador de dados \_ \_ assinado**</dt> <dt>((UCHAR) 0x04)</dt></span><span class="sxs-lookup"><span data-stu-id="d02d8-129"><dt>**WINBIO\_DATA\_FLAG\_SIGNED**</dt> <dt>((UCHAR)0x04)</dt></span></span> </dl>                                          | <span data-ttu-id="d02d8-130">Se esse sinalizador e o sinalizador de **\_ integridade do \_ sinalizador \_ de dados WINBIO** estiverem definidos, os dados serão assinados.</span><span class="sxs-lookup"><span data-stu-id="d02d8-130">If this flag and the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag are set, the data is signed.</span></span> <span data-ttu-id="d02d8-131">Se esse sinalizador não for definido, mas o sinalizador de **\_ integridade do \_ sinalizador \_ de dados WINBIO** for definido, um Mac será calculado sobre os dados.</span><span class="sxs-lookup"><span data-stu-id="d02d8-131">If this flag is not set but the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag is set, a MAC is computed over the data.</span></span><br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <span data-ttu-id="d02d8-132"><dt>**WINBIO \_ Sinalizador de dados \_ \_ RAW**</dt> <dt>((UCHAR) 0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="d02d8-132"><dt>**WINBIO\_DATA\_FLAG\_RAW**</dt> <dt>((UCHAR)0x20)</dt></span></span> </dl>                                                   | <span data-ttu-id="d02d8-133">Os dados estão no formato com o qual foram capturados.</span><span class="sxs-lookup"><span data-stu-id="d02d8-133">The data is in the format with which it was captured.</span></span><br/>                                                                                                                                                    |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <span data-ttu-id="d02d8-134"><dt>**WINBIO \_ Sinalizador de dados \_ \_ intermediário**</dt> <dt>((UCHAR) 0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="d02d8-134"><dt>**WINBIO\_DATA\_FLAG\_INTERMEDIATE**</dt> <dt>((UCHAR)0x40)</dt></span></span> </dl>                        | <span data-ttu-id="d02d8-135">Os dados não são brutos, mas não foram completamente processados.</span><span class="sxs-lookup"><span data-stu-id="d02d8-135">The data is not raw but has not been completely processed.</span></span><br/>                                                                                                                                               |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <span data-ttu-id="d02d8-136"><dt>**WINBIO \_ Sinalizador de dados \_ \_ processado**</dt> <dt>((UCHAR) 0x80)</dt></span><span class="sxs-lookup"><span data-stu-id="d02d8-136"><dt>**WINBIO\_DATA\_FLAG\_PROCESSED**</dt> <dt>((UCHAR)0x80)</dt></span></span> </dl>                                 | <span data-ttu-id="d02d8-137">Os dados foram processados.</span><span class="sxs-lookup"><span data-stu-id="d02d8-137">The data has been processed.</span></span><br/>                                                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <span data-ttu-id="d02d8-138"><dt>**WINBIO \_ Máscara de opção de sinalizador de dados \_ \_ \_ \_ presente**</dt> <dt>((UCHAR) 0x08)</dt></span><span class="sxs-lookup"><span data-stu-id="d02d8-138"><dt>**WINBIO\_DATA\_FLAG\_OPTION\_MASK\_PRESENT**</dt> <dt>((UCHAR)0x08)</dt></span></span> </dl> | <span data-ttu-id="d02d8-139">Esse valor é sempre 1.</span><span class="sxs-lookup"><span data-stu-id="d02d8-139">This value is always 1.</span></span><br/>                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="d02d8-140">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d02d8-140">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="d02d8-141">Um \_ \_ valor de tipo biométrico WINBIO que especifica o tipo de dados biométricos referenciados no registro de informações biométricas.</span><span class="sxs-lookup"><span data-stu-id="d02d8-141">A WINBIO\_BIOMETRIC\_TYPE value that specifies the type of biometric data referenced in the biometric information record.</span></span> <span data-ttu-id="d02d8-142">Atualmente, somente a **\_ \_ impressão digital do tipo WINBIO** tem suporte.</span><span class="sxs-lookup"><span data-stu-id="d02d8-142">Currently only **WINBIO\_TYPE\_FINGERPRINT** is supported.</span></span> <span data-ttu-id="d02d8-143">Para obter mais informações, [**consulte \_ constantes do \_ tipo biométrico WINBIO**](winbio-biometric-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d02d8-143">For more information, see [**WINBIO\_BIOMETRIC\_TYPE Constants**](winbio-biometric-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="d02d8-144">**Subtipo**</span><span class="sxs-lookup"><span data-stu-id="d02d8-144">**Subtype**</span></span>
</dt> <dd>

<span data-ttu-id="d02d8-145">Um valor de **\_ \_ subtipo biométrico WINBIO** que especifica o subfator associado aos dados biométricos.</span><span class="sxs-lookup"><span data-stu-id="d02d8-145">A **WINBIO\_BIOMETRIC\_SUBTYPE** value that specifies the sub-factor associated with the biometric data.</span></span> <span data-ttu-id="d02d8-146">Para obter mais informações, consulte [**constantes de \_ \_ subtipo de comentários e WINBIO biométricas**](winbio-biometric-subtype-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d02d8-146">For more information, see Remarks and [**WINBIO\_BIOMETRIC\_SUBTYPE Constants**](winbio-biometric-subtype-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="d02d8-147">**Finalidade**</span><span class="sxs-lookup"><span data-stu-id="d02d8-147">**Purpose**</span></span>
</dt> <dd>

<span data-ttu-id="d02d8-148">Uma máscara de **\_ \_ finalidade WINBIO Bir** que especifica o uso pretendido dos dados.</span><span class="sxs-lookup"><span data-stu-id="d02d8-148">A **WINBIO\_BIR\_PURPOSE** mask that specifies the intended use of the data.</span></span> <span data-ttu-id="d02d8-149">Isso pode ser um valor de bits **ou** um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d02d8-149">This can be a bitwise **OR** of the following values.</span></span> <span data-ttu-id="d02d8-150">Para obter mais informações, [**consulte \_ constantes de \_ finalidade do WINBIO Bir**](winbio-bir-purpose-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d02d8-150">For more information, see [**WINBIO\_BIR\_PURPOSE Constants**](winbio-bir-purpose-constants.md).</span></span>

-   <span data-ttu-id="d02d8-151">\_verificação de finalidade do WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="d02d8-151">WINBIO\_PURPOSE\_VERIFY</span></span>
-   <span data-ttu-id="d02d8-152">\_identificação de finalidade do WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="d02d8-152">WINBIO\_PURPOSE\_IDENTIFY</span></span>
-   <span data-ttu-id="d02d8-153">\_registro de finalidade do WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="d02d8-153">WINBIO\_PURPOSE\_ENROLL</span></span>
-   <span data-ttu-id="d02d8-154">\_ \_ registro de finalidade \_ do WINBIO para \_ verificação</span><span class="sxs-lookup"><span data-stu-id="d02d8-154">WINBIO\_PURPOSE\_ENROLL\_FOR\_VERIFICATION</span></span>
-   <span data-ttu-id="d02d8-155">\_ \_ registro de finalidade \_ do WINBIO para \_ identificação</span><span class="sxs-lookup"><span data-stu-id="d02d8-155">WINBIO\_PURPOSE\_ENROLL\_FOR\_IDENTIFICATION</span></span>
-   <span data-ttu-id="d02d8-156">\_auditoria de finalidade do WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="d02d8-156">WINBIO\_PURPOSE\_AUDIT</span></span>

</dd> <dt>

<span data-ttu-id="d02d8-157">**Alta qualidade**</span><span class="sxs-lookup"><span data-stu-id="d02d8-157">**DataQuality**</span></span>
</dt> <dd>

<span data-ttu-id="d02d8-158">Um valor que especifica a qualidade relativa dos dados biométricos no registro de informações biométricas (BIR).</span><span class="sxs-lookup"><span data-stu-id="d02d8-158">A value that specifies the relative quality of the biometric data in the biometric information record (BIR).</span></span> <span data-ttu-id="d02d8-159">Isso pode ser um número inteiro de 0 a 100 ou um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d02d8-159">This can be an integer from 0 to 100 or one of the following values.</span></span> <span data-ttu-id="d02d8-160">Para obter mais informações, consulte [**WINBIO \_ Bir \_ Quality Constants**](winbio-bir-quality-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d02d8-160">For more information, see [**WINBIO\_BIR\_QUALITY Constants**](winbio-bir-quality-constants.md).</span></span>



| <span data-ttu-id="d02d8-161">Valor</span><span class="sxs-lookup"><span data-stu-id="d02d8-161">Value</span></span>                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="d02d8-162">Significado</span><span class="sxs-lookup"><span data-stu-id="d02d8-162">Meaning</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <span data-ttu-id="d02d8-163"><dt>**WINBIO \_ Qualidade de dados \_ \_ não \_ definida**</dt> <dt>((WINBIO \_ Bir \_ Quality)-1)</dt></span><span class="sxs-lookup"><span data-stu-id="d02d8-163"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SET**</dt> <dt>((WINBIO\_BIR\_QUALITY)-1)</dt></span></span> </dl>                   | <span data-ttu-id="d02d8-164">As medições de qualidade têm suporte pelo criador BIR, mas nenhum valor é definido no BIR.</span><span class="sxs-lookup"><span data-stu-id="d02d8-164">Quality measurements are supported by the BIR creator but no value is set in the BIR.</span></span><br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <span data-ttu-id="d02d8-165"><dt>**WINBIO \_ Qualidade de dados \_ \_ sem \_ suporte**</dt> <dt>((WINBIO \_ Bir \_ Quality)-2)</dt></span><span class="sxs-lookup"><span data-stu-id="d02d8-165"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SUPPORTED**</dt> <dt>((WINBIO\_BIR\_QUALITY)-2)</dt></span></span> </dl> | <span data-ttu-id="d02d8-166">As medições de qualidade não são suportadas pelo criador do BIR.</span><span class="sxs-lookup"><span data-stu-id="d02d8-166">Quality measurements are not supported by the BIR creator.</span></span><br/>                            |



 

</dd> <dt>

<span data-ttu-id="d02d8-167">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="d02d8-167">**CreationDate**</span></span>
</dt> <dd>

<span data-ttu-id="d02d8-168">A data e a hora, em tempo universal coordenado (hora de Greenwich), que o BIR foi criado.</span><span class="sxs-lookup"><span data-stu-id="d02d8-168">The date and time, in Coordinated Universal Time (Greenwich Mean Time), that the BIR was created.</span></span>

</dd> <dt>

<span data-ttu-id="d02d8-169">**ValidityPeriod**</span><span class="sxs-lookup"><span data-stu-id="d02d8-169">**ValidityPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="d02d8-170">O período para o qual o BIR é válido.</span><span class="sxs-lookup"><span data-stu-id="d02d8-170">The period for which the BIR is valid.</span></span>

<dl> <dt>

<span data-ttu-id="d02d8-171">**BeginDate**</span><span class="sxs-lookup"><span data-stu-id="d02d8-171">**BeginDate**</span></span>
</dt> <dd>

<span data-ttu-id="d02d8-172">A data e a hora, no tempo universal coordenado, que o período de validade inicia.</span><span class="sxs-lookup"><span data-stu-id="d02d8-172">The date and time, in Coordinated Universal Time, that the validity period starts.</span></span>

</dd> <dt>

<span data-ttu-id="d02d8-173">**Término**</span><span class="sxs-lookup"><span data-stu-id="d02d8-173">**EndDate**</span></span>
</dt> <dd>

<span data-ttu-id="d02d8-174">A data e a hora, no tempo universal coordenado, em que o BIR deixa de ser válido.</span><span class="sxs-lookup"><span data-stu-id="d02d8-174">The date and time, in Coordinated Universal Time, at which the BIR ceases to be valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d02d8-175">**BiometricDataFormat**</span><span class="sxs-lookup"><span data-stu-id="d02d8-175">**BiometricDataFormat**</span></span>
</dt> <dd>

<span data-ttu-id="d02d8-176">Uma estrutura de [**\_ \_ formato registrada WINBIO**](winbio-registered-format.md) que especifica o formato de dados do bloco de dados Standard na estrutura [**\_ Bir WINBIO**](winbio-bir.md) .</span><span class="sxs-lookup"><span data-stu-id="d02d8-176">A [**WINBIO\_REGISTERED\_FORMAT**](winbio-registered-format.md) structure that specifies the data format of the standard data block in the [**WINBIO\_BIR**](winbio-bir.md) structure.</span></span> <span data-ttu-id="d02d8-177">Os membros do **\_ \_ formato registrado WINBIO** não podem ser zero.</span><span class="sxs-lookup"><span data-stu-id="d02d8-177">The **WINBIO\_REGISTERED\_FORMAT** members cannot be zero.</span></span> <span data-ttu-id="d02d8-178">Você pode usar as constantes a seguir para simplificar a verificação de erros.</span><span class="sxs-lookup"><span data-stu-id="d02d8-178">You can use the following constants to simplify error checking.</span></span>



| <span data-ttu-id="d02d8-179">Valor</span><span class="sxs-lookup"><span data-stu-id="d02d8-179">Value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="d02d8-180">Significado</span><span class="sxs-lookup"><span data-stu-id="d02d8-180">Meaning</span></span>                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_FORMAT_OWNER_AVAILABLE"></span><span id="winbio_no_format_owner_available"></span><dl> <span data-ttu-id="d02d8-181"><dt>**WINBIO \_ NENHUM \_ proprietário de formato \_ \_ disponível**</dt> <dt>((UShort) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="d02d8-181"><dt>**WINBIO\_NO\_FORMAT\_OWNER\_AVAILABLE**</dt> <dt>((USHORT)0)</dt></span></span> </dl> | <span data-ttu-id="d02d8-182">Nenhum valor de proprietário atribuído de IBIA (Associação Internacional de setores biométricos) foi especificado.</span><span class="sxs-lookup"><span data-stu-id="d02d8-182">No IBIA (International Biometric Industry Association) assigned owner value has been specified.</span></span><br/> |
| <span id="WINBIO_NO_FORMAT_TYPE_AVAILABLE"></span><span id="winbio_no_format_type_available"></span><dl> <span data-ttu-id="d02d8-183"><dt>**WINBIO \_ NENHUM \_ tipo de formato \_ \_ disponível**</dt> <dt>((UShort) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="d02d8-183"><dt>**WINBIO\_NO\_FORMAT\_TYPE\_AVAILABLE**</dt> <dt>((USHORT)0)</dt></span></span> </dl>    | <span data-ttu-id="d02d8-184">Nenhum tipo de formato foi especificado.</span><span class="sxs-lookup"><span data-stu-id="d02d8-184">No format type has been specified.</span></span><br/>                                                              |



 

</dd> <dt>

<span data-ttu-id="d02d8-185">**ProductId**</span><span class="sxs-lookup"><span data-stu-id="d02d8-185">**ProductId**</span></span>
</dt> <dd>

<span data-ttu-id="d02d8-186">Uma estrutura de [**\_ \_ formato registrada WINBIO**](winbio-registered-format.md) que especifica a ID do produto do componente que gerou o bloco de dados Standard no Bir.</span><span class="sxs-lookup"><span data-stu-id="d02d8-186">A [**WINBIO\_REGISTERED\_FORMAT**](winbio-registered-format.md) structure that specifies the product ID of the component that generated the standard data block in the BIR.</span></span> <span data-ttu-id="d02d8-187">Os membros do **\_ \_ formato registrado WINBIO** podem ser zero.</span><span class="sxs-lookup"><span data-stu-id="d02d8-187">The **WINBIO\_REGISTERED\_FORMAT** members can be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d02d8-188">Comentários</span><span class="sxs-lookup"><span data-stu-id="d02d8-188">Remarks</span></span>

<span data-ttu-id="d02d8-189">O parâmetro *subtipo* especifica o subfator associado aos dados biométricos.</span><span class="sxs-lookup"><span data-stu-id="d02d8-189">The *Subtype* parameter specifies the sub-factor associated with the biometric data.</span></span> <span data-ttu-id="d02d8-190">Atualmente, o Windows Biometric Framework (WBF) dá suporte apenas à captura de impressão digital e usa as seguintes constantes para representar informações de subtipo:</span><span class="sxs-lookup"><span data-stu-id="d02d8-190">Currently, the Windows Biometric Framework (WBF) supports only fingerprint capture and uses the following constants to represent sub-type information:</span></span>

-   <span data-ttu-id="d02d8-191">WINBIO \_ ANSI \_ 381 \_ pos \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="d02d8-191">WINBIO\_ANSI\_381\_POS\_UNKNOWN</span></span>
-   <span data-ttu-id="d02d8-192">WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ Thumb</span><span class="sxs-lookup"><span data-stu-id="d02d8-192">WINBIO\_ANSI\_381\_POS\_RH\_THUMB</span></span>
-   <span data-ttu-id="d02d8-193">Dedo do índice de RH do WINBIO \_ ANSI \_ 381 \_ pos \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="d02d8-193">WINBIO\_ANSI\_381\_POS\_RH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="d02d8-194">WINBIO \_ ANSI \_ 381 \_ pos \_ \_ meio-dedo central de RH \_</span><span class="sxs-lookup"><span data-stu-id="d02d8-194">WINBIO\_ANSI\_381\_POS\_RH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="d02d8-195">WINBIO \_ ANSI \_ 381 \_ pos \_ - \_ anel de RH \_</span><span class="sxs-lookup"><span data-stu-id="d02d8-195">WINBIO\_ANSI\_381\_POS\_RH\_RING\_FINGER</span></span>
-   <span data-ttu-id="d02d8-196">WINBIO \_ ANSI \_ 381 \_ pos \_ \_ Little \_ Finger</span><span class="sxs-lookup"><span data-stu-id="d02d8-196">WINBIO\_ANSI\_381\_POS\_RH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="d02d8-197">WINBIO \_ ANSI \_ 381 \_ pos de \_ LH \_ Thumb</span><span class="sxs-lookup"><span data-stu-id="d02d8-197">WINBIO\_ANSI\_381\_POS\_LH\_THUMB</span></span>
-   <span data-ttu-id="d02d8-198">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ index \_ Finger</span><span class="sxs-lookup"><span data-stu-id="d02d8-198">WINBIO\_ANSI\_381\_POS\_LH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="d02d8-199">WINBIO \_ ANSI \_ 381 \_ pos \_ do \_ meio- \_ dedo médio</span><span class="sxs-lookup"><span data-stu-id="d02d8-199">WINBIO\_ANSI\_381\_POS\_LH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="d02d8-200">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ Ring \_ Finger</span><span class="sxs-lookup"><span data-stu-id="d02d8-200">WINBIO\_ANSI\_381\_POS\_LH\_RING\_FINGER</span></span>
-   <span data-ttu-id="d02d8-201">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ Little \_ Finger</span><span class="sxs-lookup"><span data-stu-id="d02d8-201">WINBIO\_ANSI\_381\_POS\_LH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="d02d8-202">WINBIO \_ ANSI \_ 381 \_ pos \_ com \_ quatro \_ dedos</span><span class="sxs-lookup"><span data-stu-id="d02d8-202">WINBIO\_ANSI\_381\_POS\_RH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="d02d8-203">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ quatro \_ dedos</span><span class="sxs-lookup"><span data-stu-id="d02d8-203">WINBIO\_ANSI\_381\_POS\_LH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="d02d8-204">WINBIO \_ ANSI \_ 381 \_ pos \_ dois \_ polegares</span><span class="sxs-lookup"><span data-stu-id="d02d8-204">WINBIO\_ANSI\_381\_POS\_TWO\_THUMBS</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="d02d8-205">Não tente validar o valor fornecido para o valor do parâmetro de *subtipo* .</span><span class="sxs-lookup"><span data-stu-id="d02d8-205">Do not attempt to validate the value supplied for the *Subtype* parameter value.</span></span> <span data-ttu-id="d02d8-206">O serviço de biometria do Windows validará o valor fornecido antes de passá-lo para sua implementação.</span><span class="sxs-lookup"><span data-stu-id="d02d8-206">The Windows Biometrics Service will validate the supplied value before passing it through to your implementation.</span></span> <span data-ttu-id="d02d8-207">Se o valor for **WINBIO \_ subtipo \_ nenhuma \_ informação** ou **\_ subtipo WINBIO \_**, em seguida, valide quando apropriado.</span><span class="sxs-lookup"><span data-stu-id="d02d8-207">If the value is **WINBIO\_SUBTYPE\_NO\_INFORMATION** or **WINBIO\_SUBTYPE\_ANY**, then validate where appropriate.</span></span>

 

<span data-ttu-id="d02d8-208">Se qualquer um dos seguintes bits for declarado, a estrutura **de \_ \_ cabeçalho WINBIO Bir** não será corretamente formada.</span><span class="sxs-lookup"><span data-stu-id="d02d8-208">If any of the following bits are asserted, the **WINBIO\_BIR\_HEADER** structure is not correctly formed.</span></span>


```C++
#define WINBIO_BIR_FIELD_NEVER_VALID    (WINBIO_BIR_FIELD_SUBHEAD_COUNT |   \
                                         WINBIO_BIR_FIELD_PATRON_ID |       \
                                         WINBIO_BIR_FIELD_INDEX |           \
                                         WINBIO_BIR_FIELD_CHALLENGE |       \
                                         WINBIO_BIR_FIELD_PAYLOAD )
```



## <a name="requirements"></a><span data-ttu-id="d02d8-209">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d02d8-209">Requirements</span></span>



| <span data-ttu-id="d02d8-210">Requisito</span><span class="sxs-lookup"><span data-stu-id="d02d8-210">Requirement</span></span> | <span data-ttu-id="d02d8-211">Valor</span><span class="sxs-lookup"><span data-stu-id="d02d8-211">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d02d8-212">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d02d8-212">Minimum supported client</span></span><br/> | <span data-ttu-id="d02d8-213">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d02d8-213">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="d02d8-214">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d02d8-214">Minimum supported server</span></span><br/> | <span data-ttu-id="d02d8-215">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="d02d8-215">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d02d8-216">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d02d8-216">Header</span></span><br/>                   | <dl> <span data-ttu-id="d02d8-217"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d02d8-217"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d02d8-218">Confira também</span><span class="sxs-lookup"><span data-stu-id="d02d8-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d02d8-219">Estruturas de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="d02d8-219">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="d02d8-220">**\_Constantes de SUBtipo de biometria WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="d02d8-220">**WINBIO\_BIOMETRIC\_SUBTYPE Constants**</span></span>](winbio-biometric-subtype-constants.md)
</dt> <dt>

[<span data-ttu-id="d02d8-221">**WINBIO \_ Bir**</span><span class="sxs-lookup"><span data-stu-id="d02d8-221">**WINBIO\_BIR**</span></span>](winbio-bir.md)
</dt> <dt>

[<span data-ttu-id="d02d8-222">**\_Constantes de \_ sinalizadores de dados WINBIO Bir \_**</span><span class="sxs-lookup"><span data-stu-id="d02d8-222">**WINBIO\_BIR\_DATA\_FLAGS Constants**</span></span>](winbio-bir-data-flags-constants.md)
</dt> <dt>

[<span data-ttu-id="d02d8-223">**\_Constantes do \_ campo WINBIO Bir**</span><span class="sxs-lookup"><span data-stu-id="d02d8-223">**WINBIO\_BIR\_FIELD Constants**</span></span>](winbio-bir-field-constants.md)
</dt> <dt>

[<span data-ttu-id="d02d8-224">**Constantes de finalidade de \_ Bir WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="d02d8-224">**WINBIO\_BIR\_PURPOSE Constants**</span></span>](winbio-bir-purpose-constants.md)
</dt> <dt>

[<span data-ttu-id="d02d8-225">**WINBIO \_ \_ constantes de qualidade Bir**</span><span class="sxs-lookup"><span data-stu-id="d02d8-225">**WINBIO\_BIR\_QUALITY Constants**</span></span>](winbio-bir-quality-constants.md)
</dt> <dt>

[<span data-ttu-id="d02d8-226">**\_Constantes da \_ versão WINBIO Bir**</span><span class="sxs-lookup"><span data-stu-id="d02d8-226">**WINBIO\_BIR\_VERSION Constants**</span></span>](winbio-bir-version-constants.md)
</dt> </dl>

 

 





