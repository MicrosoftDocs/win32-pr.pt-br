---
description: Exporta o ponto de referência do sistema virtual.
ms.assetid: e4d80404-6b1b-4153-9ab2-aebab18c331a
title: Método ExportReferencePoint da classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bedd051123e4f75d7438b2e3831a84204ff4aec3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105750838"
---
# <a name="exportreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>Método ExportReferencePoint da \_ classe VirtualSystemReferencePointService Msvm

Exporta o ponto de referência do sistema virtual.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ExportReferencePoint(
  [in]  Msvm_VirtualSystemReferencePoint REF ReferencePoint,
  [in]  string                               ExportDirectory,
  [in]  string                               ExportSettingData,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ReferencePoint* \[ no\]
</dt> <dd>

Uma referência à instância [**de \_ VirtualSystemReferencePoint Msvm**](msvm-virtualsystemreferencepoint.md) que representa o ponto de referência a ser exportado.

</dd> <dt>

*ExportDirectory* \[ no\]
</dt> <dd>

O caminho totalmente qualificado do diretório no qual o ponto de referência deve ser exportado.

</dd> <dt>

*ExportSettingData* \[ no\]
</dt> <dd>

Uma instância de [**Msvm \_ VirtualSystemReferencePointExportSettingData**](msvm-virtualsystemreferencepointexportsettingdata.md) que representa as configurações da operação de exportação.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Um parâmetro opcional para monitorar o progresso da operação, que é usado se o método não pôde ser executado de forma síncrona. Se a operação estiver sendo executada de forma assíncrona, o valor de retorno será 4096.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Em caso de sucesso, retorna um 0 (completo sem erro) ou 4096 (trabalho iniciado); caso contrário, retorne um erro.

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




