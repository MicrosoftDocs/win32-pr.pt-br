---
title: Constantes de WINBIO_DATABASE_TYPE (WinBio \_ Types. h)
description: Sinalizadores que podem ser usados para o membro Attributes da \_ estrutura de esquema de armazenamento WINBIO \_ .
ms.assetid: 07e7e91c-3ca6-41cd-a2c7-ac43bb5156a6
topic_type:
- apiref
api_name:
- WINBIO_DATABASE_TYPE_MASK
- WINBIO_DATABASE_TYPE_FILE
- WINBIO_DATABASE_TYPE_DBMS
- WINBIO_DATABASE_TYPE_ONCHIP
- WINBIO_DATABASE_TYPE_SMARTCARD
- WINBIO_DATABASE_FLAG_MASK
- WINBIO_DATABASE_FLAG_REMOVABLE
- WINBIO_DATABASE_FLAG_REMOTE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acd67f49c5fa689fb4418789aae7c4d6c9a305a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644656"
---
# <a name="winbio_database_type-constants"></a>\_Constantes de tipo de banco de dados WINBIO \_

Os sinalizadores a seguir podem ser usados para o membro **Attributes** da estrutura de [**\_ \_ esquema de armazenamento WINBIO**](winbio-storage-schema.md) .



| Constante/valor                                                                                                                                                                                                                                                                     | Description                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <dt>**WINBIO \_ \_ \_ Máscara de tipo de banco de dados**</dt> <dt>0x0000FFFF</dt> </dl>                | Representa uma máscara para todos os \_ bits de tipo \_ .<br/>                                                                   |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <dt>**WINBIO \_ \_ \_ Arquivo de tipo de banco de dados**</dt> <dt>0x00000001</dt> </dl>                | O banco de dados está contido em um arquivo.<br/>                                                                              |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <dt>**WINBIO \_ Tipo de banco de dados \_ \_ DBMS**</dt> <dt>0x00000002</dt> </dl>                | O banco de dados é gerenciado por um componente de DBMS (sistema de gerenciamento de banco de dados) externo, como Microsoft SQL Server.<br/> |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <dt>**WINBIO \_ Tipo de banco de dados \_ \_ OnChip**</dt> <dt>0x00000003</dt> </dl>          | O banco de dados reside no sensor biométrico.<br/>                                                                     |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <dt>**WINBIO \_ \_ \_ Cartão inteligente de tipo de banco de dados**</dt> <dt>0x00000004</dt> </dl> | O banco de dados reside em um cartão inteligente.<br/>                                                                             |
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <dt>**WINBIO \_ \_ \_ Máscara de sinalizador de banco de dados**</dt> <dt>0xFFFF0000</dt> </dl>                | Representa uma máscara para todos os \_ bits de sinalizador \_ .<br/>                                                                   |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <dt>**WINBIO \_ 0x00010000 \_ \_ removível do sinalizador de banco de dados**</dt> <dt></dt> </dl> | A mídia de armazenamento que contém o banco de dados pode ser fisicamente removida do computador.<br/>                           |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <dt>**WINBIO \_ 0x00020000 \_ \_ remoto do sinalizador de banco de dados**</dt> <dt></dt> </dl>          | O banco de dados reside em um computador remoto.<br/>                                                                        |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Constantes de aplicativo cliente](client-application-constants.md)
</dt> </dl>

 

 





