---
description: Exporta uma coleção de pontos de referência para um arquivo. A coleção de pontos de referência, suas definições de configuração associadas e suas configurações de recurso associadas serão preservadas no arquivo resultante.
ms.assetid: 0ed61ded-b4d6-40c5-98be-e192eb934387
title: Método ExportReferencePoint da classe Msvm_CollectionReferencePointService classe
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
ms.openlocfilehash: 3084cdecdd9a5c5808884a609b6bd91f4d50b814d64a96c8ea9e7470c9ece728
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681896"
---
# <a name="exportreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a>Método ExportReferencePoint da classe Msvm \_ CollectionReferencePointService

Exporta uma coleção de pontos de referência para um arquivo. A coleção de pontos de referência, suas definições de configuração associadas e suas configurações de recurso associadas serão preservadas no arquivo resultante.

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

*ReferencePointCollection* \[ Em\]
</dt> <dd>

Uma referência a uma [**Coleção CIM \_**](cim-collection.md) que representa a coleção de pontos de referência a ser exportada.

</dd> <dt>

*ExportDirectory* \[ Em\]
</dt> <dd>

O caminho totalmente qualificado do diretório para o qual a coleção de pontos de referência deve ser exportada.

</dd> <dt>

*ExportSettingData* \[ Em\]
</dt> <dd>

Uma instância do [**Msvm \_ CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) que representa as configurações da operação de exportação.

</dd> <dt>

*Trabalho* \[ out\]
</dt> <dd>

Uma referência opcional que será retornada se a operação for executada de forma assíncrona. Se presente, a referência retornada a uma instância de [**CIM \_ ConcreteJob**](cim-concretejob.md) pode ser usada para monitorar o progresso e obter o resultado do método.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for executado de forma síncrona, ele retornará 0 se for bem-sucedido. Se esse método for executado de forma assíncrona, ele retornará 4096 e o parâmetro de saída do trabalho poderá ser usado para acompanhar o progresso da operação assíncrona. Qualquer outro valor de retorno indica um erro.

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

[**Msvm \_ CollectionReferencePointService**](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




