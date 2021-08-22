---
description: Remove parâmetros DH-CHAP (Diffie Hellman – Challenge Handshake Authentication Protocol) de uma porta Fibre Channel sintética em uma máquina virtual.
ms.assetid: f15673e2-287d-4e87-bee4-6c0f5f9178c8
title: Método RemoveFibreChannelChap da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9b934839f6d908594ee58f0838c884fdedc48f372de061482ddf2147123a351c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147789"
---
# <a name="removefibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método RemoveFibreChannelChap da classe Msvm \_ VirtualSystemManagementService

Remove parâmetros DH-CHAP (Diffie Hellman – Challenge Handshake Authentication Protocol) de uma porta Fibre Channel sintética em uma máquina virtual. Esse método falhará se a máquina virtual estiver em execução.

## <a name="syntax"></a>Sintaxe


```mof
uint32 RemoveFibreChannelChap(
  [in] string FcPortSettings[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FcPortSettings* \[ Em\]
</dt> <dd>

Uma matriz de cadeias de caracteres que contêm uma instância inserida da classe [**Msvm \_ SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) que define as portas Fibre Channel sintéticas das quais remover os parâmetros DH-CHAP. A **propriedade InstanceID** de cada uma dessas instâncias identifica os elementos a serem modificados.

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

**O status é desconhecido** (32771)
</dt> <dt>

**Tempoout** (32772)
</dt> <dt>

**Parâmetro inválido** (32773)
</dt> <dt>

**O sistema está em uso** (32774)
</dt> <dt>

**Estado inválido para esta operação** (32775)
</dt> <dt>

**Tipo de dados incorreto** (32776)
</dt> <dt>

**O sistema não está disponível** (32777)
</dt> <dt>

**Memória sem memória** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




