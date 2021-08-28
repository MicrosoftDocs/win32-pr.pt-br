---
description: Exporta uma coleção de instantâneos de sistemas de computador virtual para um arquivo. A coleção de instantâneos, suas definições de configuração associadas e suas configurações de recurso associadas serão preservadas no arquivo resultante.
ms.assetid: 61fbc81c-c3e8-4058-b11a-4ed69481207c
title: Método ExportSnapshot da classe Msvm_CollectionSnapshotService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ExportSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ec61899e92da562250bf392077468adef14a35eda72d89d28ad9b3ddc3da2f5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119426836"
---
# <a name="exportsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Método ExportSnapshot da classe Msvm \_ CollectionSnapshotService

Exporta uma coleção de instantâneos de sistemas de computador virtual para um arquivo. A coleção de instantâneos, suas definições de configuração associadas e suas configurações de recurso associadas serão preservadas no arquivo resultante.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ExportSnapshot(
  [in]  CIM_Collection  REF SnapshotCollection,
  [in]  string              ExportDirectory,
  [in]  string              ExportSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SnapshotCollection* \[ Em\]
</dt> <dd>

Uma referência a uma [**Coleção CIM \_**](cim-collection.md) que representa a coleção de instantâneos a ser exportada.

</dd> <dt>

*ExportDirectory* \[ Em\]
</dt> <dd>

O caminho totalmente qualificado do diretório para o qual a coleção do sistema virtual deve ser exportada. Se a propriedade **CreateVmExportSubdirectory** no parâmetro *ExportSettingData* estiver definida como **True,** esse diretório poderá ser reutilizado para exportar várias coleções de sistema virtual e esse método colocará cada definição de coleção do sistema virtual em um subdiretório separado nesse caminho.

</dd> <dt>

*ExportSettingData* \[ Em\]
</dt> <dd>

Uma instância do [**Msvm \_ CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md) que representa as configurações para a operação de exportação.

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

[**Coleção \_ MsvmSnapshotService**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




