---
description: Representa os recursos e o gerenciamento de dispositivos lógicos relacionados à memória.
ms.assetid: 802c1c0e-7eab-4a17-9a29-6502ece6cb24
title: Classe CIM_Memory (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Memory
- CIM_Memory.Volatile
- CIM_Memory.ErrorMethodology
- CIM_Memory.StartingAddress
- CIM_Memory.EndingAddress
- CIM_Memory.ErrorInfo
- CIM_Memory.OtherErrorDescription
- CIM_Memory.CorrectableError
- CIM_Memory.ErrorTime
- CIM_Memory.ErrorAccess
- CIM_Memory.ErrorTransferSize
- CIM_Memory.ErrorData
- CIM_Memory.ErrorDataOrder
- CIM_Memory.ErrorAddress
- CIM_Memory.SystemLevelAddress
- CIM_Memory.ErrorResolution
- CIM_Memory.AdditionalErrorData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 410d580542421aee153b610726bed1f438efbcde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506011"
---
# <a name="cim_memory-class-hyper-v-management"></a>Classe CIM_Memory (gerenciamento do Hyper-V)

Representa os recursos e o gerenciamento de dispositivos lógicos relacionados à memória.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::Memory"), AMENDMENT]
class CIM_Memory : CIM_StorageExtent
{
  boolean  Volatile;
  string   ErrorMethodology;
  uint64   StartingAddress;
  uint64   EndingAddress;
  uint16   ErrorInfo;
  string   OtherErrorDescription;
  boolean  CorrectableError;
  datetime ErrorTime;
  uint16   ErrorAccess;
  uint32   ErrorTransferSize;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint64   ErrorAddress;
  boolean  SystemLevelAddress;
  uint64   ErrorResolution;
  uint8    AdditionalErrorData[];
};
```

## <a name="members"></a>Membros

A classe de **\_ memória CIM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ memória CIM** tem essas propriedades.

<dl> <dt>

**AdditionalErrorData**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. AdditionalErrorData"), **octetstring**, [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 5,18 "," MIF. \|Matriz de memória física da DMTF \| 1,13 ")
</dt> </dl>

Uma matriz de octetos que contém informações adicionais sobre o erro. Um exemplo é a síndrome de ECC ou o retorno dos bits de verificação se uma metodologia de erro baseada em CRC for usada. No último caso, se um único erro de bit for reconhecido e o algoritmo CRC for conhecido, será possível determinar o bit exato que falhou.

Se a propriedade **errorInfo** contiver "3" (OK), essa propriedade não será usada.

</dd> <dt>

**CorrectableError**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. CorrectableError"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memória física da DMTF \| 1,8 ")
</dt> </dl>

**true** se o erro mais recente for corrigível; caso contrário, **false**. Se a propriedade **errorInfo** contiver "3" (OK), essa propriedade não será usada.

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("quilobytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Os \| endereços mapeados da matriz de memória DMTF \| 1,4 "," MIF. \|Endereços mapeados do dispositivo de memória DMTF \| 1,5 "), **PUnit** (" byte \* 10 ^ 3 ")
</dt> </dl>

O endereço final que é referenciado por um aplicativo ou sistema operacional e é mapeado por um controlador de memória para o objeto de memória. O endereço final é especificado em kilobytes.

</dd> <dt>

**ErrorAccess**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorAccess"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memória física da DMTF \| 1,10 ")
</dt> </dl>

A operação de acesso à memória que causou o último erro. Se a propriedade **errorInfo** contiver "3" (OK), essa propriedade não será usada.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

**Leitura** (3)


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

**Gravação** (4)


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

**Gravação parcial** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. StartingAddress"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 5,19 "," MIF. \|Matriz de memória física da DMTF \| 1,14 ")
</dt> </dl>

O endereço do último erro de memória. O tipo de erro é descrito pela propriedade **errorInfo** . Se a propriedade **errorInfo** contiver "3" (OK), essa propriedade não será usada.

</dd> <dt>

**ErrorData**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorData"), **octetstring**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memória física da DMTF \| 1,12 ")
</dt> </dl>

Uma matriz que contém dados capturados durante o último acesso de memória errado. Os dados ocupam os primeiros n octetos da matriz necessários para manter o número de bits especificado pela propriedade **ErrorTransferSize** .

Se a propriedade **ErrorTransferSize** contiver "0" (OK), essa propriedade não será usada.

</dd> <dt>

**ErrorDataOrder**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorDataOrder")
</dt> </dl>

A ordenação de dados armazenados na propriedade **ErrorData** . "Byte menos significativo primeiro" (valor = 1) ou "o byte mais significativo primeiro" (2) pode ser especificado. Se a propriedade **ErrorTransferSize** contiver "0" (OK), essa propriedade não será usada.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

**Byte menos significativo primeiro** (1)


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

**Byte mais significativo primeiro** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorInfo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 5,12 "," MIF. \|Matriz de memória física da DMTF \| 1,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ memória CIM**.**OtherErrorDescription**")
</dt> </dl>

O tipo do último erro a ocorrer.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

**OK** (3)


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

**Leitura inadequada** (4)


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

**Erro de paridade** (5)


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

**Erro de bit único** (6)


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

**Erro de bit duplo** (7)


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

**Erro de vários bits** (8)


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

**Erro de Nibble** (9)


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

**Erro de soma de verificação** (10)


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

**Erro de CRC** (11)


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

**Indefinido** (12)


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

**Indefinido** (13)


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

**Indefinido** (14)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memória física da DMTF \| 1,7 ")
</dt> </dl>

Indica se algoritmos de paridade, algoritmos de CRC, ECC ou outros mecanismos são usados pelo objeto de memória. Também é possível fornecer detalhes sobre o algoritmo.

</dd> <dt>

**ErrorResolution**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorResolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 5,21 "," MIF. \|Matriz de memória física da DMTF \| 1,15 "), **PUnit** (" byte ")
</dt> </dl>

O intervalo, em bytes, no qual o último erro pode ser resolvido. Por exemplo, se os endereços de erro forem resolvidos para 11 bits, como em uma base de página típica; em seguida, os erros podem ser resolvidos para limites de 4K e essa propriedade é definida como "4000". Se a propriedade **errorInfo** contiver "3" (OK), essa propriedade não será usada.

</dd> <dt>

**ErrorTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorTime")
</dt> </dl>

A hora em que ocorreu o último erro de memória. Se a propriedade **errorInfo** contiver "3" (OK), essa propriedade não será usada.

</dd> <dt>

**ErrorTransferSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorTransferSize"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memória física da DMTF \| 1,11 "), **PUnit** (" bit ")
</dt> </dl>

O tamanho da transferência de dados, em bits, que causou o último erro. "0" indica que não há erro. Se a propriedade **errorInfo** contiver "3" (OK), essa propriedade não será usada.

</dd> <dt>

**OtherErrorDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. OtherErrorDescription"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ memória CIM**.**ErrorInfo**")
</dt> </dl>

Uma descrição do tipo de erro, quando a propriedade **ErrorType** é definida como "1" (Other).

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("quilobytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Os \| endereços mapeados da matriz de memória DMTF \| 1,3 "," MIF. \|Endereços mapeados do dispositivo de memória DMTF \| 1,4 "), **PUnit** (" byte \* 10 ^ 3 ")
</dt> </dl>

O endereço inicial que é referenciado por um aplicativo ou sistema operacional e é mapeado por um controlador de memória para o objeto de memória. O endereço inicial é especificado em kilobytes.

</dd> <dt>

**SystemLevelAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_MemoryError.SystemLevelAddress")
</dt> </dl>

**true** se as informações de endereço na propriedade **ErrorAddress** forem um endereço de nível de sistema, **false** se for um endereço físico.

</dd> <dt>

**Volátil**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

**true** se a memória for volátil; caso contrário, **false**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_STORAGEEXTENT CIM**](cim-storageextent.md)
</dt> </dl>

 

