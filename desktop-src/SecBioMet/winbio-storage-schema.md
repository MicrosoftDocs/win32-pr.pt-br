---
title: Estrutura de WINBIO_STORAGE_SCHEMA (WinBio \_ Types. h)
description: Descreve os recursos de um adaptador de armazenamento biométrico.
ms.assetid: e4924803-5a1b-4e0a-b2cb-01d018d27ba1
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_STORAGE_SCHEMA
- ponteiro de estrutura de PWINBIO_STORAGE_SCHEMA Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_STORAGE_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc0bd0d61814b4133c3789b0c8119edcaf79945452cc26aa313504c055ac2f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909253"
---
# <a name="winbio_storage_schema-structure"></a>Estrutura de esquema de \_ armazenamento WINBIO \_

A estrutura de **\_ \_ esquema de armazenamento do WINBIO** descreve os recursos de um adaptador de armazenamento biométrico. Essa estrutura é usada pela função [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WINBIO_STORAGE_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           DatabaseId;
  WINBIO_UUID           DataFormat;
  ULONG                 Attributes;
  WINBIO_STRING         FilePath;
  WINBIO_STRING         ConnectionString;
} WINBIO_STORAGE_SCHEMA, *PWINBIO_STORAGE_SCHEMA;
```



## <a name="members"></a>Membros

<dl> <dt>

**BiometricFactor**
</dt> <dd>

O tipo de medição biométrica salva no banco de dados.

</dd> <dt>

**DatabaseId**
</dt> <dd>

Um GUID que identifica o banco de dados.

</dd> <dt>

**DataFormat**
</dt> <dd>

Um GUID que identifica o formato dos modelos no banco de dados.

</dd> <dt>

**Atributos**
</dt> <dd>

Informações sobre as características do banco de dados. Isso pode ser uma **ou** uma das constantes a seguir.



| Valor                                                                                                                                                                                                                                                                              | Significado                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <dt>**WINBIO \_ \_ \_ Máscara de sinalizador de banco de dados**</dt> <dt>0xFFFF0000</dt> </dl>                | Representa uma máscara para os bits de sinalizador.<br/>                     |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <dt>**WINBIO \_ 0x00020000 \_ \_ remoto do sinalizador de banco de dados**</dt> <dt></dt> </dl>          | O banco de dados reside em um computador remoto.<br/>               |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <dt>**WINBIO \_ 0x00010000 \_ \_ removível do sinalizador de banco de dados**</dt> <dt></dt> </dl> | O banco de dados reside em uma unidade removível.<br/>               |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <dt>**WINBIO \_ Tipo de banco de dados \_ \_ DBMS**</dt> <dt>0x00000002</dt> </dl>                | O banco de dados é gerenciado por um sistema de gerenciamento de banco de dados.<br/> |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <dt>**WINBIO \_ \_ \_ Arquivo de tipo de banco de dados**</dt> <dt>0x00000001</dt> </dl>                | O banco de dados está contido em um arquivo.<br/>                     |
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <dt>**WINBIO \_ \_ \_ Máscara de tipo de banco de dados**</dt> <dt>0x0000FFFF</dt> </dl>                | Representa uma máscara para o tipo bits.<br/>                     |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <dt>**WINBIO \_ Tipo de banco de dados \_ \_ OnChip**</dt> <dt>0x00000003</dt> </dl>          | O banco de dados reside no sensor biométrico.<br/>            |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <dt>**WINBIO \_ \_ \_ Cartão inteligente de tipo de banco de dados**</dt> <dt>0x00000004</dt> </dl> | O banco de dados reside em um cartão inteligente.<br/>                    |



 

</dd> <dt>

**FilePath**
</dt> <dd>

O caminho e o nome do arquivo do banco de dados se ele residir no disco do computador.

</dd> <dt>

**ConnectionString**
</dt> <dd>

Um valor de cadeia de caracteres que pode ser enviado a um servidor de banco de dados para identificar o banco de dados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de aplicativo cliente](client-application-structures.md)
</dt> <dt>

[**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)
</dt> </dl>

 

 





