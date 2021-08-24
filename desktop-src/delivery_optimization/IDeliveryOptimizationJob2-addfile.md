---
title: Método AddFile IDeliveryOptimizationJob2
description: O método AddFile adiciona um único arquivo a um trabalho existente DO.
keywords:
- Método AddFile
- Método AddFile, interface IDeliveryOptimizationJob2
- Interface IDeliveryOptimizationJob2, método AddFile
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.AddFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e6d27bca855bb9c719b485060fabf1f10b7130bd864569e74f98516ca76b8fb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544631"
---
# <a name="ideliveryoptimizationjob2addfilewithranges-method"></a>Método IDeliveryOptimizationJob2:: AddFileWithRanges

O método AddFile adiciona um único arquivo a um trabalho existente DO.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT AddFile(
  [in]                              LPCWSTR       fileId,
  [in, unique]                      LPCWSTR       remoteUrl,
  [in]                              DWORD         rangeCount,
  [in, size_is(rangeCount), unique] BG_FILE_RANGE ranges[],
  [in]                              REFIID        riid,
  [out]                             void          **object
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FileID* \[ no\]
</dt> <dd>

A cadeia de caracteres de ID de arquivo, que identifica exclusivamente o arquivo a ser baixado.

</dd> <dt>

*remoteUrl* \[ no\]
</dt> <dd>

A URL do arquivo que tentará se conectar para baixar o arquivo.

</dd> <dt>

*rangeCount* \[ no\]
</dt> <dd>

O número de itens contidos em *intervalos*. Um valor zero significa que nenhum intervalo é usado para o arquivo.

</dd> <dt>

*intervalos* \[ de no\]
</dt> <dd>

A lista de intervalos opcionais. Cada intervalo na lista é uma estrutura de [**BG_FILE_RANGE**](bg-file-range.md) .

</dd> <dt>

*riid* \[ no\]
</dt> <dd>

O tipo de objeto contido no objeto. Isso deve ser pelo tipo IID_IDeliveryOptimizationFile.

</dd> <dt>

*objeto* \[ do fora\]
</dt> <dd>

O objeto IDeliveryOptimizationFile, que representa o arquivo de download. 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna S_OK em caso de êxito ou um dos valores de HRESULT padrão em caso de erro.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|---------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo com suporte  | Windows 10, \[ somente aplicativos da área de trabalho da versão 1803\]                                  |
| Servidor mínimo com suporte  | Windows Servidor, versão 1709 \[ aplicativos da área de trabalho\]                              |
| Cabeçalho                    | Deliveryoptimization. h                                                          |
| INSERI                       | DeliveryOptimization. idl                                                        |
| Biblioteca                   | Dosvc. lib                                                                       |
| DLL                       | Dosvc.dll                                                                       |
| IID                       | IID_IDeliveryOptimizationJob é definido como EE2584CF-A69C-4848-B633-2649962B3EF7 |

## <a name="see-also"></a>Confira também

[**IDeliveryOptimizationJob2**](ideliveryoptimizationjob2.md)
