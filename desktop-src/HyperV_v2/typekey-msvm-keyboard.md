---
description: Simula uma sequência de teclas de liberação de prensa.
ms.assetid: 4166BA71-315D-41BD-857C-48AFB702911E
title: Método TypeKey da classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1b978da48600cc52472ab8bdec011ddbaa5ff624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922553"
---
# <a name="typekey-method-of-the-msvm_keyboard-class"></a>Método TypeKey da classe de \_ teclado Msvm

Simula uma sequência de teclas de liberação de prensa. Isso é equivalente a chamar [**PressKey**](presskey-msvm-keyboard.md) seguido por [**ReleaseKey**](releasekey-msvm-keyboard.md).

## <a name="syntax"></a>Sintaxe


```mof
uint32 TypeKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*KeyCode* \[ no\]
</dt> <dd>

Tipo: **UInt32**

O código de chave virtual da chave a ser pressionada. Para obter a lista de códigos de chave virtual, consulte [**códigos de chave virtual**](../inputdev/virtual-key-codes.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Um valor de retorno igual A zero indica êxito. Um valor diferente de zero indica uma falha ao modificar o estado da chave.

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
</dt> <dt>

[**Códigos de chave virtual**](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

