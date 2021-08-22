---
description: Desloca a posição do ponteiro do mouse pelos deltas horizontais e verticais especificados.
ms.assetid: C74E4BEA-C7E1-44C7-B4FC-8926F23DF1FE
title: Método SetRelativePosition da classe Msvm_Ps2Mouse classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.SetRelativePosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: dc3b0915795142b725ce26a2b8eac09dca613dc6094495fd3c188ba58aecbf1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147729"
---
# <a name="setrelativeposition-method-of-the-msvm_ps2mouse-class"></a>Método SetRelativePosition da classe Msvm \_ Ps2Mouse

Desloca a posição do ponteiro do mouse pelos deltas horizontais e verticais especificados.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetRelativePosition(
  [in] sint8 horizontalDelta,
  [in] sint8 verticalDelta
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*horizontalDelta* \[ Em\]
</dt> <dd>

Tipo: **sint8**

A alteração horizontal para a posição do mouse, em pixels.

</dd> <dt>

*verticalDelta* \[ Em\]
</dt> <dd>

Tipo: **sint8**

A alteração vertical para a posição do mouse, em pixels.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Um valor de retorno de zero indica êxito. Um valor não zero indica uma falha ao alterar a posição do mouse.

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

O acesso à [**classe Msvm \_ Ps2Mouse**](msvm-ps2mouse.md) pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md)
</dt> </dl>

 

