---
description: Ajusta a coordenada z do controle de roda do dispositivo apontador.
ms.assetid: FF1929EE-4A2D-4761-8919-488369FAEE1F
title: Método SetScrollPosition da classe Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.SetScrollPosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ffec8e05acf2210c55038edde5def8373e900ed7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829021"
---
# <a name="setscrollposition-method-of-the-msvm_ps2mouse-class"></a>Método SetScrollPosition da \_ classe Ps2Mouse Msvm

Ajusta a coordenada z do controle de roda do dispositivo apontador. Os valores gravados nessa propriedade são sempre deslocamentos de coordenadas relativos.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetScrollPosition(
  [in] sint8 scrollPositionDelta
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*scrollPositionDelta* \[ no\]
</dt> <dd>

Tipo: **sint8**

O Delta da posição de rolagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Um valor de retorno igual A zero indica êxito. Um valor diferente de zero indica uma falha ao alterar a posição de rolagem.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Parâmetros de método marcados-trabalho iniciado** (4096)
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

## <a name="remarks"></a>Comentários

O acesso à classe [**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md) pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md)
</dt> </dl>

 

