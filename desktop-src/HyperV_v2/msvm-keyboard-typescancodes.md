---
description: Simula uma sequência de chaves usando códigos de verificação.
ms.assetid: F67D2FBA-3CE0-4135-9043-FAB59381DE3C
title: Método TypeScancodes da classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeScancodes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 97479a1a0926894f72472b7459f77cd9325ac6fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647364"
---
# <a name="typescancodes-method-of-the-msvm_keyboard-class"></a>Método TypeScancodes da classe de \_ teclado Msvm

Simula uma sequência de chaves usando códigos de verificação.

## <a name="syntax"></a>Sintaxe


```mof
uint32 TypeScancodes(
  [in] uint8 Scancodes[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Scancodes* \[ no\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Uma matriz que contém os códigos de verificação a serem digitados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará 0 se tiver sucesso. Qualquer outro valor de retorno indica um erro. O valor de retorno pode ser um dos valores a seguir.

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

O acesso à classe de [**\_ teclado Msvm**](msvm-keyboard.md) pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_Teclado Msvm**](msvm-keyboard.md)
</dt> </dl>

 

