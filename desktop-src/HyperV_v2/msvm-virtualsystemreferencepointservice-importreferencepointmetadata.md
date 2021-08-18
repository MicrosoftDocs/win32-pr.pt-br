---
description: Importa os metadados do ponto de referência do sistema virtual.
ms.assetid: 8e32fded-cd84-4586-83c4-c23200d4698e
title: Método ImportReferencePointMetadata da classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ImportReferencePointMetadata
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2757464e8b101819dc46a778df142e4e8ed37d93b774a87a037a7d272812f883
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147929"
---
# <a name="importreferencepointmetadata-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>Método ImportReferencePointMetadata da \_ classe VirtualSystemReferencePointService Msvm

Importa os metadados do ponto de referência do sistema virtual.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ImportReferencePointMetadata(
  [in]  Msvm_ComputerSystem REF AffectedSystem,
  [in]  string                  ConfigFilePath,
  [in]  string                  RuntimeStateFilePath,
  [out] CIM_ConcreteJob     REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AffectedSystem* \[ no\]
</dt> <dd>

Uma referência a um [**\_ ComputerSystem Msvm**](msvm-computersystem.md) que descreve o sistema afetado.

</dd> <dt>

*ConfigFilePath* \[ no\]
</dt> <dd>

O caminho totalmente qualificado do arquivo de configuração de onde os metadados do ponto de referência serão importados.

</dd> <dt>

*RuntimeStateFilePath* \[ no\]
</dt> <dd>

O caminho totalmente qualificado do arquivo de estado de tempo de execução de onde os metadados do ponto de referência serão importados.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Um parâmetro opcional para monitorar o progresso da operação, que é usado se o método não pôde ser executado de forma síncrona. Se a operação estiver sendo executada de forma assíncrona, o valor de retorno será 4096.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna 0 (sem erro) ou uma das seguintes mensagens de erro:

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

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1703\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




