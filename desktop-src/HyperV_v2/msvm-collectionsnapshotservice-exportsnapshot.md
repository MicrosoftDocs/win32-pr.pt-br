---
description: Exporta uma coleção de instantâneos de sistemas de computador virtual para um arquivo. A coleção de instantâneos, suas definições de configuração associadas e suas configurações de recurso associadas serão preservadas no arquivo resultante.
ms.assetid: 61fbc81c-c3e8-4058-b11a-4ed69481207c
title: Método ExportSnapshot da classe Msvm_CollectionSnapshotService
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
ms.openlocfilehash: f4dd29e001c8335477451e86151d950c25edb9b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165254"
---
# <a name="exportsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Método ExportSnapshot da \_ classe CollectionSnapshotService Msvm

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

*Instantâneocollection* \[ no\]
</dt> <dd>

Uma referência a uma [**\_ coleção CIM**](cim-collection.md) que representa a coleção de instantâneos a ser exportada.

</dd> <dt>

*ExportDirectory* \[ no\]
</dt> <dd>

O caminho totalmente qualificado do diretório para o qual a coleção do sistema virtual deve ser exportada. Se a propriedade **CreateVmExportSubdirectory** no parâmetro *ExportSettingData* for definida como **true** , esse diretório poderá ser reutilizado para exportar várias coleções de sistema virtual e esse método colocará cada definição de coleção do sistema virtual em um subdiretório separado sob esse caminho.

</dd> <dt>

*ExportSettingData* \[ no\]
</dt> <dd>

Uma instância de [**Msvm \_ CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md) que representa as configurações da operação de exportação.

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

[**Msvm \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




