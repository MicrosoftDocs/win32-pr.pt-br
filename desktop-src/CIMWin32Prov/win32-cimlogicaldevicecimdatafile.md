---
description: A classe WMI de associação Win32 \_ CIMLogicalDeviceCIMDataFile relaciona dispositivos lógicos e arquivos de dados, indicando os arquivos de driver usados pelo dispositivo. Essa classe é usada para descobrir quais drivers de dispositivo um dispositivo usa.
ms.assetid: 892272de-920d-4fa0-adbc-f584ed6e8748
ms.tgt_platform: multiple
title: Win32_CIMLogicalDeviceCIMDataFile classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CIMLogicalDeviceCIMDataFile
- Win32_CIMLogicalDeviceCIMDataFile.Dependent
- Win32_CIMLogicalDeviceCIMDataFile.Antecedent
- Win32_CIMLogicalDeviceCIMDataFile.Purpose
- Win32_CIMLogicalDeviceCIMDataFile.PurposeDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8124031c07091399241ce355eef0a499235892bff3875e4248641f0454671540
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917976"
---
# <a name="win32_cimlogicaldevicecimdatafile-class"></a>Classe Win32 \_ CIMLogicalDeviceCIMDataFile

A classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **Win32 \_ CIMLogicalDeviceCIMDataFile** relaciona dispositivos lógicos e arquivos de dados, indicando os arquivos de driver usados pelo dispositivo. Essa classe é usada para descobrir quais drivers de dispositivo um dispositivo usa.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C510-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CIMLogicalDeviceCIMDataFile : CIM_Dependency
{
  CIM_DataFile      REF Dependent;
  CIM_LogicalDevice REF Antecedent;
  uint16                Purpose;
  string                PurposeDescription;
};
```

## <a name="members"></a>Membros

A **classe Win32 \_ CIMLogicalDeviceCIMDataFile** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Win32 \_ CIMLogicalDeviceCIMDataFile** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ LogicalDevice**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

Um [**\_ LogicalDevice cim**](cim-logicaldevice.md) que representa as propriedades do dispositivo lógico que está sendo usado pelo arquivo de dados.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ DataFile**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ DataFile")
</dt> </dl>

Um [**Cim \_ DataFile**](cim-datafile.md) que representa as propriedades do arquivo de dados atribuído ao dispositivo lógico.

</dd> <dt>

**Finalidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")
</dt> </dl>

Função que o arquivo de dados desempenha em relação ao dispositivo lógico associado.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outros** (1)


</dt> <dd></dd> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>

**Driver** (2)


</dt> <dd></dd> <dt>

<span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>

**Software de configuração** (3)


</dt> <dd></dd> <dt>

<span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>

**Application Software** (4)


</dt> <dd></dd> <dt>

<span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>

**Instrumentação** (5)


</dt> <dd></dd> <dt>

<span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>

**Firmware** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**PurposeDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")
</dt> </dl>

Estende o valor da propriedade **Purpose** desta classe.

Exemplo: "Driver de Disquete"

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe Win32 \_ CIMLogicalDeviceCIMDataFile** é derivada da [**\_ Dependência CIM.**](cim-logicaldevice.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Dependência cim \_**](cim-dependency.md)
</dt> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

