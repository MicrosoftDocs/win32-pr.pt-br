---
description: Recupera o estado da chave de uma chave.
ms.assetid: 4AEB732D-274E-42BB-AA97-9E4D30B81338
title: Método IsKeyPressed da classe Msvm_Keyboard classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.IsKeyPressed
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bb8b4e2da0a6f1cd3c30e3d65404ecf308c71e88483e322193497216586b20b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392439"
---
# <a name="iskeypressed-method-of-the-msvm_keyboard-class"></a>Método IsKeyPressed da classe Teclado Msvm \_

Recupera o estado da chave de uma chave.

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsKeyPressed(
  [in]  uint32  keyCode,
  [out] boolean keyState
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*keyCode* \[ Em\]
</dt> <dd>

Tipo: **uint32**

O código de chave virtual da chave a ser consultada. Para ver a lista de códigos de chave virtual, consulte [**Códigos de chave virtual.**](../inputdev/virtual-key-codes.md)

</dd> <dt>

*keyState* \[ out\]
</dt> <dd>

Tipo: **booliana**

O estado down atual da chave. Um **valor True** significa que a chave está inobada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Um valor de retorno de zero indica êxito. Um valor não zero indica uma falha ao consultar o estado da chave.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Parâmetros de método verificados – Trabalho iniciado** (4096)
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

**O sistema está em usado** (32774)
</dt> <dt>

**Estado inválido para esta operação** (32775)
</dt> <dt>

**Tipo de dados incorreto** (32776)
</dt> <dt>

**O sistema não está disponível** (32777)
</dt> <dt>

**Memória sem memória** (32778)
</dt> </dl>

## <a name="remarks"></a>Comentários

O **método IsKeyPressed** sempre retornará **False** para o **\_ MENU da VK** (18), CONTROLE **de VK \_** (17) e **SHIFT da VK \_** (16) porque essas não são chaves reais em um teclado. Esses códigos de chave virtual são sempre mapeados para **\_ LMENU** da VK (164), **VK \_ LCONTROL** (162) e **VK \_ LSHIFT** (160), respectivamente, pelos métodos [**PressKey**](presskey-msvm-keyboard.md) e [**ReleaseKey.**](releasekey-msvm-keyboard.md)

O acesso à [**classe \_ Teclado Msvm**](msvm-keyboard.md) pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**Teclado Msvm \_**](msvm-keyboard.md)
</dt> <dt>

[**Códigos de chave virtual**](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

