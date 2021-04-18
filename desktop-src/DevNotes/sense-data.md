---
description: Usado para relatar informações de status ou erro em resposta a um comando de detecção de solicitação SCSI.
ms.assetid: 43B2FE98-1468-4457-AB7D-3038C16E20B6
title: Estrutura de SENSE_DATA (SCSI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SENSE_DATA
api_type:
- HeaderDef
api_location:
- Scsi.h
ms.openlocfilehash: b5eacf9bee8c2cebf93b27c97a88c691852a3841
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105748684"
---
# <a name="sense_data-structure"></a><span data-ttu-id="af7cb-103">Estrutura de dados de detecção \_</span><span class="sxs-lookup"><span data-stu-id="af7cb-103">SENSE\_DATA structure</span></span>

<span data-ttu-id="af7cb-104">Usado para relatar informações de status ou erro em resposta a um comando de **detecção de solicitação** SCSI.</span><span class="sxs-lookup"><span data-stu-id="af7cb-104">Used to report status or error information in response to a SCSI **Request Sense** command.</span></span>

## <a name="syntax"></a><span data-ttu-id="af7cb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af7cb-105">Syntax</span></span>


```C++
typedef struct _SENSE_DATA {
  UCHAR  ErrorCode  :7;
  UCHAR  Valid  :1;
  UCHAR  SegmentNumber;
  UCHAR  SenseKey  :4;
  UCHAR  Reserved  :1;
  UCHAR  IncorrectLength  :1;
  UCHAR  EndOfMedia  :1;
  UCHAR  FileMark  :1;
  UCHAR  Information[4];
  UCHAR  AdditionalSenseLength;
  UCHAR  CommandSpecificInformation[4];
  UCHAR  AdditionalSenseCode;
  UCHAR  AdditionalSenseCodeQualifier;
  UCHAR  FieldReplaceableUnitCode;
  UCHAR  SenseKeySpecific[3];
} SENSE_DATA, *PSENSE_DATA;
```



## <a name="members"></a><span data-ttu-id="af7cb-106">Membros</span><span class="sxs-lookup"><span data-stu-id="af7cb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="af7cb-107">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="af7cb-107">**ErrorCode**</span></span>
</dt> <dd>

<span data-ttu-id="af7cb-108">O tipo de relatório.</span><span class="sxs-lookup"><span data-stu-id="af7cb-108">The report type.</span></span>



| <span data-ttu-id="af7cb-109">Valor</span><span class="sxs-lookup"><span data-stu-id="af7cb-109">Value</span></span>                                                                           | <span data-ttu-id="af7cb-110">Significado</span><span class="sxs-lookup"><span data-stu-id="af7cb-110">Meaning</span></span>                     |
|---------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="af7cb-111"><dt>0x70</dt></span><span class="sxs-lookup"><span data-stu-id="af7cb-111"><dt>0x70</dt></span></span> </dl> | <span data-ttu-id="af7cb-112">Erros atuais.</span><span class="sxs-lookup"><span data-stu-id="af7cb-112">Current errors.</span></span><br/>  |
| <dl> <span data-ttu-id="af7cb-113"><dt>0x71</dt></span><span class="sxs-lookup"><span data-stu-id="af7cb-113"><dt>0x71</dt></span></span> </dl> | <span data-ttu-id="af7cb-114">Erros adiados.</span><span class="sxs-lookup"><span data-stu-id="af7cb-114">Deferred errors.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="af7cb-115">**Válido**</span><span class="sxs-lookup"><span data-stu-id="af7cb-115">**Valid**</span></span>
</dt> <dd>

<span data-ttu-id="af7cb-116">1 se o campo de **informações** for definido em um padrão; caso contrário, o campo de **informações** será específico do fornecedor e não será definido por um padrão.</span><span class="sxs-lookup"><span data-stu-id="af7cb-116">1 if the **Information** field is defined in a standard; otherwise the **Information** field is vendor-specific and not defined by a standard.</span></span>

</dd> <dt>

<span data-ttu-id="af7cb-117">**SegmentNumber**</span><span class="sxs-lookup"><span data-stu-id="af7cb-117">**SegmentNumber**</span></span>
</dt> <dd>

<span data-ttu-id="af7cb-118">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="af7cb-118">Obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="af7cb-119">**SenseKey**</span><span class="sxs-lookup"><span data-stu-id="af7cb-119">**SenseKey**</span></span>
</dt> <dd>

<span data-ttu-id="af7cb-120">Indica a categoria de erro.</span><span class="sxs-lookup"><span data-stu-id="af7cb-120">Indicates the category of error.</span></span>

<dl> <dt>

<span data-ttu-id="af7cb-121"><span id="No_Sense"></span><span id="no_sense"></span><span id="NO_SENSE"></span>**Sem sentido** (0x0)</span><span class="sxs-lookup"><span data-stu-id="af7cb-121"><span id="No_Sense"></span><span id="no_sense"></span><span id="NO_SENSE"></span>**No Sense** (0x0)</span></span>
</dt> <dt>

<span data-ttu-id="af7cb-122"><span id="Recovered_Error"></span><span id="recovered_error"></span><span id="RECOVERED_ERROR"></span>**Erro recuperado** (0x1)</span><span class="sxs-lookup"><span data-stu-id="af7cb-122"><span id="Recovered_Error"></span><span id="recovered_error"></span><span id="RECOVERED_ERROR"></span>**Recovered Error** (0x1)</span></span>
</dt> <dt>

<span data-ttu-id="af7cb-123"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não está pronto** (0x2)</span><span class="sxs-lookup"><span data-stu-id="af7cb-123"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (0x2)</span></span>
</dt> <dt>

<span data-ttu-id="af7cb-124"><span id="Medium_Error"></span><span id="medium_error"></span><span id="MEDIUM_ERROR"></span>**Erro médio** (0x3)</span><span class="sxs-lookup"><span data-stu-id="af7cb-124"><span id="Medium_Error"></span><span id="medium_error"></span><span id="MEDIUM_ERROR"></span>**Medium Error** (0x3)</span></span>
</dt> <dt>

<span data-ttu-id="af7cb-125"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Erro de hardware** (0x4)</span><span class="sxs-lookup"><span data-stu-id="af7cb-125"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Hardware Error** (0x4)</span></span>
</dt> <dt>

<span data-ttu-id="af7cb-126"><span id="Illegal_Request"></span><span id="illegal_request"></span><span id="ILLEGAL_REQUEST"></span>**Solicitação inválida** (0x5)</span><span class="sxs-lookup"><span data-stu-id="af7cb-126"><span id="Illegal_Request"></span><span id="illegal_request"></span><span id="ILLEGAL_REQUEST"></span>**Illegal Request** (0x5)</span></span>
</dt> <dt>

<span data-ttu-id="af7cb-127"><span id="Unit_Attention"></span><span id="unit_attention"></span><span id="UNIT_ATTENTION"></span>**Atenção de unidade** (0x6)</span><span class="sxs-lookup"><span data-stu-id="af7cb-127"><span id="Unit_Attention"></span><span id="unit_attention"></span><span id="UNIT_ATTENTION"></span>**Unit Attention** (0x6)</span></span>
</dt> <dt>

<span data-ttu-id="af7cb-128"><span id="Data_Protect"></span><span id="data_protect"></span><span id="DATA_PROTECT"></span>**Proteção de dados** (0x7)</span><span class="sxs-lookup"><span data-stu-id="af7cb-128"><span id="Data_Protect"></span><span id="data_protect"></span><span id="DATA_PROTECT"></span>**Data Protect** (0x7)</span></span>
</dt> <dt>

<span data-ttu-id="af7cb-129"><span id="Firmware_Error"></span><span id="firmware_error"></span><span id="FIRMWARE_ERROR"></span>**Erro de firmware** (0x9)</span><span class="sxs-lookup"><span data-stu-id="af7cb-129"><span id="Firmware_Error"></span><span id="firmware_error"></span><span id="FIRMWARE_ERROR"></span>**Firmware Error** (0x9)</span></span>
</dt> <dt>

<span data-ttu-id="af7cb-130"><span id="Aborted_Command"></span><span id="aborted_command"></span><span id="ABORTED_COMMAND"></span>**Comando anulado** (0xB)</span><span class="sxs-lookup"><span data-stu-id="af7cb-130"><span id="Aborted_Command"></span><span id="aborted_command"></span><span id="ABORTED_COMMAND"></span>**Aborted Command** (0xB)</span></span>
</dt> <dt>

<span data-ttu-id="af7cb-131"><span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>**Igual** (0xc)</span><span class="sxs-lookup"><span data-stu-id="af7cb-131"><span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>**Equal** (0xC)</span></span>
</dt> <dt>

<span data-ttu-id="af7cb-132"><span id="Volume_Overflow"></span><span id="volume_overflow"></span><span id="VOLUME_OVERFLOW"></span>**Estouro de volume** (0xD)</span><span class="sxs-lookup"><span data-stu-id="af7cb-132"><span id="Volume_Overflow"></span><span id="volume_overflow"></span><span id="VOLUME_OVERFLOW"></span>**Volume Overflow** (0xD)</span></span>
</dt> <dt>

<span data-ttu-id="af7cb-133"><span id="Miscompare"></span><span id="miscompare"></span><span id="MISCOMPARE"></span>0xE ( **recompare** )</span><span class="sxs-lookup"><span data-stu-id="af7cb-133"><span id="Miscompare"></span><span id="miscompare"></span><span id="MISCOMPARE"></span>**Miscompare** (0xE)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="af7cb-134">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="af7cb-134">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="af7cb-135">Reservado.</span><span class="sxs-lookup"><span data-stu-id="af7cb-135">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="af7cb-136">**IncorrectLength**</span><span class="sxs-lookup"><span data-stu-id="af7cb-136">**IncorrectLength**</span></span>
</dt> <dd>

<span data-ttu-id="af7cb-137">1 se o comprimento de bloco lógico solicitado não corresponder ao comprimento de bloco lógico dos dados na mídia.</span><span class="sxs-lookup"><span data-stu-id="af7cb-137">1 if the requested logical block length does not match the logical block length of the data on the media.</span></span>

</dd> <dt>

<span data-ttu-id="af7cb-138">**EndOfMedia**</span><span class="sxs-lookup"><span data-stu-id="af7cb-138">**EndOfMedia**</span></span>
</dt> <dd>

<span data-ttu-id="af7cb-139">1 se um dispositivo de acesso sequencial tiver atingido o fim da mídia ou se uma impressora estiver sem papel.</span><span class="sxs-lookup"><span data-stu-id="af7cb-139">1 if a sequential-access device has reached end-of-media, or a printer is out of paper.</span></span>

</dd> <dt>

<span data-ttu-id="af7cb-140">**Marca**</span><span class="sxs-lookup"><span data-stu-id="af7cb-140">**FileMark**</span></span>
</dt> <dd>

<span data-ttu-id="af7cb-141">1 se o comando atual tiver atingido uma marca de caixa de um ou um setmark.</span><span class="sxs-lookup"><span data-stu-id="af7cb-141">1 if the current command has reached a filemark or setmark.</span></span> <span data-ttu-id="af7cb-142">Válido somente para dispositivos de acesso sequencial.</span><span class="sxs-lookup"><span data-stu-id="af7cb-142">Only valid for sequential-access devices.</span></span>

</dd> <dt>

<span data-ttu-id="af7cb-143">**Informações**</span><span class="sxs-lookup"><span data-stu-id="af7cb-143">**Information**</span></span>
</dt> <dd>

<span data-ttu-id="af7cb-144">Dados específicos do tipo de dispositivo ou comando.</span><span class="sxs-lookup"><span data-stu-id="af7cb-144">Device-type or command specific data.</span></span>

</dd> <dt>

<span data-ttu-id="af7cb-145">**AdditionalSenseLength**</span><span class="sxs-lookup"><span data-stu-id="af7cb-145">**AdditionalSenseLength**</span></span>
</dt> <dd>

<span data-ttu-id="af7cb-146">O comprimento em bytes do restante da estrutura.</span><span class="sxs-lookup"><span data-stu-id="af7cb-146">The length in bytes of the remainder of the structure.</span></span> <span data-ttu-id="af7cb-147">O comprimento total menos 7.</span><span class="sxs-lookup"><span data-stu-id="af7cb-147">The total length minus 7.</span></span>

</dd> <dt>

<span data-ttu-id="af7cb-148">**CommandSpecificInformation**</span><span class="sxs-lookup"><span data-stu-id="af7cb-148">**CommandSpecificInformation**</span></span>
</dt> <dd>

<span data-ttu-id="af7cb-149">Dados específicos do comando.</span><span class="sxs-lookup"><span data-stu-id="af7cb-149">Command-specific data.</span></span> <span data-ttu-id="af7cb-150">Os valores são definidos no padrão de comando apropriado.</span><span class="sxs-lookup"><span data-stu-id="af7cb-150">Values are defined in the appropriate command standard.</span></span>

</dd> <dt>

<span data-ttu-id="af7cb-151">**AdditionalSenseCode**</span><span class="sxs-lookup"><span data-stu-id="af7cb-151">**AdditionalSenseCode**</span></span>
</dt> <dd>

<span data-ttu-id="af7cb-152">Código específico do dispositivo que descreve o erro relatado no campo **SenseKey** .</span><span class="sxs-lookup"><span data-stu-id="af7cb-152">Device specific code that describes the error reported in the **SenseKey** field.</span></span>

</dd> <dt>

<span data-ttu-id="af7cb-153">**AdditionalSenseCodeQualifier**</span><span class="sxs-lookup"><span data-stu-id="af7cb-153">**AdditionalSenseCodeQualifier**</span></span>
</dt> <dd>

<span data-ttu-id="af7cb-154">Pode conter detalhes adicionais sobre o campo **AdditionalSenseCode** .</span><span class="sxs-lookup"><span data-stu-id="af7cb-154">Can contain additional detail about the **AdditionalSenseCode** field.</span></span>

</dd> <dt>

<span data-ttu-id="af7cb-155">**FieldReplaceableUnitCode**</span><span class="sxs-lookup"><span data-stu-id="af7cb-155">**FieldReplaceableUnitCode**</span></span>
</dt> <dd>

<span data-ttu-id="af7cb-156">Informações específicas do fornecedor sobre o componente associado a esses dados de detecção.</span><span class="sxs-lookup"><span data-stu-id="af7cb-156">Vender-specific information about the component associated with this sense data.</span></span>

</dd> <dt>

<span data-ttu-id="af7cb-157">**SenseKeySpecific**</span><span class="sxs-lookup"><span data-stu-id="af7cb-157">**SenseKeySpecific**</span></span>
</dt> <dd>

<span data-ttu-id="af7cb-158">O conteúdo e o formato das informações específicas da chave de detecção são determinados pelo valor do campo **SenseKey** .</span><span class="sxs-lookup"><span data-stu-id="af7cb-158">The content and format of the sense key specific information is determined by the value of the **SenseKey** field.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af7cb-159">Comentários</span><span class="sxs-lookup"><span data-stu-id="af7cb-159">Remarks</span></span>

<span data-ttu-id="af7cb-160">Para obter mais informações sobre o formato de dados de detecção, consulte [comando de detecção de solicitação SCSI](https://wikipedia.org/wiki/SCSI_command) ( https://wikipedia.org/wiki/SCSI_command) .</span><span class="sxs-lookup"><span data-stu-id="af7cb-160">For more information about the sense data format, see [SCSI Request Sense Command](https://wikipedia.org/wiki/SCSI_command) (https://wikipedia.org/wiki/SCSI_command).</span></span>

## <a name="requirements"></a><span data-ttu-id="af7cb-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af7cb-161">Requirements</span></span>



| <span data-ttu-id="af7cb-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="af7cb-162">Requirement</span></span> | <span data-ttu-id="af7cb-163">Valor</span><span class="sxs-lookup"><span data-stu-id="af7cb-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="af7cb-164">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af7cb-164">Minimum supported client</span></span><br/> | <span data-ttu-id="af7cb-165">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="af7cb-165">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="af7cb-166">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af7cb-166">Minimum supported server</span></span><br/> | <span data-ttu-id="af7cb-167">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="af7cb-167">Windows Server 2003 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="af7cb-168">parâmetro</span><span class="sxs-lookup"><span data-stu-id="af7cb-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="af7cb-169"><dt>SCSI. h</dt></span><span class="sxs-lookup"><span data-stu-id="af7cb-169"><dt>Scsi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af7cb-170">Confira também</span><span class="sxs-lookup"><span data-stu-id="af7cb-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af7cb-171">Passagem de destino iSCSI</span><span class="sxs-lookup"><span data-stu-id="af7cb-171">iSCSI Target Pass-Through</span></span>](/powershell/module/iscsi)
</dt> <dt>

[<span data-ttu-id="af7cb-172">\_passagem de \_ SCSI \_ via Direct</span><span class="sxs-lookup"><span data-stu-id="af7cb-172">SCSI\_PASS\_THROUGH\_DIRECT</span></span>](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_pass_through_direct)
</dt> </dl>

 

 




