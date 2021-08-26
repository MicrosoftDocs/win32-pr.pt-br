---
description: Recupera informações sobre um instantâneo VHD em um arquivo de conjunto VHD.
ms.assetid: 43745935-9bc3-4a87-8762-54693b2cdef6
title: Método GetVHDSnapshotInformation da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVHDSnapshotInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: faac0c7b52d8e066ffa658a539a18d6423b50c861b772e536abca2aca010ea47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046626"
---
# <a name="getvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a>Método GetVHDSnapshotInformation da \_ classe imagens Msvm

Recupera informações sobre um instantâneo VHD em um arquivo de conjunto VHD.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetVHDSnapshotInformation(
  [in]  string              VHDSetPath,
  [in]  string              SnapshotIds[],
  [in]  uint32              AdditionalInformation[],
  [out] string              SnapshotInformation[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VHDSetPath* \[ no\]
</dt> <dd>

Um caminho totalmente qualificado que especifica o local do arquivo de conjunto de VHD.

</dd> <dt>

*SnapshotIds* \[ no\]
</dt> <dd>

Uma lista de GUIDs que representa as IDs de instantâneo de cada instantâneo para o qual as informações estão sendo solicitadas. Se esse parâmetro for nulo, as informações de todos os instantâneos serão recuperadas.

</dd> <dt>

*AdditionalInformation* \[ no\]
</dt> <dd>

Uma matriz que especifica quais informações adicionais devem ser coletadas sobre cada instantâneo do VHD. Cada entrada na matriz é um tipo de informação adicional. Se esse parâmetro for nulo, nenhuma informação adicional será recuperada.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Parent_Paths"></span><span id="parent_paths"></span><span id="PARENT_PATHS"></span>

**Caminhos pai** (2)


</dt> <dd></dd> </dl> </dd> <dt>

*SnapshotInformation* \[ fora\]
</dt> <dd>

Se for bem-sucedido, uma matriz de informações sobre cada instantâneo solicitado. Cada elemento é uma instância incorporada de [**Msvm \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Uma referência ao trabalho (pode ser NULL se a tarefa for concluída).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos seguintes valores:

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

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ imagens**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




