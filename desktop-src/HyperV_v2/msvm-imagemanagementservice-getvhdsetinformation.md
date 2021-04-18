---
description: Recupera informações sobre um arquivo de conjunto de VHD.
ms.assetid: efdfd4c6-b762-4369-add3-e152652c6802
title: Método GetVHDSetInformation da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVHDSetInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 16cdcf4a354e6d6b47b6a67c071daf8883905f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770216"
---
# <a name="getvhdsetinformation-method-of-the-msvm_imagemanagementservice-class"></a>Método GetVHDSetInformation da \_ classe imagens Msvm

Recupera informações sobre um arquivo de conjunto de VHD.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetVHDSetInformation(
  [in]  string              VHDSetPath,
  [in]  uint32              AdditionalInformation[],
  [out] string              Information,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VHDSetPath* \[ no\]
</dt> <dd>

Um caminho totalmente qualificado que especifica o local do arquivo de conjunto de VHD.

</dd> <dt>

*AdditionalInformation* \[ no\]
</dt> <dd>

Uma matriz que especifica quais informações adicionais devem ser coletadas sobre o arquivo de conjunto de VHD. Cada entrada na matriz é um tipo de informação adicional. Se esse parâmetro for nulo, nenhuma informação adicional será recuperada.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Paths"></span><span id="paths"></span><span id="PATHS"></span>

**Caminhos** (2)


</dt> <dd></dd> </dl> </dd> <dt>

*Informações* \[ do fora\]
</dt> <dd>

Se for bem-sucedido, esse objeto conterá as informações para o arquivo de conjunto de VHD solicitado. Esta é uma instância incorporada de [**Msvm \_ VHDSetInformation**](msvm-vhdsetinformation.md).

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Uma referência ao trabalho (pode ser NULL se a tarefa for concluída).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ imagens**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




