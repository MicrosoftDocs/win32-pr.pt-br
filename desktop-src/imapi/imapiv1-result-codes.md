---
title: Códigos de resultado do IMAPIv1 (Imapierror. h)
description: Os métodos das interfaces IMAPi retornarão S \_ OK se o método tiver sido bem-sucedido. Caso contrário, eles retornam um dos seguintes códigos de resultado.
ms.assetid: 0143ad10-9b65-4621-9bed-71dadd38c3fc
topic_type:
- apiref
api_name:
- IMAPI_S_PROPERTIESIGNORED
- IMAPI_S_BUFFER_TO_SMALL
- IMAPI_E_NOTOPENED
- IMAPI_E_NOTINITIALIZED
- IMAPI_E_USERABORT
- IMAPI_E_GENERIC
- IMAPI_E_MEDIUM_NOTPRESENT
- IMAPI_E_MEDIUM_INVALIDTYPE
- IMAPI_E_DEVICE_NOPROPERTIES
- IMAPI_E_DEVICE_NOTACCESSIBLE
- IMAPI_E_DEVICE_NOTPRESENT
- IMAPI_E_DEVICE_INVALIDTYPE
- IMAPI_E_INITIALIZE_WRITE
- IMAPI_E_INITIALIZE_ENDWRITE
- IMAPI_E_FILESYSTEM
- IMAPI_E_FILEACCESS
- IMAPI_E_DISCINFO
- IMAPI_E_TRACKNOTOPEN
- IMAPI_E_TRACKOPEN
- IMAPI_E_DISCFULL
- IMAPI_E_BADJOLIETNAME
- IMAPI_E_INVALIDIMAGE
- IMAPI_E_NOACTIVEFORMAT
- IMAPI_E_NOACTIVERECORDER
- IMAPI_E_WRONGFORMAT
- IMAPI_E_ALREADYOPEN
- IMAPI_E_WRONGDISC
- IMAPI_E_FILEEXISTS
- IMAPI_E_STASHINUSE
- IMAPI_E_DEVICE_STILL_IN_USE
- IMAPI_E_LOSS_OF_STREAMING
- IMAPI_E_COMPRESSEDSTASH
- IMAPI_E_ENCRYPTEDSTASH
- IMAPI_E_NOTENOUGHDISKFORSTASH
- IMAPI_E_REMOVABLESTASH
- IMAPI_E_CANNOT_WRITE_TO_MEDIA
- IMAPI_E_TRACK_NOT_BIG_ENOUGH
api_location:
- Imapierror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80e8aba2a2d3d12628a45c6716c6f94a405d752f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644270"
---
# <a name="imapiv1-result-codes"></a>Códigos de resultado do IMAPIv1

Os métodos das interfaces IMAPi retornarão S \_ OK se o método tiver sido bem-sucedido. Caso contrário, eles retornam um dos seguintes códigos de resultado.



| Constante/valor                                                                                                                                                                                                                                                                    | Descrição                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IMAPI_S_PROPERTIESIGNORED"></span><span id="imapi_s_propertiesignored"></span><dl> <dt>**\_ IMAPI 0x40200 \_ PROPERTIESIGNORED S**</dt> <dt></dt> </dl>                   | Uma propriedade desconhecida foi passada em um conjunto de propriedades e foi ignorada.<br/>                                                                                                                                                                              |
| <span id="IMAPI_S_BUFFER_TO_SMALL"></span><span id="imapi_s_buffer_to_small"></span><dl> <dt>**\_ IMAPI \_Buffer S \_ para \_**</dt> <dt>0x40201</dt> pequeno </dl>                       | O buffer de saída é muito pequeno.<br/>                                                                                                                                                                                                                   |
| <span id="IMAPI_E_NOTOPENED"></span><span id="imapi_e_notopened"></span><dl> <dt>**\_ IMAPI 0x8004020b E não \_ aberto**</dt> <dt></dt> </dl>                                        | Uma chamada para [**IDiscMaster:: Open**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-open) não foi feita.<br/>                                                                                                                                                                        |
| <span id="IMAPI_E_NOTINITIALIZED"></span><span id="imapi_e_notinitialized"></span><dl> <dt>**\_ IMAPI E 0x8004020c não \_ inicializado**</dt> <dt></dt> </dl>                         | Um objeto de gravador não foi inicializado.<br/>                                                                                                                                                                                                       |
| <span id="IMAPI_E_USERABORT"></span><span id="imapi_e_userabort"></span><dl> <dt>**\_ IMAPI E \_ userabort**</dt> <dt>0x8004020d</dt> </dl>                                        | O usuário cancelou a operação.<br/>                                                                                                                                                                                                                  |
| <span id="IMAPI_E_GENERIC"></span><span id="imapi_e_generic"></span><dl> <dt>**\_ IMAPI 0x8004020e \_ genérico E**</dt> <dt></dt> </dl>                                              | Ocorreu um erro genérico.<br/>                                                                                                                                                                                                                         |
| <span id="IMAPI_E_MEDIUM_NOTPRESENT"></span><span id="imapi_e_medium_notpresent"></span><dl> <dt>**\_ IMAPI E & 0x8004020f \_ médio de \_ presentes**</dt> <dt></dt> </dl>               | Não há disco no dispositivo.<br/>                                                                                                                                                                                                                   |
| <span id="IMAPI_E_MEDIUM_INVALIDTYPE"></span><span id="imapi_e_medium_invalidtype"></span><dl> <dt>**\_ IMAPI E \_ médio \_ invalidatype**</dt> <dt>0x80040210</dt> </dl>            | A mídia não é um tipo que possa ser usado.<br/>                                                                                                                                                                                                         |
| <span id="IMAPI_E_DEVICE_NOPROPERTIES"></span><span id="imapi_e_device_noproperties"></span><dl> <dt>**\_ IMAPI E \_ & \_**</dt> <dt>0x80040211</dt> de propriedades do dispositivo </dl>         | O gravador não oferece suporte a nenhuma propriedade.<br/>                                                                                                                                                                                                     |
| <span id="IMAPI_E_DEVICE_NOTACCESSIBLE"></span><span id="imapi_e_device_notaccessible"></span><dl> <dt>**\_ IMAPI \_Dispositivo E \_**</dt> <dt>0x80040212</dt> não acessíveis </dl>      | O dispositivo não pode ser usado ou já está em uso.<br/>                                                                                                                                                                                                   |
| <span id="IMAPI_E_DEVICE_NOTPRESENT"></span><span id="imapi_e_device_notpresent"></span><dl> <dt>**\_ IMAPI E & 0x80040213 do \_ dispositivo \_ presente**</dt> <dt></dt> </dl>               | O dispositivo não está presente ou foi removido.<br/>                                                                                                                                                                                                    |
| <span id="IMAPI_E_DEVICE_INVALIDTYPE"></span><span id="imapi_e_device_invalidtype"></span><dl> <dt>**\_ IMAPI E & 0x80040214 do \_ dispositivo \_ inválida**</dt> <dt></dt> </dl>            | O gravador não oferece suporte a uma operação.<br/>                                                                                                                                                                                                       |
| <span id="IMAPI_E_INITIALIZE_WRITE"></span><span id="imapi_e_initialize_write"></span><dl> <dt>**\_ IMAPI E \_ inicializar \_ gravação**</dt> <dt>0x80040215</dt> </dl>                  | A interface da unidade não pôde ser inicializada para gravação.<br/>                                                                                                                                                                                         |
| <span id="IMAPI_E_INITIALIZE_ENDWRITE"></span><span id="imapi_e_initialize_endwrite"></span><dl> <dt>**\_ IMAPI E \_ inicializar \_ EndWrite**</dt> <dt>0x80040216</dt> </dl>         | Não foi possível inicializar a interface da unidade para fechamento.<br/>                                                                                                                                                                                         |
| <span id="IMAPI_E_FILESYSTEM"></span><span id="imapi_e_filesystem"></span><dl> <dt>**\_ IMAPI E \_**</dt> <dt>0x80040217</dt> FileSystem </dl>                                     | Ocorreu um erro ao habilitar/desabilitar o acesso ao sistema de arquivos ou durante a detecção de inserção automática.<br/>                                                                                                                                                 |
| <span id="IMAPI_E_FILEACCESS"></span><span id="imapi_e_fileaccess"></span><dl> <dt>**\_ IMAPI E \_**</dt> <dt>0x80040218</dt> FILEACCESS </dl>                                     | Ocorreu um erro ao gravar o arquivo de imagem.<br/>                                                                                                                                                                                                   |
| <span id="IMAPI_E_DISCINFO"></span><span id="imapi_e_discinfo"></span><dl> <dt>**\_ IMAPI E \_ DISCINFO**</dt> <dt>0x80040219</dt> </dl>                                           | Ocorreu um erro ao tentar ler os dados do disco do dispositivo.<br/>                                                                                                                                                                                 |
| <span id="IMAPI_E_TRACKNOTOPEN"></span><span id="imapi_e_tracknotopen"></span><dl> <dt>**\_ IMAPI E \_ TRACKNOTOPEN**</dt> <dt>0x8004021a</dt> </dl>                               | Uma faixa de áudio não está aberta para gravação.<br/>                                                                                                                                                                                                           |
| <span id="IMAPI_E_TRACKOPEN"></span><span id="imapi_e_trackopen"></span><dl> <dt>**\_ IMAPI E \_ TRACKOPEN**</dt> <dt>0x8004021b</dt> </dl>                                        | Uma faixa de áudio aberta já está sendo preparada.<br/>                                                                                                                                                                                                      |
| <span id="IMAPI_E_DISCFULL"></span><span id="imapi_e_discfull"></span><dl> <dt>**\_ IMAPI E \_ DISCFULL**</dt> <dt>0x8004021c</dt> </dl>                                           | O disco não pode conter mais dados.<br/>                                                                                                                                                                                                               |
| <span id="IMAPI_E_BADJOLIETNAME"></span><span id="imapi_e_badjolietname"></span><dl> <dt>**\_ IMAPI E \_ BADJOLIETNAME**</dt> <dt>0x8004021d</dt> </dl>                            | O aplicativo tentou adicionar um elemento com nome incorreto a um disco.<br/>                                                                                                                                                                                     |
| <span id="IMAPI_E_INVALIDIMAGE"></span><span id="imapi_e_invalidimage"></span><dl> <dt>**\_ IMAPI E \_ INVALIDIMAGE**</dt> <dt>0x8004021e</dt> </dl>                               | A imagem preparada não é adequada para uma gravação. Ele foi corrompido ou limpo e não tem conteúdo utilizável.<br/>                                                                                                                                          |
| <span id="IMAPI_E_NOACTIVEFORMAT"></span><span id="imapi_e_noactiveformat"></span><dl> <dt>**\_ IMAPI E \_ NOACTIVEFORMAT**</dt> <dt>0x8004021f</dt> </dl>                         | Um mestre de formato ativo não foi selecionado usando [**IDiscMaster:: SetActiveDiscMasterFormat**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscmasterformat).<br/>                                                                                                      |
| <span id="IMAPI_E_NOACTIVERECORDER"></span><span id="imapi_e_noactiverecorder"></span><dl> <dt>**\_ IMAPI E \_ NOACTIVERECORDER**</dt> <dt>0x80040220</dt> </dl>                   | Um gravador de disco ativo não foi selecionado usando [**IDiscMaster:: SetActiveDiscRecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder).<br/>                                                                                                              |
| <span id="IMAPI_E_WRONGFORMAT"></span><span id="imapi_e_wrongformat"></span><dl> <dt>**\_ IMAPI E \_ WRONGFORMAT**</dt> <dt>0x80040221</dt> </dl>                                  | Uma chamada para [**IJolietDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) foi feita quando [**IRedbookDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster) é o formato ativo ou vice-versa. Para usar um formato diferente, altere o formato e limpe o conteúdo do arquivo de imagem.<br/> |
| <span id="IMAPI_E_ALREADYOPEN"></span><span id="imapi_e_alreadyopen"></span><dl> <dt>**\_ IMAPI E \_ ALREADYOPEN**</dt> <dt>0x80040222</dt> </dl>                                  | Uma chamada para [**IDiscMaster:: Open**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-open) já foi feita nesse objeto pelo seu aplicativo.<br/>                                                                                                                            |
| <span id="IMAPI_E_WRONGDISC"></span><span id="imapi_e_wrongdisc"></span><dl> <dt>**\_ IMAPI E \_ WRONGDISC**</dt> <dt>0x80040223</dt> </dl>                                        | O disco de várias sessões do IMAPi foi removido do gravador ativo.<br/>                                                                                                                                                                           |
| <span id="IMAPI_E_FILEEXISTS"></span><span id="imapi_e_fileexists"></span><dl> <dt>**\_ IMAPI E \_ fileexiste**</dt> <dt>0x80040224</dt> </dl>                                     | O arquivo a ser adicionado já está no arquivo de imagem e o sinalizador de substituição não foi definido.<br/>                                                                                                                                                                  |
| <span id="IMAPI_E_STASHINUSE"></span><span id="imapi_e_stashinuse"></span><dl> <dt>**\_ IMAPI E \_ STASHINUSE**</dt> <dt>0x80040225</dt> </dl>                                     | Outro aplicativo já está usando o arquivo stash IMAPi necessário para preparar uma imagem de disco. Tente novamente depois.<br/>                                                                                                                                        |
| <span id="IMAPI_E_DEVICE_STILL_IN_USE"></span><span id="imapi_e_device_still_in_use"></span><dl> <dt>**\_ IMAPI O \_ dispositivo E \_ ainda está \_ em \_ uso**</dt> <dt>0x80040226</dt> </dl>       | Outro aplicativo já está usando este dispositivo; portanto, o IMAPi não pode acessar o dispositivo.<br/>                                                                                                                                                              |
| <span id="IMAPI_E_LOSS_OF_STREAMING"></span><span id="imapi_e_loss_of_streaming"></span><dl> <dt>**\_ IMAPI E \_ perda \_ de 0x80040227 de \_ streaming**</dt> <dt></dt> </dl>              | O streaming de conteúdo foi perdido; pode ter ocorrido um buffer em execução.<br/>                                                                                                                                                                                 |
| <span id="IMAPI_E_COMPRESSEDSTASH"></span><span id="imapi_e_compressedstash"></span><dl> <dt>**\_ IMAPI E \_ COMPRESSEDSTASH**</dt> <dt>0x80040228</dt> </dl>                      | O stash está localizado em um volume compactado e não pode ser lido.<br/>                                                                                                                                                                                   |
| <span id="IMAPI_E_ENCRYPTEDSTASH"></span><span id="imapi_e_encryptedstash"></span><dl> <dt>**\_ IMAPI E \_ ENCRYPTEDSTASH**</dt> <dt>0x80040229</dt> </dl>                         | O stash está localizado em um volume criptografado e não pode ser lido.<br/>                                                                                                                                                                                   |
| <span id="IMAPI_E_NOTENOUGHDISKFORSTASH"></span><span id="imapi_e_notenoughdiskforstash"></span><dl> <dt>**\_ IMAPI E \_ NOTENOUGHDISKFORSTASH**</dt> <dt>0x8004022a</dt> </dl>    | Não há espaço livre suficiente para criar o arquivo stash no volume especificado.<br/>                                                                                                                                                                  |
| <span id="IMAPI_E_REMOVABLESTASH"></span><span id="imapi_e_removablestash"></span><dl> <dt>**\_ IMAPI E \_ REMOVABLESTASH**</dt> <dt>0x8004022b</dt> </dl>                         | O local do Stash selecionado está em uma mídia removível.<br/>                                                                                                                                                                                              |
| <span id="IMAPI_E_CANNOT_WRITE_TO_MEDIA"></span><span id="imapi_e_cannot_write_to_media"></span><dl> <dt>**\_ IMAPI E \_ não é possível \_ gravar \_ no 0x8004022c de \_ mídia**</dt> <dt></dt> </dl> | A mídia não pode ser gravada.<br/>                                                                                                                                                                                                                   |
| <span id="IMAPI_E_TRACK_NOT_BIG_ENOUGH"></span><span id="imapi_e_track_not_big_enough"></span><dl> <dt>**\_ IMAPI E \_ Track \_ não \_ 0x8004022d \_ suficientemente grande**</dt> <dt></dt> </dl>    | A faixa não é grande o suficiente.<br/>                                                                                                                                                                                                                      |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Imapierror. h</dt> </dl> |



 

 





