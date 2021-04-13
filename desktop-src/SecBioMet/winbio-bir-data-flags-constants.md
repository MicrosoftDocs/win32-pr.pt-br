---
title: Constantes de WINBIO_BIR_DATA_FLAGS (WinBio \_ Types. h)
description: Especifique a condição dos dados.
ms.assetid: F6F7F68A-3294-4AF8-A1A7-C6A869A2CC3C
topic_type:
- apiref
api_name:
- WINBIO_DATA_FLAG_PRIVACY
- WINBIO_DATA_FLAG_INTEGRITY
- WINBIO_DATA_FLAG_SIGNED
- WINBIO_DATA_FLAG_RAW
- WINBIO_DATA_FLAG_INTERMEDIATE
- WINBIO_DATA_FLAG_PROCESSED
- WINBIO_DATA_FLAG_OPTION_MASK_PRESENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8195cf17040c35b9e42f8977b36c5ddc6f2ea33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369918"
---
# <a name="winbio_bir_data_flags-constants"></a>\_Constantes de \_ sinalizadores de dados WINBIO Bir \_

As constantes a seguir são usadas pelo membro **dataFlags** da estrutura de [**\_ \_ cabeçalho WINBIO Bir**](winbio-bir-header.md) .



| Constante/valor                                                                                                                                                                                                                                                                                   | Descrição                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <dt>**WINBIO \_ \_Sinalizador de \_ privacidade de dados**</dt> <dt>0x02</dt> </dl>                                       | Os dados estão criptografados.<br/>                                                                                                                                                                                 |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <dt>**WINBIO \_ \_ \_ Integridade de sinalizador de dados**</dt> <dt>0x01</dt> </dl>                                 | Os dados são assinados digitalmente ou protegidos por um MAC (código de autenticação de mensagens).<br/>                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <dt>**WINBIO \_ Sinalizador de dados 0x04 \_ \_ assinado**</dt> <dt></dt> </dl>                                          | Se esse sinalizador e o sinalizador de **\_ integridade do \_ sinalizador \_ de dados WINBIO** estiverem definidos, os dados serão assinados. Se esse sinalizador não for definido, mas o sinalizador de **\_ integridade do \_ sinalizador \_ de dados WINBIO** for definido, um Mac será calculado nos dados.<br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <dt>**WINBIO \_ 0x20 de sinalizador de dados \_ \_ brutos**</dt> <dt></dt> </dl>                                                   | Os dados estão no formato com o qual foram capturados.<br/>                                                                                                                                                  |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <dt>**WINBIO \_ Sinalizador de dados \_ \_ intermediário**</dt> <dt>0x40</dt> </dl>                        | Os dados não são brutos, mas não foram completamente processados.<br/>                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <dt>**WINBIO \_ Sinalizador de dados \_ \_ processado**</dt> <dt>0x80</dt> </dl>                                 | Os dados foram processados.<br/>                                                                                                                                                                           |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <dt>**WINBIO \_ Máscara de opção de sinalizador de dados \_ \_ \_ \_ presente**</dt> <dt>0x08</dt> </dl> | A máscara do sinalizador. Esse valor é sempre um (1).<br/>                                                                                                                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de aplicativo cliente](client-application-constants.md)
</dt> </dl>

 

 





