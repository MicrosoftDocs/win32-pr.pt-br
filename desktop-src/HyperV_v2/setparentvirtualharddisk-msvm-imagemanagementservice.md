---
description: Atualiza o pai para os arquivos de disco rígido virtual de folha e filho especificados.
ms.assetid: 5ad41218-bcfd-449a-a66e-2096a1d96bf5
title: Método SetParentVirtualHardDisk da classe Msvm_ImageManagementService
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
ms.openlocfilehash: f1d14d3b2ee19a9768e1ee9ed9333a452153cc9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782802"
---
# <a name="setparentvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>Método SetParentVirtualHardDisk da \_ classe imagens Msvm

Atualiza o pai para os arquivos de disco rígido virtual de folha e filho especificados. Consulte comentários para restrições de uso para este método.

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

*ChildPath* \[ no\]
</dt> <dd>

Um caminho totalmente qualificado que especifica o local do arquivo de disco rígido virtual filho.

</dd> <dt>

*ParentPath* \[ no\]
</dt> <dd>

Um caminho totalmente qualificado que especifica o local do arquivo de disco rígido virtual pai.

</dd> <dt>

*LeafPath* \[ no\]
</dt> <dd>

Um caminho totalmente qualificado que especifica o local do arquivo de disco rígido virtual de folha. O parâmetro poderá ser **nulo** se o disco rígido virtual estiver offline, mas deverá ser especificado se o disco rígido virtual estiver em uso.

</dd> <dt>

*IgnoreIDMismatch* \[ no\]
</dt> <dd>

Indica se o pai deve ser forçado a definir quando os identificadores de disco virtual não correspondem. Esse parâmetro deve ser usado com cautela porque se o novo disco rígido virtual pai não for idêntico ao pai original, poderá ocorrer corrupção de dados.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um dos valores a seguir.

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
</dt> <dt>

**Arquivo não encontrado** (32779)
</dt> </dl>

## <a name="remarks"></a>Comentários

Somente os seguintes tipos de discos rígidos virtuais podem ser usados com este método:

-   VHD diferencial
-   VHDX diferencial

O acesso à classe [**Msvm \_ imagens**](msvm-imagemanagementservice.md) pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**Msvm \_ imagens**](msvm-imagemanagementservice.md)
</dt> </dl>

 

