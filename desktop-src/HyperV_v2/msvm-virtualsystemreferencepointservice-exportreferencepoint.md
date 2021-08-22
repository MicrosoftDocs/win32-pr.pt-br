---
description: Exporta o ponto de referência do sistema virtual.
ms.assetid: e4d80404-6b1b-4153-9ab2-aebab18c331a
title: Método ExportReferencePoint da Msvm_VirtualSystemReferencePointService classe
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
ms.openlocfilehash: 3273c4781858b02e60b632ae491b1694068a32f5feaddea885576dade6876989
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147949"
---
# <a name="exportreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>Método ExportReferencePoint da classe Msvm \_ VirtualSystemReferencePointService

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

*ReferencePoint* \[ Em\]
</dt> <dd>

Uma referência à [**instância \_ virtualSystemReferencePoint do Msvm**](msvm-virtualsystemreferencepoint.md) que representa o ponto de referência a ser exportado.

</dd> <dt>

*ExportDirectory* \[ Em\]
</dt> <dd>

O caminho totalmente qualificado do diretório para o qual o ponto de referência deve ser exportado.

</dd> <dt>

*ExportSettingData* \[ Em\]
</dt> <dd>

Uma instância do [**Msvm \_ VirtualSystemReferencePointExportSettingData**](msvm-virtualsystemreferencepointexportsettingdata.md) que representa as configurações para a operação de exportação.

</dd> <dt>

*Trabalho* \[ out\]
</dt> <dd>

Um parâmetro opcional para monitorar o progresso da operação, que será usado se o método não puder ser executado de forma síncrona. Se a operação estiver sendo executada de forma assíncrona, o valor de retorno será 4096.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Em caso de êxito, retorna um 0 (Concluído sem Erro) ou 4096 (Trabalho Iniciado); caso contrário, retorne um erro.

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
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




