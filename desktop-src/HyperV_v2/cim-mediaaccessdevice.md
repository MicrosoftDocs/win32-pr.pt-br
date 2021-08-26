---
description: Representa um dispositivo que pode usar a mídia para armazenar e recuperar dados.
ms.assetid: c63b1731-dbc0-4e5e-acb8-cd91b5569dd2
title: Classe CIM_MediaAccessDevice (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice
- CIM_MediaAccessDevice.Capabilities
- CIM_MediaAccessDevice.CapabilityDescriptions
- CIM_MediaAccessDevice.ErrorMethodology
- CIM_MediaAccessDevice.CompressionMethod
- CIM_MediaAccessDevice.NumberOfMediaSupported
- CIM_MediaAccessDevice.MaxMediaSize
- CIM_MediaAccessDevice.DefaultBlockSize
- CIM_MediaAccessDevice.MaxBlockSize
- CIM_MediaAccessDevice.MinBlockSize
- CIM_MediaAccessDevice.NeedsCleaning
- CIM_MediaAccessDevice.MediaIsLocked
- CIM_MediaAccessDevice.Security
- CIM_MediaAccessDevice.LastCleaned
- CIM_MediaAccessDevice.MaxAccessTime
- CIM_MediaAccessDevice.UncompressedDataRate
- CIM_MediaAccessDevice.LoadTime
- CIM_MediaAccessDevice.UnloadTime
- CIM_MediaAccessDevice.MountCount
- CIM_MediaAccessDevice.TimeOfLastMount
- CIM_MediaAccessDevice.TotalMountTime
- CIM_MediaAccessDevice.UnitsDescription
- CIM_MediaAccessDevice.MaxUnitsBeforeCleaning
- CIM_MediaAccessDevice.UnitsUsed
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bb97ded03cfc853fc0dde6ede26083be01cf218f210c31f947f315634599e179
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900256"
---
# <a name="cim_mediaaccessdevice-class-hyper-v-management"></a>Classe CIM_MediaAccessDevice (gerenciamento do Hyper-V)

Representa um dispositivo que pode usar a mídia para armazenar e recuperar dados.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices"), AMENDMENT]
class CIM_MediaAccessDevice : CIM_LogicalDevice
{
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   ErrorMethodology;
  string   CompressionMethod;
  uint32   NumberOfMediaSupported;
  uint64   MaxMediaSize;
  uint64   DefaultBlockSize;
  uint64   MaxBlockSize;
  uint64   MinBlockSize;
  boolean  NeedsCleaning;
  boolean  MediaIsLocked;
  uint16   Security;
  datetime LastCleaned;
  uint64   MaxAccessTime;
  uint32   UncompressedDataRate;
  uint64   LoadTime;
  uint64   UnloadTime;
  uint64   MountCount;
  datetime TimeOfLastMount;
  uint64   TotalMountTime;
  string   UnitsDescription;
  uint64   MaxUnitsBeforeCleaning;
  uint64   UnitsUsed;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ MediaAccessDevice** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **CIM \_ MediaAccessDevice** tem esses métodos.



| Método                                               | Descrição                                                            |
|:-----------------------------------------------------|:-----------------------------------------------------------------------|
| [**LockMedia**](cim-mediaaccessdevice-lockmedia.md) | Bloqueia e desbloqueia a mídia removível em um dispositivo de acesso à mídia.<br/> |



 

### <a name="properties"></a>Propriedades

A classe **CIM \_ MediaAccessDevice** tem essas propriedades.

<dl> <dt>

**Funcionalidades**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|dispositivos DMTF Armazenamento \| 1,9 "," MIF. \|dispositivos DMTF Armazenamento \| 1,11 "," MIF. \|dispositivos DMTF Armazenamento \| 1,12 "," MIF. \|Discos DMTF \| 3,7 "," MIF. \|Disco do host DMTF \| 1,2 "," MIF. \|Disco do host DMTF \| 1,4 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**CapabilityDescriptions**")
</dt> </dl>

Uma matriz que contém os recursos do dispositivo de acesso à mídia.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

**Acesso sequencial** (2)


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

**Acesso aleatório** (3)


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

**Dá suporte à gravação** (4)


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

**Criptografia** (5)


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

**Compactação** (6)


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

**Dá suporte à mídia removida** (7)


</dt> <dd></dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

**Limpeza manual** (8)


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

**Limpeza automática** (9)


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

**Notificação inteligente** (10)


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

**Dá suporte à mídia de dois lados** (11)


</dt> <dd></dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

**Ejeção de desmontagem não necessária** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM MediaAccessDevice**.**Recursos**")
</dt> </dl>

Uma matriz de descrições de recursos para os itens na matriz de **recursos** .

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do algoritmo ou da ferramenta usada pelo dispositivo para dar suporte à compactação.

Se um tipo de compactação não for especificado, um dos seguintes valores poderá ser usado:

-   O suporte à compactação "desconhecida" é desconhecido ou não foi especificado.
-   Há suporte para compactação "compactada", mas o tipo é desconhecido ou não especificado.
-   "Não compactado" o dispositivo não oferece suporte a recursos de compactação.

</dd> <dt>

**Defaultblockize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **PUnit** ("byte")
</dt> </dl>

O tamanho do bloco padrão, em bytes, para o dispositivo.

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tipo de detecção de erros e correção com suporte do dispositivo.

</dd> <dt>

**LastCleaned**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A data e a hora da última limpeza do dispositivo.

</dd> <dt>

**Loadtime**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milissegundos"), **PUnit** ("segundo \* 10 ^-3")
</dt> </dl>

O tempo necessário, em milissegundos, para que o dispositivo possa ler ou gravar uma mídia depois que o dispositivo começar a ser carregado. Por exemplo, para unidades de disco, esse é o intervalo entre um disco que não está girando para o disco relatando que está pronto para operações de leitura/gravação. Para unidades de fita, isso é iniciado quando a mídia é inserida e termina quando a unidade relata que está pronta para um aplicativo. Isso geralmente está na área de BOT (início de fita) da fita.

</dd> <dt>

**MaxAccessTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milissegundos"), **PUnit** ("segundo \* 10 ^-3")
</dt> </dl>

O tempo de acesso máximo da mídia, em milissegundos. Para uma unidade de disco, isso representa a busca completa e o atraso de rotação completo. Para unidades de fita, isso representa uma pesquisa desde o início da fita até o ponto distante fisicamente.

</dd> <dt>

**MaxBlockSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **PUnit** ("byte")
</dt> </dl>

O tamanho máximo do bloco, em bytes, para a mídia acessada pelo dispositivo.

</dd> <dt>

**MaxMediaSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de acesso sequencial DMTF \| 1,2 "," MIF. \|Disco do host DMTF \| 1,5 ")
</dt> </dl>

O tamanho máximo, em kilobytes, da mídia com suporte neste dispositivo.

</dd> <dt>

**MaxUnitsBeforeCleaning**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**UnitsDescription**")
</dt> </dl>

O número máximo de unidades que podem ser usadas antes de o dispositivo ser limpo. **UnitsDescription** define como o tipo de unidade.

</dd> <dt>

**MediaIsLocked**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

**true** se a mídia estiver bloqueada no dispositivo e não puder ser ejetada; caso contrário, **false**. Para dispositivos não removíveis, esse valor deve ser **true**.

</dd> <dt>

**MinBlockSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")
</dt> </dl>

O tamanho mínimo do bloco, em bytes, para mídia acessada pelo dispositivo.

</dd> <dt>

**MountCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **Contador**
</dt> </dl>

O número de vezes que a mídia foi montada para transferência de dados ou para limpar o dispositivo. Se o dispositivo não dá suporte a mídia removível, essa propriedade deve ser definida como zero.

</dd> <dt>

**NeedsCleaning**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

**true** se o dispositivo precisar de limpeza; caso contrário, **false.**

> [!Note]  
> A **propriedade Recursos** indica se a limpeza manual ou automática é possível.

 

</dd> <dt>

**NumberOfMediaSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se o dispositivo dá suporte a várias mídias individuais, essa propriedade define o número máximo que pode ser compatível ou inserido.

</dd> <dt>

**Segurança**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Discos DMTF \| \| 003.22")
</dt> </dl>

A segurança operacional do dispositivo.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nenhum** (3)


</dt> <dd></dd> <dt>

<span id="Read_Only"></span><span id="read_only"></span><span id="READ_ONLY"></span>

**Somente leitura** (4)


</dt> <dd></dd> <dt>

<span id="Locked_Out"></span><span id="locked_out"></span><span id="LOCKED_OUT"></span>

**Bloqueado** (5)


</dt> <dd></dd> <dt>

<span id="Boot_Bypass"></span><span id="boot_bypass"></span><span id="BOOT_BYPASS"></span>

**Bypass de inicialização** (6)


</dt> <dd></dd> <dt>

<span id="Boot_Bypass_and_Read_Only"></span><span id="boot_bypass_and_read_only"></span><span id="BOOT_BYPASS_AND_READ_ONLY"></span>

**Bypass de inicialização e somente leitura** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**TimeOfLastMount**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A data e a hora mais recentes em que a mídia foi montada no dispositivo. Essa propriedade só é usada por dispositivos que suportam mídia removível.

</dd> <dt>

**TotalMountTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tempo, em segundos, em que a mídia foi montada para transferência de dados ou para limpar o dispositivo. Se o dispositivo não dá suporte a mídia removível, essa propriedade deve ser definida como zero.

</dd> <dt>

**UncompressedDataRate**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("QuiloBytes por Segundo"), **PUnit** ("byte / segundo \* 10^3")
</dt> </dl>

A taxa de transferência de dados sustentada em quilobytes na qual o dispositivo pode ler e gravar em uma mídia. Essa é uma taxa de dados bruta e sustentada. Taxas máximas ou taxas com compactação não devem ser relatadas nesta propriedade.

</dd> <dt>

**UnitsDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**MaxUnitsBeforeCleaning**", "**CIM \_ MediaAccessDevice**.**UnitsUsed**")
</dt> </dl>

Descreve o tipo de unidade das **propriedades MaxUnitsBeforeCleaning** e **UnitsUsed.**

</dd> <dt>

**UnidadesUsadas**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Medidor**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**UnitsDescription**", "**CIM \_ MediaAccessDevice**.**MaxUnitsBeforeCleaning**")
</dt> </dl>

O número de unidades usadas pelo dispositivo. Essa propriedade é usada para determinar quando o dispositivo deve ser limpo. **UnitsDescription define** como o tipo de unidade.

</dd> <dt>

**UnloadTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("segundo \* 10^-3")
</dt> </dl>

O tempo necessário, em milissegundos, para o dispositivo fazer a transição da leitura ou da escrita da mídia para o descarregamento. Por exemplo, para unidades de disco, esse é o intervalo entre um disco girando em velocidades nominais e um disco não girando. Para unidades de fita, esse é o momento para uma mídia passar de seu BOT para ser totalmente ejetada e acessível a um elemento selador ou operador humano.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

