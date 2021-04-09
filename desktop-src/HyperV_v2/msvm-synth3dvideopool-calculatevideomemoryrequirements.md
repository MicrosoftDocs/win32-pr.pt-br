---
description: Calcula a quantidade de memória de vídeo necessária para uma máquina virtual do RemoteFX.
ms.assetid: F8C30601-EDA3-47F1-A717-9FE7E9DB8F62
title: Método CalculateVideoMemoryRequirements da classe Msvm_Synth3dVideoPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synth3dVideoPool.CalculateVideoMemoryRequirements
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2a9fd80e777a9d166b896c2ce51d03bd91bbabfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090669"
---
# <a name="calculatevideomemoryrequirements-method-of-the-msvm_synth3dvideopool-class"></a>Método CalculateVideoMemoryRequirements da \_ classe Synth3dVideoPool Msvm

Calcula a quantidade de memória de vídeo necessária para uma máquina virtual do RemoteFX.

## <a name="syntax"></a>Sintaxe


```mof
uint32 CalculateVideoMemoryRequirements(
  [in]  uint32 monitorResolution,
  [in]  uint32 numberOfMonitors,
  [out] uint64 requiredVideoMemory
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*monitorResolution* \[ no\]
</dt> <dd>

A resolução máxima do monitor para a máquina virtual. Deve ser um dos valores a seguir.



| Valor                                                                        | Significado                                           |
|------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>0</dt> </dl> | A resolução máxima é 1024 768.<br/>  |
| <dl> <dt>1</dt> </dl> | A resolução máxima é 1280 1024.<br/> |
| <dl> <dt>2</dt> </dl> | A resolução máxima é 1600 1200.<br/> |
| <dl> <dt>3</dt> </dl> | A resolução máxima é 1920 1200.<br/> |



 

</dd> <dt>

*numberOfMonitors* \[ no\]
</dt> <dd>

O número máximo de monitores para a máquina virtual. O número mínimo de monitores é um e o máximo depende da resolução máxima da tela. A tabela a seguir define o número máximo de monitores permitidos para resoluções diferentes.



| Resolução             | Máximo de monitores |
|------------------------|------------------|
| 1024 768<br/>  | 4<br/>     |
| 1280 1024<br/> | 4<br/>     |
| 1600 1200<br/> | 3<br/>     |
| 1920 1200<br/> | 2<br/>     |



 

</dd> <dt>

*requiredVideoMemory* \[ fora\]
</dt> <dd>

Recebe a quantidade necessária de memória de vídeo, em bytes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um código de status, que pode ser um dos valores a seguir.



| Código/valor de retorno                                                                                                                                                                | Descrição                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**Concluído sem erro**</dt> <dt>0</dt> </dl>                    | Bem-sucedida.<br/>                                |
| <dl> <dt>**Parâmetros de método verificados-trabalho iniciado**</dt> <dt>4096</dt> </dl> | Trabalho iniciado.<br/>                               |
| <dl> <dt>32768</dt> <dt>**com falha**</dt> </dl>                                 | Falhou.<br/>                                    |
| <dl> <dt>**Acesso negado**</dt> <dt>32769</dt> </dl>                          | Acesso negado.<br/>                             |
| <dl> <dt>**Sem suporte**</dt> <dt>32770</dt> </dl>                          | Não há suporte.<br/>                             |
| <dl> O <dt>**status é desconhecido**</dt> <dt>32771</dt> </dl>                      | O status é desconhecido.<br/>                         |
| <dl> <dt>**Tempo limite**</dt> <dt>32772</dt> </dl>                                | Tempo limite.<br/>                                   |
| <dl> <dt>**Parâmetro inválido**</dt> <dt>32773</dt> </dl>                      | Um parâmetro não é válido.<br/>                  |
| <dl> O <dt>**sistema está em uso**</dt> <dt>32774</dt> </dl>                      | O sistema está em uso.<br/>                          |
| <dl> <dt>**Estado inválido para esta operação**</dt> <dt>32775</dt> </dl>       | O estado não é válido para esta operação.<br/> |
| <dl> <dt>**Tipo de dados incorreto**</dt> <dt>32776</dt> </dl>                    | Tipo de dados incorreto.<br/>                       |
| <dl> O <dt>**sistema não está disponível**</dt> <dt>32777</dt> </dl>                | O sistema não está disponível.<br/>                   |
| <dl> <dt>**Memória insuficiente**</dt> <dt>32778</dt> </dl>                          | Sem memória.<br/>                             |



 

## <a name="remarks"></a>Comentários

Esse método é normalmente chamado no sistema host para determinar se o host tem memória de vídeo disponível suficiente para hospedar uma máquina virtual do RemoteFX. Para fazer isso, você compara a quantidade de memória de vídeo calculada por esse método com a propriedade [**Msvm \_ PhysicalGPUInfo. AvailableVideoMemory**](msvm-physicalgpuinfo.md) para determinar se o computador host tem memória de vídeo disponível suficiente. Você pode usar essas informações para determinar se uma máquina virtual pode ser movida para o sistema host.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ PhysicalGPUInfo**](msvm-physicalgpuinfo.md)
</dt> <dt>

[**Msvm \_ Synth3dVideoPool**](msvm-synth3dvideopool.md)
</dt> </dl>

 

 




