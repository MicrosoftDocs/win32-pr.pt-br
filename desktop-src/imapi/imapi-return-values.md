---
title: Valores de retorno de IMAPI (Imapi2error.h)
description: Os métodos IMAPI retornarão valores não negativos (normalmente S \_ OK) se o método tiver sido bem-sucedido. Os métodos IMAPI retornam códigos de erro ou êxito de Winerror.h, Imapi2error.h ou Imapi2fserror.h, em caso de falha.
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
ms.openlocfilehash: 857f9c018fc34a16a0dc431714aacc1fcdf6a5b1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474792"
---
# <a name="imapi-return-values"></a>Valores de retorno do IMAPI

Os métodos IMAPI retornarão valores não negativos (normalmente S \_ OK) se o método tiver sido bem-sucedido. Os métodos IMAPI retornam códigos de erro ou êxito de Winerror.h, Imapi2error.h ou Imapi2fserror.h, em caso de falha.

Os códigos de êxito e erro a seguir são definidos.




| Constante/valor | Descrição | 
|----------------|-------------|
| <span id="E_IMAPI_BURN_VERIFICATION_FAILED"></span><span id="e_imapi_burn_verification_failed"></span><dl><dt><strong>E_IMAPI_BURN_VERIFICATION_FAILED</strong></dt><dt>(HRESULT)0xC0AA0007L</dt></dl> | O disco não passou na verificação de gravar e pode conter dados corrompidos ou inutilizáveis.<br /> | 
| <span id="E_IMAPI_REQUEST_CANCELLED"></span><span id="e_imapi_request_cancelled"></span><dl><dt><strong>E_IMAPI_REQUEST_CANCELLED</strong></dt><dt>(HRESULT)0xC0AA0002</dt></dl> | A solicitação foi cancelada.<br /> | 
| <span id="E_IMAPI_RECORDER_REQUIRED"></span><span id="e_imapi_recorder_required"></span><dl><dt><strong>E_IMAPI_RECORDER_REQUIRED</strong></dt><dt>(HRESULT)0xC0AA0003</dt></dl> | A solicitação requer que um gravador de disco atual seja selecionado.<br /> | 
| <span id="S_IMAPI_WRITE_NOT_IN_PROGRESS"></span><span id="s_imapi_write_not_in_progress"></span><dl><dt><strong>S_IMAPI_WRITE_NOT_IN_PROGRESS</strong></dt><dt>(HRESULT)0x00AAA0302L</dt></dl> | Nenhuma operação de gravação está em andamento no momento.<br /> | 
| <span id="S_IMAPI_SPEEDADJUSTED"></span><span id="s_imapi_speedadjusted"></span><dl><dt><strong>S_IMAPI_SPEEDADJUSTED</strong></dt><dt>(HRESULT)0x00AA0004</dt></dl> | A velocidade de gravação solicitada não era suportada pela unidade e a velocidade foi ajustada.<br /> | 
| <span id="S_IMAPI_ROTATIONADJUSTED"></span><span id="s_imapi_rotationadjusted"></span><dl><dt><strong>S_IMAPI_ROTATIONADJUSTED</strong></dt><dt>(HRESULT)0x00AA0005</dt></dl> | O tipo de rotação solicitado não era suportado pela unidade e o tipo de rotação era ajustado.<br /> | 
| <span id="S_IMAPI_BOTHADJUSTED"></span><span id="s_imapi_bothadjusted"></span><dl><dt><strong>S_IMAPI_BOTHADJUSTED</strong></dt><dt>(HRESULT)0x00AA0006</dt></dl> | O tipo de rotação e a velocidade de gravação solicitados não eram suportados pela unidade e ambos foram ajustados.<br /> | 
| <span id="S_IMAPI_COMMAND_HAS_SENSE_DATA"></span><span id="s_imapi_command_has_sense_data"></span><dl><dt><strong>S_IMAPI_COMMAND_HAS_SENSE_DATA</strong></dt><dt>(HRESULT)0x00AA0200</dt></dl> | O dispositivo aceitou o comando, mas retornou dados de sentido, indicando um erro.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_IS_READ_ONLY"></span><span id="e_imapi_raw_image_is_read_only"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_IS_READ_ONLY</strong></dt><dt>(HRESULT)0x80AAA0A00L</dt></dl> | A imagem se tornou somente leitura devido a uma chamada para <a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-createresultimage"><strong>IRawCDImageCreator::CreateResultImage</strong></a>. Como resultado, o objeto não pode mais ser modificado.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS"></span><span id="e_imapi_raw_image_too_many_tracks"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS</strong></dt><dt>(HRESULT)0x80AAA0A01L</dt></dl> | Não é possível adicionar mais faixas. A mídia de CD é restrita a um intervalo de 1 a 99 faixas.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_NO_TRACKS"></span><span id="e_imapi_raw_image_no_tracks"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_NO_TRACKS</strong></dt><dt>(HRESULT)0x80AAA0A03L</dt></dl> | As faixas devem ser adicionadas à imagem antes de usar essa função.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED"></span><span id="e_imapi_raw_image_sector_type_not_supported"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0x80AAA0A02L</dt></dl> | Não há suporte para o tipo de setor solicitado.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED"></span><span id="e_imapi_raw_image_tracks_already_added"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED</strong></dt><dt>(HRESULT)0x80AAA0A04L</dt></dl> | As faixas não podem ser adicionadas à imagem antes do uso dessa função.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE"></span><span id="e_imapi_raw_image_insufficient_space"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE</strong></dt><dt>(HRESULT)0x80AAA0A05L</dt></dl> | Adicionar essa faixa excederia as limitações do início do leadout.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES"></span><span id="e_imapi_raw_image_too_many_track_indexes"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES</strong></dt><dt>(HRESULT)0x80AAA0A06L</dt></dl> | Adicionar essa faixa excederia o limite de 99 índices.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND"></span><span id="e_imapi_raw_image_track_index_not_found"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND</strong></dt><dt>(HRESULT)0x80AAA0A07L</dt></dl> | O deslocamento LBA especificado não está na lista de índices de faixa.<br /> | 
| <span id="S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS"></span><span id="s_imapi_raw_image_track_index_already_exists"></span><dl><dt><strong>S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS</strong></dt><dt>(HRESULT)0x00AAA0A08L</dt></dl> | O deslocamento LBA especificado já está na lista de índices de faixa.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED"></span><span id="e_imapi_raw_image_track_index_offset_zero_cannot_be_cleared"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED</strong></dt><dt>(HRESULT)0x80AAA0A09L</dt></dl> | O índice 1 (deslocamento LBA zero) não pode ser limpo.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX"></span><span id="e_imapi_raw_image_track_index_too_close_to_other_index"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX</strong></dt><dt>(HRESULT)0x80AAA0A0AL</dt></dl> | Cada índice deve ter um tamanho mínimo de dez setores.<br /> | 
| <span id="E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE"></span><span id="e_imapi_recorder_no_such_mode_page"></span><dl><dt><strong>E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE</strong></dt><dt>(HRESULT)0xC0AA0201</dt></dl> | O dispositivo relatou que a página de modo solicitado (e tipo) não está presente.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_NO_MEDIA"></span><span id="e_imapi_recorder_media_no_media"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_NO_MEDIA</strong></dt><dt>(HRESULT)0xC0AA0202</dt></dl> | Não há nenhuma mídia no dispositivo.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE"></span><span id="e_imapi_recorder_media_incompatible"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE</strong></dt><dt>(HRESULT)0xC0AA0203</dt></dl> | A mídia não é compatível ou de formato físico desconhecido.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN"></span><span id="e_imapi_recorder_media_upside_down"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN</strong></dt><dt>(HRESULT)0xC0AA0204</dt></dl> | A mídia é inserida de cabeça para baixo.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_BECOMING_READY"></span><span id="e_imapi_recorder_media_becoming_ready"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_BECOMING_READY</strong></dt><dt>(HRESULT)0xC0AA0205</dt></dl> | A unidade relatou que ela está no processo de se tornar pronta. Tente a solicitação novamente mais tarde.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS"></span><span id="e_imapi_recorder_media_format_in_progress"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS</strong></dt><dt>(HRESULT)0xC0AA0206</dt></dl> | A mídia está sendo formatada no momento. Aguarde até que o formato seja concluído antes de tentar usar a mídia.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_BUSY"></span><span id="e_imapi_recorder_media_busy"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_BUSY</strong></dt><dt>(HRESULT)0xC0AA0207</dt></dl> | A unidade relatou que está executando uma operação de execução longa, como concluir uma gravação. A unidade pode ficar inutilizável por um longo período de tempo.<br /> | 
| <span id="E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS"></span><span id="e_imapi_recorder_invalid_mode_parameters"></span><dl><dt><strong>E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS</strong></dt><dt>(HRESULT)0xC0AA0208</dt></dl> | A unidade relatou que não havia suporte para a combinação de parâmetros fornecidos na página de modo para um comando MODE SELECT.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED"></span><span id="e_imapi_recorder_media_write_protected"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED</strong></dt><dt>(HRESULT)0xC0AA0209</dt></dl> | A unidade relatou que a mídia está protegida por gravação.<br /> | 
| <span id="E_IMAPI_RECORDER_NO_SUCH_FEATURE"></span><span id="e_imapi_recorder_no_such_feature"></span><dl><dt><strong>E_IMAPI_RECORDER_NO_SUCH_FEATURE</strong></dt><dt>(HRESULT)0xC0AA020A</dt></dl> | Não há suporte para a página de recursos solicitada pelo dispositivo.<br /> | 
| <span id="E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT"></span><span id="e_imapi_recorder_feature_is_not_current"></span><dl><dt><strong>E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT</strong></dt><dt>(HRESULT)0xC0AA020B</dt></dl> | A página de recursos solicitada tem suporte, mas não está marcada como atual.<br /> | 
| <span id="E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED"></span><span id="e_imapi_recorder_get_configuration_not_supported"></span><dl><dt><strong>E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA020C</dt></dl> | A unidade não dá suporte ao comando GET CONFIGURATION.<br /> | 
| <span id="E_IMAPI_RECORDER_COMMAND_TIMEOUT"></span><span id="e_imapi_recorder_command_timeout"></span><dl><dt><strong>E_IMAPI_RECORDER_COMMAND_TIMEOUT</strong></dt><dt>(HRESULT)0xC0AA020D</dt></dl> | O dispositivo não aceitou o comando dentro do período de tempo de tempo. Isso pode ser causado pelo dispositivo ter entrado em um estado inconsistente ou o valor de tempo-final do comando pode precisar ser aumentado.<br /> | 
| <span id="E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT"></span><span id="e_imapi_recorder_dvd_structure_not_present"></span><dl><dt><strong>E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT</strong></dt><dt>(HRESULT)0xC0AA020E</dt></dl> | A estrutura de DVD não está presente. Isso pode ser causado por unidade/média incompatível usada.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH"></span><span id="e_imapi_recorder_media_speed_mismatch"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH</strong></dt><dt>(HRESULT)0xC0AA020F</dt></dl> | A velocidade da mídia é incompatível com o dispositivo. Isso pode ser causado pelo uso de mídia de velocidade mais alta ou menor do que o intervalo de velocidades com suporte pelo dispositivo.<br /> | 
| <span id="E_IMAPI_RECORDER_LOCKED"></span><span id="e_imapi_recorder_locked"></span><dl><dt><strong>E_IMAPI_RECORDER_LOCKED</strong></dt><dt>(HRESULT)0xC0AA0210</dt></dl> | O dispositivo associado a esse gravador durante a última operação foi bloqueado exclusivamente, fazendo com que essa operação falhe.<br /> | 
| <span id="E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_recorder_client_name_is_not_valid"></span><dl><dt><strong>E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID</strong></dt><dt>(HRESULT)0xC0AA0211</dt></dl> | O nome do cliente não é válido.<br /> | 
| <span id="E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE"></span><span id="e_imapi_recorder_invalid_response_from_device"></span><dl><dt><strong>E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE</strong></dt><dt>(HRESULT)0xC0AA02FF</dt></dl> | O dispositivo relatou dados inesperados ou inválidos para um comando.<br /> | 
| <span id="E_IMAPI_LOSS_OF_STREAMING"></span><span id="e_imapi_loss_of_streaming"></span><dl><dt><strong>E_IMAPI_LOSS_OF_STREAMING</strong></dt><dt>(HRESULT)0xC0AA0300</dt></dl> | A gravação falhou porque a unidade não recebeu dados rapidamente o suficiente para continuar a gravação. Mover os dados de origem para o computador local, reduzindo a velocidade de gravação ou habilitando uma configuração de "buffer sem buffer livre" pode resolver esse problema.<br /> | 
| <span id="E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE"></span><span id="e_imapi_unexpected_response_from_device"></span><dl><dt><strong>E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE</strong></dt><dt>(HRESULT)0xC0AA0301</dt></dl> | A gravação falhou porque a unidade retornou informações de erro das que não puderam ser recuperadas.<br /> | 
| <span id="E_IMAPI_DF2DATA_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2data_write_in_progress"></span><dl><dt><strong>E_IMAPI_DF2DATA_WRITE_IN_PROGRESS</strong></dt><dt>(HRESULT)0xC0AA0400</dt></dl> | Atualmente, há uma operação de gravação em andamento.<br /> | 
| <span id="E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2data_write_not_in_progress"></span><dl><dt><strong>E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS</strong></dt><dt>(HRESULT)0xC0AA0401</dt></dl> | Não há nenhuma operação de gravação em andamento no momento.<br /> | 
| <span id="E_IMAPI_DF2DATA_INVALID_MEDIA_STATE"></span><span id="e_imapi_df2data_invalid_media_state"></span><dl><dt><strong>E_IMAPI_DF2DATA_INVALID_MEDIA_STATE</strong></dt><dt>(HRESULT) 0xC0AA0402</dt></dl> | A operação solicitada só é válida com mídia com suporte.<br /> | 
| <span id="E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2data_stream_not_supported"></span><dl><dt><strong>E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AA0403</dt></dl> | Não há suporte para o fluxo fornecido para gravação.<br /> | 
| <span id="E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA"></span><span id="e_imapi_df2data_stream_too_large_for_current_media"></span><dl><dt><strong>E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA</strong></dt><dt>(HRESULT) 0xC0AA0404</dt></dl> | O fluxo fornecido para gravação é muito grande para a mídia inserida no momento.<br /> | 
| <span id="E_IMAPI_DF2DATA_MEDIA_NOT_BLANK"></span><span id="e_imapi_df2data_media_not_blank"></span><dl><dt><strong>E_IMAPI_DF2DATA_MEDIA_NOT_BLANK</strong></dt><dt>(HRESULT) 0xC0AA0405</dt></dl> | A substituição de mídias não em branco não é permitida sem a propriedade ForceOverwrite definida como VARIANT_TRUE.<br /> | 
| <span id="E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2data_media_is_not_supported"></span><dl><dt><strong>E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AA0406</dt></dl> | Não há suporte para o tipo de mídia atual.<br /> | 
| <span id="E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2data_recorder_not_supported"></span><dl><dt><strong>E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AA0407</dt></dl> | Este dispositivo não oferece suporte às operações exigidas por este formato de disco.<br /> | 
| <span id="E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2data_client_name_is_not_valid"></span><dl><dt><strong>E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID</strong></dt><dt>(HRESULT) 0xC0AA0408</dt></dl> | O nome do cliente não é válido.<br /> | 
| <span id="E_IMAPI_DF2TAO_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2tao_write_in_progress"></span><dl><dt><strong>E_IMAPI_DF2TAO_WRITE_IN_PROGRESS</strong></dt><dt>(HRESULT) 0xC0AA0500</dt></dl> | Atualmente, há uma operação de gravação em andamento.<br /> | 
| <span id="E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2tao_write_not_in_progress"></span><dl><dt><strong>E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS</strong></dt><dt>(HRESULT) 0xC0AA0501</dt></dl> | Não há nenhuma operação de gravação em andamento no momento.<br /> | 
| <span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED"></span><span id="e_imapi_df2tao_media_is_not_prepared"></span><dl><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED</strong></dt><dt>(HRESULT) 0xC0AA0502</dt></dl> | A operação solicitada só será válida quando a mídia tiver sido "preparada".<br /> | 
| <span id="E_IMAPI_DF2TAO_MEDIA_IS_PREPARED"></span><span id="e_imapi_df2tao_media_is_prepared"></span><dl><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_PREPARED</strong></dt><dt>(HRESULT) 0xC0AA0503</dt></dl> | A operação solicitada não é válida quando a mídia foi "preparada", mas não foi liberada.<br /> | 
| <span id="E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY"></span><span id="e_imapi_df2tao_property_for_blank_media_only"></span><dl><dt><strong>E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY</strong></dt><dt>(HRESULT) 0xC0AA0504</dt></dl> | A propriedade não pode ser alterada depois que a mídia tiver sido gravada.<br /> | 
| <span id="E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC"></span><span id="e_imapi_df2tao_table_of_contents_empty_disc"></span><dl><dt><strong>E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC</strong></dt><dt>(HRESULT) 0xC0AA0505</dt></dl> | O Sumário não pode ser recuperado de um disco vazio.<br /> | 
| <span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK"></span><span id="e_imapi_df2tao_media_is_not_blank"></span><dl><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK</strong></dt><dt>(HRESULT) 0xC0AA0506</dt></dl> | Há suporte apenas para mídia de CD-R/RW em branco.<br /> | 
| <span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_media_is_not_supported"></span><dl><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AA0507</dt></dl> | Há suporte apenas para mídia de CD-R/RW em branco.<br /> | 
| <span id="E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED"></span><span id="e_imapi_df2tao_track_limit_reached"></span><dl><dt><strong>E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED</strong></dt><dt>(HRESULT) 0xC0AA0508</dt></dl> | As mídias CD-R e CD-RW dão suporte a um máximo de 99 faixas de áudio.<br /> | 
| <span id="E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE"></span><span id="e_imapi_df2tao_not_enough_space"></span><dl><dt><strong>E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE</strong></dt><dt>(HRESULT) 0xC0AA0509</dt></dl> | Não há espaço suficiente restante na mídia para adicionar a faixa de áudio fornecida.<br /> | 
| <span id="E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED"></span><span id="e_imapi_df2tao_no_recorder_specified"></span><dl><dt><strong>E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED</strong></dt><dt>(HRESULT) 0xC0AA050A</dt></dl> | Você não pode preparar a mídia até escolher um gravador para usar.<br /> | 
| <span id="E_IMAPI_DF2TAO_INVALID_ISRC"></span><span id="e_imapi_df2tao_invalid_isrc"></span><dl><dt><strong>E_IMAPI_DF2TAO_INVALID_ISRC</strong></dt><dt>(HRESULT) 0xC0AA050B</dt></dl> | O ISRC fornecido não é válido.<br /> | 
| <span id="E_IMAPI_DF2TAO_INVALID_MCN"></span><span id="e_imapi_df2tao_invalid_mcn"></span><dl><dt><strong>E_IMAPI_DF2TAO_INVALID_MCN</strong></dt><dt>(HRESULT) 0xC0AA050C</dt></dl> | O número de catálogo de mídia fornecido não é válido.<br /> | 
| <span id="E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_stream_not_supported"></span><dl><dt><strong>E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AA050D</dt></dl> | O fluxo de áudio fornecido não é válido.<br /> | 
| <span id="E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_recorder_not_supported"></span><dl><dt><strong>E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AA050E</dt></dl> | Este dispositivo não oferece suporte às operações exigidas por este formato de disco.<br /> | 
| <span id="E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2tao_client_name_is_not_valid"></span><dl><dt><strong>E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID</strong></dt><dt>(HRESULT) 0xC0AA050F</dt></dl> | O nome do cliente não é válido.<br /> | 
| <span id="E_IMAPI_DF2RAW_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2raw_write_in_progress"></span><dl><dt><strong>E_IMAPI_DF2RAW_WRITE_IN_PROGRESS</strong></dt><dt>(HRESULT) 0xC0AA0600</dt></dl> | Atualmente, há uma operação de gravação em andamento.<br /> | 
| <span id="E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2raw_write_not_in_progress"></span><dl><dt><strong>E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS</strong></dt><dt>(HRESULT) 0xC0AA0601</dt></dl> | Não há nenhuma operação de gravação em andamento no momento.<br /> | 
| <span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED"></span><span id="e_imapi_df2raw_media_is_not_prepared"></span><dl><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED</strong></dt><dt>(HRESULT) 0xC0AA0602</dt></dl> | A operação solicitada só será válida quando a mídia tiver sido "preparada".<br /> | 
| <span id="E_IMAPI_DF2RAW_MEDIA_IS_PREPARED"></span><span id="e_imapi_df2raw_media_is_prepared"></span><dl><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_PREPARED</strong></dt><dt>(HRESULT) 0xC0AA0603</dt></dl> | A operação solicitada não é válida quando a mídia foi "preparada", mas não foi liberada.<br /> | 
| <span id="E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2raw_client_name_is_not_valid"></span><dl><dt><strong>E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID</strong></dt><dt>(HRESULT) 0xC0AA0604</dt></dl> | O nome do cliente não é válido.<br /> | 
| <span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK"></span><span id="e_imapi_df2raw_media_is_not_blank"></span><dl><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK</strong></dt><dt>(HRESULT) 0xC0AA0606</dt></dl> | Há suporte apenas para mídia de CD-R/RW em branco.<br /> | 
| <span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_media_is_not_supported"></span><dl><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AA0607</dt></dl> | Há suporte apenas para mídia de CD-R/RW em branco.<br /> | 
| <span id="E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE"></span><span id="e_imapi_df2raw_not_enough_space"></span><dl><dt><strong>E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE</strong></dt><dt>(HRESULT) 0xC0AA0609</dt></dl> | Não há espaço suficiente na mídia para adicionar a sessão fornecida.<br /> | 
| <span id="E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED"></span><span id="e_imapi_df2raw_no_recorder_specified"></span><dl><dt><strong>E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED</strong></dt><dt>(HRESULT) 0xC0AA060A</dt></dl> | Você não pode preparar a mídia até escolher um gravador para usar.<br /> | 
| <span id="E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_stream_not_supported"></span><dl><dt><strong>E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AA060D</dt></dl> | O fluxo de áudio fornecido não é válido.<br /> | 
| <span id="E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_data_block_type_not_supported"></span><dl><dt><strong>E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AA060E</dt></dl> | O tipo de bloco de dados solicitado não é suportado pelo dispositivo atual.<br /> | 
| <span id="E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT"></span><span id="e_imapi_df2raw_stream_leadin_too_short"></span><dl><dt><strong>E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT</strong></dt><dt>(HRESULT) 0xC0AA060F</dt></dl> | O fluxo não contém um número suficiente de setores na liderança para a mídia atual.<br /> | 
| <span id="E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_recorder_not_supported"></span><dl><dt><strong>E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AA0610</dt></dl> | Este dispositivo não oferece suporte às operações exigidas por este formato de disco.<br /> | 
| <span id="E_IMAPI_ERASE_RECORDER_IN_USE"></span><span id="e_imapi_erase_recorder_in_use"></span><dl><dt><strong>E_IMAPI_ERASE_RECORDER_IN_USE</strong></dt><dt>(HRESULT) 0x80AA0900</dt></dl> | No momento, o formato está usando o gravador de disco para uma operação de apagamento. Aguarde até que o apagamento seja concluído antes de tentar definir ou limpar o gravador de disco atual.<br /> | 
| <span id="E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED"></span><span id="e_imapi_erase_only_one_recorder_supported"></span><dl><dt><strong>E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED</strong></dt><dt>(HRESULT) 0x80AA0901</dt></dl> | O formato de apagamento só dá suporte a um gravador. Você deve limpar o gravador atual antes de definir um novo.<br /> | 
| <span id="E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL"></span><span id="e_imapi_erase_disc_information_too_small"></span><dl><dt><strong>E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL</strong></dt><dt>(HRESULT) 0x80AA0902</dt></dl> | A unidade não relate dados suficientes para um comando ler informações do disco. A unidade pode não ter suporte ou a mídia pode não estar correta.<br /> | 
| <span id="E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL"></span><span id="e_imapi_erase_mode_page_2a_too_small"></span><dl><dt><strong>E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL</strong></dt><dt>(HRESULT) 0x80AA0903</dt></dl> | A unidade não relate dados suficientes para um comando MODE SENSE (Page 0x2A). A unidade pode não ter suporte ou a mídia pode não estar correta.<br /> | 
| <span id="E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE"></span><span id="e_imapi_erase_media_is_not_erasable"></span><dl><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE</strong></dt><dt>(HRESULT) 0x80AA0904</dt></dl> | A unidade relatou que a mídia não é apagável.<br /> | 
| <span id="E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND"></span><span id="e_imapi_erase_drive_failed_erase_command"></span><dl><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND</strong></dt><dt>(HRESULT) 0x80AA0905</dt></dl> | Falha do comando de apagamento na unidade.<br /> | 
| <span id="E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR"></span><span id="e_imapi_erase_took_longer_than_one_hour"></span><dl><dt><strong>E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR</strong></dt><dt>(HRESULT) 0x80AA0906</dt></dl> | A unidade não concluiu o apagamento em uma hora. A unidade pode exigir um ciclo de energia, remoção de mídia ou outra intervenção manual para retomar a operação adequada.<br /><blockquote>[!Note]<br />Atualmente, esse valor também será retornado se uma tentativa de executar um apagamento em mídia de CD-RW ou DVD-RW por meio da interface <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a> falhar como resultado da mídia estar inadequada.</blockquote><br /> | 
| <span id="E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE"></span><span id="e_imapi_erase_unexpected_drive_response_during_erase"></span><dl><dt><strong>E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE</strong></dt><dt>(HRESULT) 0x80AA0907</dt></dl> | A unidade retornou um erro inesperado durante o apagamento. A mídia pode ser inutilizável, o apagamento pode estar concluído ou a unidade ainda pode estar no processo de apagamento do disco.<br /> | 
| <span id="E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND"></span><span id="e_imapi_erase_drive_failed_spinup_command"></span><dl><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND</strong></dt><dt>(HRESULT) 0x80AA0908</dt></dl> | A unidade retornou um erro para um comando de unidade inicial (SPINUP). A intervenção manual pode ser necessária.<br /> | 
| <span id="E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_erase_media_is_not_supported"></span><dl><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AA0909</dt></dl> | Não há suporte para o tipo de mídia atual.<br /> | 
| <span id="E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_erase_recorder_not_supported"></span><dl><dt><strong>E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA090A</dt></dl> | Esse dispositivo não dá suporte às operações exigidas por esse formato de disco.<br /> | 
| <span id="E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_erase_client_name_is_not_valid"></span><dl><dt><strong>E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID</strong></dt><dt>(HRESULT)0xC0AA090B</dt></dl> | O nome do cliente não é válido.<br /> | 




Os códigos de êxito e erro a seguir são definidos em Imapi2fserror.h.




| Constante/valor | Descrição | 
|----------------|-------------|
| <span id="IMAPI_E_FSI_INTERNAL_ERROR"></span><span id="imapi_e_fsi_internal_error"></span><dl><dt><strong>IMAPI_E_FSI_INTERNAL_ERROR</strong></dt><dt>(HRESULT)0xC0AAB100</dt></dl> | Erro interno: %1!ls!.<br /> | 
| <span id="IMAPI_E_INVALID_PARAM"></span><span id="imapi_e_invalid_param"></span><dl><dt><strong>IMAPI_E_INVALID_PARAM</strong></dt><dt>(HRESULT)0xC0AAB101</dt></dl> | O valor especificado para o parâmetro '%1!ls!' não é válido.<br /> | 
| <span id="IMAPI_E_READONLY"></span><span id="imapi_e_readonly"></span><dl><dt><strong>IMAPI_E_READONLY</strong></dt><dt>(HRESULT)0xC0AAB102</dt></dl> | O objeto FileSystemImage está no modo somente leitura.<br /> | 
| <span id="IMAPI_E_NO_OUTPUT"></span><span id="imapi_e_no_output"></span><dl><dt><strong>IMAPI_E_NO_OUTPUT</strong></dt><dt>(HRESULT)0xC0AAB103</dt></dl> | Nenhum sistema de arquivos de saída especificado.<br /> | 
| <span id="IMAPI_E_INVALID_VOLUME_NAME"></span><span id="imapi_e_invalid_volume_name"></span><dl><dt><strong>IMAPI_E_INVALID_VOLUME_NAME</strong></dt><dt>(HRESULT)0xC0AAB104</dt></dl> | O Identificador de Volume especificado é muito longo ou contém um ou mais caracteres inválidos.<br /> | 
| <span id="IMAPI_E_INVALID_DATE"></span><span id="imapi_e_invalid_date"></span><dl><dt><strong>IMAPI_E_INVALID_DATE</strong></dt><dt>(HRESULT)0xC0AAB105</dt></dl> | Datas de arquivo inválidas. %1!ls! time é anterior a %2!ls! tempo.<br /> | 
| <span id="IMAPI_E_FILE_SYSTEM_NOT_EMPTY"></span><span id="imapi_e_file_system_not_empty"></span><dl><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_EMPTY</strong></dt><dt>(HRESULT)0xC0AAB106</dt></dl> | O sistema de arquivos deve estar vazio para essa função.<br /> | 
| <span id="IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED"></span><span id="imapi_e_file_system_change_not_allowed"></span><dl><dt><strong>IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED</strong></dt><dt>(HRESULT)0xC0AAB163L</dt></dl> | Não é possível alterar o sistema de arquivos especificado para criação, pois o sistema de arquivos da sessão importada e o sistema de arquivos na sessão atual não são corresponderem.<br /> | 
| <span id="IMAPI_E_NOT_FILE"></span><span id="imapi_e_not_file"></span><dl><dt><strong>IMAPI_E_NOT_FILE</strong></dt><dt>(HRESULT)0xC0AAB108</dt></dl> | Caminho especificado '%1!ls!' não identifica um arquivo.<br /> | 
| <span id="IMAPI_E_NOT_DIR"></span><span id="imapi_e_not_dir"></span><dl><dt><strong>IMAPI_E_NOT_DIR</strong></dt><dt>(HRESULT)0xC0AAB109</dt></dl> | Caminho especificado '%1!ls!' não identifica um diretório.<br /> | 
| <span id="IMAPI_E_DIR_NOT_EMPTY"></span><span id="imapi_e_dir_not_empty"></span><dl><dt><strong>IMAPI_E_DIR_NOT_EMPTY</strong></dt><dt>(HRESULT)0xC0AAB10A</dt></dl> | O diretório '%1!s!' não está vazio.<br /> | 
| <span id="IMAPI_E_NOT_IN_FILE_SYSTEM"></span><span id="imapi_e_not_in_file_system"></span><dl><dt><strong>IMAPI_E_NOT_IN_FILE_SYSTEM</strong></dt><dt>(HRESULT)0xC0AAB10B</dt></dl> | ls!' não faz parte do sistema de arquivos. Ele deve ser adicionado para concluir essa operação.<br /> | 
| <span id="IMAPI_E_INVALID_PATH"></span><span id="imapi_e_invalid_path"></span><dl><dt><strong>IMAPI_E_INVALID_PATH</strong></dt><dt>(HRESULT)0xC0AAB110</dt></dl> | Caminho '%1!s!' está mal formado ou contém caracteres inválidos.<br /> | 
| <span id="IMAPI_E_RESTRICTED_NAME_VIOLATION"></span><span id="imapi_e_restricted_name_violation"></span><dl><dt><strong>IMAPI_E_RESTRICTED_NAME_VIOLATION</strong></dt><dt>(HRESULT)0xC0AAB111</dt></dl> | O nome '%1!ls!' especificado não é legal: o nome do objeto de arquivo ou diretório criado enquanto a propriedade UseRestrictedCharacterSet está definida pode conter apenas caracteres ANSI.<br /> | 
| <span id="IMAPI_E_DUP_NAME"></span><span id="imapi_e_dup_name"></span><dl><dt><strong>IMAPI_E_DUP_NAME</strong></dt><dt>(HRESULT)0xC0AAB112</dt></dl> | ls!' name já existe.<br /> | 
| <span id="IMAPI_E_NO_UNIQUE_NAME"></span><span id="imapi_e_no_unique_name"></span><dl><dt><strong>IMAPI_E_NO_UNIQUE_NAME</strong></dt><dt>(HRESULT)0xC0AAB113</dt></dl> | Tentativa de adicionar '%1!ls!' failed: não é possível criar um nome exclusivo específico do sistema de arquivos para %2!ls! .<br /> | 
| <span id="IMAPI_E_ITEM_NOT_FOUND"></span><span id="imapi_e_item_not_found"></span><dl><dt><strong>IMAPI_E_ITEM_NOT_FOUND</strong></dt><dt>(HRESULT)0xC0AAB118</dt></dl> | Não é possível encontrar o item '%1!ls!' na hierarquia FileSystemImage.<br /> | 
| <span id="IMAPI_E_FILE_NOT_FOUND"></span><span id="imapi_e_file_not_found"></span><dl><dt><strong>IMAPI_E_FILE_NOT_FOUND</strong></dt><dt>(HRESULT)0xC0AAB119</dt></dl> | O arquivo '%1!s!' não encontrado na hierarquia FileSystemImage.<br /> | 
| <span id="IMAPI_E_DIR_NOT_FOUND"></span><span id="imapi_e_dir_not_found"></span><dl><dt><strong>IMAPI_E_DIR_NOT_FOUND</strong></dt><dt>(HRESULT)0xC0AAB11A</dt></dl> | O diretório '%1!s!' não encontrado na hierarquia FileSystemImage.<br /> | 
| <span id="IMAPI_E_IMAGE_SIZE_LIMIT"></span><span id="imapi_e_image_size_limit"></span><dl><dt><strong>IMAPI_E_IMAGE_SIZE_LIMIT</strong></dt><dt>(HRESULT)0xC0AAB120</dt></dl> | Adicionando '%1!ls!' resultaria em uma imagem de resultado com um tamanho maior que o limite configurado atual.<br /> | 
| <span id="IMAPI_E_IMAGE_TOO_BIG"></span><span id="imapi_e_image_too_big"></span><dl><dt><strong>IMAPI_E_IMAGE_TOO_BIG</strong></dt><dt>(HRESULT)0xC0AAB121</dt></dl> | O valor especificado para a propriedade FreeMediaBlocks é muito pequeno para o tamanho estimado da imagem com base nos dados atuais. <br /> | 
| <span id="IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED"></span><span id="imapi_e_imagemanager_image_not_aligned"></span><dl><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED</strong></dt><dt>(HRESULT)0xC0AAB200L</dt></dl> | A imagem não está alinhada em um limite de setor de 2kb.<br /> | 
| <span id="IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND"></span><span id="imapi_e_imagemanager_no_valid_vd_found"></span><dl><dt><strong>IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND</strong></dt><dt>(HRESULT)0xC0AAB201L)</dt></dl> | A imagem não contém um descritor de volume válido.<br /> | 
| <span id="IMAPI_E_IMAGEMANAGER_NO_IMAGE"></span><span id="imapi_e_imagemanager_no_image"></span><dl><dt><strong>IMAPI_E_IMAGEMANAGER_NO_IMAGE</strong></dt><dt>(HRESULT)0xC0AAB202L</dt></dl> | A imagem não foi definida usando os métodos <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setpath"><strong>IIsoImageManager::SetPath</strong></a> ou <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setstream"><strong>IIsoImageManager::SetStream</strong></a> antes de chamar o método <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-validate"><strong>IIsoImageManager::Validate.</strong></a><br /> | 
| <span id="IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG"></span><span id="imapi_e_imagemanager_image_too_big"></span><dl><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG</strong></dt><dt>(HRESULT)0xC0AAB203L</dt></dl> | A imagem fornecida é muito grande para ser validada, pois o tamanho excede <strong>MAXLONG.</strong><br /> | 
| <span id="IMAPI_E_DATA_STREAM_INCONSISTENCY"></span><span id="imapi_e_data_stream_inconsistency"></span><dl><dt><strong>IMAPI_E_DATA_STREAM_INCONSISTENCY</strong></dt><dt>(HRESULT)0xC0AAB128</dt></dl> | Fluxo de dados fornecido para o arquivo '%1!ls!' está inconsistente: %2 esperado! I64d! bytes, encontrado %3! I64d!. <br /> | 
| <span id="IMAPI_E_DATA_STREAM_READ_FAILURE"></span><span id="imapi_e_data_stream_read_failure"></span><dl><dt><strong>IMAPI_E_DATA_STREAM_READ_FAILURE</strong></dt><dt>(HRESULT)0xC0AAB129</dt></dl> | Não é possível ler dados do fluxo fornecido para o arquivo '%1!ls!'.<br /> | 
| <span id="IMAPI_E_DATA_STREAM_CREATE_FAILURE"></span><span id="imapi_e_data_stream_create_failure"></span><dl><dt><strong>IMAPI_E_DATA_STREAM_CREATE_FAILURE</strong></dt><dt>(HRESULT)0xC0AAB12A</dt></dl> | O erro a seguir foi encontrado ao tentar criar um fluxo de dados para o arquivo '%1!ls!': <br /> | 
| <span id="IMAPI_E_DIRECTORY_READ_FAILURE"></span><span id="imapi_e_directory_read_failure"></span><dl><dt><strong>IMAPI_E_DIRECTORY_READ_FAILURE</strong></dt><dt>(HRESULT)0xC0AAB12BL</dt></dl> | Falha ao enumerar arquivos na árvore de diretórios está inacessível devido a permissões.<br /> | 
| <span id="IMAPI_E_TOO_MANY_DIRS"></span><span id="imapi_e_too_many_dirs"></span><dl><dt><strong>IMAPI_E_TOO_MANY_DIRS</strong></dt><dt>(HRESULT)0xC0AAB130</dt></dl> | Essa imagem do sistema de arquivos tem muitos diretórios para %1!ls! .<br /> | 
| <span id="IMAPI_E_ISO9660_LEVELS"></span><span id="imapi_e_iso9660_levels"></span><dl><dt><strong>IMAPI_E_ISO9660_LEVELS</strong></dt><dt>(HRESULT)0xC0AAB131</dt></dl> | ISO9660 é limitado a 8 níveis de diretórios.<br /> | 
| <span id="IMAPI_E_DATA_TOO_BIG"></span><span id="imapi_e_data_too_big"></span><dl><dt><strong>IMAPI_E_DATA_TOO_BIG</strong></dt><dt>(HRESULT)0xC0AAB132</dt></dl> | O arquivo de dados é muito grande para '%1!ls!' .<br /> | 
| <span id="IMAPI_E_STASHFILE_OPEN_FAILURE"></span><span id="imapi_e_stashfile_open_failure"></span><dl><dt><strong>IMAPI_E_STASHFILE_OPEN_FAILURE</strong></dt><dt>(HRESULT)0xC0AAB138</dt></dl> | Não é possível inicializar %1!ls! arquivo de stash.<br /> | 
| <span id="IMAPI_E_STASHFILE_SEEK_FAILURE"></span><span id="imapi_e_stashfile_seek_failure"></span><dl><dt><strong>IMAPI_E_STASHFILE_SEEK_FAILURE</strong></dt><dt>(HRESULT)0xC0AAB139</dt></dl> | Erro ao procurar '%1!ls!' arquivo de stash.<br /> | 
| <span id="IMAPI_E_STASHFILE_WRITE_FAILURE"></span><span id="imapi_e_stashfile_write_failure"></span><dl><dt><strong>IMAPI_E_STASHFILE_WRITE_FAILURE</strong></dt><dt>(HRESULT)0xC0AAB13A</dt></dl> | Erro encontrado ao gravar em ' %1! ls! ' arquivo stash.<br /> | 
| <span id="IMAPI_E_STASHFILE_READ_FAILURE"></span><span id="imapi_e_stashfile_read_failure"></span><dl><dt><strong>IMAPI_E_STASHFILE_READ_FAILURE</strong></dt><dt>(HRESULT) 0xC0AAB13B</dt></dl> | Erro encontrado ao ler de ' %1! ls! ' arquivo stash.<br /> | 
| <span id="IMAPI_E_INVALID_WORKING_DIRECTORY"></span><span id="imapi_e_invalid_working_directory"></span><dl><dt><strong>IMAPI_E_INVALID_WORKING_DIRECTORY</strong></dt><dt>(HRESULT) 0xC0AAB140</dt></dl> | O diretório de trabalho ' %1! ls! ' não é válido.<br /> | 
| <span id="IMAPI_E_WORKING_DIRECTORY_SPACE"></span><span id="imapi_e_working_directory_space"></span><dl><dt><strong>IMAPI_E_WORKING_DIRECTORY_SPACE</strong></dt><dt>(HRESULT) 0xC0AAB141</dt></dl> | Não é possível definir o diretório de trabalho como ' %1! ls! '. O espaço disponível é %2! I64d! bytes, aproximadamente %3! I64d! bytes necessários. <br /> | 
| <span id="IMAPI_E_STASHFILE_MOVE"></span><span id="imapi_e_stashfile_move"></span><dl><dt><strong>IMAPI_E_STASHFILE_MOVE</strong></dt><dt>(HRESULT) 0xC0AAB142</dt></dl> | Tentativa de mover o arquivo stash de dados para o diretório ' %1! ls! ' Não foi bem-sucedido.<br /> | 
| <span id="IMAPI_E_BOOT_IMAGE_DATA"></span><span id="imapi_e_boot_image_data"></span><dl><dt><strong>IMAPI_E_BOOT_IMAGE_DATA</strong></dt><dt>(HRESULT) 0xC0AAB148</dt></dl> | Não foi possível adicionar o objeto de inicialização à imagem.<br /> | 
| <span id="IMAPI_E_BOOT_OBJECT_CONFLICT"></span><span id="imapi_e_boot_object_conflict"></span><dl><dt><strong>IMAPI_E_BOOT_OBJECT_CONFLICT</strong></dt><dt>(HRESULT) 0xC0AAB149</dt></dl> | Um objeto de inicialização só pode ser incluído em uma imagem de disco inicial.<br /> | 
| <span id="IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH"></span><span id="imapi_e_boot_emulation_image_size_mismatch"></span><dl><dt><strong>IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH</strong></dt><dt>(HRESULT) 0xC0AAB14A</dt></dl> | O tipo de emulação solicitado não corresponde ao tamanho da imagem de inicialização.<br /> | 
| <span id="IMAPI_E_EMPTY_DISC"></span><span id="imapi_e_empty_disc"></span><dl><dt><strong>IMAPI_E_EMPTY_DISC</strong></dt><dt>(HRESULT) 0xC0AAB150</dt></dl> | A mídia óptica está vazia.<br /> | 
| <span id="IMAPI_E_NO_SUPPORTED_FILE_SYSTEM"></span><span id="imapi_e_no_supported_file_system"></span><dl><dt><strong>IMAPI_E_NO_SUPPORTED_FILE_SYSTEM</strong></dt><dt>(HRESULT) 0xC0AAB151</dt></dl> | O disco especificado não contém um dos sistemas de arquivos com suporte.<br /> | 
| <span id="IMAPI_E_FILE_SYSTEM_NOT_FOUND"></span><span id="imapi_e_file_system_not_found"></span><dl><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_FOUND</strong></dt><dt>(HRESULT) 0xC0AAB152</dt></dl> | O disco especificado não contém um ' %1! ls! ' .<br /> | 
| <span id="IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR"></span><span id="imapi_e_file_system_read_consistency_error"></span><dl><dt><strong>IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR</strong></dt><dt>(HRESULT) 0xC0AAB153</dt></dl> | Erro de consistência encontrado ao importar o ' %1! ls! ' .<br /> | 
| <span id="IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED"></span><span id="imapi_e_file_system_feature_not_supported"></span><dl><dt><strong>IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AAB154</dt></dl> | O ' %1! ls! ' o sistema de arquivos no disco selecionado contém um recurso sem suporte para importação: %2! ls!.<br /> | 
| <span id="IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY"></span><span id="imapi_e_import_type_collision_file_exists_as_directory"></span><dl><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY</strong></dt><dt>(HRESULT) 0xC0AAB155</dt></dl> | Não foi possível importar %2! ls! sistema de arquivos do disco. O arquivo ' %1! ls! ' Já existe na hierarquia de imagens como um diretório.<br /> | 
| <span id="IMAPI_E_IMPORT_SEEK_FAILURE"></span><span id="imapi_e_import_seek_failure"></span><dl><dt><strong>IMAPI_E_IMPORT_SEEK_FAILURE</strong></dt><dt>(HRESULT) 0xC0AAB156</dt></dl> | Não é possível buscar no bloco %1! I64d! no disco de origem. <br /> | 
| <span id="IMAPI_E_IMPORT_READ_FAILURE"></span><span id="imapi_e_import_read_failure"></span><dl><dt><strong>IMAPI_E_IMPORT_READ_FAILURE</strong></dt><dt>(HRESULT) 0xC0AAB157</dt></dl> | Falha na importação da sessão anterior devido a um erro ao ler um bloco na mídia (bloco mais provável %1! u!).<br /> | 
| <span id="IMAPI_E_DISC_MISMATCH"></span><span id="imapi_e_disc_mismatch"></span><dl><dt><strong>IMAPI_E_DISC_MISMATCH</strong></dt><dt>(HRESULT) 0xC0AAB158</dt></dl> | O disco atual não é o mesmo do qual o sistema de arquivos foi importado.<br /> | 
| <span id="IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED"></span><span id="imapi_e_import_media_not_allowed"></span><dl><dt><strong>IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED</strong></dt><dt>(HRESULT) 0xC0AAB159</dt></dl> | O IMAPi não permite várias sessões com o tipo de mídia atual.<br /> | 
| <span id="IMAPI_E_UDF_NOT_WRITE_COMPATIBLE"></span><span id="imapi_e_udf_not_write_compatible"></span><dl><dt><strong>IMAPI_E_UDF_NOT_WRITE_COMPATIBLE</strong></dt><dt>(HRESULT) 0xC0AAB15A</dt></dl> | O IMAPi não pode fazer várias sessões com a mídia atual porque não dá suporte a uma revisão UDF compatível para gravação.<br /> | 
| <span id="IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE"></span><span id="imapi_e_incompatible_multisession_type"></span><dl><dt><strong>IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE</strong></dt><dt>(HRESULT) 0xC0AAB15B</dt></dl> | O IMAPi não oferece suporte ao tipo de várias sessões solicitado.<br /> | 
| <span id="IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION"></span><span id="imapi_e_incompatible_previous_session"></span><dl><dt><strong>IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION</strong></dt><dt>(HRESULT) 0xC0AAB133</dt></dl> | Falha na operação devido a um layout incompatível da sessão anterior importada da mídia.<br /> | 
| <span id="IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE"></span><span id="imapi_e_no_compatible_multisession_type"></span><dl><dt><strong>IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE</strong></dt><dt>(HRESULT) 0xC0AAB15C</dt></dl> | O IMAPi não dá suporte a nenhum dos tipos de várias sessões fornecidos na mídia atual.<br /><blockquote>[!Note]<br />O método [<strong>IFileSystemImage:: ImportFileSystem</strong>](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) retornará esse erro se não houver nenhuma mídia no dispositivo de gravação.</blockquote><br /> | 
| <span id="IMAPI_E_MULTISESSION_NOT_SET"></span><span id="imapi_e_multisession_not_set"></span><dl><dt><strong>IMAPI_E_MULTISESSION_NOT_SET</strong></dt><dt>(HRESULT) 0xC0AAB15D</dt></dl> | A propriedade MultisessionInterfaces deve ser definida antes de chamar este método.<br /> | 
| <span id="IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE"></span><span id="imapi_e_import_type_collision_directory_exists_as_file"></span><dl><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE</strong></dt><dt>(HRESULT) 0xC0AAB15E</dt></dl> | Não foi possível importar %2! ls! sistema de arquivos do disco. O diretório ' %1! ls! ' Já existe na hierarquia de imagens como um arquivo.<br /> | 
| <span id="IMAPI_E_BAD_MULTISESSION_PARAMETER"></span><span id="imapi_e_bad_multisession_parameter"></span><dl><dt><strong>IMAPI_E_BAD_MULTISESSION_PARAMETER</strong></dt><dt>(HRESULT) 0xC0AAB162</dt></dl> | Um dos parâmetros de várias sessões não pode ser recuperado ou tem um valor incorreto.<br /> | 
| <span id="IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED"></span><span id="imapi_s_image_feature_not_supported"></span><dl><dt><strong>IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0x00AAB15FL</dt></dl> | Não há suporte para esse recurso na revisão atual do sistema de arquivos. A imagem será criada sem esse recurso.<br /> | 




## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                                                                                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                                                                            |
| Cabeçalho<br/>                   | <dl> <dt>Imapi2error. h; </dt> <dt>Imapi2fserror. h</dt> </dl> |



 

 





