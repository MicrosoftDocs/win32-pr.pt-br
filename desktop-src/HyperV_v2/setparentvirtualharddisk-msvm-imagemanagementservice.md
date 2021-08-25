---
description: Atualiza o pai para os arquivos de disco rígido virtual folha e filho especificados.
ms.assetid: 5ad41218-bcfd-449a-a66e-2096a1d96bf5
title: Método SetParentVirtualHardDisk da classe Msvm_ImageManagementService dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetParentVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 47be9f3f383da237a3679633ac1d663bbc81ef078a7529662b8f21d10246761f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050536"
---
# <a name="setparentvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>Método SetParentVirtualHardDisk da classe Msvm \_ ImageManagementService

Atualiza o pai para os arquivos de disco rígido virtual folha e filho especificados. Consulte Comentários sobre restrições de uso para esse método.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetParentVirtualHardDisk(
  [in]  string              ChildPath,
  [in]  string              ParentPath,
  [in]  string              LeafPath,
  [in]  boolean             IgnoreIDMismatch,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ChildPath* \[ Em\]
</dt> <dd>

Um caminho totalmente qualificado que especifica o local do arquivo de disco rígido virtual filho.

</dd> <dt>

*ParentPath* \[ Em\]
</dt> <dd>

Um caminho totalmente qualificado que especifica o local do arquivo de disco rígido virtual pai.

</dd> <dt>

*LeafPath* \[ Em\]
</dt> <dd>

Um caminho totalmente qualificado que especifica o local do arquivo de disco rígido virtual folha. O parâmetro poderá ser **Null se** o disco rígido virtual estiver offline, mas deverá ser especificado se o disco rígido virtual estiver em uso.

</dd> <dt>

*IgnoreIDMismatch* \[ Em\]
</dt> <dd>

Indica se o pai deve ser definido à força quando os identificadores de disco virtual não corresponderem. Esse parâmetro deve ser usado com cuidado porque, se o novo disco rígido virtual pai não for idêntico ao pai original, poderá ocorrer corrupção de dados.

</dd> <dt>

*Trabalho* \[ out\]
</dt> <dd>

Se a operação for executada de forma assíncrona, esse método retornará 4096 e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob.**](/previous-versions//cc136808(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos valores a seguir.

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

**O sistema está em uso** (32774)
</dt> <dt>

**Estado inválido para esta operação** (32775)
</dt> <dt>

**Tipo de dados incorreto** (32776)
</dt> <dt>

**O sistema não está disponível** (32777)
</dt> <dt>

**Memória sem memória** (32778)
</dt> <dt>

**Arquivo não encontrado** (32779)
</dt> </dl>

## <a name="remarks"></a>Comentários

Somente os seguintes tipos de discos rígidos virtuais podem ser usados com este método:

-   VHD diferencial
-   Diferenciando VHDX

O acesso à [**classe Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md) pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

