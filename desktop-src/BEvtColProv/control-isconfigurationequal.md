---
description: Compare o argumento com a configuração ativa do coletor.
ms.assetid: 8decb674-c905-4eb6-9f78-7bc7b99db908
ms.tgt_platform: multiple
title: Método IsConfigurationEqual da classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.IsConfigurationEqual
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: fb471f144a39519f1f724db458b57b624db2846d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646221"
---
# <a name="isconfigurationequal-method-of-the-control-class"></a>Método IsConfigurationEqual da classe Control

Compare o argumento com a configuração ativa do coletor.

## <a name="syntax"></a>Sintaxe


```mof
Uint32 IsConfigurationEqual(
  [in] string Config
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Configuração* \[ do no\]
</dt> <dd>

A configuração para comparar com a configuração ativa.

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

 

 




