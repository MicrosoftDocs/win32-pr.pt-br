---
description: Gera um conjunto de WWNs (World Wide Port Names).
ms.assetid: 36f393eb-6f34-4ae3-a976-c5da60211f3e
title: Método GenerateWwpn da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GenerateWwpn
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1952954d107185fdcc31634b9d0e19bd4cd3450db5a63d78aa3ef823cdf38afe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119532516"
---
# <a name="generatewwpn-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método GenerateWwpn da \_ classe VirtualSystemManagementService Msvm

Gera um conjunto de WWNs (World Wide Port Names). Os WWPNs são gerados de dentro do intervalo pré-configurado definido pelas propriedades **MinimumWWPNAddress** e **MaximumWWPNAddress** da classe [**Msvm \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) . Se o número válido de WWPNs que pode ser gerado for menor que o número solicitado, as entradas restantes na matriz *GeneratedWwpn* terão a entrada inválida de "0000000000000000" e o valor de retorno indicará êxito (0).

## <a name="syntax"></a>Sintaxe


```mof
uint32 GenerateWwpn(
  [in]  uint32 NumberOfWwpns,
  [out] string GeneratedWwpn[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NumberOfWwpns* \[ no\]
</dt> <dd>

O número de WWPNs a ser gerado.

</dd> <dt>

*GeneratedWwpn* \[ fora\]
</dt> <dd>

Uma matriz de cadeias de caracteres, cada uma delas conterá um WWPN gerado. Ele será formatado em formato de cadeia de caracteres como "01:23:45:67:89: AB: CD: EF".

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos valores a seguir.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Falha** (32768)
</dt> <dt>

**Acesso negado** (32769)
</dt> <dt>

**Sem suporte** (32770)
</dt> <dt>

O **status é desconhecido** (32771)
</dt> <dt>

**Tempo limite** (32772)
</dt> <dt>

**Parâmetro inválido** (32773)
</dt> <dt>

O **sistema está em uso** (32774)
</dt> <dt>

**Estado inválido para esta operação** (32775)
</dt> <dt>

**Tipo de dados incorreto** (32776)
</dt> <dt>

O **sistema não está disponível** (32777)
</dt> <dt>

**Memória insuficiente** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




