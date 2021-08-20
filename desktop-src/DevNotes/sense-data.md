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
ms.openlocfilehash: 2f6b3bd9fd4353e396bc7fe4ff7273e598704d1348062fec1c2f64aed9380686
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075949"
---
# <a name="sense_data-structure"></a>Estrutura de dados de detecção \_

Usado para relatar informações de status ou erro em resposta a um comando de **detecção de solicitação** SCSI.

## <a name="syntax"></a>Sintaxe


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



## <a name="members"></a>Membros

<dl> <dt>

**ErrorCode**
</dt> <dd>

O tipo de relatório.



| Valor                                                                           | Significado                     |
|---------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>0x70</dt> </dl> | Erros atuais.<br/>  |
| <dl> <dt>0x71</dt> </dl> | Erros adiados.<br/> |



 

</dd> <dt>

**Válido**
</dt> <dd>

1 se o campo de **informações** for definido em um padrão; caso contrário, o campo de **informações** será específico do fornecedor e não será definido por um padrão.

</dd> <dt>

**SegmentNumber**
</dt> <dd>

Obsoleto.

</dd> <dt>

**SenseKey**
</dt> <dd>

Indica a categoria de erro.

<dl> <dt>

<span id="No_Sense"></span><span id="no_sense"></span><span id="NO_SENSE"></span>**Sem sentido** (0x0)
</dt> <dt>

<span id="Recovered_Error"></span><span id="recovered_error"></span><span id="RECOVERED_ERROR"></span>**Erro recuperado** (0x1)
</dt> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não está pronto** (0x2)
</dt> <dt>

<span id="Medium_Error"></span><span id="medium_error"></span><span id="MEDIUM_ERROR"></span>**Erro médio** (0x3)
</dt> <dt>

<span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Erro de hardware** (0x4)
</dt> <dt>

<span id="Illegal_Request"></span><span id="illegal_request"></span><span id="ILLEGAL_REQUEST"></span>**Solicitação inválida** (0x5)
</dt> <dt>

<span id="Unit_Attention"></span><span id="unit_attention"></span><span id="UNIT_ATTENTION"></span>**Atenção de unidade** (0x6)
</dt> <dt>

<span id="Data_Protect"></span><span id="data_protect"></span><span id="DATA_PROTECT"></span>**Proteção de dados** (0x7)
</dt> <dt>

<span id="Firmware_Error"></span><span id="firmware_error"></span><span id="FIRMWARE_ERROR"></span>**Erro de firmware** (0x9)
</dt> <dt>

<span id="Aborted_Command"></span><span id="aborted_command"></span><span id="ABORTED_COMMAND"></span>**Comando anulado** (0xB)
</dt> <dt>

<span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>**Igual** (0xc)
</dt> <dt>

<span id="Volume_Overflow"></span><span id="volume_overflow"></span><span id="VOLUME_OVERFLOW"></span>**Estouro de volume** (0xD)
</dt> <dt>

<span id="Miscompare"></span><span id="miscompare"></span><span id="MISCOMPARE"></span>0xE ( **recompare** )
</dt> </dl> </dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> <dt>

**IncorrectLength**
</dt> <dd>

1 se o comprimento de bloco lógico solicitado não corresponder ao comprimento de bloco lógico dos dados na mídia.

</dd> <dt>

**EndOfMedia**
</dt> <dd>

1 se um dispositivo de acesso sequencial tiver atingido o fim da mídia ou se uma impressora estiver sem papel.

</dd> <dt>

**Marca**
</dt> <dd>

1 se o comando atual tiver atingido uma marca de caixa de um ou um setmark. Válido somente para dispositivos de acesso sequencial.

</dd> <dt>

**Informações**
</dt> <dd>

Dados específicos do tipo de dispositivo ou comando.

</dd> <dt>

**AdditionalSenseLength**
</dt> <dd>

O comprimento em bytes do restante da estrutura. O comprimento total menos 7.

</dd> <dt>

**CommandSpecificInformation**
</dt> <dd>

Dados específicos do comando. Os valores são definidos no padrão de comando apropriado.

</dd> <dt>

**AdditionalSenseCode**
</dt> <dd>

Código específico do dispositivo que descreve o erro relatado no campo **SenseKey** .

</dd> <dt>

**AdditionalSenseCodeQualifier**
</dt> <dd>

Pode conter detalhes adicionais sobre o campo **AdditionalSenseCode** .

</dd> <dt>

**FieldReplaceableUnitCode**
</dt> <dd>

Informações específicas do fornecedor sobre o componente associado a esses dados de detecção.

</dd> <dt>

**SenseKeySpecific**
</dt> <dd>

O conteúdo e o formato das informações específicas da chave de detecção são determinados pelo valor do campo **SenseKey** .

</dd> </dl>

## <a name="remarks"></a>Comentários

Para obter mais informações sobre o formato de dados de detecção, consulte [comando de detecção de solicitação SCSI](https://wikipedia.org/wiki/SCSI_command) ( https://wikipedia.org/wiki/SCSI_command) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>SCSI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Passagem de destino iSCSI](/powershell/module/iscsi)
</dt> <dt>

[\_passagem de \_ SCSI \_ via Direct](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_pass_through_direct)
</dt> </dl>

 

 




