---
description: Leia a configuração ativa do coletor.
ms.assetid: ea26142d-5dcd-466d-b9df-5349f58a190f
ms.tgt_platform: multiple
title: Método GetConfiguration da classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.GetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 5adfedb833043ffc56da09c7bdab95c1c4698587
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920141"
---
# <a name="getconfiguration-method-of-the-control-class"></a>Método GetConfiguration da classe Control

Leia a configuração ativa do coletor.

## <a name="syntax"></a>Sintaxe


```mof
Uint32 GetConfiguration(
  [out] Uint32 TimestampLow,
  [out] Uint32 TimestampHigh
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TimestampLow* \[ fora\]
</dt> <dd>

Quando esse método retorna, esse parâmetro contém os bits de ordem inferior de um carimbo de data/hora que indica quando a configuração foi definida.

</dd> <dt>

*TimestampHigh* \[ fora\]
</dt> <dd>

Quando esse método retorna, esse parâmetro contém os bits de ordem superior de um carimbo de data/hora que indica quando a configuração foi definida.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

<dl> <dt>


</dt> <dd>

0

Falha

</dd> <dt>


</dt> <dd>

1

Sucesso

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                       |
| Namespace<br/>                | Raiz \\ do Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

 




