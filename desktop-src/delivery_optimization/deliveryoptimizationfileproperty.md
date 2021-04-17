---
title: Enumeração DeliveryOptimizationFileProperty (Deliveryoptimization. h)
description: A enumeração DeliveryOptimizationFileProperty especifica a ID de uma propriedade opcional para o arquivo do.
keywords:
- Enumeração DeliveryOptimizationFileProperty
topic_type:
- apiref
api_name:
- DeliveryOptimizationFileProperty
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 238ad815149f7d40dd1902b991608e0a3005eb35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105766512"
---
# <a name="deliveryoptimizationfileproperty-enumeration"></a>Enumeração DeliveryOptimizationFileProperty

A enumeração DeliveryOptimizationFileProperty especifica a ID de uma propriedade opcional para o arquivo do. Essa enumeração é usada na interface IDeliveryOptimizationFile2 em que o valor da Propriedade do tipo VARIANT é passado

## <a name="syntax"></a>Syntax

```C++
typedef enum _DeliveryOptimizationFileProperty {  
  DOFilePropertyId_DecryptionInfo,
  DOFilePropertyId_IntegrityCheckInfo,
  DOFilePropertyId_IntegrityCheckMandatory,
  DOFilePropertyId_DownloadSinkInterface,
  DOFilePropertyId_DownloadSinkFilePath,
  DOFilePropertyId_DownloadSinkMemoryStream,
  DOFilePropertyId_TotalSizeBytes
} DOFilePropertyId;
```

## <a name="constants"></a>Constantes

<dl> <dt>

DOFilePropertyId_DecryptionInfo
</dt> <dd>

A ID de propriedade DOFilePropertyId_DecryptionInfo define informações de descriptografia na forma de uma cadeia de caracteres JSON. DOFilePropertyId_DecryptionInfo é uma propriedade somente gravação do tipo VT_BSTR.

</dd> <dt>

DOFilePropertyId_IntegrityCheckInfo
</dt> <dd>

A ID da propriedade DOFilePropertyId_IntegrityCheckInfo define o local do arquivo de hash da parte (PHF), que é usado pelo DO para executar verificações de integridade de tempo de execução no conteúdo baixado. DOFilePropertyId_IntegrityCheckInfo é uma propriedade somente gravação do tipo VT_BSTR.

</dd> <dt>

DOFilePropertyId_IntegrityCheckMandatory
</dt> <dd>

A ID de propriedade DOFilePropertyId_IntegrityCheckMandatory define um sinalizador booliano que indica se o uso de PHF é obrigatório. Se for TRUE, o download será anulado quando a verificação de integridade falhar. DOFilePropertyId_IntegrityCheckMandatory é uma propriedade de leitura/gravação do tipo VT_BOOL.

</dd> <dt>

DOFilePropertyId_DownloadSinkFilePath
</dt> <dd>

A ID de propriedade de DOFilePropertyId_DownloadSinkFilePath define um local DO sistema de arquivos totalmente qualificado onde o deve armazenar as partes baixadas. DOFilePropertyId_DownloadSinkFilePath é do tipo VT_BSTR.

</dd> <dt>

DOFilePropertyId_DownloadSinkMemoryStream
</dt> <dd>

A ID da propriedade de DOFilePropertyId_DownloadSinkMemoryStream foi preterida. Não use.

</dd> <dt>

DOFilePropertyId_TotalSizeBytes
</dt> <dd>

A ID da propriedade DOFilePropertyId_TotalSizeBytes especifica o tamanho total do download. DOFilePropertyId_TotalSizeBytes é do tipo VT_UI8.
</dd> </dl>

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------|----------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]<br/>      |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>  |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>               |
