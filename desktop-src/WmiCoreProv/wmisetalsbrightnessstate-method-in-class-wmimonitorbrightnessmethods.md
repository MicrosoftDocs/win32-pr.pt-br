---
description: Usado para controlar o estado de brilho do sensor de luz ambiente.
ms.assetid: ff400d4e-be8c-450b-ad53-d43b0ab84ab3
title: Método WmiSetALSBrightnessState da classe WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetALSBrightnessState
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 1c8a99ea92391626975d635802f82dd81b663247f4bb3522db19d14237d920f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051114"
---
# <a name="wmisetalsbrightnessstate-method-of-the-wmimonitorbrightnessmethods-class"></a>Método WmiSetALSBrightnessState da classe WmiMonitorBrightnessMethods

O **método WmiSetALSBrightnessState** é usado para controlar o estado de brilho do sensor de luz ambiente. Se uma substituição de brilho ativo tiver sido estabelecida usando o método [**WmiSetBrightness,**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) essa substituição terá precedência sobre o brilho ALS definido usando esse método. Para que uma substituição de brilho alS habilitada entre em vigor, a política de brilho deve ser revertida usando o [**método WmiRevertToPolicyBrightness.**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md)

## <a name="syntax"></a>Sintaxe


```mof
uint32 WmiSetALSBrightnessState(
   boolean State
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*State* 
</dt> <dd>

Estado de brilho de ALS. False desabilita a substituição de brilho de ALS e true o habilita.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna zero (0) para indicar êxito. Qualquer outro número indica um erro. Para obter mais informações sobre códigos de erro, consulte [**Constantes de**](/windows/desktop/WmiSdk/wmi-error-constants) erro WMI ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | WMI \\ raiz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**WmiMonitorBrightnessMethods**](wmimonitorbrightnessmethods.md)
</dt> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

