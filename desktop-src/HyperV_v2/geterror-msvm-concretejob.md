---
description: Método GetError da classe Msvm_ConcreteJob - recupera o objeto de erro para o trabalho, se houver um.
ms.assetid: 7E810CBE-F18F-4EFA-B52E-631CD071D136
title: Método GetError da classe Msvm_ConcreteJob dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c169636931ff0d284d20cb616450a5a716848dd074347f3e96abafd4a153693a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682426"
---
# <a name="geterror-method-of-the-msvm_concretejob-class"></a>Método GetError da classe Msvm \_ ConcreteJob

Recupera o objeto de erro para o trabalho, se houver um. Quando o trabalho está em execução ou foi encerrado sem erro, esse método não retorna um [**objeto de \_ erro CIM.**](/previous-versions//cc150671(v=vs.85)) No entanto, se o trabalho tiver falhado devido a algum problema interno ou porque o trabalho foi encerrado por um cliente, uma instância de Erro **CIM \_** será retornada.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Erro* \[ out\]
</dt> <dd>

Tipo: cadeia **de caracteres**

Se o status operacional do trabalho não for 2 (OK), esse método retornará uma instância inserida da [**classe Msvm \_ Error,**](msvm-error.md) no formato CIM-XML. Se o status operacional do trabalho for 2 (OK), **Null** será retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

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

O acesso à [**classe Msvm \_ ConcreteJob**](msvm-concretejob.md) pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**Msvm \_ ConcreteJob**](msvm-concretejob.md)
</dt> </dl>

 

