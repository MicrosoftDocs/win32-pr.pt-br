---
description: Representa os parâmetros de entrada de vídeo analógicos de um monitor de computador.
ms.assetid: 87d4260d-06c7-4a76-a3a1-8f6e51e23d92
title: Classe WmiMonitorAnalogVideoInputParams
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorAnalogVideoInputParams
- WmiMonitorAnalogVideoInputParams.Active
- WmiMonitorAnalogVideoInputParams.CompositeSyncSupported
- WmiMonitorAnalogVideoInputParams.InstanceName
- WmiMonitorAnalogVideoInputParams.SeparateSyncsSupported
- WmiMonitorAnalogVideoInputParams.SerrationOfVsyncRequired
- WmiMonitorAnalogVideoInputParams.SetupExpected
- WmiMonitorAnalogVideoInputParams.SignalLevelStandard
- WmiMonitorAnalogVideoInputParams.SyncOnGreenVideoSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 900bf4353de0c81acb5aa2c69578256b0212a2c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922081"
---
# <a name="wmimonitoranalogvideoinputparams-class"></a>Classe WmiMonitorAnalogVideoInputParams

A classe WMI **WmiMonitorAnalogVideoInputParams** representa os parâmetros de entrada de vídeo analógicos de um monitor de computador. Os dados nessa classe correspondem aos dados na definição de entrada de vídeo do padrão de dados de identificação de vídeo estendido (E-EDID) avançado de associação de vídeo de eletrônicos (VESA). Uma instância dessa classe está disponível somente quando o valor da propriedade **VideoInputType** da classe [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) é "analógico".

## <a name="syntax"></a>Sintaxe

``` syntax
class WmiMonitorAnalogVideoInputParams : MSMonitorClass
{
  boolean Active;
  uint8   CompositeSyncSupported;
  string  InstanceName;
  uint8   SeparateSyncsSupported;
  uint8   SerrationOfVsyncRequired;
  uint8   SetupExpected;
  uint8   SignalLevelStandard;
  uint8   SyncOnGreenVideoSupported;
};
```

## <a name="members"></a>Membros

A classe **WmiMonitorAnalogVideoInputParams** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **WmiMonitorAnalogVideoInputParams** tem essas propriedades.

<dl> <dt>

**Ativo**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o monitor ativo.

</dd> <dt>

**CompositeSyncSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se há suporte para a sincronização composta.



| Valor                                                                              | Significado                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Há suporte para a sincronização composta na linha de sincronização horizontal.<br/>     |
| <dl> <dt>1 (0x1)</dt> </dl> | Não há suporte para a sincronização composta na linha de sincronização horizontal.<br/> |



 

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Nome da instância de monitor específica.

</dd> <dt>

**SeparateSyncsSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se há suporte para sincronizações separadas.



| Valor                                                                              | Significado                                      |
|------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Há suporte para sincronizações separadas.<br/>     |
| <dl> <dt>1 (0x1)</dt> </dl> | Não há suporte para sincronizações separadas.<br/> |



 

</dd> <dt>

**SerrationOfVsyncRequired**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o pulso de sincronização vertical serration é necessário.



| Valor                                                                              | Significado                                                                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Serration do pulso de sincronização vertical é necessário quando a sincronização de composição ou o vídeo de sincronização em verde é usado.<br/>     |
| <dl> <dt>1 (0x1)</dt> </dl> | Serration do pulso de sincronização vertical não é necessário quando a sincronização de composição ou o vídeo de sincronização em verde é usado.<br/> |



 

</dd> <dt>

**SetupExpected**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a configuração é esperada.



| Valor                                                                              | Significado                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | O monitor espera uma instalação em branco ou pedestal por padrão de nível de sinal apropriado.<br/>                      |
| <dl> <dt>1 (0x1)</dt> </dl> | O monitor não espera uma instalação em branco ou pedestal de acordo com o padrão de nível de sinal apropriado.<br/> |



 

</dd> <dt>

**SignalLevelStandard**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Padrão de nível de sinal para conexões EVC (conector de vídeo avançado).



| Valor                                                                              | Significado                     |
|------------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | 0,7, 0,3 \[ V\]<br/>     |
| <dl> <dt>1 (0x1)</dt> </dl> | 0.714, 0.286 \[ V\]<br/> |
| <dl> <dt>2 (0x2)</dt> </dl> | 1.0, 0.4 \[ V\]<br/>     |
| <dl> <dt>3 (0x3)</dt> </dl> | 0,7, 0,0 \[ V\]<br/>     |



 

</dd> <dt>

**SyncOnGreenVideoSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se há suporte para sincronização em verde.



| Valor                                                                              | Significado                                          |
|------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Há suporte para sincronização em vídeo verde.<br/>     |
| <dl> <dt>1 (0x1)</dt> </dl> | Não há suporte para sincronização em vídeo verde.<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | \\WMI raiz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




