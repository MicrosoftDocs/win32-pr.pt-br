---
description: Simula um clique do botão de dispositivo especificado.
ms.assetid: 77CFA2E9-E422-464C-B124-6F7D3D56BA4C
title: Método ClickButton da classe Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.ClickButton
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8209e12d6bef02a048b783c98a0299a32ec5ffb96e964ebb7d776e351daecedb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119254496"
---
# <a name="clickbutton-method-of-the-msvm_ps2mouse-class"></a>Método ClickButton da \_ classe Ps2Mouse Msvm

Simula um clique do botão de dispositivo especificado. Isso é equivalente a chamar [**Setbuttonstate**](setbuttonstate-msvm-syntheticmouse.md) duas vezes, primeiro para pressionar o botão e novamente para liberá-lo.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ClickButton(
  [in] uint32 buttonIndex
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*buttonIndex* \[ no\]
</dt> <dd>

Tipo: **UInt32**

O índice de base 1 do botão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **UInt32**

Um valor de retorno igual A zero indica êxito. Um valor diferente de zero indica uma falha ao modificar o estado do botão.

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
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md)
</dt> </dl>

 

