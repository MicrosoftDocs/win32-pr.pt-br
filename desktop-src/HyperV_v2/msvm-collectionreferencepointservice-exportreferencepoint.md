---
description: Exporta uma coleção de pontos de referência para um arquivo. A coleção de pontos de referência, suas definições de configuração associadas e suas configurações de recursos associadas serão preservadas no arquivo resultante.
ms.assetid: 0ed61ded-b4d6-40c5-98be-e192eb934387
title: Método ExportReferencePoint da classe Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 49517da44cc7955d825792afcc475c56e37fad37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782355"
---
# <a name="exportreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a>Método ExportReferencePoint da \_ classe CollectionReferencePointService Msvm

Exporta uma coleção de pontos de referência para um arquivo. A coleção de pontos de referência, suas definições de configuração associadas e suas configurações de recursos associadas serão preservadas no arquivo resultante.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ExportReferencePoint(
  [in]  CIM_Collection  REF ReferencePointCollection,
  [in]  string              ExportDirectory,
  [in]  string              ExportSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ReferencePointCollection* \[ no\]
</dt> <dd>

Uma referência a uma [**\_ coleção CIM**](cim-collection.md) que representa a coleção de pontos de referência a ser exportada.

</dd> <dt>

*ExportDirectory* \[ no\]
</dt> <dd>

O caminho totalmente qualificado do diretório para o qual a coleção de pontos de referência deve ser exportada.

</dd> <dt>

*ExportSettingData* \[ no\]
</dt> <dd>

Uma instância de [**Msvm \_ CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) que representa as configurações da operação de exportação.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Uma referência opcional que será retornada se a operação for executada de forma assíncrona. Se estiver presente, a referência retornada a uma instância de [**CIM \_ ConcreteJob**](cim-concretejob.md) poderá ser usada para monitorar o progresso e obter o resultado do método.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for executado de forma síncrona, ele retornará 0 se tiver sucesso. Se esse método for executado de forma assíncrona, ele retornará 4096 e o parâmetro de saída do trabalho poderá ser usado para acompanhar o progresso da operação assíncrona. Qualquer outro valor de retorno indica um erro.

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

[**Msvm \_ CollectionReferencePointService**](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




