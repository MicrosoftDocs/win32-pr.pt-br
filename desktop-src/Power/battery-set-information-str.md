---
description: Contém informações de bateria a serem definidas.
ms.assetid: 535e56cb-2bab-458a-84a8-2d9a4d96412b
title: BATTERY_SET_INFORMATION estrutura (Poclass.h)
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
ms.openlocfilehash: c53e9c539f8ef20b184c6c056999c7c541f3c1718bafaa58c0b1e20dcef16a97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143609"
---
# <a name="battery_set_information-structure"></a>Estrutura DE INFORMAÇÕES DO CONJUNTO \_ \_ DE BATERIA

Contém informações de bateria a serem definidas. Essa estrutura é usada com o código [**de controle IOCTL \_ BATTERY SET \_ \_ INFORMATION.**](ioctl-battery-set-information.md)

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

A marca da bateria atual para a bateria. As informações de uma bateria que corresponde à marca só podem ser retornadas. Sempre que esse valor não corresponder à marca atual da bateria, a solicitação IOCTL será concluída com ERROR FILE NOT FOUND, que indica ao chamador que a bateria para a qual ela tem uma marca não existe \_ \_ \_ mais. O chamador pode optar por usar a operação [**IOCTL \_ BATTERY \_ QUERY \_ TAG**](ioctl-battery-query-tag.md) para determinar a marca da bateria recém-instalada, se houver. (Consulte [Marcas de bateria](battery-information.md) para obter mais informações.)

Quando uma solicitação de informações de consulta é feita, esse valor é verificado. Além disso, se a solicitação estiver em andamento enquanto esse valor mudar, a solicitação será anulada com o status ARQUIVO \_ DE ERRO \_ NÃO \_ ENCONTRADO.

</dd> <dt>

**InformationLevel**
</dt> <dd>

As informações da bateria a serem definidas. O tipo de dados no **membro Buffer** depende do valor desse membro. Esse membro pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryCharge"></span><span id="batterycharge"></span><span id="BATTERYCHARGE"></span><dl> <dt>**BatteryCharge**</dt> <dt>1</dt> </dl>                         | Informa ao dispositivo de bateria que o usuário solicitou que a bateria deve ser carregada no momento. Por exemplo, com uma bateria/bateria/bateria/seletor inteligente, o aplicativo pode carregar uma bateria por vez. O **membro** buffer dessa estrutura é ignorado.<br/>                                                                      |
| <span id="BatteryCriticalBias"></span><span id="batterycriticalbias"></span><span id="BATTERYCRITICALBIAS"></span><dl> <dt>**BatteryCriticalBias**</dt> <dt>0</dt> </dl> | Define o ajuste de desvio crítico da bateria. Observe que não é previsto que esse valor normalmente seria alterado pelo software e está presente nas interfaces apenas como um recurso de manutenção. Nem todas as baterias podem manter essa configuração e as informações da bateria devem ser lidas para confirmar que a bateria aceitou a configuração.<br/> |
| <span id="BatteryDischarge"></span><span id="batterydischarge"></span><span id="BATTERYDISCHARGE"></span><dl> <dt>**BatteryDischarge**</dt> <dt>2</dt> </dl>             | Informa ao dispositivo de bateria que o usuário solicitou que a bateria seja descarregada no momento. Por exemplo, isso pode ser usado para indicar qual bateria o usuário deseja energia no sistema no momento. O **membro** buffer dessa estrutura é ignorado.<br/>                                                                          |



 

</dd> <dt>

**Buffer**
</dt> <dd>

As informações da bateria a serem definidas. Os dados dependem do valor **de InformationLevel.**

</dd> </dl>

## <a name="remarks"></a>Comentários

A **estrutura BATTERY SET \_ \_ INFORMATION** é uma estrutura de comprimento variável e você deve alocar um buffer de tamanho adequado para que as informações sejam incluídas na estrutura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Cabeçalho<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>Batclass.h no Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INFORMAÇÕES DO CONJUNTO DE BATERIA IOCTL \_ \_ \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

 




