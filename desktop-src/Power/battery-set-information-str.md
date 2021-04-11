---
description: Contém as informações da bateria a serem definidas.
ms.assetid: 535e56cb-2bab-458a-84a8-2d9a4d96412b
title: Estrutura de BATTERY_SET_INFORMATION (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 0b23489bc5a7608e2e8afb297bb4be7ba35cecb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091633"
---
# <a name="battery_set_information-structure"></a>Estrutura de informações de \_ conjunto de bateria \_

Contém as informações da bateria a serem definidas. Essa estrutura é usada com o código de controle de [**informações do conjunto de baterias do IOCTL \_ \_ \_**](ioctl-battery-set-information.md) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _BATTERY_SET_INFORMATION {
  ULONG                         BatteryTag;
  BATTERY_SET_INFORMATION_LEVEL InformationLevel;
  UCHAR                         Buffer[1];
} BATTERY_SET_INFORMATION, *PBATTERY_SET_INFORMATION;
```



## <a name="members"></a>Membros

<dl> <dt>

**BatteryTag**
</dt> <dd>

A marca de bateria atual para a bateria. As informações para uma bateria que correspondem à marca só podem ser retornadas. Sempre que esse valor não corresponder à marca atual da bateria, a solicitação de IOCTL será concluída com o \_ arquivo \_ de erro não \_ encontrado, que indica ao chamador que a bateria para a qual ela tem uma marca não existe mais. O chamador pode optar por usar a operação de [**\_ \_ \_ marca de consulta da bateria do IOCTL**](ioctl-battery-query-tag.md) para determinar a marca da bateria recém-instalada, se existir uma. (Consulte [marcas de bateria](battery-information.md) para obter mais informações.)

Quando uma solicitação de informações de consulta é feita, esse valor é verificado. Além disso, se a solicitação estiver em andamento enquanto esse valor for alterado, a solicitação será anulada com o status do \_ arquivo de erro \_ não \_ encontrado.

</dd> <dt>

**InformationLevel**
</dt> <dd>

As informações da bateria a serem definidas. O tipo de dados no membro do **buffer** depende do valor desse membro. Esse membro pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryCharge"></span><span id="batterycharge"></span><span id="BATTERYCHARGE"></span><dl> <dt>**BatteryCharge**</dt> <dt>1</dt> </dl>                         | Informa ao dispositivo de bateria que o usuário solicitou que a bateria deve cobrar no momento. Por exemplo, com uma bateria/carregador/seletor inteligente, o aplicativo pode cobrar uma bateria por vez. O membro de **buffer** dessa estrutura é ignorado.<br/>                                                                      |
| <span id="BatteryCriticalBias"></span><span id="batterycriticalbias"></span><span id="BATTERYCRITICALBIAS"></span><dl> <dt>**BatteryCriticalBias**</dt> <dt>0</dt> </dl> | Define o ajuste de tendência crítica da bateria. Observe que esse valor normalmente seria alterado pelo software, e está presente no recurso interfaces somente como uma manutenção de recursos. Nem todas as baterias podem manter essa configuração, e as informações da bateria devem ser lidas para confirmar que a bateria aceitou a configuração.<br/> |
| <span id="BatteryDischarge"></span><span id="batterydischarge"></span><span id="BATTERYDISCHARGE"></span><dl> <dt>**BatteryDischarge**</dt> <dt>2</dt> </dl>             | Informa ao dispositivo de bateria que o usuário solicitou que a bateria está sendo descarregada no momento. Por exemplo, isso pode ser usado para indicar a bateria que o usuário deseja para ligar o sistema no momento. O membro de **buffer** dessa estrutura é ignorado.<br/>                                                                          |



 

</dd> <dt>

**Buffer**
</dt> <dd>

As informações da bateria a serem definidas. Os dados dependem do valor de **InformationLevel**.

</dd> </dl>

## <a name="remarks"></a>Comentários

A estrutura de **\_ \_ informações do conjunto de bateria** é uma estrutura de comprimento variável e você deve alocar um buffer de tamanho adequado para que as informações sejam incluídas na estrutura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                                                                                                                                                                                |
| parâmetro<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>Batclass. h no Windows server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_informações do \_ conjunto de baterias do IOCTL \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

 




