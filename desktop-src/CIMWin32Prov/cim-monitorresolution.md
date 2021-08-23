---
description: A classe CIM MonitorResolution representa a relação entre resoluções horizontais e verticais e a taxa de atualização e o modo de verificação \_ para um monitor da área de trabalho. Os valores são especificados no objeto do controlador de vídeo.
ms.assetid: 064620dd-2d92-42d0-9167-35867830a077
ms.tgt_platform: multiple
title: CIM_MonitorResolution classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MonitorResolution
- CIM_MonitorResolution.Caption
- CIM_MonitorResolution.Description
- CIM_MonitorResolution.SettingID
- CIM_MonitorResolution.HorizontalResolution
- CIM_MonitorResolution.MaxRefreshRate
- CIM_MonitorResolution.MinRefreshRate
- CIM_MonitorResolution.RefreshRate
- CIM_MonitorResolution.ScanMode
- CIM_MonitorResolution.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: aa1fd025c87b3b497e400351aed91af71bf4958f3ee8748bf5d23255540dc6cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506707"
---
# <a name="cim_monitorresolution-class"></a>Classe CIM \_ MonitorResolution

A **classe CIM \_ MonitorResolution** representa a relação entre resoluções horizontais e verticais e a taxa de atualização e o modo de verificação para um monitor da área de trabalho. Os valores são especificados no objeto do controlador de vídeo.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{1008CCEC-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_MonitorResolution : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 HorizontalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint32 RefreshRate;
  uint16 ScanMode;
  uint32 VerticalResolution;
};
```

## <a name="members"></a>Membros

A **classe CIM \_ MonitorResolution** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ MonitorResolution** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Descrição textual curta do objeto atual.

Essa propriedade é herdada da [**Configuração cim \_**](cim-setting.md).

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição textual do objeto atual.

Essa propriedade é herdada da [**Configuração cim \_**](cim-setting.md).

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Resoluções do Monitor DMTF \| \| 002.2"), [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")
</dt> </dl>

Resolução horizontal do monitor, em pixels.

</dd> <dt>

**MaxRefreshRate**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Resoluções do Monitor DMTF \| \| 002.7"), [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")
</dt> </dl>

Taxa máxima de atualização do monitor, em hertz, quando há suporte para um intervalo de taxas nas resoluções especificadas.

</dd> <dt>

**MinRefreshRate**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Resoluções do Monitor DMTF \| \| 002.6"), [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")
</dt> </dl>

Taxa de atualização mínima do monitor, em hertz, quando há suporte para um intervalo de taxas nas resoluções especificadas.

</dd> <dt>

**Taxa de atualização**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Resoluções do Monitor DMTF \| \| 002.4"), [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")
</dt> </dl>

Taxa de atualização do monitor, em hertz. Se um intervalo de taxas for suportado, use as propriedades **MinRefreshRate** e **MaxRefreshRate** e de definir essa propriedade como 0.

</dd> <dt>

**ScanMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Resoluções do Monitor DMTF \| \| 002.5")
</dt> </dl>

Modo de verificação que o monitor usa.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

**Sem suporte** (3)


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

**Operação não entrelaçada** (4)


</dt> <dd></dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

**Operação entrelaçadas** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**Settingid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Serve como parte da chave para a instância atual.

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Resoluções do Monitor DMTF \| \| 002.3"), [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")
</dt> </dl>

Resolução vertical do monitor em pixels.

</dd> </dl>

## <a name="remarks"></a>Comentários

O WMI não implementa essa classe.

Esta documentação é derivada das descrições da classe CIM publicadas pelo DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, estar em conformidade com os padrões de documentação do SDK da Microsoft ou fornecer mais informações.

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

[**Configuração cim \_**](cim-setting.md)
</dt> </dl>

 

