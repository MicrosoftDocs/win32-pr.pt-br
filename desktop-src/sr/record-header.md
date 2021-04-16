---
title: Estrutura de RECORD_HEADER
description: O cabeçalho de registro usado pela entrada de log de alteração \_ e as \_ estruturas de cabeçalho de log de alteração \_ \_ .
ms.assetid: f8d2147c-ad13-4be4-94d7-ae0ca26511da
keywords:
- Restauração do sistema de estrutura RECORD_HEADER
- Restauração do sistema de ponteiro de estrutura de PRECORD_HEADER
topic_type:
- apiref
api_name:
- RECORD_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2fd304d2f1b6a5ece08d3d3535aacd7a1abcf614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455671"
---
# <a name="record_header-structure"></a>Estrutura do cabeçalho do registro \_

\[Essas informações se aplicam somente ao Windows XP com Service Pack 2 (SP2).\]

O cabeçalho de registro usado pela [**\_ \_ entrada de log de alteração**](change-log-entry.md) e as estruturas de [**\_ \_ cabeçalho de log de alteração**](change-log-header.md) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _RECORD_HEADER {
  DWORD dwRecordSize;
  DWORD dwRecordType;
} RECORD_HEADER, *PRECORD_HEADER;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwRecordSize**
</dt> <dd>

O tamanho total do registro, incluindo o cabeçalho, em bytes.

</dd> <dt>

**dwRecordType**
</dt> <dd>

O tipo de registro. Esse membro pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RecordTypeLogHeader"></span><span id="recordtypelogheader"></span><span id="RECORDTYPELOGHEADER"></span><dl> <dt>**RecordTypeLogHeader**</dt> <dt>0</dt> </dl>     | O registro é o cabeçalho do log de alterações.<br/>                                                                                                                                                                                                                            |
| <span id="RecordTypeLogEntry"></span><span id="recordtypelogentry"></span><span id="RECORDTYPELOGENTRY"></span><dl> <dt>**RecordTypeLogEntry**</dt> <dt>1</dt> </dl>         | O registro é o cabeçalho de uma entrada de log de alterações.<br/>                                                                                                                                                                                                                        |
| <span id="RecordTypeVolumePath"></span><span id="recordtypevolumepath"></span><span id="RECORDTYPEVOLUMEPATH"></span><dl> <dt>**RecordTypeVolumePath**</dt> <dt>2</dt> </dl> | Os dados são o caminho do volume para a entrada do log de alterações.<br/>                                                                                                                                                                                                                   |
| <span id="RecordTypeFirstPath"></span><span id="recordtypefirstpath"></span><span id="RECORDTYPEFIRSTPATH"></span><dl> <dt>**RecordTypeFirstPath**</dt> <dt>3</dt> </dl>     | Os dados são o caminho do arquivo para a entrada do log de alterações.<br/>                                                                                                                                                                                                                     |
| <span id="RecordTypeSecondPath"></span><span id="recordtypesecondpath"></span><span id="RECORDTYPESECONDPATH"></span><dl> <dt>**RecordTypeSecondPath**</dt> <dt>4</dt> </dl> | Os dados são usados ao renomear as entradas do log de alterações; esse caminho é onde o arquivo renomeado é armazenado.<br/>                                                                                                                                                                       |
| <span id="RecordTypeTempPath"></span><span id="recordtypetemppath"></span><span id="RECORDTYPETEMPPATH"></span><dl> <dt>**RecordTypeTempPath**</dt> <dt>5</dt> </dl>         | Os dados são o nome do arquivo de backup usado para restaurar a entrada do log de alterações. Os arquivos de backup estão localizados na pasta RP *n* . O nome do arquivo tem o seguinte formato: um *xxxxxxx*. *ext*, em que *xxxxxxx* é um número de sete dígitos e *ext* é a extensão de nome de arquivo.<br/> |
| <span id="RecordTypeAclInline"></span><span id="recordtypeaclinline"></span><span id="RECORDTYPEACLINLINE"></span><dl> <dt>**RecordTypeAclInline**</dt> <dt>6</dt> </dl>     | Os dados são uma ACL. O formato de dados é uma estrutura de [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) . <br/> Esse valor não pode ser maior que 8.192 bytes. Para especificar um valor maior que 8.192 bytes, use o membro **RecordTypeAclFile** .<br/>                |
| <span id="RecordTypeAclFile"></span><span id="recordtypeaclfile"></span><span id="RECORDTYPEACLFILE"></span><dl> <dt>**RecordTypeAclFile**</dt> <dt>7</dt> </dl>             | Os dados são o nome do arquivo ACL usado para armazenar a ACL. Os arquivos ACL estão localizados na pasta RP *n* . O nome do arquivo tem o seguinte formato: S *xxxxxxx*. ACL, em que *xxxxxxx* é um número de sete dígitos.<br/>                                                             |
| <span id="RecordTypeDebugInfo"></span><span id="recordtypedebuginfo"></span><span id="RECORDTYPEDEBUGINFO"></span><dl> <dt>**RecordTypeDebugInfo**</dt> <dt>8</dt> </dl>     | Os dados são informações de depuração para a entrada do log de alterações. O formato de dados é uma estrutura de **informações de depuração de log do Sr \_ \_ \_** . Para obter mais informações, consulte Comentários.<br/>                                                                                                                     |
| <span id="RecordTypeShortName"></span><span id="recordtypeshortname"></span><span id="RECORDTYPESHORTNAME"></span><dl> <dt>**RecordTypeShortName**</dt> <dt>9</dt> </dl>     | Os dados são o nome curto do arquivo de backup.<br/>                                                                                                                                                                                                                          |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

A estrutura de informações de depuração do log do Sr é definida da seguinte maneira. **\_ \_ \_**

``` syntax
typedef struct _SR_LOG_DEBUG_INFO {
    RECORD_HEADER Header;         // log entry header
    HANDLE ThreadId;              // thread identifier
    HANDLE ProcessId;             // process identifier
    ULARGER_INTEGER TimeStamp;    // event time stamp
    CHAR ProcesName[13];          // process name
} SR_LOG_DEBUG_INFO, *PSR_LOG_DEBUG_INFO;
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                            |
| Fim do suporte do cliente<br/>    | Windows XP com SP2<br/>                       |



 

