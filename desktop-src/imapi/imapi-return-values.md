---
title: Valores de retorno de IMAPi (Imapi2error. h)
description: Os métodos IMAPi retornam valores não negativos, (normalmente S \_ OK) se o método foi bem-sucedido. Os métodos IMAPi retornam códigos de êxito ou de erro do Winerror. h, Imapi2error. h ou Imapi2fserror. h, em caso de falha.
ms.assetid: 0e62ed6c-4810-4d36-a759-9b02b68face6
topic_type:
- apiref
api_name:
- E_IMAPI_BURN_VERIFICATION_FAILED
- E_IMAPI_REQUEST_CANCELLED
- E_IMAPI_RECORDER_REQUIRED
- S_IMAPI_WRITE_NOT_IN_PROGRESS
- S_IMAPI_SPEEDADJUSTED
- S_IMAPI_ROTATIONADJUSTED
- S_IMAPI_BOTHADJUSTED
- S_IMAPI_COMMAND_HAS_SENSE_DATA
- E_IMAPI_RAW_IMAGE_IS_READ_ONLY
- E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS
- E_IMAPI_RAW_IMAGE_NO_TRACKS
- E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED
- E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED
- E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE
- E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES
- E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND
- S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS
- E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED
- E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX
- E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE
- E_IMAPI_RECORDER_MEDIA_NO_MEDIA
- E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE
- E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN
- E_IMAPI_RECORDER_MEDIA_BECOMING_READY
- E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS
- E_IMAPI_RECORDER_MEDIA_BUSY
- E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS
- E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED
- E_IMAPI_RECORDER_NO_SUCH_FEATURE
- E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT
- E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED
- E_IMAPI_RECORDER_COMMAND_TIMEOUT
- E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT
- E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH
- E_IMAPI_RECORDER_LOCKED
- E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID
- E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE
- E_IMAPI_LOSS_OF_STREAMING
- E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE
- E_IMAPI_DF2DATA_WRITE_IN_PROGRESS
- E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS
- E_IMAPI_DF2DATA_INVALID_MEDIA_STATE
- E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED
- E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA
- E_IMAPI_DF2DATA_MEDIA_NOT_BLANK
- E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED
- E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED
- E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID
- E_IMAPI_DF2TAO_WRITE_IN_PROGRESS
- E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS
- E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED
- E_IMAPI_DF2TAO_MEDIA_IS_PREPARED
- E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY
- E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC
- E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK
- E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED
- E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED
- E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE
- E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED
- E_IMAPI_DF2TAO_INVALID_ISRC
- E_IMAPI_DF2TAO_INVALID_MCN
- E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED
- E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED
- E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID
- E_IMAPI_DF2RAW_WRITE_IN_PROGRESS
- E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS
- E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED
- E_IMAPI_DF2RAW_MEDIA_IS_PREPARED
- E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID
- E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK
- E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED
- E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE
- E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED
- E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED
- E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED
- E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT
- E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED
- E_IMAPI_ERASE_RECORDER_IN_USE
- E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED
- E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL
- E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL
- E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE
- E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND
- E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR
- E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE
- E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND
- E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED
- E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED
- E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID
- IMAPI_E_FSI_INTERNAL_ERROR
- IMAPI_E_INVALID_PARAM
- IMAPI_E_READONLY
- IMAPI_E_NO_OUTPUT
- IMAPI_E_INVALID_VOLUME_NAME
- IMAPI_E_INVALID_DATE
- IMAPI_E_FILE_SYSTEM_NOT_EMPTY
- IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED
- IMAPI_E_NOT_FILE
- IMAPI_E_NOT_DIR
- IMAPI_E_DIR_NOT_EMPTY
- IMAPI_E_NOT_IN_FILE_SYSTEM
- IMAPI_E_INVALID_PATH
- IMAPI_E_RESTRICTED_NAME_VIOLATION
- IMAPI_E_DUP_NAME
- IMAPI_E_NO_UNIQUE_NAME
- IMAPI_E_ITEM_NOT_FOUND
- IMAPI_E_FILE_NOT_FOUND
- IMAPI_E_DIR_NOT_FOUND
- IMAPI_E_IMAGE_SIZE_LIMIT
- IMAPI_E_IMAGE_TOO_BIG
- IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED
- IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND
- IMAPI_E_IMAGEMANAGER_NO_IMAGE
- IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG
- IMAPI_E_DATA_STREAM_INCONSISTENCY
- IMAPI_E_DATA_STREAM_READ_FAILURE
- IMAPI_E_DATA_STREAM_CREATE_FAILURE
- IMAPI_E_DIRECTORY_READ_FAILURE
- IMAPI_E_TOO_MANY_DIRS
- IMAPI_E_ISO9660_LEVELS
- IMAPI_E_DATA_TOO_BIG
- IMAPI_E_STASHFILE_OPEN_FAILURE
- IMAPI_E_STASHFILE_SEEK_FAILURE
- IMAPI_E_STASHFILE_WRITE_FAILURE
- IMAPI_E_STASHFILE_READ_FAILURE
- IMAPI_E_INVALID_WORKING_DIRECTORY
- IMAPI_E_WORKING_DIRECTORY_SPACE
- IMAPI_E_STASHFILE_MOVE
- IMAPI_E_BOOT_IMAGE_DATA
- IMAPI_E_BOOT_OBJECT_CONFLICT
- IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH
- IMAPI_E_EMPTY_DISC
- IMAPI_E_NO_SUPPORTED_FILE_SYSTEM
- IMAPI_E_FILE_SYSTEM_NOT_FOUND
- IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR
- IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED
- IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY
- IMAPI_E_IMPORT_SEEK_FAILURE
- IMAPI_E_IMPORT_READ_FAILURE
- IMAPI_E_DISC_MISMATCH
- IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED
- IMAPI_E_UDF_NOT_WRITE_COMPATIBLE
- IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE
- IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION
- IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE
- IMAPI_E_MULTISESSION_NOT_SET
- IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE
- IMAPI_E_BAD_MULTISESSION_PARAMETER
- IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED
api_location:
- Imapi2error.h
- Imapi2fserror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6bc4b99bb5ac123ea26ca1deb755fa29598811b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455294"
---
# <a name="imapi-return-values"></a><span data-ttu-id="e0759-104">Valores de retorno de IMAPi</span><span class="sxs-lookup"><span data-stu-id="e0759-104">IMAPI Return Values</span></span>

<span data-ttu-id="e0759-105">Os métodos IMAPi retornam valores não negativos, (normalmente S \_ OK) se o método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e0759-105">The IMAPI methods return non-negative values, (typically S\_OK) if the method was successful.</span></span> <span data-ttu-id="e0759-106">Os métodos IMAPi retornam códigos de êxito ou de erro do Winerror. h, Imapi2error. h ou Imapi2fserror. h, em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="e0759-106">The IMAPI methods return success or error codes from Winerror.h, Imapi2error.h, or Imapi2fserror.h, on failure.</span></span>

<span data-ttu-id="e0759-107">Os seguintes códigos de êxito e de erro são definidos.</span><span class="sxs-lookup"><span data-stu-id="e0759-107">The following success and error codes are defined.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="e0759-108">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="e0759-108">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="e0759-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0759-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_BURN_VERIFICATION_FAILED"></span><span id="e_imapi_burn_verification_failed"></span><dl> <span data-ttu-id="e0759-110"><dt><strong>E_IMAPI_BURN_VERIFICATION_FAILED</strong></dt> <dt>(HRESULT) 0xC0AA0007L</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-110"><dt><strong>E_IMAPI_BURN_VERIFICATION_FAILED</strong></dt> <dt>(HRESULT)0xC0AA0007L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-111">O disco não passou na verificação de gravação e pode conter dados corrompidos ou ser inutilizável.</span><span class="sxs-lookup"><span data-stu-id="e0759-111">The disc did not pass burn verification and may contain corrupt data or be unusable.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_REQUEST_CANCELLED"></span><span id="e_imapi_request_cancelled"></span><dl> <span data-ttu-id="e0759-112"><dt><strong>E_IMAPI_REQUEST_CANCELLED</strong></dt> <dt>(HRESULT) 0xC0AA0002</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-112"><dt><strong>E_IMAPI_REQUEST_CANCELLED</strong></dt> <dt>(HRESULT)0xC0AA0002</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-113">A solicitação foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="e0759-113">The request was canceled.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_REQUIRED"></span><span id="e_imapi_recorder_required"></span><dl> <span data-ttu-id="e0759-114"><dt><strong>E_IMAPI_RECORDER_REQUIRED</strong></dt> <dt>(HRESULT) 0xC0AA0003</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-114"><dt><strong>E_IMAPI_RECORDER_REQUIRED</strong></dt> <dt>(HRESULT)0xC0AA0003</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-115">A solicitação requer que um gravador de disco atual seja selecionado.</span><span class="sxs-lookup"><span data-stu-id="e0759-115">The request requires a current disc recorder to be selected.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="S_IMAPI_WRITE_NOT_IN_PROGRESS"></span><span id="s_imapi_write_not_in_progress"></span><dl> <span data-ttu-id="e0759-116"><dt><strong>S_IMAPI_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0x00AA0302L</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-116"><dt><strong>S_IMAPI_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT)0x00AA0302L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-117">Nenhuma operação de gravação está em andamento no momento.</span><span class="sxs-lookup"><span data-stu-id="e0759-117">No write operation is currently in progress.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="S_IMAPI_SPEEDADJUSTED"></span><span id="s_imapi_speedadjusted"></span><dl> <span data-ttu-id="e0759-118"><dt><strong>S_IMAPI_SPEEDADJUSTED</strong></dt> <dt>(HRESULT) 0x00AA0004</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-118"><dt><strong>S_IMAPI_SPEEDADJUSTED</strong></dt> <dt>(HRESULT)0x00AA0004</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-119">A unidade não dá suporte à velocidade de gravação solicitada e a velocidade foi ajustada.</span><span class="sxs-lookup"><span data-stu-id="e0759-119">The requested write speed was not supported by the drive and the speed was adjusted.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="S_IMAPI_ROTATIONADJUSTED"></span><span id="s_imapi_rotationadjusted"></span><dl> <span data-ttu-id="e0759-120"><dt><strong>S_IMAPI_ROTATIONADJUSTED</strong></dt> <dt>(HRESULT) 0x00AA0005</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-120"><dt><strong>S_IMAPI_ROTATIONADJUSTED</strong></dt> <dt>(HRESULT)0x00AA0005</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-121">O tipo de rotação solicitado não era suportado pela unidade e o tipo de rotação foi ajustado.</span><span class="sxs-lookup"><span data-stu-id="e0759-121">The requested rotation type was not supported by the drive and the rotation type was adjusted.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="S_IMAPI_BOTHADJUSTED"></span><span id="s_imapi_bothadjusted"></span><dl> <span data-ttu-id="e0759-122"><dt><strong>S_IMAPI_BOTHADJUSTED</strong></dt> <dt>(HRESULT) 0x00AA0006</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-122"><dt><strong>S_IMAPI_BOTHADJUSTED</strong></dt> <dt>(HRESULT)0x00AA0006</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-123">A unidade de velocidade de gravação solicitada e o tipo de rotação não eram compatíveis com ela e foram ajustadas.</span><span class="sxs-lookup"><span data-stu-id="e0759-123">The requested write speed and rotation type were not supported by the drive and they were both adjusted.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="S_IMAPI_COMMAND_HAS_SENSE_DATA"></span><span id="s_imapi_command_has_sense_data"></span><dl> <span data-ttu-id="e0759-124"><dt><strong>S_IMAPI_COMMAND_HAS_SENSE_DATA</strong></dt> <dt>(HRESULT) 0x00AA0200</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-124"><dt><strong>S_IMAPI_COMMAND_HAS_SENSE_DATA</strong></dt> <dt>(HRESULT)0x00AA0200</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-125">O dispositivo aceitou o comando, mas retornou dados de detecção, indicando um erro.</span><span class="sxs-lookup"><span data-stu-id="e0759-125">The device accepted the command, but returned sense data, indicating an error.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_IS_READ_ONLY"></span><span id="e_imapi_raw_image_is_read_only"></span><dl> <span data-ttu-id="e0759-126"><dt><strong>E_IMAPI_RAW_IMAGE_IS_READ_ONLY</strong></dt> <dt>(HRESULT) 0x80AA0A00L</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-126"><dt><strong>E_IMAPI_RAW_IMAGE_IS_READ_ONLY</strong></dt> <dt>(HRESULT)0x80AA0A00L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-127">A imagem tornou-se somente leitura devido a uma chamada para <a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-createresultimage"><strong>IRawCDImageCreator:: CreateResultImage</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e0759-127">The image has become read-only due to a call to <a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-createresultimage"><strong>IRawCDImageCreator::CreateResultImage</strong></a>.</span></span> <span data-ttu-id="e0759-128">Como resultado, o objeto não pode mais ser modificado.</span><span class="sxs-lookup"><span data-stu-id="e0759-128">As a result the object can no longer be modified.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS"></span><span id="e_imapi_raw_image_too_many_tracks"></span><dl> <span data-ttu-id="e0759-129"><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS</strong></dt> <dt>(HRESULT) 0x80AA0A01L</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-129"><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS</strong></dt> <dt>(HRESULT)0x80AA0A01L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-130">Não é possível adicionar mais faixas.</span><span class="sxs-lookup"><span data-stu-id="e0759-130">No more tracks may be added.</span></span> <span data-ttu-id="e0759-131">A mídia de CD está restrita a um intervalo de 1-99 faixas.</span><span class="sxs-lookup"><span data-stu-id="e0759-131">CD media is restricted to a range of 1-99 tracks.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_NO_TRACKS"></span><span id="e_imapi_raw_image_no_tracks"></span><dl> <span data-ttu-id="e0759-132"><dt><strong>E_IMAPI_RAW_IMAGE_NO_TRACKS</strong></dt> <dt>(HRESULT) 0x80AA0A03L</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-132"><dt><strong>E_IMAPI_RAW_IMAGE_NO_TRACKS</strong></dt> <dt>(HRESULT)0x80AA0A03L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-133">As faixas devem ser adicionadas à imagem antes de usar essa função.</span><span class="sxs-lookup"><span data-stu-id="e0759-133">Tracks must be added to the image before using this function.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED"></span><span id="e_imapi_raw_image_sector_type_not_supported"></span><dl> <span data-ttu-id="e0759-134"><dt><strong>E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0x80AA0A02L</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-134"><dt><strong>E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0x80AA0A02L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-135">Não há suporte para o tipo de setor solicitado.</span><span class="sxs-lookup"><span data-stu-id="e0759-135">The requested sector type is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED"></span><span id="e_imapi_raw_image_tracks_already_added"></span><dl> <span data-ttu-id="e0759-136"><dt><strong>E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED</strong></dt> <dt>(HRESULT) 0x80AA0A04L</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-136"><dt><strong>E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED</strong></dt> <dt>(HRESULT)0x80AA0A04L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-137">As faixas não podem ser adicionadas à imagem antes do uso dessa função.</span><span class="sxs-lookup"><span data-stu-id="e0759-137">Tracks may not be added to the image prior to the use of this function.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE"></span><span id="e_imapi_raw_image_insufficient_space"></span><dl> <span data-ttu-id="e0759-138"><dt><strong>E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE</strong></dt> <dt>(HRESULT) 0x80AA0A05L</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-138"><dt><strong>E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE</strong></dt> <dt>(HRESULT)0x80AA0A05L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-139">Adicionar essa faixa excederia as limitações do início do cliente potencial.</span><span class="sxs-lookup"><span data-stu-id="e0759-139">Adding this track would exceed the limitations of the start of the leadout.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES"></span><span id="e_imapi_raw_image_too_many_track_indexes"></span><dl> <span data-ttu-id="e0759-140"><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES</strong></dt> <dt>(HRESULT) 0x80AA0A06L</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-140"><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES</strong></dt> <dt>(HRESULT)0x80AA0A06L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-141">Adicionar essa faixa excederia o limite de índice de 99.</span><span class="sxs-lookup"><span data-stu-id="e0759-141">Adding this track would exceed the 99 index limit.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND"></span><span id="e_imapi_raw_image_track_index_not_found"></span><dl> <span data-ttu-id="e0759-142"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND</strong></dt> <dt>(HRESULT) 0x80AA0A07L</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-142"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND</strong></dt> <dt>(HRESULT)0x80AA0A07L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-143">O deslocamento de LBA especificado não está na lista de índices de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="e0759-143">The specified LBA offset is not in the list of track indexes.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS"></span><span id="s_imapi_raw_image_track_index_already_exists"></span><dl> <span data-ttu-id="e0759-144"><dt><strong>S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS</strong></dt> <dt>(HRESULT) 0x00AA0A08L</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-144"><dt><strong>S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS</strong></dt> <dt>(HRESULT)0x00AA0A08L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-145">O deslocamento de LBA especificado já está na lista de índices de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="e0759-145">The specified LBA offset is already in the list of track indexes.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED"></span><span id="e_imapi_raw_image_track_index_offset_zero_cannot_be_cleared"></span><dl> <span data-ttu-id="e0759-146"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED</strong></dt> <dt>(HRESULT) 0x80AA0A09L</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-146"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED</strong></dt> <dt>(HRESULT)0x80AA0A09L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-147">O índice 1 (deslocamento de LBA zero) não pode ser limpo.</span><span class="sxs-lookup"><span data-stu-id="e0759-147">Index 1 (LBA offset zero) cannot be cleared.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX"></span><span id="e_imapi_raw_image_track_index_too_close_to_other_index"></span><dl> <span data-ttu-id="e0759-148"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX</strong></dt> <dt>(HRESULT) 0x80AA0A0AL</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-148"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX</strong></dt> <dt>(HRESULT)0x80AA0A0AL</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-149">Cada índice deve ter um tamanho mínimo de dez setores.</span><span class="sxs-lookup"><span data-stu-id="e0759-149">Each index must have a minimum size of ten sectors.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE"></span><span id="e_imapi_recorder_no_such_mode_page"></span><dl> <span data-ttu-id="e0759-150"><dt><strong>E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE</strong></dt> <dt>(HRESULT) 0xC0AA0201</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-150"><dt><strong>E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE</strong></dt> <dt>(HRESULT)0xC0AA0201</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-151">O dispositivo relatou que a página de modo solicitada (e tipo) não está presente.</span><span class="sxs-lookup"><span data-stu-id="e0759-151">The device reported that the requested mode page (and type) is not present.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_NO_MEDIA"></span><span id="e_imapi_recorder_media_no_media"></span><dl> <span data-ttu-id="e0759-152"><dt><strong>E_IMAPI_RECORDER_MEDIA_NO_MEDIA</strong></dt> <dt>(HRESULT) 0xC0AA0202</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-152"><dt><strong>E_IMAPI_RECORDER_MEDIA_NO_MEDIA</strong></dt> <dt>(HRESULT)0xC0AA0202</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-153">Não há mídia no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e0759-153">There is no media in the device.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE"></span><span id="e_imapi_recorder_media_incompatible"></span><dl> <span data-ttu-id="e0759-154"><dt><strong>E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE</strong></dt> <dt>(HRESULT) 0xC0AA0203</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-154"><dt><strong>E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE</strong></dt> <dt>(HRESULT)0xC0AA0203</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-155">A mídia não é compatível ou tem formato físico desconhecido.</span><span class="sxs-lookup"><span data-stu-id="e0759-155">The media is not compatible or of unknown physical format.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN"></span><span id="e_imapi_recorder_media_upside_down"></span><dl> <span data-ttu-id="e0759-156"><dt><strong>E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN</strong></dt> <dt>(HRESULT) 0xC0AA0204</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-156"><dt><strong>E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN</strong></dt> <dt>(HRESULT)0xC0AA0204</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-157">A mídia é inserida de cabeça para baixo.</span><span class="sxs-lookup"><span data-stu-id="e0759-157">The media is inserted upside down.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_BECOMING_READY"></span><span id="e_imapi_recorder_media_becoming_ready"></span><dl> <span data-ttu-id="e0759-158"><dt><strong>E_IMAPI_RECORDER_MEDIA_BECOMING_READY</strong></dt> <dt>(HRESULT) 0xC0AA0205</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-158"><dt><strong>E_IMAPI_RECORDER_MEDIA_BECOMING_READY</strong></dt> <dt>(HRESULT)0xC0AA0205</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-159">A unidade relatou que está em processo de se tornar pronta.</span><span class="sxs-lookup"><span data-stu-id="e0759-159">The drive reported that it is in the process of becoming ready.</span></span> <span data-ttu-id="e0759-160">Tente a solicitação novamente mais tarde.</span><span class="sxs-lookup"><span data-stu-id="e0759-160">Please try the request again later.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS"></span><span id="e_imapi_recorder_media_format_in_progress"></span><dl> <span data-ttu-id="e0759-161"><dt><strong>E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xC0AA0206</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-161"><dt><strong>E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0206</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-162">A mídia está sendo formatada no momento.</span><span class="sxs-lookup"><span data-stu-id="e0759-162">The media is currently being formatted.</span></span> <span data-ttu-id="e0759-163">Aguarde até que o formato seja concluído antes de tentar usar a mídia.</span><span class="sxs-lookup"><span data-stu-id="e0759-163">Please wait for the format to complete before attempting to use the media.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_BUSY"></span><span id="e_imapi_recorder_media_busy"></span><dl> <span data-ttu-id="e0759-164"><dt><strong>E_IMAPI_RECORDER_MEDIA_BUSY</strong></dt> <dt>(HRESULT) 0xC0AA0207</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-164"><dt><strong>E_IMAPI_RECORDER_MEDIA_BUSY</strong></dt> <dt>(HRESULT)0xC0AA0207</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-165">A unidade relatou que está executando uma operação de longa execução, como concluir uma gravação.</span><span class="sxs-lookup"><span data-stu-id="e0759-165">The drive reported that it is performing a long-running operation, such as finishing a write.</span></span> <span data-ttu-id="e0759-166">A unidade pode ser inutilizável por um longo período de tempo.</span><span class="sxs-lookup"><span data-stu-id="e0759-166">The drive may be unusable for a long period of time.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS"></span><span id="e_imapi_recorder_invalid_mode_parameters"></span><dl> <span data-ttu-id="e0759-167"><dt><strong>E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS</strong></dt> <dt>(HRESULT) 0xC0AA0208</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-167"><dt><strong>E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS</strong></dt> <dt>(HRESULT)0xC0AA0208</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-168">A unidade relatou que a combinação de parâmetros fornecida na página modo para um comando de modo SELECT não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="e0759-168">The drive reported that the combination of parameters provided in the mode page for a MODE SELECT command were not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED"></span><span id="e_imapi_recorder_media_write_protected"></span><dl> <span data-ttu-id="e0759-169"><dt><strong>E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED</strong></dt> <dt>(HRESULT) 0xC0AA0209</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-169"><dt><strong>E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED</strong></dt> <dt>(HRESULT)0xC0AA0209</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-170">A unidade relatou que a mídia está protegida contra gravação.</span><span class="sxs-lookup"><span data-stu-id="e0759-170">The drive reported that the media is write protected.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_NO_SUCH_FEATURE"></span><span id="e_imapi_recorder_no_such_feature"></span><dl> <span data-ttu-id="e0759-171"><dt><strong>E_IMAPI_RECORDER_NO_SUCH_FEATURE</strong></dt> <dt>(HRESULT) 0xC0AA020A</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-171"><dt><strong>E_IMAPI_RECORDER_NO_SUCH_FEATURE</strong></dt> <dt>(HRESULT)0xC0AA020A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-172">O dispositivo não dá suporte à página de recursos solicitada.</span><span class="sxs-lookup"><span data-stu-id="e0759-172">The feature page requested is not supported by the device.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT"></span><span id="e_imapi_recorder_feature_is_not_current"></span><dl> <span data-ttu-id="e0759-173"><dt><strong>E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT</strong></dt> <dt>(HRESULT) 0xC0AA020B</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-173"><dt><strong>E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT</strong></dt> <dt>(HRESULT)0xC0AA020B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-174">A página de recursos solicitada tem suporte, mas não está marcada como atual.</span><span class="sxs-lookup"><span data-stu-id="e0759-174">The feature page requested is supported, but is not marked as current.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED"></span><span id="e_imapi_recorder_get_configuration_not_supported"></span><dl> <span data-ttu-id="e0759-175"><dt><strong>E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA020C</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-175"><dt><strong>E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA020C</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-176">A unidade não dá suporte ao comando obter configuração.</span><span class="sxs-lookup"><span data-stu-id="e0759-176">The drive does not support the GET CONFIGURATION command.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_COMMAND_TIMEOUT"></span><span id="e_imapi_recorder_command_timeout"></span><dl> <span data-ttu-id="e0759-177"><dt><strong>E_IMAPI_RECORDER_COMMAND_TIMEOUT</strong></dt> <dt>(HRESULT) 0xC0AA020D</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-177"><dt><strong>E_IMAPI_RECORDER_COMMAND_TIMEOUT</strong></dt> <dt>(HRESULT)0xC0AA020D</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-178">O dispositivo não pôde aceitar o comando no período de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="e0759-178">The device failed to accept the command within the timeout period.</span></span> <span data-ttu-id="e0759-179">Isso pode ser causado pelo dispositivo ter inserido um estado inconsistente ou o valor de tempo limite para o comando pode precisar ser aumentado.</span><span class="sxs-lookup"><span data-stu-id="e0759-179">This may be caused by the device having entered an inconsistent state, or the timeout value for the command may need to be increased.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT"></span><span id="e_imapi_recorder_dvd_structure_not_present"></span><dl> <span data-ttu-id="e0759-180"><dt><strong>E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT</strong></dt> <dt>(HRESULT) 0xC0AA020E</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-180"><dt><strong>E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT</strong></dt> <dt>(HRESULT)0xC0AA020E</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-181">A estrutura do DVD não está presente.</span><span class="sxs-lookup"><span data-stu-id="e0759-181">The DVD structure is not present.</span></span> <span data-ttu-id="e0759-182">Isso pode ser causado por unidade/mídia incompatível usada.</span><span class="sxs-lookup"><span data-stu-id="e0759-182">This may be caused by incompatible drive/medium used.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH"></span><span id="e_imapi_recorder_media_speed_mismatch"></span><dl> <span data-ttu-id="e0759-183"><dt><strong>E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH</strong></dt> <dt>(HRESULT) 0xC0AA020F</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-183"><dt><strong>E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH</strong></dt> <dt>(HRESULT)0xC0AA020F</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-184">A velocidade da mídia é incompatível com o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e0759-184">The media's speed is incompatible with the device.</span></span> <span data-ttu-id="e0759-185">Isso pode ser causado pelo uso de uma mídia de velocidade maior ou menor do que o intervalo de velocidades suportado pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e0759-185">This may be caused by using higher or lower speed media than the range of speeds supported by the device.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_LOCKED"></span><span id="e_imapi_recorder_locked"></span><dl> <span data-ttu-id="e0759-186"><dt><strong>E_IMAPI_RECORDER_LOCKED</strong></dt> <dt>(HRESULT) 0xC0AA0210</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-186"><dt><strong>E_IMAPI_RECORDER_LOCKED</strong></dt> <dt>(HRESULT)0xC0AA0210</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-187">O dispositivo associado a este gravador durante a última operação foi bloqueado exclusivamente, causando a falha dessa operação.</span><span class="sxs-lookup"><span data-stu-id="e0759-187">The device associated with this recorder during the last operation has been exclusively locked, causing this operation to fail.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_recorder_client_name_is_not_valid"></span><dl> <span data-ttu-id="e0759-188"><dt><strong>E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT) 0xC0AA0211</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-188"><dt><strong>E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT)0xC0AA0211</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-189">O nome do cliente não é válido.</span><span class="sxs-lookup"><span data-stu-id="e0759-189">The client name is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE"></span><span id="e_imapi_recorder_invalid_response_from_device"></span><dl> <span data-ttu-id="e0759-190"><dt><strong>E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE</strong></dt> <dt>(HRESULT) 0xC0AA02FF</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-190"><dt><strong>E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE</strong></dt> <dt>(HRESULT)0xC0AA02FF</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-191">O dispositivo relatou dados inesperados ou inválidos para um comando.</span><span class="sxs-lookup"><span data-stu-id="e0759-191">The device reported unexpected or invalid data for a command.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_LOSS_OF_STREAMING"></span><span id="e_imapi_loss_of_streaming"></span><dl> <span data-ttu-id="e0759-192"><dt><strong>E_IMAPI_LOSS_OF_STREAMING</strong></dt> <dt>(HRESULT) 0xC0AA0300</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-192"><dt><strong>E_IMAPI_LOSS_OF_STREAMING</strong></dt> <dt>(HRESULT)0xC0AA0300</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-193">A gravação falhou porque a unidade não recebeu dados rápido o suficiente para continuar a gravação.</span><span class="sxs-lookup"><span data-stu-id="e0759-193">The write failed because the drive did not receive data quickly enough to continue writing.</span></span> <span data-ttu-id="e0759-194">Mover os dados de origem para o computador local, reduzir a velocidade de gravação ou habilitar uma &quot; configuração gratuita do buffer &quot; pode resolver esse problema.</span><span class="sxs-lookup"><span data-stu-id="e0759-194">Moving the source data to the local computer, reducing the write speed, or enabling a &quot;buffer underrun free&quot; setting may resolve this issue.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE"></span><span id="e_imapi_unexpected_response_from_device"></span><dl> <span data-ttu-id="e0759-195"><dt><strong>E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE</strong></dt> <dt>(HRESULT) 0xC0AA0301</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-195"><dt><strong>E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE</strong></dt> <dt>(HRESULT)0xC0AA0301</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-196">A gravação falhou porque a unidade retornou informações de erro que não puderam ser recuperadas do.</span><span class="sxs-lookup"><span data-stu-id="e0759-196">The write failed because the drive returned error information that could not be recovered from.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2data_write_in_progress"></span><dl> <span data-ttu-id="e0759-197"><dt><strong>E_IMAPI_DF2DATA_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xC0AA0400</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-197"><dt><strong>E_IMAPI_DF2DATA_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0400</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-198">Atualmente, há uma operação de gravação em andamento.</span><span class="sxs-lookup"><span data-stu-id="e0759-198">There is currently a write operation in progress.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2data_write_not_in_progress"></span><dl> <span data-ttu-id="e0759-199"><dt><strong>E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xC0AA0401</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-199"><dt><strong>E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0401</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-200">Não há nenhuma operação de gravação em andamento no momento.</span><span class="sxs-lookup"><span data-stu-id="e0759-200">There is no write operation currently in progress.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_INVALID_MEDIA_STATE"></span><span id="e_imapi_df2data_invalid_media_state"></span><dl> <span data-ttu-id="e0759-201"><dt><strong>E_IMAPI_DF2DATA_INVALID_MEDIA_STATE</strong></dt> <dt>(HRESULT) 0xC0AA0402</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-201"><dt><strong>E_IMAPI_DF2DATA_INVALID_MEDIA_STATE</strong></dt> <dt>(HRESULT)0xC0AA0402</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-202">A operação solicitada só é válida com mídia com suporte.</span><span class="sxs-lookup"><span data-stu-id="e0759-202">The requested operation is only valid with supported media.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2data_stream_not_supported"></span><dl> <span data-ttu-id="e0759-203"><dt><strong>E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA0403</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-203"><dt><strong>E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0403</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-204">Não há suporte para o fluxo fornecido para gravação.</span><span class="sxs-lookup"><span data-stu-id="e0759-204">The provided stream to write is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA"></span><span id="e_imapi_df2data_stream_too_large_for_current_media"></span><dl> <span data-ttu-id="e0759-205"><dt><strong>E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA</strong></dt> <dt>(HRESULT) 0xC0AA0404</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-205"><dt><strong>E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA</strong></dt> <dt>(HRESULT)0xC0AA0404</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-206">O fluxo fornecido para gravação é muito grande para a mídia inserida no momento.</span><span class="sxs-lookup"><span data-stu-id="e0759-206">The provided stream to write is too large for the currently inserted media.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_MEDIA_NOT_BLANK"></span><span id="e_imapi_df2data_media_not_blank"></span><dl> <span data-ttu-id="e0759-207"><dt><strong>E_IMAPI_DF2DATA_MEDIA_NOT_BLANK</strong></dt> <dt>(HRESULT) 0xC0AA0405</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-207"><dt><strong>E_IMAPI_DF2DATA_MEDIA_NOT_BLANK</strong></dt> <dt>(HRESULT)0xC0AA0405</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-208">A substituição de mídias não em branco não é permitida sem a propriedade ForceOverwrite definida como VARIANT_TRUE.</span><span class="sxs-lookup"><span data-stu-id="e0759-208">Overwriting non-blank media is not allowed without the ForceOverwrite property set to VARIANT_TRUE.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2data_media_is_not_supported"></span><dl> <span data-ttu-id="e0759-209"><dt><strong>E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA0406</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-209"><dt><strong>E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0406</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-210">Não há suporte para o tipo de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="e0759-210">The current media type is unsupported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2data_recorder_not_supported"></span><dl> <span data-ttu-id="e0759-211"><dt><strong>E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA0407</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-211"><dt><strong>E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0407</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-212">Este dispositivo não oferece suporte às operações exigidas por este formato de disco.</span><span class="sxs-lookup"><span data-stu-id="e0759-212">This device does not support the operations required by this disc format.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2data_client_name_is_not_valid"></span><dl> <span data-ttu-id="e0759-213"><dt><strong>E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT) 0xC0AA0408</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-213"><dt><strong>E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT)0xC0AA0408</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-214">O nome do cliente não é válido.</span><span class="sxs-lookup"><span data-stu-id="e0759-214">The client name is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2tao_write_in_progress"></span><dl> <span data-ttu-id="e0759-215"><dt><strong>E_IMAPI_DF2TAO_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xC0AA0500</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-215"><dt><strong>E_IMAPI_DF2TAO_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0500</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-216">Atualmente, há uma operação de gravação em andamento.</span><span class="sxs-lookup"><span data-stu-id="e0759-216">There is currently a write operation in progress.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2tao_write_not_in_progress"></span><dl> <span data-ttu-id="e0759-217"><dt><strong>E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xC0AA0501</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-217"><dt><strong>E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0501</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-218">Não há nenhuma operação de gravação em andamento no momento.</span><span class="sxs-lookup"><span data-stu-id="e0759-218">There is no write operation currently in progress.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED"></span><span id="e_imapi_df2tao_media_is_not_prepared"></span><dl> <span data-ttu-id="e0759-219"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED</strong></dt> <dt>(HRESULT) 0xC0AA0502</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-219"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED</strong></dt> <dt>(HRESULT)0xC0AA0502</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-220">A operação solicitada só é válida quando a mídia foi &quot; preparada &quot; .</span><span class="sxs-lookup"><span data-stu-id="e0759-220">The requested operation is only valid when media has been &quot;prepared&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_MEDIA_IS_PREPARED"></span><span id="e_imapi_df2tao_media_is_prepared"></span><dl> <span data-ttu-id="e0759-221"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_PREPARED</strong></dt> <dt>(HRESULT) 0xC0AA0503</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-221"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_PREPARED</strong></dt> <dt>(HRESULT)0xC0AA0503</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-222">A operação solicitada não é válida quando a mídia foi &quot; preparada &quot; , mas não foi liberada.</span><span class="sxs-lookup"><span data-stu-id="e0759-222">The requested operation is not valid when media has been &quot;prepared&quot; but not released.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY"></span><span id="e_imapi_df2tao_property_for_blank_media_only"></span><dl> <span data-ttu-id="e0759-223"><dt><strong>E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY</strong></dt> <dt>(HRESULT) 0xC0AA0504</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-223"><dt><strong>E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY</strong></dt> <dt>(HRESULT)0xC0AA0504</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-224">A propriedade não pode ser alterada depois que a mídia tiver sido gravada.</span><span class="sxs-lookup"><span data-stu-id="e0759-224">The property cannot be changed once the media has been written to.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC"></span><span id="e_imapi_df2tao_table_of_contents_empty_disc"></span><dl> <span data-ttu-id="e0759-225"><dt><strong>E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC</strong></dt> <dt>(HRESULT) 0xC0AA0505</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-225"><dt><strong>E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC</strong></dt> <dt>(HRESULT)0xC0AA0505</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-226">O Sumário não pode ser recuperado de um disco vazio.</span><span class="sxs-lookup"><span data-stu-id="e0759-226">The table of contents cannot be retrieved from an empty disc.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK"></span><span id="e_imapi_df2tao_media_is_not_blank"></span><dl> <span data-ttu-id="e0759-227"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK</strong></dt> <dt>(HRESULT) 0xC0AA0506</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-227"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK</strong></dt> <dt>(HRESULT)0xC0AA0506</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-228">Há suporte apenas para mídia de CD-R/RW em branco.</span><span class="sxs-lookup"><span data-stu-id="e0759-228">Only blank CD-R/RW media is supported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_media_is_not_supported"></span><dl> <span data-ttu-id="e0759-229"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA0507</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-229"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0507</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-230">Há suporte apenas para mídia de CD-R/RW em branco.</span><span class="sxs-lookup"><span data-stu-id="e0759-230">Only blank CD-R/RW media is supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED"></span><span id="e_imapi_df2tao_track_limit_reached"></span><dl> <span data-ttu-id="e0759-231"><dt><strong>E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED</strong></dt> <dt>(HRESULT) 0xC0AA0508</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-231"><dt><strong>E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED</strong></dt> <dt>(HRESULT)0xC0AA0508</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-232">As mídias CD-R e CD-RW dão suporte a um máximo de 99 faixas de áudio.</span><span class="sxs-lookup"><span data-stu-id="e0759-232">CD-R and CD-RW media support a maximum of 99 audio tracks.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE"></span><span id="e_imapi_df2tao_not_enough_space"></span><dl> <span data-ttu-id="e0759-233"><dt><strong>E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE</strong></dt> <dt>(HRESULT) 0xC0AA0509</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-233"><dt><strong>E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE</strong></dt> <dt>(HRESULT)0xC0AA0509</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-234">Não há espaço suficiente restante na mídia para adicionar a faixa de áudio fornecida.</span><span class="sxs-lookup"><span data-stu-id="e0759-234">There is not enough space left on the media to add the provided audio track.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED"></span><span id="e_imapi_df2tao_no_recorder_specified"></span><dl> <span data-ttu-id="e0759-235"><dt><strong>E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED</strong></dt> <dt>(HRESULT) 0xC0AA050A</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-235"><dt><strong>E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED</strong></dt> <dt>(HRESULT)0xC0AA050A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-236">Você não pode preparar a mídia até escolher um gravador para usar.</span><span class="sxs-lookup"><span data-stu-id="e0759-236">You cannot prepare the media until you choose a recorder to use.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_INVALID_ISRC"></span><span id="e_imapi_df2tao_invalid_isrc"></span><dl> <span data-ttu-id="e0759-237"><dt><strong>E_IMAPI_DF2TAO_INVALID_ISRC</strong></dt> <dt>(HRESULT) 0xC0AA050B</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-237"><dt><strong>E_IMAPI_DF2TAO_INVALID_ISRC</strong></dt> <dt>(HRESULT)0xC0AA050B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-238">O ISRC fornecido não é válido.</span><span class="sxs-lookup"><span data-stu-id="e0759-238">The ISRC provided is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_INVALID_MCN"></span><span id="e_imapi_df2tao_invalid_mcn"></span><dl> <span data-ttu-id="e0759-239"><dt><strong>E_IMAPI_DF2TAO_INVALID_MCN</strong></dt> <dt>(HRESULT) 0xC0AA050C</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-239"><dt><strong>E_IMAPI_DF2TAO_INVALID_MCN</strong></dt> <dt>(HRESULT)0xC0AA050C</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-240">O número de catálogo de mídia fornecido não é válido.</span><span class="sxs-lookup"><span data-stu-id="e0759-240">The Media Catalog Number provided is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_stream_not_supported"></span><dl> <span data-ttu-id="e0759-241"><dt><strong>E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA050D</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-241"><dt><strong>E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA050D</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-242">O fluxo de áudio fornecido não é válido.</span><span class="sxs-lookup"><span data-stu-id="e0759-242">The provided audio stream is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_recorder_not_supported"></span><dl> <span data-ttu-id="e0759-243"><dt><strong>E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA050E</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-243"><dt><strong>E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA050E</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-244">Este dispositivo não oferece suporte às operações exigidas por este formato de disco.</span><span class="sxs-lookup"><span data-stu-id="e0759-244">This device does not support the operations required by this disc format.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2tao_client_name_is_not_valid"></span><dl> <span data-ttu-id="e0759-245"><dt><strong>E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT) 0xC0AA050F</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-245"><dt><strong>E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT)0xC0AA050F</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-246">O nome do cliente não é válido.</span><span class="sxs-lookup"><span data-stu-id="e0759-246">The client name is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2raw_write_in_progress"></span><dl> <span data-ttu-id="e0759-247"><dt><strong>E_IMAPI_DF2RAW_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xC0AA0600</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-247"><dt><strong>E_IMAPI_DF2RAW_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0600</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-248">Atualmente, há uma operação de gravação em andamento.</span><span class="sxs-lookup"><span data-stu-id="e0759-248">There is currently a write operation in progress.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2raw_write_not_in_progress"></span><dl> <span data-ttu-id="e0759-249"><dt><strong>E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xC0AA0601</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-249"><dt><strong>E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0601</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-250">Não há nenhuma operação de gravação em andamento no momento.</span><span class="sxs-lookup"><span data-stu-id="e0759-250">There is no write operation currently in progress.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED"></span><span id="e_imapi_df2raw_media_is_not_prepared"></span><dl> <span data-ttu-id="e0759-251"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED</strong></dt> <dt>(HRESULT) 0xC0AA0602</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-251"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED</strong></dt> <dt>(HRESULT)0xC0AA0602</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-252">A operação solicitada só é válida quando a mídia foi &quot; preparada &quot; .</span><span class="sxs-lookup"><span data-stu-id="e0759-252">The requested operation is only valid when media has been &quot;prepared&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_MEDIA_IS_PREPARED"></span><span id="e_imapi_df2raw_media_is_prepared"></span><dl> <span data-ttu-id="e0759-253"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_PREPARED</strong></dt> <dt>(HRESULT) 0xC0AA0603</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-253"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_PREPARED</strong></dt> <dt>(HRESULT)0xC0AA0603</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-254">A operação solicitada não é válida quando a mídia foi &quot; preparada &quot; , mas não foi liberada.</span><span class="sxs-lookup"><span data-stu-id="e0759-254">The requested operation is not valid when media has been &quot;prepared&quot; but not released.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2raw_client_name_is_not_valid"></span><dl> <span data-ttu-id="e0759-255"><dt><strong>E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT) 0xC0AA0604</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-255"><dt><strong>E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT)0xC0AA0604</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-256">O nome do cliente não é válido.</span><span class="sxs-lookup"><span data-stu-id="e0759-256">The client name is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK"></span><span id="e_imapi_df2raw_media_is_not_blank"></span><dl> <span data-ttu-id="e0759-257"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK</strong></dt> <dt>(HRESULT) 0xC0AA0606</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-257"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK</strong></dt> <dt>(HRESULT)0xC0AA0606</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-258">Há suporte apenas para mídia de CD-R/RW em branco.</span><span class="sxs-lookup"><span data-stu-id="e0759-258">Only blank CD-R/RW media is supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_media_is_not_supported"></span><dl> <span data-ttu-id="e0759-259"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA0607</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-259"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0607</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-260">Há suporte apenas para mídia de CD-R/RW em branco.</span><span class="sxs-lookup"><span data-stu-id="e0759-260">Only blank CD-R/RW media is supported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE"></span><span id="e_imapi_df2raw_not_enough_space"></span><dl> <span data-ttu-id="e0759-261"><dt><strong>E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE</strong></dt> <dt>(HRESULT) 0xC0AA0609</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-261"><dt><strong>E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE</strong></dt> <dt>(HRESULT)0xC0AA0609</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-262">Não há espaço suficiente na mídia para adicionar a sessão fornecida.</span><span class="sxs-lookup"><span data-stu-id="e0759-262">There is not enough space on the media to add the provided session.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED"></span><span id="e_imapi_df2raw_no_recorder_specified"></span><dl> <span data-ttu-id="e0759-263"><dt><strong>E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED</strong></dt> <dt>(HRESULT) 0xC0AA060A</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-263"><dt><strong>E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED</strong></dt> <dt>(HRESULT)0xC0AA060A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-264">Você não pode preparar a mídia até escolher um gravador para usar.</span><span class="sxs-lookup"><span data-stu-id="e0759-264">You cannot prepare the media until you choose a recorder to use.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_stream_not_supported"></span><dl> <span data-ttu-id="e0759-265"><dt><strong>E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA060D</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-265"><dt><strong>E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA060D</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-266">O fluxo de áudio fornecido não é válido.</span><span class="sxs-lookup"><span data-stu-id="e0759-266">The provided audio stream is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_data_block_type_not_supported"></span><dl> <span data-ttu-id="e0759-267"><dt><strong>E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA060E</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-267"><dt><strong>E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA060E</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-268">O tipo de bloco de dados solicitado não é suportado pelo dispositivo atual.</span><span class="sxs-lookup"><span data-stu-id="e0759-268">The requested data block type is not supported by the current device.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT"></span><span id="e_imapi_df2raw_stream_leadin_too_short"></span><dl> <span data-ttu-id="e0759-269"><dt><strong>E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT</strong></dt> <dt>(HRESULT) 0xC0AA060F</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-269"><dt><strong>E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT</strong></dt> <dt>(HRESULT)0xC0AA060F</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-270">O fluxo não contém um número suficiente de setores na liderança para a mídia atual.</span><span class="sxs-lookup"><span data-stu-id="e0759-270">The stream does not contain a sufficient number of sectors in the leadin for the current media.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_recorder_not_supported"></span><dl> <span data-ttu-id="e0759-271"><dt><strong>E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA0610</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-271"><dt><strong>E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0610</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-272">Este dispositivo não oferece suporte às operações exigidas por este formato de disco.</span><span class="sxs-lookup"><span data-stu-id="e0759-272">This device does not support the operations required by this disc format.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_RECORDER_IN_USE"></span><span id="e_imapi_erase_recorder_in_use"></span><dl> <span data-ttu-id="e0759-273"><dt><strong>E_IMAPI_ERASE_RECORDER_IN_USE</strong></dt> <dt>(HRESULT) 0x80AA0900</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-273"><dt><strong>E_IMAPI_ERASE_RECORDER_IN_USE</strong></dt> <dt>(HRESULT)0x80AA0900</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-274">No momento, o formato está usando o gravador de disco para uma operação de apagamento.</span><span class="sxs-lookup"><span data-stu-id="e0759-274">The format is currently using the disc recorder for an erase operation.</span></span> <span data-ttu-id="e0759-275">Aguarde até que o apagamento seja concluído antes de tentar definir ou limpar o gravador de disco atual.</span><span class="sxs-lookup"><span data-stu-id="e0759-275">Please wait for the erase to complete before attempting to set or clear the current disc recorder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED"></span><span id="e_imapi_erase_only_one_recorder_supported"></span><dl> <span data-ttu-id="e0759-276"><dt><strong>E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED</strong></dt> <dt>(HRESULT) 0x80AA0901</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-276"><dt><strong>E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED</strong></dt> <dt>(HRESULT)0x80AA0901</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-277">O formato de apagamento só dá suporte a um gravador.</span><span class="sxs-lookup"><span data-stu-id="e0759-277">The erase format only supports one recorder.</span></span> <span data-ttu-id="e0759-278">Você deve limpar o gravador atual antes de definir um novo.</span><span class="sxs-lookup"><span data-stu-id="e0759-278">You must clear the current recorder before setting a new one.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL"></span><span id="e_imapi_erase_disc_information_too_small"></span><dl> <span data-ttu-id="e0759-279"><dt><strong>E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL</strong></dt> <dt>(HRESULT) 0x80AA0902</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-279"><dt><strong>E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL</strong></dt> <dt>(HRESULT)0x80AA0902</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-280">A unidade não relate dados suficientes para um comando ler informações do disco.</span><span class="sxs-lookup"><span data-stu-id="e0759-280">The drive did not report sufficient data for a READ DISC INFORMATION command.</span></span> <span data-ttu-id="e0759-281">A unidade pode não ter suporte ou a mídia pode não estar correta.</span><span class="sxs-lookup"><span data-stu-id="e0759-281">The drive may not be supported, or the media may not be correct.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL"></span><span id="e_imapi_erase_mode_page_2a_too_small"></span><dl> <span data-ttu-id="e0759-282"><dt><strong>E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL</strong></dt> <dt>(HRESULT) 0x80AA0903</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-282"><dt><strong>E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL</strong></dt> <dt>(HRESULT)0x80AA0903</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-283">A unidade não relate dados suficientes para um comando MODE SENSE (Page 0x2A).</span><span class="sxs-lookup"><span data-stu-id="e0759-283">The drive did not report sufficient data for a MODE SENSE (page 0x2A) command.</span></span> <span data-ttu-id="e0759-284">A unidade pode não ter suporte ou a mídia pode não estar correta.</span><span class="sxs-lookup"><span data-stu-id="e0759-284">The drive may not be supported, or the media may not be correct.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE"></span><span id="e_imapi_erase_media_is_not_erasable"></span><dl> <span data-ttu-id="e0759-285"><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE</strong></dt> <dt>(HRESULT) 0x80AA0904</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-285"><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE</strong></dt> <dt>(HRESULT)0x80AA0904</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-286">A unidade relatou que a mídia não é apagável.</span><span class="sxs-lookup"><span data-stu-id="e0759-286">The drive reported that the media is not erasable.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND"></span><span id="e_imapi_erase_drive_failed_erase_command"></span><dl> <span data-ttu-id="e0759-287"><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND</strong></dt> <dt>(HRESULT) 0x80AA0905</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-287"><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND</strong></dt> <dt>(HRESULT)0x80AA0905</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-288">Falha do comando de apagamento na unidade.</span><span class="sxs-lookup"><span data-stu-id="e0759-288">The drive failed the erase command.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR"></span><span id="e_imapi_erase_took_longer_than_one_hour"></span><dl> <span data-ttu-id="e0759-289"><dt><strong>E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR</strong></dt> <dt>(HRESULT) 0x80AA0906</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-289"><dt><strong>E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR</strong></dt> <dt>(HRESULT)0x80AA0906</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-290">A unidade não concluiu o apagamento em uma hora.</span><span class="sxs-lookup"><span data-stu-id="e0759-290">The drive did not complete the erase in one hour.</span></span> <span data-ttu-id="e0759-291">A unidade pode exigir um ciclo de energia, remoção de mídia ou outra intervenção manual para retomar a operação adequada.</span><span class="sxs-lookup"><span data-stu-id="e0759-291">The drive may require a power cycle, media removal, or other manual intervention to resume proper operation.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e0759-292">Atualmente, esse valor também será retornado se uma tentativa de executar um apagamento em mídia de CD-RW ou DVD-RW por meio da interface <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a> falhar como resultado da mídia estar inadequada.</span><span class="sxs-lookup"><span data-stu-id="e0759-292">Currently, this value will also be returned if an attempt to perform an erase on CD-RW or DVD-RW media via the <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a> interface fails as a result of the media being bad.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE"></span><span id="e_imapi_erase_unexpected_drive_response_during_erase"></span><dl> <span data-ttu-id="e0759-293"><dt><strong>E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE</strong></dt> <dt>(HRESULT) 0x80AA0907</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-293"><dt><strong>E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE</strong></dt> <dt>(HRESULT)0x80AA0907</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-294">A unidade retornou um erro inesperado durante o apagamento.</span><span class="sxs-lookup"><span data-stu-id="e0759-294">The drive returned an unexpected error during the erase.</span></span> <span data-ttu-id="e0759-295">A mídia pode ser inutilizável, o apagamento pode estar concluído ou a unidade ainda pode estar no processo de apagamento do disco.</span><span class="sxs-lookup"><span data-stu-id="e0759-295">The media may be unusable, the erase may be complete, or the drive may still be in the process of erasing the disc.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND"></span><span id="e_imapi_erase_drive_failed_spinup_command"></span><dl> <span data-ttu-id="e0759-296"><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND</strong></dt> <dt>(HRESULT) 0x80AA0908</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-296"><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND</strong></dt> <dt>(HRESULT)0x80AA0908</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-297">A unidade retornou um erro para um comando de unidade inicial (SPINUP).</span><span class="sxs-lookup"><span data-stu-id="e0759-297">The drive returned an error for a START UNIT (spinup) command.</span></span> <span data-ttu-id="e0759-298">A intervenção manual pode ser necessária.</span><span class="sxs-lookup"><span data-stu-id="e0759-298">Manual intervention may be required.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_erase_media_is_not_supported"></span><dl> <span data-ttu-id="e0759-299"><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA0909</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-299"><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0909</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-300">Não há suporte para o tipo de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="e0759-300">The current media type is unsupported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_erase_recorder_not_supported"></span><dl> <span data-ttu-id="e0759-301"><dt><strong>E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA090A</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-301"><dt><strong>E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA090A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-302">Este dispositivo não oferece suporte às operações exigidas por este formato de disco.</span><span class="sxs-lookup"><span data-stu-id="e0759-302">This device does not support the operations required by this disc format.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_erase_client_name_is_not_valid"></span><dl> <span data-ttu-id="e0759-303"><dt><strong>E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT) 0xC0AA090B</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-303"><dt><strong>E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT)0xC0AA090B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-304">O nome do cliente não é válido.</span><span class="sxs-lookup"><span data-stu-id="e0759-304">The client name is not valid.</span></span><br/></td>
</tr>
</tbody>
</table>



<span data-ttu-id="e0759-305">Os seguintes códigos de êxito e de erro são definidos em Imapi2fserror. h.</span><span class="sxs-lookup"><span data-stu-id="e0759-305">The following success and error codes are defined in Imapi2fserror.h.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="e0759-306">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="e0759-306">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="e0759-307">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0759-307">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_FSI_INTERNAL_ERROR"></span><span id="imapi_e_fsi_internal_error"></span><dl> <span data-ttu-id="e0759-308"><dt><strong>IMAPI_E_FSI_INTERNAL_ERROR</strong></dt> <dt>(HRESULT) 0xC0AAB100</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-308"><dt><strong>IMAPI_E_FSI_INTERNAL_ERROR</strong></dt> <dt>(HRESULT)0xC0AAB100</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-309">Ocorreu um erro interno: %1! ls!.</span><span class="sxs-lookup"><span data-stu-id="e0759-309">Internal error occurred: %1!ls!.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_PARAM"></span><span id="imapi_e_invalid_param"></span><dl> <span data-ttu-id="e0759-310"><dt><strong>IMAPI_E_INVALID_PARAM</strong></dt> <dt>(HRESULT) 0xC0AAB101</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-310"><dt><strong>IMAPI_E_INVALID_PARAM</strong></dt> <dt>(HRESULT)0xC0AAB101</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-311">O valor especificado para o parâmetro ' %1! ls! '</span><span class="sxs-lookup"><span data-stu-id="e0759-311">The value specified for parameter '%1!ls!'</span></span> <span data-ttu-id="e0759-312">não é válido.</span><span class="sxs-lookup"><span data-stu-id="e0759-312">is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_READONLY"></span><span id="imapi_e_readonly"></span><dl> <span data-ttu-id="e0759-313"><dt><strong>IMAPI_E_READONLY</strong></dt> <dt>(HRESULT) 0xC0AAB102</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-313"><dt><strong>IMAPI_E_READONLY</strong></dt> <dt>(HRESULT)0xC0AAB102</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-314">O objeto FileSystemImage está no modo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="e0759-314">FileSystemImage object is in read only mode.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NO_OUTPUT"></span><span id="imapi_e_no_output"></span><dl> <span data-ttu-id="e0759-315"><dt><strong>IMAPI_E_NO_OUTPUT</strong></dt> <dt>(HRESULT) 0xC0AAB103</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-315"><dt><strong>IMAPI_E_NO_OUTPUT</strong></dt> <dt>(HRESULT)0xC0AAB103</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-316">Nenhum sistema de arquivos de saída especificado.</span><span class="sxs-lookup"><span data-stu-id="e0759-316">No output file system specified.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_VOLUME_NAME"></span><span id="imapi_e_invalid_volume_name"></span><dl> <span data-ttu-id="e0759-317"><dt><strong>IMAPI_E_INVALID_VOLUME_NAME</strong></dt> <dt>(HRESULT) 0xC0AAB104</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-317"><dt><strong>IMAPI_E_INVALID_VOLUME_NAME</strong></dt> <dt>(HRESULT)0xC0AAB104</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-318">O identificador de volume especificado é muito longo ou contém um ou mais caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="e0759-318">The specified Volume Identifier is either too long or contains one or more invalid characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_DATE"></span><span id="imapi_e_invalid_date"></span><dl> <span data-ttu-id="e0759-319"><dt><strong>IMAPI_E_INVALID_DATE</strong></dt> <dt>(HRESULT) 0xC0AAB105</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-319"><dt><strong>IMAPI_E_INVALID_DATE</strong></dt> <dt>(HRESULT)0xC0AAB105</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-320">Datas de arquivo inválidas.</span><span class="sxs-lookup"><span data-stu-id="e0759-320">Invalid file dates.</span></span> <span data-ttu-id="e0759-321">%1! ls!</span><span class="sxs-lookup"><span data-stu-id="e0759-321">%1!ls!</span></span> <span data-ttu-id="e0759-322">a hora é anterior a %2! ls!</span><span class="sxs-lookup"><span data-stu-id="e0759-322">time is earlier than %2!ls!</span></span> <span data-ttu-id="e0759-323">tempo.</span><span class="sxs-lookup"><span data-stu-id="e0759-323">time.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_NOT_EMPTY"></span><span id="imapi_e_file_system_not_empty"></span><dl> <span data-ttu-id="e0759-324"><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_EMPTY</strong></dt> <dt>(HRESULT) 0xC0AAB106</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-324"><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_EMPTY</strong></dt> <dt>(HRESULT)0xC0AAB106</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-325">O sistema de arquivos deve estar vazio para esta função.</span><span class="sxs-lookup"><span data-stu-id="e0759-325">The file system must be empty for this function.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED"></span><span id="imapi_e_file_system_change_not_allowed"></span><dl> <span data-ttu-id="e0759-326"><dt><strong>IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED</strong></dt> <dt>(HRESULT) 0xC0AAB163L</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-326"><dt><strong>IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED</strong></dt> <dt>(HRESULT)0xC0AAB163L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-327">Não é possível alterar o sistema de arquivos especificado para criação, pois o sistema de arquivos da sessão importada e o sistema de arquivos na sessão atual não correspondem.</span><span class="sxs-lookup"><span data-stu-id="e0759-327">You cannot change the file system specified for creation, because the file system from the imported session and the file system in the current session do not match.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_NOT_FILE"></span><span id="imapi_e_not_file"></span><dl> <span data-ttu-id="e0759-328"><dt><strong>IMAPI_E_NOT_FILE</strong></dt> <dt>(HRESULT) 0xC0AAB108</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-328"><dt><strong>IMAPI_E_NOT_FILE</strong></dt> <dt>(HRESULT)0xC0AAB108</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-329">Caminho especificado ' %1! ls! '</span><span class="sxs-lookup"><span data-stu-id="e0759-329">Specified path '%1!ls!'</span></span> <span data-ttu-id="e0759-330">não identifica um arquivo.</span><span class="sxs-lookup"><span data-stu-id="e0759-330">does not identify a file.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NOT_DIR"></span><span id="imapi_e_not_dir"></span><dl> <span data-ttu-id="e0759-331"><dt><strong>IMAPI_E_NOT_DIR</strong></dt> <dt>(HRESULT) 0xC0AAB109</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-331"><dt><strong>IMAPI_E_NOT_DIR</strong></dt> <dt>(HRESULT)0xC0AAB109</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-332">Caminho especificado ' %1! ls! '</span><span class="sxs-lookup"><span data-stu-id="e0759-332">Specified path '%1!ls!'</span></span> <span data-ttu-id="e0759-333">não identifica um diretório.</span><span class="sxs-lookup"><span data-stu-id="e0759-333">does not identify a directory.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DIR_NOT_EMPTY"></span><span id="imapi_e_dir_not_empty"></span><dl> <span data-ttu-id="e0759-334"><dt><strong>IMAPI_E_DIR_NOT_EMPTY</strong></dt> <dt>(HRESULT) 0xC0AAB10A</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-334"><dt><strong>IMAPI_E_DIR_NOT_EMPTY</strong></dt> <dt>(HRESULT)0xC0AAB10A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-335">O diretório ' %1! s! '</span><span class="sxs-lookup"><span data-stu-id="e0759-335">The directory '%1!s!'</span></span> <span data-ttu-id="e0759-336">Não está vazio.</span><span class="sxs-lookup"><span data-stu-id="e0759-336">is not empty.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NOT_IN_FILE_SYSTEM"></span><span id="imapi_e_not_in_file_system"></span><dl> <span data-ttu-id="e0759-337"><dt><strong>IMAPI_E_NOT_IN_FILE_SYSTEM</strong></dt> <dt>(HRESULT) 0xC0AAB10B</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-337"><dt><strong>IMAPI_E_NOT_IN_FILE_SYSTEM</strong></dt> <dt>(HRESULT)0xC0AAB10B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-338">ls! '</span><span class="sxs-lookup"><span data-stu-id="e0759-338">ls!'</span></span> <span data-ttu-id="e0759-339">Não faz parte do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="e0759-339">is not part of the file system.</span></span> <span data-ttu-id="e0759-340">Ele deve ser adicionado para concluir esta operação.</span><span class="sxs-lookup"><span data-stu-id="e0759-340">It must be added to complete this operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_PATH"></span><span id="imapi_e_invalid_path"></span><dl> <span data-ttu-id="e0759-341"><dt><strong>IMAPI_E_INVALID_PATH</strong></dt> <dt>(HRESULT) 0xC0AAB110</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-341"><dt><strong>IMAPI_E_INVALID_PATH</strong></dt> <dt>(HRESULT)0xC0AAB110</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-342">Caminho ' %1! s! '</span><span class="sxs-lookup"><span data-stu-id="e0759-342">Path '%1!s!'</span></span> <span data-ttu-id="e0759-343">está mal formado ou contém caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="e0759-343">is badly formed or contains invalid characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_RESTRICTED_NAME_VIOLATION"></span><span id="imapi_e_restricted_name_violation"></span><dl> <span data-ttu-id="e0759-344"><dt><strong>IMAPI_E_RESTRICTED_NAME_VIOLATION</strong></dt> <dt>(HRESULT) 0xC0AAB111</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-344"><dt><strong>IMAPI_E_RESTRICTED_NAME_VIOLATION</strong></dt> <dt>(HRESULT)0xC0AAB111</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-345">O nome ' %1! ls! '</span><span class="sxs-lookup"><span data-stu-id="e0759-345">The name '%1!ls!'</span></span> <span data-ttu-id="e0759-346">especificado não é válido: o nome do objeto de arquivo ou diretório criado enquanto a propriedade UseRestrictedCharacterSet está definida pode conter apenas caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="e0759-346">specified is not legal: Name of file or directory object created while the UseRestrictedCharacterSet property is set may only contain ANSI characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DUP_NAME"></span><span id="imapi_e_dup_name"></span><dl> <span data-ttu-id="e0759-347"><dt><strong>IMAPI_E_DUP_NAME</strong></dt> <dt>(HRESULT) 0xC0AAB112</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-347"><dt><strong>IMAPI_E_DUP_NAME</strong></dt> <dt>(HRESULT)0xC0AAB112</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-348">ls! '</span><span class="sxs-lookup"><span data-stu-id="e0759-348">ls!'</span></span> <span data-ttu-id="e0759-349">o nome já existe.</span><span class="sxs-lookup"><span data-stu-id="e0759-349">name already exists.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NO_UNIQUE_NAME"></span><span id="imapi_e_no_unique_name"></span><dl> <span data-ttu-id="e0759-350"><dt><strong>IMAPI_E_NO_UNIQUE_NAME</strong></dt> <dt>(HRESULT) 0xC0AAB113</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-350"><dt><strong>IMAPI_E_NO_UNIQUE_NAME</strong></dt> <dt>(HRESULT)0xC0AAB113</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-351">Tentativa de adicionar ' %1! ls! '</span><span class="sxs-lookup"><span data-stu-id="e0759-351">Attempt to add '%1!ls!'</span></span> <span data-ttu-id="e0759-352">falha: não é possível criar um nome exclusivo específico do sistema de arquivos para %2! ls!</span><span class="sxs-lookup"><span data-stu-id="e0759-352">failed: cannot create a file-system-specific unique name for the %2!ls!</span></span> <span data-ttu-id="e0759-353">.</span><span class="sxs-lookup"><span data-stu-id="e0759-353">file system.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_ITEM_NOT_FOUND"></span><span id="imapi_e_item_not_found"></span><dl> <span data-ttu-id="e0759-354"><dt><strong>IMAPI_E_ITEM_NOT_FOUND</strong></dt> <dt>(HRESULT) 0xC0AAB118</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-354"><dt><strong>IMAPI_E_ITEM_NOT_FOUND</strong></dt> <dt>(HRESULT)0xC0AAB118</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-355">Não é possível encontrar o item ' %1! ls! '</span><span class="sxs-lookup"><span data-stu-id="e0759-355">Cannot find item '%1!ls!'</span></span> <span data-ttu-id="e0759-356">na hierarquia de FileSystemImage.</span><span class="sxs-lookup"><span data-stu-id="e0759-356">in FileSystemImage hierarchy.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_FILE_NOT_FOUND"></span><span id="imapi_e_file_not_found"></span><dl> <span data-ttu-id="e0759-357"><dt><strong>IMAPI_E_FILE_NOT_FOUND</strong></dt> <dt>(HRESULT) 0xC0AAB119</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-357"><dt><strong>IMAPI_E_FILE_NOT_FOUND</strong></dt> <dt>(HRESULT)0xC0AAB119</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-358">O arquivo ' %1! s! '</span><span class="sxs-lookup"><span data-stu-id="e0759-358">The file '%1!s!'</span></span> <span data-ttu-id="e0759-359">não encontrado na hierarquia de FileSystemImage.</span><span class="sxs-lookup"><span data-stu-id="e0759-359">not found in FileSystemImage hierarchy.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DIR_NOT_FOUND"></span><span id="imapi_e_dir_not_found"></span><dl> <span data-ttu-id="e0759-360"><dt><strong>IMAPI_E_DIR_NOT_FOUND</strong></dt> <dt>(HRESULT) 0xC0AAB11A</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-360"><dt><strong>IMAPI_E_DIR_NOT_FOUND</strong></dt> <dt>(HRESULT)0xC0AAB11A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-361">O diretório ' %1! s! '</span><span class="sxs-lookup"><span data-stu-id="e0759-361">The directory '%1!s!'</span></span> <span data-ttu-id="e0759-362">não encontrado na hierarquia de FileSystemImage.</span><span class="sxs-lookup"><span data-stu-id="e0759-362">not found in FileSystemImage hierarchy.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMAGE_SIZE_LIMIT"></span><span id="imapi_e_image_size_limit"></span><dl> <span data-ttu-id="e0759-363"><dt><strong>IMAPI_E_IMAGE_SIZE_LIMIT</strong></dt> <dt>(HRESULT) 0xC0AAB120</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-363"><dt><strong>IMAPI_E_IMAGE_SIZE_LIMIT</strong></dt> <dt>(HRESULT)0xC0AAB120</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-364">Adicionando ' %1! ls! '</span><span class="sxs-lookup"><span data-stu-id="e0759-364">Adding '%1!ls!'</span></span> <span data-ttu-id="e0759-365">resultaria em uma imagem de resultado com um tamanho maior do que o limite configurado atual.</span><span class="sxs-lookup"><span data-stu-id="e0759-365">would result in a result image having a size larger than the current configured limit.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_IMAGE_TOO_BIG"></span><span id="imapi_e_image_too_big"></span><dl> <span data-ttu-id="e0759-366"><dt><strong>IMAPI_E_IMAGE_TOO_BIG</strong></dt> <dt>(HRESULT) 0xC0AAB121</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-366"><dt><strong>IMAPI_E_IMAGE_TOO_BIG</strong></dt> <dt>(HRESULT)0xC0AAB121</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-367">O valor especificado para a propriedade FreeMediaBlocks é muito pequeno para o tamanho estimado da imagem com base nos dados atuais.</span><span class="sxs-lookup"><span data-stu-id="e0759-367">Value specified for FreeMediaBlocks property is too small for estimated image size based on current data.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED"></span><span id="imapi_e_imagemanager_image_not_aligned"></span><dl> <span data-ttu-id="e0759-368"><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED</strong></dt> <dt>(HRESULT) 0xC0AAB200L</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-368"><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED</strong></dt> <dt>(HRESULT)0xC0AAB200L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-369">A imagem não está alinhada em um limite de setor 2 KB.</span><span class="sxs-lookup"><span data-stu-id="e0759-369">The image is not aligned on a 2kb sector boundary.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND"></span><span id="imapi_e_imagemanager_no_valid_vd_found"></span><dl> <span data-ttu-id="e0759-370"><dt><strong>IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND</strong></dt> <dt>(HRESULT) 0xC0AAB201L)</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-370"><dt><strong>IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND</strong></dt> <dt>(HRESULT)0xC0AAB201L)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-371">A imagem não contém um descritor de volume válido.</span><span class="sxs-lookup"><span data-stu-id="e0759-371">The image does not contain a valid volume descriptor.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMAGEMANAGER_NO_IMAGE"></span><span id="imapi_e_imagemanager_no_image"></span><dl> <span data-ttu-id="e0759-372"><dt><strong>IMAPI_E_IMAGEMANAGER_NO_IMAGE</strong></dt> <dt>(HRESULT) 0xC0AAB202L</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-372"><dt><strong>IMAPI_E_IMAGEMANAGER_NO_IMAGE</strong></dt> <dt>(HRESULT)0xC0AAB202L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-373">A imagem não foi definida usando os métodos <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setpath"><strong>IIsoImageManager:: SetPath</strong></a> ou <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setstream"><strong>IIsoImageManager:: SetStream</strong></a> antes de chamar o método <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-validate"><strong>IIsoImageManager:: Validate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e0759-373">The image has not been set using the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setpath"><strong>IIsoImageManager::SetPath</strong></a> or <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setstream"><strong>IIsoImageManager::SetStream</strong></a> methods prior to calling the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-validate"><strong>IIsoImageManager::Validate</strong></a> method.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG"></span><span id="imapi_e_imagemanager_image_too_big"></span><dl> <span data-ttu-id="e0759-374"><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG</strong></dt> <dt>(HRESULT) 0xC0AAB203L</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-374"><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG</strong></dt> <dt>(HRESULT)0xC0AAB203L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-375">A imagem fornecida é muito grande para ser validada, pois o tamanho excede <strong>MAXLONG</strong>.</span><span class="sxs-lookup"><span data-stu-id="e0759-375">The provided image is too large to be validated as the size exceeds <strong>MAXLONG</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_DATA_STREAM_INCONSISTENCY"></span><span id="imapi_e_data_stream_inconsistency"></span><dl> <span data-ttu-id="e0759-376"><dt><strong>IMAPI_E_DATA_STREAM_INCONSISTENCY</strong></dt> <dt>(HRESULT) 0xC0AAB128</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-376"><dt><strong>IMAPI_E_DATA_STREAM_INCONSISTENCY</strong></dt> <dt>(HRESULT)0xC0AAB128</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-377">Fluxo de dados fornecido para o arquivo ' %1! ls! '</span><span class="sxs-lookup"><span data-stu-id="e0759-377">Data stream supplied for file '%1!ls!'</span></span> <span data-ttu-id="e0759-378">está inconsistente: esperado %2! I64d!</span><span class="sxs-lookup"><span data-stu-id="e0759-378">is inconsistent: expected %2!I64d!</span></span> <span data-ttu-id="e0759-379">bytes, encontrado %3! I64d!.</span><span class="sxs-lookup"><span data-stu-id="e0759-379">bytes, found %3!I64d!.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DATA_STREAM_READ_FAILURE"></span><span id="imapi_e_data_stream_read_failure"></span><dl> <span data-ttu-id="e0759-380"><dt><strong>IMAPI_E_DATA_STREAM_READ_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB129</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-380"><dt><strong>IMAPI_E_DATA_STREAM_READ_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB129</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-381">Não é possível ler dados do fluxo fornecido para o arquivo ' %1! ls! '.</span><span class="sxs-lookup"><span data-stu-id="e0759-381">Cannot read data from stream supplied for file '%1!ls!'.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_DATA_STREAM_CREATE_FAILURE"></span><span id="imapi_e_data_stream_create_failure"></span><dl> <span data-ttu-id="e0759-382"><dt><strong>IMAPI_E_DATA_STREAM_CREATE_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB12A</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-382"><dt><strong>IMAPI_E_DATA_STREAM_CREATE_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB12A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-383">O seguinte erro foi encontrado ao tentar criar o fluxo de dados para o arquivo ' %1! ls! ':</span><span class="sxs-lookup"><span data-stu-id="e0759-383">The following error was encountered when trying to create data stream for file '%1!ls!':</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DIRECTORY_READ_FAILURE"></span><span id="imapi_e_directory_read_failure"></span><dl> <span data-ttu-id="e0759-384"><dt><strong>IMAPI_E_DIRECTORY_READ_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB12BL</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-384"><dt><strong>IMAPI_E_DIRECTORY_READ_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB12BL</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-385">Falha ao enumerar arquivos na árvore de diretórios é inacessível devido a permissões.</span><span class="sxs-lookup"><span data-stu-id="e0759-385">Failure enumerating files in the directory tree is inaccessible due to permissions.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_TOO_MANY_DIRS"></span><span id="imapi_e_too_many_dirs"></span><dl> <span data-ttu-id="e0759-386"><dt><strong>IMAPI_E_TOO_MANY_DIRS</strong></dt> <dt>(HRESULT) 0xC0AAB130</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-386"><dt><strong>IMAPI_E_TOO_MANY_DIRS</strong></dt> <dt>(HRESULT)0xC0AAB130</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-387">Esta imagem do sistema de arquivos possui muitos diretórios para %1! ls!</span><span class="sxs-lookup"><span data-stu-id="e0759-387">This file system image has too many directories for the %1!ls!</span></span> <span data-ttu-id="e0759-388">.</span><span class="sxs-lookup"><span data-stu-id="e0759-388">file system.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_ISO9660_LEVELS"></span><span id="imapi_e_iso9660_levels"></span><dl> <span data-ttu-id="e0759-389"><dt><strong>IMAPI_E_ISO9660_LEVELS</strong></dt> <dt>(HRESULT) 0xC0AAB131</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-389"><dt><strong>IMAPI_E_ISO9660_LEVELS</strong></dt> <dt>(HRESULT)0xC0AAB131</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-390">ISO9660 é limitado a 8 níveis de diretórios.</span><span class="sxs-lookup"><span data-stu-id="e0759-390">ISO9660 is limited to 8 levels of directories.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_DATA_TOO_BIG"></span><span id="imapi_e_data_too_big"></span><dl> <span data-ttu-id="e0759-391"><dt><strong>IMAPI_E_DATA_TOO_BIG</strong></dt> <dt>(HRESULT) 0xC0AAB132</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-391"><dt><strong>IMAPI_E_DATA_TOO_BIG</strong></dt> <dt>(HRESULT)0xC0AAB132</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-392">O arquivo de dados é muito grande para ' %1! ls! '</span><span class="sxs-lookup"><span data-stu-id="e0759-392">Data file is too large for '%1!ls!'</span></span> <span data-ttu-id="e0759-393">.</span><span class="sxs-lookup"><span data-stu-id="e0759-393">file system.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_OPEN_FAILURE"></span><span id="imapi_e_stashfile_open_failure"></span><dl> <span data-ttu-id="e0759-394"><dt><strong>IMAPI_E_STASHFILE_OPEN_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB138</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-394"><dt><strong>IMAPI_E_STASHFILE_OPEN_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB138</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-395">Não é possível inicializar %1! ls!</span><span class="sxs-lookup"><span data-stu-id="e0759-395">Cannot initialize %1!ls!</span></span> <span data-ttu-id="e0759-396">arquivo stash.</span><span class="sxs-lookup"><span data-stu-id="e0759-396">stash file.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_SEEK_FAILURE"></span><span id="imapi_e_stashfile_seek_failure"></span><dl> <span data-ttu-id="e0759-397"><dt><strong>IMAPI_E_STASHFILE_SEEK_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB139</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-397"><dt><strong>IMAPI_E_STASHFILE_SEEK_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB139</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-398">Erro ao procurar em ' %1! ls! '</span><span class="sxs-lookup"><span data-stu-id="e0759-398">Error seeking in '%1!ls!'</span></span> <span data-ttu-id="e0759-399">arquivo stash.</span><span class="sxs-lookup"><span data-stu-id="e0759-399">stash file.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_WRITE_FAILURE"></span><span id="imapi_e_stashfile_write_failure"></span><dl> <span data-ttu-id="e0759-400"><dt><strong>IMAPI_E_STASHFILE_WRITE_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB13A</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-400"><dt><strong>IMAPI_E_STASHFILE_WRITE_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB13A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-401">Erro encontrado ao gravar em ' %1! ls! '</span><span class="sxs-lookup"><span data-stu-id="e0759-401">Error encountered writing to '%1!ls!'</span></span> <span data-ttu-id="e0759-402">arquivo stash.</span><span class="sxs-lookup"><span data-stu-id="e0759-402">stash file.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_READ_FAILURE"></span><span id="imapi_e_stashfile_read_failure"></span><dl> <span data-ttu-id="e0759-403"><dt><strong>IMAPI_E_STASHFILE_READ_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB13B</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-403"><dt><strong>IMAPI_E_STASHFILE_READ_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB13B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-404">Erro encontrado ao ler de ' %1! ls! '</span><span class="sxs-lookup"><span data-stu-id="e0759-404">Error encountered reading from '%1!ls!'</span></span> <span data-ttu-id="e0759-405">arquivo stash.</span><span class="sxs-lookup"><span data-stu-id="e0759-405">stash file.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_WORKING_DIRECTORY"></span><span id="imapi_e_invalid_working_directory"></span><dl> <span data-ttu-id="e0759-406"><dt><strong>IMAPI_E_INVALID_WORKING_DIRECTORY</strong></dt> <dt>(HRESULT) 0xC0AAB140</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-406"><dt><strong>IMAPI_E_INVALID_WORKING_DIRECTORY</strong></dt> <dt>(HRESULT)0xC0AAB140</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-407">O diretório de trabalho ' %1! ls! '</span><span class="sxs-lookup"><span data-stu-id="e0759-407">The working directory '%1!ls!'</span></span> <span data-ttu-id="e0759-408">não é válido.</span><span class="sxs-lookup"><span data-stu-id="e0759-408">is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_WORKING_DIRECTORY_SPACE"></span><span id="imapi_e_working_directory_space"></span><dl> <span data-ttu-id="e0759-409"><dt><strong>IMAPI_E_WORKING_DIRECTORY_SPACE</strong></dt> <dt>(HRESULT) 0xC0AAB141</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-409"><dt><strong>IMAPI_E_WORKING_DIRECTORY_SPACE</strong></dt> <dt>(HRESULT)0xC0AAB141</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-410">Não é possível definir o diretório de trabalho como ' %1! ls! '.</span><span class="sxs-lookup"><span data-stu-id="e0759-410">Cannot set working directory to '%1!ls!'.</span></span> <span data-ttu-id="e0759-411">O espaço disponível é %2! I64d!</span><span class="sxs-lookup"><span data-stu-id="e0759-411">Space available is %2!I64d!</span></span> <span data-ttu-id="e0759-412">bytes, aproximadamente %3! I64d!</span><span class="sxs-lookup"><span data-stu-id="e0759-412">bytes, approximately %3!I64d!</span></span> <span data-ttu-id="e0759-413">bytes necessários.</span><span class="sxs-lookup"><span data-stu-id="e0759-413">bytes required.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_MOVE"></span><span id="imapi_e_stashfile_move"></span><dl> <span data-ttu-id="e0759-414"><dt><strong>IMAPI_E_STASHFILE_MOVE</strong></dt> <dt>(HRESULT) 0xC0AAB142</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-414"><dt><strong>IMAPI_E_STASHFILE_MOVE</strong></dt> <dt>(HRESULT)0xC0AAB142</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-415">Tentativa de mover o arquivo stash de dados para o diretório ' %1! ls! '</span><span class="sxs-lookup"><span data-stu-id="e0759-415">Attempt to move the data stash file to directory '%1!ls!'</span></span> <span data-ttu-id="e0759-416">Não foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e0759-416">was not successful.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_BOOT_IMAGE_DATA"></span><span id="imapi_e_boot_image_data"></span><dl> <span data-ttu-id="e0759-417"><dt><strong>IMAPI_E_BOOT_IMAGE_DATA</strong></dt> <dt>(HRESULT) 0xC0AAB148</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-417"><dt><strong>IMAPI_E_BOOT_IMAGE_DATA</strong></dt> <dt>(HRESULT)0xC0AAB148</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-418">Não foi possível adicionar o objeto de inicialização à imagem.</span><span class="sxs-lookup"><span data-stu-id="e0759-418">The boot object could not be added to the image.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_BOOT_OBJECT_CONFLICT"></span><span id="imapi_e_boot_object_conflict"></span><dl> <span data-ttu-id="e0759-419"><dt><strong>IMAPI_E_BOOT_OBJECT_CONFLICT</strong></dt> <dt>(HRESULT) 0xC0AAB149</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-419"><dt><strong>IMAPI_E_BOOT_OBJECT_CONFLICT</strong></dt> <dt>(HRESULT)0xC0AAB149</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-420">Um objeto de inicialização só pode ser incluído em uma imagem de disco inicial.</span><span class="sxs-lookup"><span data-stu-id="e0759-420">A boot object can only be included in an initial disc image.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH"></span><span id="imapi_e_boot_emulation_image_size_mismatch"></span><dl> <span data-ttu-id="e0759-421"><dt><strong>IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH</strong></dt> <dt>(HRESULT) 0xC0AAB14A</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-421"><dt><strong>IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH</strong></dt> <dt>(HRESULT)0xC0AAB14A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-422">O tipo de emulação solicitado não corresponde ao tamanho da imagem de inicialização.</span><span class="sxs-lookup"><span data-stu-id="e0759-422">The emulation type requested does not match the boot image size.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_EMPTY_DISC"></span><span id="imapi_e_empty_disc"></span><dl> <span data-ttu-id="e0759-423"><dt><strong>IMAPI_E_EMPTY_DISC</strong></dt> <dt>(HRESULT) 0xC0AAB150</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-423"><dt><strong>IMAPI_E_EMPTY_DISC</strong></dt> <dt>(HRESULT)0xC0AAB150</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-424">A mídia óptica está vazia.</span><span class="sxs-lookup"><span data-stu-id="e0759-424">Optical media is empty.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NO_SUPPORTED_FILE_SYSTEM"></span><span id="imapi_e_no_supported_file_system"></span><dl> <span data-ttu-id="e0759-425"><dt><strong>IMAPI_E_NO_SUPPORTED_FILE_SYSTEM</strong></dt> <dt>(HRESULT) 0xC0AAB151</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-425"><dt><strong>IMAPI_E_NO_SUPPORTED_FILE_SYSTEM</strong></dt> <dt>(HRESULT)0xC0AAB151</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-426">O disco especificado não contém um dos sistemas de arquivos com suporte.</span><span class="sxs-lookup"><span data-stu-id="e0759-426">The specified disc does not contain one of the supported file systems.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_NOT_FOUND"></span><span id="imapi_e_file_system_not_found"></span><dl> <span data-ttu-id="e0759-427"><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_FOUND</strong></dt> <dt>(HRESULT) 0xC0AAB152</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-427"><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_FOUND</strong></dt> <dt>(HRESULT)0xC0AAB152</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-428">O disco especificado não contém um ' %1! ls! '</span><span class="sxs-lookup"><span data-stu-id="e0759-428">The specified disc does not contain a '%1!ls!'</span></span> <span data-ttu-id="e0759-429">.</span><span class="sxs-lookup"><span data-stu-id="e0759-429">file system.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR"></span><span id="imapi_e_file_system_read_consistency_error"></span><dl> <span data-ttu-id="e0759-430"><dt><strong>IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR</strong></dt> <dt>(HRESULT) 0xC0AAB153</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-430"><dt><strong>IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR</strong></dt> <dt>(HRESULT)0xC0AAB153</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-431">Erro de consistência encontrado ao importar o ' %1! ls! '</span><span class="sxs-lookup"><span data-stu-id="e0759-431">Consistency error encountered while importing the '%1!ls!'</span></span> <span data-ttu-id="e0759-432">.</span><span class="sxs-lookup"><span data-stu-id="e0759-432">file system.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED"></span><span id="imapi_e_file_system_feature_not_supported"></span><dl> <span data-ttu-id="e0759-433"><dt><strong>IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AAB154</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-433"><dt><strong>IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AAB154</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-434">O ' %1! ls! ' o sistema de arquivos no disco selecionado contém um recurso sem suporte para importação: %2! ls!.</span><span class="sxs-lookup"><span data-stu-id="e0759-434">The '%1!ls!'file system on the selected disc contains a feature not supported for import: %2!ls!.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY"></span><span id="imapi_e_import_type_collision_file_exists_as_directory"></span><dl> <span data-ttu-id="e0759-435"><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY</strong></dt> <dt>(HRESULT) 0xC0AAB155</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-435"><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY</strong></dt> <dt>(HRESULT)0xC0AAB155</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-436">Não foi possível importar %2! ls!</span><span class="sxs-lookup"><span data-stu-id="e0759-436">Could not import %2!ls!</span></span> <span data-ttu-id="e0759-437">sistema de arquivos do disco. O arquivo ' %1! ls! '</span><span class="sxs-lookup"><span data-stu-id="e0759-437">file system from disc. The file '%1!ls!'</span></span> <span data-ttu-id="e0759-438">Já existe na hierarquia de imagens como um diretório.</span><span class="sxs-lookup"><span data-stu-id="e0759-438">already exists within the image hierarchy as a directory.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_SEEK_FAILURE"></span><span id="imapi_e_import_seek_failure"></span><dl> <span data-ttu-id="e0759-439"><dt><strong>IMAPI_E_IMPORT_SEEK_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB156</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-439"><dt><strong>IMAPI_E_IMPORT_SEEK_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB156</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-440">Não é possível buscar no bloco %1! I64d!</span><span class="sxs-lookup"><span data-stu-id="e0759-440">Cannot seek to block %1!I64d!</span></span> <span data-ttu-id="e0759-441">no disco de origem.</span><span class="sxs-lookup"><span data-stu-id="e0759-441">on source disc.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_READ_FAILURE"></span><span id="imapi_e_import_read_failure"></span><dl> <span data-ttu-id="e0759-442"><dt><strong>IMAPI_E_IMPORT_READ_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB157</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-442"><dt><strong>IMAPI_E_IMPORT_READ_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB157</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-443">Falha na importação da sessão anterior devido a um erro ao ler um bloco na mídia (bloco mais provável %1! u!).</span><span class="sxs-lookup"><span data-stu-id="e0759-443">Import from previous session failed due to an error reading a block on the media (most likely block %1!u!).</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DISC_MISMATCH"></span><span id="imapi_e_disc_mismatch"></span><dl> <span data-ttu-id="e0759-444"><dt><strong>IMAPI_E_DISC_MISMATCH</strong></dt> <dt>(HRESULT) 0xC0AAB158</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-444"><dt><strong>IMAPI_E_DISC_MISMATCH</strong></dt> <dt>(HRESULT)0xC0AAB158</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-445">O disco atual não é o mesmo do qual o sistema de arquivos foi importado.</span><span class="sxs-lookup"><span data-stu-id="e0759-445">Current disc is not the same one from which file system was imported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED"></span><span id="imapi_e_import_media_not_allowed"></span><dl> <span data-ttu-id="e0759-446"><dt><strong>IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED</strong></dt> <dt>(HRESULT) 0xC0AAB159</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-446"><dt><strong>IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED</strong></dt> <dt>(HRESULT)0xC0AAB159</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-447">O IMAPi não permite várias sessões com o tipo de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="e0759-447">IMAPI does not allow multi-session with the current media type.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_UDF_NOT_WRITE_COMPATIBLE"></span><span id="imapi_e_udf_not_write_compatible"></span><dl> <span data-ttu-id="e0759-448"><dt><strong>IMAPI_E_UDF_NOT_WRITE_COMPATIBLE</strong></dt> <dt>(HRESULT) 0xC0AAB15A</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-448"><dt><strong>IMAPI_E_UDF_NOT_WRITE_COMPATIBLE</strong></dt> <dt>(HRESULT)0xC0AAB15A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-449">O IMAPi não pode fazer várias sessões com a mídia atual porque não dá suporte a uma revisão UDF compatível para gravação.</span><span class="sxs-lookup"><span data-stu-id="e0759-449">IMAPI cannot do multi-session with the current media because it does not support a compatible UDF revision for write.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE"></span><span id="imapi_e_incompatible_multisession_type"></span><dl> <span data-ttu-id="e0759-450"><dt><strong>IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE</strong></dt> <dt>(HRESULT) 0xC0AAB15B</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-450"><dt><strong>IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE</strong></dt> <dt>(HRESULT)0xC0AAB15B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-451">O IMAPi não oferece suporte ao tipo de várias sessões solicitado.</span><span class="sxs-lookup"><span data-stu-id="e0759-451">IMAPI does not support the multisession type requested.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION"></span><span id="imapi_e_incompatible_previous_session"></span><dl> <span data-ttu-id="e0759-452"><dt><strong>IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION</strong></dt> <dt>(HRESULT) 0xC0AAB133</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-452"><dt><strong>IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION</strong></dt> <dt>(HRESULT)0xC0AAB133</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-453">Falha na operação devido a um layout incompatível da sessão anterior importada da mídia.</span><span class="sxs-lookup"><span data-stu-id="e0759-453">Operation failed due to an incompatible layout of the previous session imported from the medium.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE"></span><span id="imapi_e_no_compatible_multisession_type"></span><dl> <span data-ttu-id="e0759-454"><dt><strong>IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE</strong></dt> <dt>(HRESULT) 0xC0AAB15C</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-454"><dt><strong>IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE</strong></dt> <dt>(HRESULT)0xC0AAB15C</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-455">O IMAPi não dá suporte a nenhum dos tipos de várias sessões fornecidos na mídia atual.</span><span class="sxs-lookup"><span data-stu-id="e0759-455">IMAPI supports none of the multisession type(s) provided on the current media.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e0759-456">[<strong>IFileSystemImage:: ImportFileSystem</strong>] o método (/Windows/Desktop/API/imapi2fs/NF-imapi2fs-ifilesystemimage-importfilesystem) retornará esse erro se não houver nenhuma mídia no dispositivo de gravação.</span><span class="sxs-lookup"><span data-stu-id="e0759-456">[<strong>IFileSystemImage::ImportFileSystem</strong>](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) method returns this error if there is no media in the recording device.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_MULTISESSION_NOT_SET"></span><span id="imapi_e_multisession_not_set"></span><dl> <span data-ttu-id="e0759-457"><dt><strong>IMAPI_E_MULTISESSION_NOT_SET</strong></dt> <dt>(HRESULT) 0xC0AAB15D</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-457"><dt><strong>IMAPI_E_MULTISESSION_NOT_SET</strong></dt> <dt>(HRESULT)0xC0AAB15D</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-458">A propriedade MultisessionInterfaces deve ser definida antes de chamar este método.</span><span class="sxs-lookup"><span data-stu-id="e0759-458">MultisessionInterfaces property must be set prior calling this method.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE"></span><span id="imapi_e_import_type_collision_directory_exists_as_file"></span><dl> <span data-ttu-id="e0759-459"><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE</strong></dt> <dt>(HRESULT) 0xC0AAB15E</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-459"><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE</strong></dt> <dt>(HRESULT)0xC0AAB15E</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-460">Não foi possível importar %2! ls!</span><span class="sxs-lookup"><span data-stu-id="e0759-460">Could not import %2!ls!</span></span> <span data-ttu-id="e0759-461">sistema de arquivos do disco. O diretório ' %1! ls! '</span><span class="sxs-lookup"><span data-stu-id="e0759-461">file system from disc. The directory '%1!ls!'</span></span> <span data-ttu-id="e0759-462">Já existe na hierarquia de imagens como um arquivo.</span><span class="sxs-lookup"><span data-stu-id="e0759-462">already exists within the image hierarchy as a file.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_BAD_MULTISESSION_PARAMETER"></span><span id="imapi_e_bad_multisession_parameter"></span><dl> <span data-ttu-id="e0759-463"><dt><strong>IMAPI_E_BAD_MULTISESSION_PARAMETER</strong></dt> <dt>(HRESULT) 0xC0AAB162</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-463"><dt><strong>IMAPI_E_BAD_MULTISESSION_PARAMETER</strong></dt> <dt>(HRESULT)0xC0AAB162</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-464">Um dos parâmetros de várias sessões não pode ser recuperado ou tem um valor incorreto.</span><span class="sxs-lookup"><span data-stu-id="e0759-464">One of multisession parameters cannot be retrieved or has a wrong value.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED"></span><span id="imapi_s_image_feature_not_supported"></span><dl> <span data-ttu-id="e0759-465"><dt><strong>IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0x00AAB15FL</dt> </span><span class="sxs-lookup"><span data-stu-id="e0759-465"><dt><strong>IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0x00AAB15FL</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e0759-466">Não há suporte para esse recurso na revisão atual do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="e0759-466">This feature is not supported for the current file system revision.</span></span> <span data-ttu-id="e0759-467">A imagem será criada sem esse recurso.</span><span class="sxs-lookup"><span data-stu-id="e0759-467">The image will be created without this feature.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="e0759-468">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0759-468">Requirements</span></span>



| <span data-ttu-id="e0759-469">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0759-469">Requirement</span></span> | <span data-ttu-id="e0759-470">Valor</span><span class="sxs-lookup"><span data-stu-id="e0759-470">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0759-471">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0759-471">Minimum supported client</span></span><br/> | <span data-ttu-id="e0759-472">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e0759-472">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="e0759-473">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0759-473">Minimum supported server</span></span><br/> | <span data-ttu-id="e0759-474">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e0759-474">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                            |
| <span data-ttu-id="e0759-475">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e0759-475">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0759-476"><dt>Imapi2error. h; </dt> <dt>Imapi2fserror. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0759-476"><dt>Imapi2error.h; </dt> <dt>Imapi2fserror.h</dt></span></span> </dl> |



 

 





