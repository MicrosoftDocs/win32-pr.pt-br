---
description: Retorna informações de resumo da máquina virtual para os arquivos de definição de máquina virtual especificados.
ms.assetid: 5a3d7f2c-3b89-4dd6-909d-4452afc3705f
title: Método GetDefinitionFileSummaryInformation da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetDefinitionFileSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7c6d3da6ef920488edb7fde723880b9f53768cfd246e91d287390bb6fb02fb17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117995293"
---
# <a name="getdefinitionfilesummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método GetDefinitionFileSummaryInformation da \_ classe VirtualSystemManagementService Msvm

Retorna informações de resumo da máquina virtual para os arquivos de definição de máquina virtual especificados.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetDefinitionFileSummaryInformation(
  [in]  string                      DefinitionFiles[],
  [out] Msvm_SummaryInformationBase SummaryInformation[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DefinitionFiles* \[ no\]
</dt> <dd>

Uma matriz de caminhos para arquivos de configuração XML para os quais retornar informações de resumo.

</dd> <dt>

*SummaryInformation* \[ fora\]
</dt> <dd>

Uma matriz de instâncias do [**Msvm \_ SummaryInformationBase**](msvm-summaryinformation.md) que contém as informações solicitadas para as máquinas virtuais e/ou os instantâneos especificados na matriz *DefinitionFiles* . Somente as propriedades **Name**, **ElementName**, **CreationTime** e **Notes** são retornadas, todas as outras propriedades serão **nulas**.

> [!Note]  

 

antes da Windows 10, a versão 1703, datatype era [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




