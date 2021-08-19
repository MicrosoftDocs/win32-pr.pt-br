---
title: Constantes BFT (Ntdsbcli.h)
description: As constantes BFT são usadas como sinalizadores de bits para identificar diferentes tipos de arquivo em um Active Directory Domain Services backup.
ms.assetid: 3658a657-d9e3-4fbf-9120-4b0205b81a36
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- BFT_LOG_DIRECTORY
- BFT_DATABASE_DIRECTORY
- BFT_DIRECTORY
- BFT_LOG
- BFT_LOG_DIR
- BFT_CHECKPOINT_DIR
- BFT_NTDS_DATABASE
- BFT_PATCH_FILE
- BFT_UNKNOWN
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b5e9275e01b8c33d308b55b2638d4eaf186b8f5265834acc27acd2f146f0d09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024045"
---
# <a name="bft-constants"></a>Constantes BFT

As constantes BFT são usadas como sinalizadores de bits para identificar diferentes tipos de arquivo em um Active Directory Domain Services backup.

<dl> <dt>

<span id="BFT_LOG_DIRECTORY"></span><span id="bft_log_directory"></span>**BFT \_ LOG \_ DIRECTORY**
</dt> <dd> <dl> <dt>

0x20
</dt> <dt>



O arquivo pertence ao diretório de log.


</dt> </dl> </dd> <dt>

<span id="BFT_DATABASE_DIRECTORY"></span><span id="bft_database_directory"></span>**BFT \_ DATABASE \_ DIRECTORY**
</dt> <dd> <dl> <dt>

0x40
</dt> <dt>



O arquivo pertence ao diretório do banco de dados.


</dt> </dl> </dd> <dt>

<span id="BFT_DIRECTORY"></span><span id="bft_directory"></span>**BFT \_ DIRECTORY**
</dt> <dd> <dl> <dt>

0x80
</dt> <dt>



O caminho especificado é um diretório e não um nome de arquivo.


</dt> </dl> </dd> <dt>

<span id="BFT_LOG"></span><span id="bft_log"></span>**BFT \_ LOG**
</dt> <dd> <dl> <dt>

0x21
</dt> <dt>



Especifica um arquivo de log que pertence ao diretório de log.


</dt> </dl> </dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT \_ LOG \_ DIR**
</dt> <dd> <dl> <dt>

0x22
</dt> <dt>



O arquivo é o caminho do diretório de log.


</dt> </dl> </dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**DIR DO \_ PONTO DE VERIFICAÇÃO do BFT \_**
</dt> <dd> <dl> <dt>

0x23
</dt> <dt>



O arquivo é o caminho do diretório de ponto de verificação.


</dt> </dl> </dd> <dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT \_ NTDS \_ DATABASE**
</dt> <dd> <dl> <dt>

0x44
</dt> <dt>



O arquivo é um banco de dados de serviço de diretório que pertence ao diretório do banco de dados.


</dt> </dl> </dd> <dt>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**BFT \_ PATCH \_ FILE**
</dt> <dd> <dl> <dt>

0x25
</dt> <dt>



O arquivo é um arquivo de patch que pertence ao diretório de log.


</dt> </dl> </dd> <dt>

<span id="BFT_UNKNOWN"></span><span id="bft_unknown"></span>**BFT \_ UNKNOWN**
</dt> <dd> <dl> <dt>

0x0F
</dt> <dt>



O arquivo não pode ser reconhecido. O arquivo não coincide com os nomes de arquivo conhecidos e tipos de arquivo.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                        |
| Cabeçalho<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl> |



 

 





